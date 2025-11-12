# Pandas Quick Reference

For examples of these functions in action, refer to the workshop notebook!

## Useful `pandas` functions

**Note**: In this table, `df` represents your dataframe variable

| Function | Purpose |
| --- | --- |
| `df.describe()` | Computes summary statistics for numerical columns |
| `df["colname"]` | Selects column and outputs the column as a series  |
| `df[["colname"]]` | Selects column and outputs the column as a dataframe |
| `df["colname"].value_counts()` | Counts unique values in specified column |
| `df[df["colname"] == 'searchTerm']` | Filters your dataframe to only show rows that include the search term |
| `df["colname"].isna()` **OR** `df["colname"].notna()` | Checks for values that are NaN (aka cells that are empty) |
| `df["colname"].fillna("text")` | Replaces NaN values with specified "text" |
| `df.rename(columns={"current_colname": "new_colname"})` | Allows you to rename column |
| `df.drop(columns="colname")` | Removes or "drops" column from dataframe |
| `df["new_colname"] = ["list", "of", "values"]` | To add a new column, simply declare column name and then assign the values (as a list) you want to use to populate the column |
| `df["colname"].str.lower()` | Example of how any string methods can be used to transform all strings in specified column of dataframe |

## Further Resources
- [Pandas in 10 Minutes](https://pandas.pydata.org/pandas-docs/stable/user_guide/10min.html)