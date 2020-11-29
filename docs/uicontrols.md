# UI Controls
Ui Controls or input controls in android are the interactive or Compose components that are used to design the user interface of an application.

## Textfield
The Textfield is the standard text entry widget in Android apps. If the user needs to enter text into an app, this is the primary way for them to do that.

```
@Composable
fun TextFieldExample() {
    Column(Modifier.padding(16.dp)) {
        val textState = remember { mutableStateOf(TextFieldValue()) }
        TextField(
                value = textState.value,
                onValueChange = { textState.value = it }
        )
        Text( textState.value.text)
    }
}
```
**Retrieving the Value**

Getting the value of the text entered into an EditText is as follows:
> remember function will save your state for later use
```
 val textState = remember { mutableStateOf(TextFieldValue()) }
   TextField(
                value = textState.value,
                onValueChange = { textState.value = it }
        )
```
to add the value gotten from the Textfield to a Text or any other UI control that can accept it, you will use the below code 
```
 Text( textState.value.text)

```

**Customizing the Input Type**

By default, any text contents within a Textfield control is displayed as plain text. By setting inputType, we can facilitate input of different types of information, 
like phone numbers:

| Type | Description |
| ------ | ----------- |
| number | A numeric only field |
| phone | For entering a phone number |


### Button