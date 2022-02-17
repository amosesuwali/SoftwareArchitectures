# Android Architecture Patterns that i use

_MVC has been my most favourite pattern in general for both backend and frontend apps but when it comes to mobile applications things can get more complicated than what MVC can handle.
The introduction of explict database classes (DAO,entities), API classes (services, etcs), viewmodels and general models has motivated me to redefine the architecture patterns that i use._


## File Structure

First things first, is the file structure the architecture? or what.

` -app
    -manifest
    -java
        -com.your.packages
            -models
            -api
            -helpers
                -Ui binders
            -database    
    -res
        -layouts
        -values
        -navigations
`

## Separate what needs to be separated

_It's a common mistake to write all your code in an Activity or a Fragment. These UI-based classes should only contain logic that handles UI and operating system interactions. By keeping these classes as lean as possible, you can avoid many problems related to the component lifecycle, and improve the testability of these classes._

## The Nomines are ...
1. MVC (Model — View — Controller)
    * Model: Layer for storing data. It is responsible for handling the domain logic(real-world business rules) and communication with the database and network layers.
    * View: UI(User Interface) layer. It provides the visualization of the data stored in the Model.
    * Controller: Layer which contains core logic. It gets informed of the user’s behavior and updates the Model as per the need.
2. MVP (Model — View — Presenter)
   * Model: Layer for storing data. It is responsible for handling the domain logic(real-world business rules) and communication with the database and network layers.
   * View: UI(User Interface) layer. It provides the visualization of the data and keep a track of the user’s action in order to notify the Presenter.
   * Presenter: Fetch the data from the model and applies the UI logic to decide what to display. It manages the state of the View and takes actions according to the user’s input notification from the View.

3. MVVM (Model — View — ViewModel)
    * Model: This layer is responsible for the abstraction of the data sources. Model and ViewModel work together to get and save the data.
    * View: The purpose of this layer is to inform the ViewModel about the user’s action.
    * ViewModel: It exposes those data streams which are relevant to the View.

## The winner of the 2022 Android Architecture Pattern is


# MVVM (Model View ViewModel) Architecture Pattern
![picture alt](https://media.geeksforgeeks.org/wp-content/uploads/20201002215007/MVVMSchema.png "Architecture Diagram for MVVM")
