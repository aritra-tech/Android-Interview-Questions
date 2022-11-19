## Android Interview Questions
> Free CheatSheet for Android Interview Questions

## Content
- [Android](#android)

### Android 

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