Usage
=====

Basic Usage
----------

Here's how to use the basic functionality of dashcamcsv:

.. code-block:: python

    from dashcamcsv import load_and_describe, missing_report, info_summary

    # Load a dataset from a URL
    df = load_and_describe("https://raw.githubusercontent.com/mwaskom/seaborn-data/master/iris.csv")
    
    # Generate a report of missing values
    missing_report(df)
    
    # Get summary information about the DataFrame
    info_summary(df)

Visualization
------------

The package provides simple visualization functions:

.. code-block:: python

    from dashcamcsv import quick_plot, plot_advanced
    
    # Create a simple histogram
    quick_plot(df, "sepal_length", figsize=(12, 6))
    
    # Create more advanced visualizations
    plot_advanced(df, 'sepal_length', 'sepal_width', kind='scatter', figsize=(10, 8))
    plot_advanced(df, 'species', 'sepal_length', kind='box', figsize=(8, 6))
    plot_advanced(df, kind='heatmap', figsize=(12, 10)) 