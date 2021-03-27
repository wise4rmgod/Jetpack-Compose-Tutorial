# State Management
A state in an application is any value that can change over time. 
A Typical example of a state in a sofware application is below:

# Example
- When a text widget changes it value from 1 to 2 

# State in Compose
Jetpack Compose makes it easy to handle state management and it can be seen below:

```


```

if you run the above code you will notice that the text widget changes it default value when you click on the button, the text widget has changed its state 
 
 Few key terms to note in Compose state
 - Remember
 - MutableStateOf
 - Composition
 - Recomposition

## Remember function 
A remember is a composable function that can store a single object in memory and also it can hold any value from initial composition to recomposition stage(it ) 
> remember can store both mutable and immutable objects

## MutableStateOf
 A MutableStateOf 