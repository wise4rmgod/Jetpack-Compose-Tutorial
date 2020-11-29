# Hello World Example
Create A Compose Application

![Welcome to jetpackcompose.com](https://miro.medium.com/max/1400/1*Dz8H_lJ7TyMmgrsP9YB3Vw.png)

Click on “Create New Project”

![Welcome to jetpackcompose.com](https://miro.medium.com/max/1400/1*hbK3UCWSluoqQExYM85nGA.png)

you will click o the “Empty Compose Activity”

![Welcome to jetpackcompose.com](https://miro.medium.com/max/1400/1*1DHAKWDaaZeKS1Tbdj2WNA.png)

In this section, you give your compose project a name, package name, save location, language(default is Kotlin) and Minimum SDK. then you click the **“Finish”** button

![Welcome to jetpackcompose.com](https://miro.medium.com/max/1400/1*mwyZ9T3qe3qrMNHxEyydog.png)

your Hello World Compose project has been created now run your app, you will see the image below

![Welcome to jetpackcompose.com](https://miro.medium.com/max/896/1*cjI3QogKusrJ6VZxb2u5Og.png)

```
class MainActivity : AppCompatActivity() {
    override fun onCreate(savedInstanceState: Bundle?) {
        super.onCreate(savedInstanceState)
        setContent {
            Text("Hello world!")
        }
    }
}
```
This is how easy and simple it is to create a Hello World app in  Jetpack compose, in the next section you will learn about Compose UI Layouts.
