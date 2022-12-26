## Android Interview Questions
> Free CheatSheet for Android Interview Questions

## Content
- [Android](#android)
- [Kotlin Questions](#kotlin)

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

    **View.GONE** - This view is invisible, and it doesn't take any space for layout purposes.

    **View.INVISIBLE** - This view is invisible, but it still takes up space for layout purposes.

- **What is a `Toast`?**

    `Toast` is a message that pops up on the screen. It is used to display the message regarding the status of the operation initiated by the user and covers only the expanse of space required for the message while the user’s recent activity remains visible and interactive.
   
## Advanced Questions
   
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

    `DAOs` are used to access your application’s persisted data. They are a better and modular way to access your database as compared to query builders or direct queries..

- **What is the life cycle of Android activity?**

    - `OnCreate()`: It is called when activity is created. Using this, the views are created and data is collected from bundles.
    - `OnStart()`: It is called if the activity is becoming visible to the user. It may be succeeded by onResume() if the activity comes to the foreground, or onStop() if it becomes hidden.
    - `OnResume()`: It is called when the activity will start an interaction with the user.
    - `OnPause()`: This is called when the activity is moving to the background but hasn’t been killed yet.
    - `OnStop()`: This is called when an activity is no longer visible to the user.
    - `OnDestroy()`: This is called when the activity is finished or destroyed.
    - `OnRestart()`: This is called after the activity has been stopped, prior to it being started again.

- **What’s the difference between `onCreate()` and `onStart()`?**

    - `onCreate()` -  method is called once during the Activity lifecycle, either when the application starts, or when the Activity has been destroyed and then recreated, for example during a configuration change.
    - `onStart()` - method is called whenever the Activity becomes visible to the user, typically after onCreate() or onRestart().
- **What is an `intent`?**

    An intent is a messaging object that is used to request an action from other components of an application. It can also be used to launch an activity.
    There are two types of intents in Android:

    - **Implicit Intent** - Used to invoke the system components.
    - **Explicit Intent** - Used to invoke the activity class.

- **What is `context`?**

    The `context` in Android is the context of the current state of the application or object.

    There are two types of context. They are:

    **Activity context:**

    - This activity context is attached to the lifecycle of an activity.
    - The activity context can be used when you are passing the context in the scope of an activity or you need the context whose lifecycle is attached to the context of the activity.

    **Application context:**

    - This application context is attached to the lifecycle of an application.
    - The application context should be used where you need a context whose lifecycle is separate from the current context or when you are passing a context beyond the scope of activity.

- **What’s the difference between `commit()` and `apply()` in SharedPreferences?**

    - `commit()` - writes the data synchronously and returns a boolean value of success or failure depending on the result immediately.

    - `apply()` - is asynchronous and it won’t return any boolean response. Also if there is an apply() outstanding and we perform another commit(). The commit() will be blocked until the apply() is not completed.
- **What is `MVP architecture`?**
    
    The View includes the xml and the activity/fragment classes. So the activity would ideally implement a view interface making it easier for unit testing (since this will work without a view).
    
- **What is `MVVM(Model View ViewModel)`?**

    MVVM is a software design pattern that is used for developing user interfaces. It is derived from MVC, but it uses a different approach to separating the concerns of the application. In MVVM, the ViewModel is responsible for handling the data and the business logic, while the View is responsible for displaying the data.
![68747470733a2f2f646576656c6f7065722e616e64726f69642e636f6d2f746f7069632f6c69627261726965732f6172636869746563747572652f696d616765732f66696e616c2d6172636869746563747572652e706e67](https://user-images.githubusercontent.com/80090908/206382033-421c30fb-fdc9-4954-89af-fc37e53700be.png)

- **What is `ViewModel`?**

    ViewModel is a class that is responsible for preparing and managing the data for an `Activity` or a `Fragment`. It also handles the communication of the Activity / Fragment with the rest of the application
    
- **Is it necessary to use the data binding library with `MVVM` on Android?**

    While the data binding library is not required to use MVVM on Android, it can greatly simplify the process. The data binding library allows you to bind data directly to views, eliminating the need for manual view updates. This can help to keep your code clean and maintainable.
    
- **Why do you think MVVM is a better choice than MVC for developing Android apps?**

    I think that MVVM is a better choice for developing Android apps for a few reasons. 
    - First, it allows for a more separation of concerns between the different parts of the app, which can make development and maintenance simpler. 
    - Second, it can make it easier to bind data to the UI, since the ViewModel can act as a mediator between the data and the View. 
    - Finally, it can help to improve performance, since the ViewModel can handle tasks that would otherwise need to be done on the UI thread.
    
- **Explain how `data binding` works in MVVM?**

    Data binding is a process that allows you to automatically synchronize your ViewModel and View. When data binding is enabled, any changes that you make to your ViewModel will be automatically reflected in your View. This makes it easier to keep your View and ViewModel in sync, and can help to reduce the amount of boilerplate code that you need to write.
    
- **What is `LiveData`? Why should we use it in our android app?**

    `LiveData` is a data holder class that can be observed within a given lifecycle. This means that you can observe LiveData objects for changes and update the UI accordingly. LiveData is especially useful in Android applications because it helps to avoid memory leaks and can automatically update the UI when data changes.
    
    
### Kotlin Questions

- **What is the difference between the variable declaration with `var` and `val`?**

    If you want to declare some mutable(changeable) variable, then you can use `var` . For the immutable variable, use `val` i.e. val variables can't be changed once assigned.

- **What is the difference between the variable declaration with `val` and `const`?**

    Both the variables that are declared with `val` and `const` are immutable in nature. But the value of the `const` variable must be known at the compile-time whereas the value of the `val` variable can be assigned at runtime also.
    
- **What is the difference between `safe calls(?.)` and `null check(!!)`?**

    - Safe call operator i.e. ?. is used to check if the value of the variable is null or not. If it is null then null will be returned otherwise it will return the desired value.
    
    ```    
    var name: String? = "Aritra"
    println(name?.length) // 6
    name = null
    println(name?.length) // null
    ```
    
    - If you want to throw NullPointerException when the value of the variable is null, then you can use the null check or !! operator.
    
    ```
    var name: String? = "MindOrks"
    println(name?.length) // 8
    name = null
    println(name!!.length) // KotlinNullPointerException
    ```
    
- **What is String Interpolation in Kotlin?**

    If you want to use some variable or perform some operation inside a string then String Interpolation can be used. You can use the `$` sign to use some variable in the string or can perform some operation in between `{}` sign.
    
    ```
    var name = "Aritra Das"
    print("Hello! I am learning from $name")
    ```
    
- **When to use the `lateinit` keyword in Kotlin?**

    The `lateinit` keyword allows you to avoid initializing a property when an object is constructed. If your property is referenced before being initialized, Kotlin throws an UninitializedPropertyAccessException, so be sure to initialize your property as soon as possible.
    
- **What's the difference between lazy and Lateinit?**

    [Learn from here in a detailed way](https://stackoverflow.com/questions/36623177/property-initialization-using-by-lazy-vs-lateinit)
