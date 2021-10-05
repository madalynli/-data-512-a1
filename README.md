# DATA 512 A1
Madalyn Li <br>
Fall 2021

# Goal

The goal of the project is to analyze the monthly traffic data on the English Wikipedia page. In addition, the purpose of this project is to provide the opportunity to practice and implement scientific research methods in data collection and analysis to promote better practices for human centered data science. 

The code and steps available to reproduce the analysis is located within the jupyter notebook **hcds-a1-data-curation** in this repository. 

# Data Source

This project uses the [Wikimedia REST API](https://www.mediawiki.org/wiki/Wikimedia_REST_API) which includes data on Wikipedia page traffic from two API endpoints: Legacy Pagecounts and Pageviews. 

The Legacy Pagecounts API includes data between December 2007 and July 2016 and differentiates between the access types of desktop and mobile traffic. The documentation for the API can be found [here](https://wikitech.wikimedia.org/wiki/Analytics/AQS/Legacy_Pagecounts) and the endpoint information can be found [here](https://wikimedia.org/api/rest_v1/).

The Pageviews API includes data between July 2015 to September 2021 and differentiates between the access types of desktop, mobile-web, and mobile-app traffic. The documentation for the API can be found [here](https://wikitech.wikimedia.org/wiki/Analytics/AQS/Pageviews) and the enpoint information can be found [here](https://wikimedia.org/api/rest_v1/).

The data source liscence info can be found [here](https://www.mediawiki.org/wiki/API:Licensing). The data source terms of use can be found [here](https://www.mediawiki.org/wiki/Wikimedia_REST_API#Terms_and_conditions).

# Data Description

The table below includes a list of all the fields in the final data file along with a short description of each.

| Field    | Description |
| ----------- | ----------- |
| Year     | Year that traffic data was collected      |
| Month   | Month that traffic data was collected       |
| pagecount_all_views   |   Cumulative desktop and mobile traffic in Pagecount API      |
| pagecount_desktop_views   | Desktop traffic in Pagecount API      |
| pagecount_mobile_views   | Mobile traffic in Pagecount API        |
| pageview_all_views   | Cumulative desktop and mobile traffic in Pageview API        |
| pageview_desktop_views  | Desktop traffic in Pageview API        |
| pageview_mobile_views   | Desktop traffic in Pageview API        |


# Resources

The resources and documentation used for this analysis are listed below. These links are also included within the Jupyter Notebook file associated with each step they are referenced in.

- [English Wikipedia page views 2007 - 2018: 
Sample API code](https://public.paws.wmcloud.org/User:Jtmorgan/data512_a1_example.ipynb)
- [JSON.dump Documentation](https://www.kite.com/python/docs/json.dump)
- [Query API’s with Json Output in Python](https://towardsdatascience.com/query-apis-with-json-output-in-python-5e16182a9df)
- [Pandas.pivot_table Documentation](https://pandas.pydata.org/docs/reference/api/pandas.pivot_table.html)
- [Pandas reordering data frame columns Documentation](https://www.kite.com/python/answers/how-to-reorder-columns-in-a-pandas-dataframe-in-python)
- [Matplotlib xticks Documentation](https://matplotlib.org/stable/api/_as_gen/matplotlib.pyplot.xticks.html)


# Additional Notes

The Pageview API includes traffic data on web crawlers and spiders as well. However, we have eluded this from our data cleaning process by just filters to organic user traffic (agent = user). The Pagecount API, however, does not have the option to filter to only organic user traffic. 

There is only a year of overlapping data available between the PageCount and Pageview APIs, thus the graph from the analysis produced only shows the information from July 2015 to July 2016.
