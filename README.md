## Android Interview Questions
> Free CheatSheet for Android Interview Questions

## Content
- [Android](#android)

### Android 

## Basic Questions

- **What is an `Activity` in Android?**

    `Activity` in java is a single screen that represents GUI(i.e. Graphical User Interface) with which users can interact in order to do something like dial the phone, view twitter, etc.

- **What is a `Servise` in Android?**

    A `service` is a general-purpose entry point for keeping an app running in the background for all kinds of reasons. A service can run continuously in the background even if the application is closed or even after the user switches to another application.

- **Differentiate `Activities` and `Services`**

    **Activities** - An `activity` is the entry point for interacting with the user. It represents a single screen with a user interface.

    **Services** - A `service` is a general-purpose entry point for keeping an app running in the background for all kinds of reasons. It is a component that runs in the background to perform long-running operations or to perform work for remote processes. A service does not provide a user interface.

- **Use of `Bundle` in Android**

    `Bundles` are used to pass the required data between various Android activities. These are like HashMap that can take trivial data types.

- **What is `Adapter`?**

    `Adapter` in android acts as a bridge between an `AdapterView` and the underlying `data` for that view. The adapter holds the data and sends the data to the adapter view, the view can take the data from the adapter view and shows the data on different views like a spinner, Recycler View, etc.

- **What is the difference between a `Fragments` and an `Activity`? Explain the relationship between the two.**

    [Learn from here](https://stackoverflow.com/questions/10478233/why-fragments-and-when-to-use-fragments-instead-of-activities)

- **When should you use a `Fragment` rather than an `Activity`?**

     - When you have some UI components to be used across thw whole app (i.e.various activities).
     - When we have multiple view to be displayed side by side just like ViewPager.

- **What are the major differences between `ListView` and `RecyclerView`?**

    | RecyclerView  | ListView | 
    | -------- | -------- | 
    | The RecyclerView’s adaptor forces us to use the ViewHolder pattern. The views are split into onCreateViewholder() and onBindViewholder() methods.    | The ListView doesn’t give that kind of protection by default, so without implementing the ViewHolder pattern inside the getView().     |
    | Use of less memory.    | More memory is used for a long list. Sometimes devices get hung.    | 
    | Efficient Scrolling, we can choose the way of scroll-like vertically or horizontally and grids.    | Inefficient scrolling, we can only create vertical scrolling.    |   

- **What is `View` in Android?** - [Learn from here](https://developer.android.com/reference/android/view/View)

- **Difference between `View.GONE` and `View.INVISIBLE`?**

    **View.GONE** - The view will not show and the rest of the views will not take its existence into consideration.

    **View.INVISIBLE** - The view will not show, but it will take its assigned space in the layout.

- **What is a `Toast`?**

    `Toast` is a message that pops up on the screen. It is used to display the message regarding the status of the operation initiated by the user and covers only the expanse of space required for the message while the user’s recent activity remains visible and interactive.
   
## Advanced Questions
    
- **What is `ViewModel` in Android?**

    The `ViewModel`class is designed to store and manage UI-related data in a lifecycle conscious way. The ViewModel class allows data to survive configuration changes     such as screen rotations.The Android framework manages the lifecycles of UI controllers, such as activities and fragments. The framework may decide to destroy or       re-create a UI controller in response to certain user actions or device events that are completely out of your control.
    
- **What is `BroadcastReceiver` in Android?**

    A `broadcast receiver` (receiver) is an Android component which allows you to register for system or application events. Android apps can send or receive broadcast       messages from the Android system and other Android apps, similar to the publish-subscribe design pattern. Unlike activities, `android BroadcastReceiver` doesn’t contain any user interface. Broadcast receiver is generally implemented to delegate the tasks to services depending on the type of intent data that’s received.

- **What is `Context` in Android?**

    The context in Android is the context of the current state of the application or object. The context comes with services like giving access to databases and preferences, resolving resources, and more.

- **Which libraries for dependency injection?**

    **[Dagger2](https://github.com/google/dagger)** - A fast dependency injector for Java and Android. Dagger is a compile-time framework for dependency injection. It uses no reflection or runtime bytecode generation, does all its analysis at compile-time, and generates plain Java source code.

    **[Hilt](https://developer.android.com/training/dependency-injection/hilt-android)** - Hilt is a dependency injection library for Android that reduces the boilerplate of doing manual dependency injection in your project.

    **[Koin](https://github.com/InsertKoinIO/koin)** - A pragmatic lightweight dependency injection framework for Kotlin developers. Written in pure Kotlin, using functional resolution only: no proxy, no code generation, no reflection. Koin is a DSL, a lightweight container and a pragmatic API.

    **[Kodein](https://github.com/kosi-libs/Kodein)** - is a very simple and yet very useful dependency retrieval container. it is very easy to use and configure.

- **What is `Room` in Android?**

    The `Room` persistence library provides an abstraction layer over `SQLite` to allow for more robust database access while harnessing the full power of SQLite.The library helps you create a cache of your app's data on a device that's running your app. This cache, which serves as your app's single source of truth, allows users to view a consistent copy of key information within your app, regardless of whether users have an internet connection.

- **What is `Data access Object(DAO)` in Room DB**

    The following code defines a DAO called `UserDao`. `UserDao` provides the methods that the rest of the app uses to interact with data in the `user` table.
