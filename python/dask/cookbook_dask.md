# Dask Cook Book

Dask [Dataframe](https://docs.dask.org/en/latest/dataframe.html) guide


---
### import all as csv

basic import

    import dask.dataframe as dd
    df = dd.read_csv('2014-*.csv')
    df.head()
         x  y
      0  1  a
      1  2  b
      2  3  c
      3  4  a
      4  5  b

import columns as type

    df = dd.read_csv(os.path.join('data', 'nycflights', '*.csv'),
               parse_dates={'Date': [0, 1, 2]},
               dtype={'TailNum': str,
                      'CRSElapsedTime': float,
                      'Cancelled': bool})

### typical survey clean & export

    brick = dd.read_csv('*.csv', dtype={'Region':str})  # bring in everything as dask Dataframe specifiying a column to be 'str' values

    df = brick.compute() # convert dask dataframe to pandas dataframe <- only do this if the dataframe is small and you are not taking advantage of the memory efficiency of dask

    df.dropna(subset = ["Your Name"],inplace=True)
    df['Region'].fillna('NAm', inplace=True)
    df.to_csv('final_stop_work.csv', index=False)
