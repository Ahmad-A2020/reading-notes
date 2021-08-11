

Resources:
- [RecyclerView for displaying lists of data](https://developer.android.com/guide/topics/ui/layout/recyclerview#java)


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
