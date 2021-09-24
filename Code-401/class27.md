#### Resources:
- [RecyclerView for displaying lists of data](https://developer.android.com/guide/topics/ui/layout/recyclerview#java)

#### [lab](https://github.com/Ahmad-A2020/taskmaster):
![lab27](C:\Users\Ahmad\asac\reading-notes\Code-401\ScreenShot\lab27-1.PNG)
![lab27](C:\Users\Ahmad\asac\reading-notes\Code-401\ScreenShot\lab27-2.PNG)

#### Android Tasks and the Back Stack
- A task is a collection of activities that users interact with when performing a certain job. 
- The way Android manages tasks and the back stack by placing all activities started in succession in the same task and in a "last in, first out" stack.
- Launch modes allow you to define how a new instance of an activity is associated with the current task. You can define different launch modes in two ways:
#### Android SharedPreferences
- **Save key-value data**: If you have a relatively small collection of key-values that you'd like to save, you should use the SharedPreferences APIs. A SharedPreferences object points to a file containing key-value pairs and provides simple methods to read and write them.
- **Get a handle to shared preferences**:
       - `getSharedPreferences()` — Use this if you need multiple shared preference files identified by name, which you specify with the first parameter.
  
       - `getPreferences()` — Use this from an Activity if you need to use only one shared preference file for the activity.
- **Write to shared preferences**: To write to a shared preferences file, create a SharedPreferences.Editor by calling edit() on your SharedPreferences.
- **Read from shared preferences**: To retrieve values from a shared preferences file, call methods such as getInt() and getString()







### Create dynamic lists with RecyclerView

- Definition : The RecyclerView class extends the ViewGroup class and implements ScrollingView interface. It is introduced in Marshmallow. It is an advanced version of the ListView with improved performance and other benefits. RecyclerView is mostly used to design the user interface with the fine-grain control over the lists and grids of android application.
- Key classes": Several different classes work together to build your dynamic list.
       - RecyclerView is the ViewGroup that contains the views corresponding to your data.
       - Each individual element in the list is defined by a view holder object.
       - The RecyclerView requests those views, and binds the views to their data, by calling methods in the adapter.
       - The layout manager arranges the individual elements in your list.
- Steps for implementing your RecyclerView:
       - First of all, decide what the list or grid is going to look like.
       - Design how each element in the list is going to look and behave. Based on this design, extend the ViewHolder class.
       - Define the Adapter that associates your data with the ViewHolder views.
- Plan your layout: The items in your RecyclerView are arranged by a LayoutManager class. The RecyclerView library provides three layout managers, which handle the most common layout situations:
       - LinearLayoutManager arranges the items in a one-dimensional list.
       - GridLayoutManager arranges all items in a two-dimensional grid:
       - StaggeredGridLayoutManager is similar to GridLayoutManager, but it does not require that items in a row have the same height (for vertical grids) or items in the same column have the same width (for horizontal grids).
- Implementing your adapter and view holder:  When you define your adapter, you need to override three key methods:
       - onCreateViewHolder(): RecyclerView calls this method whenever it needs to create a new ViewHolder.
       - onBindViewHolder(): RecyclerView calls this method to associate a ViewHolder with data.
       - getItemCount(): RecyclerView calls this method to get the size of the data set.
