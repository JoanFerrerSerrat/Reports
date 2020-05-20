# Goals of the reports Coronavirus in the world and Coronavirus in Spain
The reports I saw before doing those reports with Jupyter where static, long and cumbersome. The goals of those reports are:
<ul>
    <li>To make interactive reports with controls.</li>
    <li>To get the report always actualised.</li>
    <li>To be able to send it with a link.</li>
</ul>

# Coronavirus in the world

This report uses three datasets that are online:
<ul>
    <li>The main dataset retrieves data in format json with number of cases and deaths by country and date. It is external and gets actualised many times during the day.</li>
    <li>There is dataset created by me to provide population to the countries that missed it.</li>
    <li>There is dataset created by me to shorten the name of some countries.</li>
</ul>

First it retrieves a table and a plot. It uses summarized dataset by country where are added the measures/population with a scale of 100.000. Those are the parameters: 
<ul>
    <li>Metric to be ordered by&nbsp;(string) : It orders by the metric chosen.</li>
    <li>Min pop/country&emsp;&emsp;&emsp;&ensp;(int)&emsp;&nbsp; : It filters by the countries with a minimum population</li>
    <li>Top n rows&emsp;&emsp;&emsp;&emsp;&emsp;&ensp;&nbsp;(int)&emsp;&nbsp; : It filters by the number of top countries</li>
</ul>

Afterwards it retrieves a plot. It uses a dataset with a granularity of country and date. From the beginning it is filtered by the countries selected in the first dataset. Those are the parameters:
<ul>
    <li>Metric&emsp;&emsp; (string) : Metric to get analyzed.</li>
    <li>From Date (date)&ensp; : From the date it will be showed the data. By dafault is minimum date when data is above 0 in any country for the selected metric</li>
    <li>To Date&emsp;&nbsp; (date)&ensp; : To the date it will be showed the data. By dafault is maximum date when data is above 0 in any country for the selected metric</li>
    <li>Plot Kind&ensp;&nbsp; (string) : Plot kind applied to plot.</li>
    <li>Countries&ensp; (string) : Countries to be analyzed. It is restricted to the countries selected in the previous table and plot.</li>
</ul>
Sum means the sum in all the days.
Last means the data of the last day. 
The countries selected in this dataset will be also pre-filtered in the next graphic.

The report can be seen in [Binder](https://mybinder.org/v2/gh/JoanFerrerSerrat/Reports/master?filepath=Jupyter%2FCoronavirus_World.ipynb).

# Coronavirus in Spain

This report returns the evolution in Spain of the measures
<ul>
    <li>cases</li>
    <li>recovered</li>
    <li>hospitalized</li>
    <li>icu</li>
    <li>deaths</li>
    <li>active</li>
    <li>new_cases/active</li>
</ul>
related to coronavirus. Each measure represent the number of individuals in each situation per 100000 people.
Granularity is day and data is also shown by CA (different autonomous communities of Spain).
Each measure is ordered in a descending order 
<ul>
    <li>to compare in the graphics autonomous comunities with similar values of measures</li>
    <li>and to identify easily which autonomous comunities have higher or lower measure values</li>
</ul>
The autonomies in the autonomic graphic are showed by descending order in the measure.
The report can be seen in [Binder](https://mybinder.org/v2/gh/JoanFerrerSerrat/Reports/master?filepath=Jupyter%2FCoronavirus_Spain.ipynb).


