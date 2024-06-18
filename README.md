# Pandas Commands Reference for Data Engineering

## Table of Contents

1. [Data Loading](#data-loading)
2. [Data Saving](#data-saving)
3. [Data Inspection](#data-inspection)
4. [Data Cleaning](#data-cleaning)
5. [Data Transformation](#data-transformation)
6. [Data Manipulation](#data-manipulation)
7. [Data Aggregation](#data-aggregation)
8. [Time Series Handling](#time-series-handling)
9. [Additional Resources](#additional-resources)
    
---

### Data Loading <a name="data-loading"></a>

| Command           | Description                                      | Example Usage                       |
|-------------------|--------------------------------------------------|-------------------------------------|
| `pd.read_csv`     | Reads a CSV file into a DataFrame.                | `df = pd.read_csv('file.csv')`      |
| `pd.read_excel`   | Reads an Excel file into a DataFrame.             | `df = pd.read_excel('file.xlsx')`   |
| `pd.read_sql`     | Reads data from a SQL database into a DataFrame.  | `df = pd.read_sql(query, connection)`|
| `pd.read_parquet` | Reads a Parquet file into a DataFrame.            | `df = pd.read_parquet('file.parquet')`|
| `pd.read_hdf`     | Reads HDF5 file into a DataFrame.                 | `df = pd.read_hdf('file.h5', 'key')`|
| `pd.read_json`    | Reads a JSON string or file into a DataFrame.     | `df = pd.read_json('file.json')`    |

### Data Saving <a name="data-saving"></a>

| Command         | Description                               | Example Usage                       |
|-----------------|-------------------------------------------|-------------------------------------|
| `df.to_csv`     | Writes a DataFrame to a CSV file.          | `df.to_csv('file.csv')`             |
| `df.to_excel`   | Writes a DataFrame to an Excel file.       | `df.to_excel('file.xlsx')`          |
| `df.to_parquet` | Writes a DataFrame to the Parquet format.  | `df.to_parquet('file.parquet')`     |
| `df.to_hdf`     | Stores a DataFrame in an HDF5 file.        | `df.to_hdf('file.h5', 'key')`       |
| `df.to_json`    | Converts the DataFrame to a JSON string.   | `df.to_json('file.json')`           |

### Data Inspection <a name="data-inspection"></a>

| Command       | Description                              | Example Usage                       |
|---------------|------------------------------------------|-------------------------------------|
| `df.head`     | Returns the first n rows of a DataFrame. | `df.head(10)`                       |
| `df.tail`     | Returns the last n rows of a DataFrame.  | `df.tail(10)`                       |
| `df.info`     | Provides a summary of the DataFrame.     | `df.info()`                         |
| `df.describe` | Generates descriptive statistics.        | `df.describe()`                     |
| `df.shape`    | Returns the dimensions of the DataFrame. | `df.shape`                          |

### Data Cleaning <a name="data-cleaning"></a>

| Command       | Description                           | Example Usage                       |
|---------------|---------------------------------------|-------------------------------------|
| `df.isnull`   | Detects missing values.                | `df.isnull()`                       |
| `df.dropna`   | Removes missing values.                | `df.dropna()`                       |
| `df.fillna`   | Fills missing values.                  | `df.fillna(value)`                  |
| `df.drop`     | Drops specified labels from rows/columns. | `df.drop(columns='column_name')`  |
| `df.rename`   | Renames labels in the DataFrame.       | `df.rename(columns={'old': 'new'})` |
| `df.duplicated` | Returns boolean Series denoting duplicate rows. | `df.duplicated()`              |

### Data Transformation <a name="data-transformation"></a>

| Command          | Description                             | Example Usage                       |
|------------------|-----------------------------------------|-------------------------------------|
| `df.sort_values` | Sorts the DataFrame by specified columns. | `df.sort_values(by='column_name')`  |
| `df.groupby`     | Groups DataFrame using a mapper or by columns. | `df.groupby(by='column_name')`  |
| `df.merge`       | Merges DataFrame objects with a database-style join. | `df.merge(other_df, on='column_name')` |
| `pd.pivot_table` | Creates a pivot table as a DataFrame.    | `pd.pivot_table(df, values='value', index='index_column', columns='column_name')` |
| `df.apply`       | Applies a function along an axis of the DataFrame. | `df.apply(np.mean)`             |

### Data Manipulation <a name="data-manipulation"></a>

| Command      | Description                               | Example Usage                       |
|--------------|-------------------------------------------|-------------------------------------|
| `df.iloc`    | Integer-location based indexing for selection. | `df.iloc[0]`                      |
| `df.loc`     | Accesses rows and columns by labels or boolean array. | `df.loc['index_label']`        |
| `df.drop`    | Drops specified labels from rows/columns. | `df.drop(columns=['column_name1', 'column_name2'])` |
| `df.set_index`| Sets the DataFrame index using existing columns. | `df.set_index('column_name')`  |
| `df.reset_index`| Resets the index of the DataFrame.       | `df.reset_index()`                 |

### Data Aggregation <a name="data-aggregation"></a>

| Command      | Description                               | Example Usage                       |
|--------------|-------------------------------------------|-------------------------------------|
| `df.sum`     | Returns the sum of values for the axis.    | `df.sum()`                          |
| `df.mean`    | Returns the mean of values for the axis.   | `df.mean()`                         |
| `df.median`  | Returns the median of values for the axis. | `df.median()`                       |
| `df.min`     | Returns the minimum of values for the axis.| `df.min()`                          |
| `df.max`     | Returns the maximum of values for the axis.| `df.max()`                          |
| `df.count`   | Returns the number of non-null values for the axis. | `df.count()`                  |

### Time Series Handling <a name="time-series-handling"></a>

| Command         | Description                               | Example Usage                       |
|-----------------|-------------------------------------------|-------------------------------------|
| `pd.date_range` | Generates a DateTimeIndex.                 | `dates = pd.date_range(start='1/1/2023', periods=100)` |
| `df.resample`   | Resamples time-series data.                | `df.resample('M').mean()`           |
| `df.shift`      | Shifts index by desired number of periods. | `df.shift(periods=1)`               |
| `df.rolling`    | Provides rolling window calculations.      | `df['column_name'].rolling(window=3).mean()` |
| `df.diff`       | Calculates the difference of DataFrame elements. | `df['column_name'].diff()`    |

## Additional Resources <a name="additional-resources"></a>

For more information on using Pandas for data engineering tasks, you may find the following resources helpful:

- Official Pandas Documentation: [Pandas Documentation](https://pandas.pydata.org/docs/)
- Pandas Tutorials and Guides: [Pandas Tutorials](https://pandas.pydata.org/docs/getting_started/index.html)
- Stack Overflow: [Pandas Questions](https://stackoverflow.com/questions/tagged/pandas)
