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
### Button