# UI Controls
Ui Controls or input controls in android are the interactive or Compose components that are used to design the user interface of an application.

## Textfield

A Textfield is the standard text entry widget in Android apps. If the user needs to enter text into an app, this is the primary way for them to do that.

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

### Text

A TextView displays text to the user 

```

@Composable
fun TextExample() {
      
        Text( textState.value.text)

}


```


### Button

A Button is a user interface control that is used to perform an action whenever the user clicks or tap on it

```

@Composable
fun ButtonExample() {
        Button(onClick = {}, colors = ButtonConstants.defaultButtonColors(
            backgroundColor = Color.Red
    )) {
        Text("Button")
    }

}


```

### Radio Button

A RadioButton is a two states button which is either checked or unchecked

```

@Composable
fun RadioButtonExample() {
    val radioOptions = listOf("A", "B", "C")
    val (selectedOption, onOptionSelected) = remember { mutableStateOf(radioOptions[1] ) }
    Column {
        radioOptions.forEach { text ->
            Row(
                Modifier
                .fillMaxWidth()
                .selectable(
                    selected = (text == selectedOption),
                    onClick = {
                        onOptionSelected
                        (text)
                    }
                )
                .padding(horizontal = 16.dp)
            ) {
                RadioButton(
                    selected = (text == selectedOption),
                    onClick = { onOptionSelected(text) }
                )
                Text(
                    text = text,
                    style = MaterialTheme.typography.body1.merge(),
                    modifier = Modifier.padding(start = 16.dp)
                )
            }
        }
    }
}


```

### Switch

A Switch is a two-state toggle switch widget that can select between two options

```

@Composable
fun SwitchExample() {
    val checkedState = remember { mutableStateOf(true) }
    Switch(
        checked = checkedState.value,
        onCheckedChange = { checkedState.value = it }
    )
}


```

### Checkbox

A checkbox is a specific type of two-states button that can be either checked or unchecked.

```


@Composable
fun CheckBoxDemo() {
    val checkedState = remember { mutableStateOf(true) }
    Checkbox(
        checked = checkedState.value,
        onCheckedChange = { checkedState.value = it }
    )
}



```


### Snackbar

A Snackbars provide lightweight feedback about an operation. They show a brief message at the bottom of the screen on mobile

```


@Composable
fun CheckBoxDemo() {
    val checkedState = remember { mutableStateOf(true) }
    Checkbox(
        checked = checkedState.value,
        onCheckedChange = { checkedState.value = it }
    )
}



```

### Slider

A Snackbars provide lightweight feedback about an operation. They show a brief message at the bottom of the screen on mobile

```


@Composable
fun SliderExample() {
    var slider by remember { mutableStateOf(0f) }
    Text(text = slider.toString())
    Slider(value = slider, onValueChange = { slider = it })
}



```

### FloatingActionButton

A floating action button (FAB) is a circular button that triggers the primary action in your app's UI.

```


@Composable
fun SliderExample() {
    var slider by remember { mutableStateOf(0f) }
    Text(text = slider.toString())
    Slider(value = slider, onValueChange = { slider = it })
}



```


### AlertDialog

An Android AlertDialog can be used to display the dialog message with OK and Cancel buttons. 
It can be used to interrupt and ask the user about his/her choice to continue or discontinue. 
Android AlertDialog is composed of three regions: title, content area and action buttons.

```


@Composable
fun AlertDialogSample() {
    MaterialTheme {
        Column {
            val openDialog = remember { mutableStateOf(false)  }

            Button(onClick = {
                openDialog.value = true
            }) {
                Text("Click me")
            }

            if (openDialog.value) {

                AlertDialog(
                    onDismissRequest = {
                        // Dismiss the dialog when the user clicks outside the dialog or on the back
                        // button. If you want to disable that functionality, simply use an empty
                        // onCloseRequest.
                        openDialog.value = false
                    },
                    title = {
                        Text(text = "Dialog Title")
                    },
                    text = {
                        Text("Here is a text ")
                    },
                    confirmButton = {
                        Button(

                            onClick = {
                                openDialog.value = false
                            }) {
                            Text("This is the Confirm Button")
                        }
                    },
                    dismissButton = {
                        Button(

                            onClick = {
                                openDialog.value = false
                            }) {
                            Text("This is the dismiss Button")
                        }
                    }
                )
            }
        }

    }
}



```

### ModalDrawerLayout

A ModalDrawerLayout is used to implement the Navigation drawer. 

```


@Composable
fun ModalDrawerLayoutSample() {
    val drawerState = rememberDrawerState(DrawerValue.Closed)

    ModalDrawerLayout(
            drawerState = drawerState,
            drawerContent = {
                Column {
                    Text("Text in Drawer")
                    Button(onClick = { drawerState.close() }) {
                        Text("Close Drawer")
                    }
                }
            },
            bodyContent = {
                Column {
                    Text("Text in Bodycontext")
                    Button(onClick = { drawerState.open() }) {
                        Text("Click to open")
                    }
                }
            }
    )
}



```

### Card

A card is a sheet of material that serves as an entry point to more detailed information. Cards may contain a photo, text, and a link about a single subject. 
They may display content containing elements of varying size, such as photos with captions of variable length. (from: Google Material Design)

```


@Composable fun CardDemo(){
    Card(Modifier.fillMaxWidth().padding(8.dp),elevation = 8.dp){
        Text("This is a Card")
    }
}



```