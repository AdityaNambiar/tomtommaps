# Tomtommaps Android Miniproject.
    - There are few things that the "Getting started" documentation makes abstract or does not clarify, for beginners who happen to have never used the Google maps SDK either.

[Getting started](https://developer.tomtom.com/maps-android-sdk/map-initialization)

- Things you need to consider:
    1. Design
        - In design, you can add Map into the XML by two ways. 
        a. Fragments (Android XML component)
        b. Direct MapView (A special library XML component)
    2. Code
        - Your code will be susceptible to change when you decide to choose either of these design approaches, we'll see that 
            ahead in this readme.
        - MapView class reference:
            ` MapView mapView; `
        - MapFragment class reference:
            ` MapFragment mapFragment; `
        
- As said before, there are two ways you can integrate the design:

    1. Adding a Fragment to the XML layout where you to show the map:
         ` <fragment
                android:id="@+id/map_fragment"
                android:name="com.tomtom.online.sdk.map.MapFragment"
                android:layout_width="match_parent"
                android:layout_height="match_parent" /> `
    2. Adding a MapView element to the XML layout:
        ` <com.tomtom.online.sdk.map.MapView 
                android:layout_width="match_parent" 
                android:layout_height="match_parent"
                app:mapBackgroundColor="#0000ff"/> `

[Documentation - MapView initialization.](https://developer.tomtom.com/maps-sdk-android/documentation#mapview-initialization)

- The lifecycle methods listed over there are required to be put in the code. They are simple methods so you only need to copy and paste them in the code.

- The original documentation page uses the "MapView" object reference. - Which is what it does not specify after telling us about the MapFragment.

**Note: The MapFragment and MapView class references are used interchangeably**

- You will find a complete example in this repository that only uses MapFragment in the code and design