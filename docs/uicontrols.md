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

### Button