# Android Architecture Patterns that i use

MVC has been my most favourite pattern in general for both backend and frontend apps but when it comes to mobile applications things can get more complicated than what MVC can handle.
The introduction explict database classes (DAO,entities), API classes (services, etcs), viewmodels and general models has motivated me to redefine the architecture patterns that i use.

# File Structure

First things first, is the file structure the architecture though? or what.

-app
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