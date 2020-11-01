## What is Grafana?
Grafana is open-source visualization and analytics software. It allows you to query, visualize, alert on, and explore your metrics no matter where they are stored. In plain English, it provides you with tools to turn your time-series database (TSDB) data into beautiful graphs and visualizations.

Grafana helps us track the user behavior, application behavior, frequency of errors popping up in production or a pre-prod environment, type of errors popping up & the contextual scenarios by providing relative data.

After creating a dashboard, there are many possible things you might do next. It all depends on your needs and your use case.

![grafana.dashboard_1.png](images/grafana.dashboard_1.png)

For example, if you want to view weather data and statistics about your smart home, then you might create a playlist. If you are the administrator for a corporation and are managing Grafana for multiple teams, then you might need to set up provisioning and authentication.

It is expandable through a plug-in system. End users can create complex monitoring dashboards using interactive query builders.

Besides the core open-source solution, there are other two services offered by the Grafana team for businesses known as the Grafana Cloud & the Enterprise.

Grafana Cloud is a highly available, fast, fully managed OpenSaaS metrics platform operated by Grafana Labs.

Grafana Enterprise is a commercial edition of Grafana that includes additional features not found in the open-source version. Building on everything you already know and love about Grafana, Grafana Enterprise includes exclusive data source plugins and additional features like Authentication & Security. On top of that, you get 24x7x365 support and training from the core Grafana team.


## Why Grafana?
While there are many solutions in the data visualization space, Grafana is proving to be one of the most exciting, exhibiting rapid growth in scope and features, broad options for deployment and support, and an enthusiastic community contributing to its future growth.

### Fast
The Grafana backend is written in Google's exciting new Go language, making it extremely performant when querying data sources or feeding thousands of data points to multiple dashboard panels.

### Open
Grafana supports a plugin model for its dashboard panels and data sources. The number of plugins is constantly growing as the Grafana community enthusiastically contributes to the project.

### Beautiful
Grafana leverages the attractive and powerful D3 library. Grafana provides fine-grained control over most graph elements including axes, lines, points, fills, annotations, and legends. It even offers the much sought-after dark mode.

### Versatile
Due to its plugin architecture, Grafana can support a variety of ever-growing databases (at last count, over 30) from traditional RDBMs, such as MySQL and PostgresQL, to modern TSDBs, such as InfluxDB and Prometheus. Not only can each graph display data from a variety of data sources, but a single graph can also combine data from multiple data sources.

### Free
Grafana is freely available under the Apache open source license, and if you do plan to run it in your enterprise, you can purchase tiered support.

## What Are the Features Offered by Grafana?
- This open-source framework takes care of all the analytics of our app. We can easily query, visualize, set up alerts, understand the data with the help of metrics.

- The dashboard is pretty equipped, & continually evolving, to make sense of complex data. From displaying graphs to heatmaps, histograms, Geo maps. The tool has a plethora of visualization options to understand data as per our business requirements.

- Alerts are set up & triggered like trip wires whenever an anticipated scenario occurs. These happenings can be notified on Slack or whatever communication platform the monitoring team uses.

- Grafana has native support for approx. a dozen databases. And with many more, facilitated by respective plugins.

- Either host it on-prem or any cloud platform of your choice.

- It has built-in support for Graphite & expressions like add, filter, avg, min, max functions etc. to custom fetch data.

- It also has a built-in Influx DB, Prometheus, ElasticSearch, CloudWatch support.

## Run Grafana Docker Image
The easiest and least complex installation method is to run Grafana from within a Docker container. Docker is available for all major platforms and can be downloaded by visitinghttps://www.docker.com/.

After installing Docker, open a terminal window and type in the following command:

 $ docker run -d --name=grafana -p 3000:3000 grafana/grafana
Docker will automatically download and run the latest version of Grafana for your computer's architecture. Bear in mind that since this basic container has no persistent storage, nothing will be retained if you delete the container. I suggest you run the container with a temporary volume so that Grafana's internal database will continue to exist, even if you destroy the container:

 $ docker volume create grafana-storage



            $ docker run -d --name
            =

            grafana -p 3000:3000\



            -v grafana-storage:/var/lib/grafana \

            grafana/grafana

All the necessary dependencies will be automatically downloaded with the container. It will also install in its own sandbox, so you don't need to worry about installing a stack of software that will be difficult to delete later.