## Pandas Dataframe Comparator

On one project I found out that comparison of two pandas dataframes is quite handy for test automation.
I picked up an original idea somewhere on Internet and modified it for my needs. This class falls into a category of
Utilities. Please, feel free to copy it, if you find it useful.

The ```DfComparator``` takes two pandas dataframes and returns an empty dataframe in case if those two dataframes are equal or a
dataframe that contains all found differences. Result dataframe has an index that identifies the location of found 
differences and two coloums ```left_df``` and ```right_df``` with values that belong to corresponding dataframes.  

I may add tolerance functionality later. As far as I could see it needs:
* examination of column value types, and
* some clear logic for comparision of ascii values

Apparently, if you work with static dtypes, adding tolerance for % or absolute value differences is not such a difficult task.

To see how it works, please, run a unit test in ```tests``` folder.