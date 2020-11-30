# UI Layouts
A layout defines the visual structure for a user interface, such as the UI for an activity or app widget.
![Welcome to jetpackcompose.com](https://miro.medium.com/max/1400/1*dG8pfE-agjdIL1hyr0IHVA.png)

This section will focus more on creating a UI based on compose layout.
> A layout may contain any type of widgets such as Fabs, buttons,Radio button , Textfield,Text etc.

Before we proceed let's talk about Scaffold and its importance.

#Scaffold

A Scaffold class used to Implements the basic material design visual layout structure.

```




```

## Jetpack Commpose Layout types:
**Column:** A Column will show each child below the previous children. It’s similar to a LinearLayout with vertical orientation.
```
@Composable
fun ColumnExample() {
    Column {
        Text("Hello World!")
        Text("Hello World!2")
    }
}
```
**Row:** A Row will show each child next to the previous children. It’s similar to a LinearLayout with a horizontal orientation.

```
@Composable
fun RowExample() {
    Row {
        Text("Hello World!")
        Text("Hello World!2")
    }
}
```

**Constraint layout:** A ConstraintLayout in Compose is similar to a ConstraintLayout from the classic Android View System
A ConstraintLayout requires a ConstraintSet as a parameter. In the ConstraintSet all constraints of the layout have to be declared. children will set the children of the layout

**Box:** The children of the Box layout will be stacked over each other. You can use the gravity modifier to specify where the composable should be drawn.

```
@Composable
fun BoxExample() {
    Box(Modifier.fillMaxSize()) {
        Text("This is first text", modifier = Modifier.align(Alignment.TopCenter))
        Box(
                Modifier.align(Alignment.TopCenter).fillMaxHeight().preferredWidth(
                        50.dp
                ).background( Color.Blue)
        )
        Text("This is second text", modifier = Modifier.align(Alignment.Center))
        FloatingActionButton(
                modifier = Modifier.align(Alignment.BottomEnd).padding(12.dp),
                onClick = {}
        ) {
            Text("+")
        }
    }
}
```