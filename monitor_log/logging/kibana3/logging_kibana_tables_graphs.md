---

copyright:
  years: 2016, 2017
lastupdated: "2017-02-07"

---
<!-- Copyright info and last updated date at top of file: REQUIRED
    The copyright and lastupdated info is YAML content that must occur at the top of the MD file, before attributes are listed.
    It must be --- surrounded by 3 dashes ---
    The value "years" can contain just one year or a two years separated by a comma. (years: 2014, 2016)
    The value "lastupdated" must be followed by a machine date in quotes in the following format: "YYYY-MM-DD"
    The value for "years" must be indented 2 spaces under "copyright", followed by "lastupdated" which should start on its own non-indented line.

-->

<!-- Common attributes used in the template are defined as follows: -->
{:new_window: target="_blank"}
{:shortdesc: .shortdesc}
{:screen:.screen}
{:codeblock:.codeblock}

<!-- Additional task topic: OPTIONAL
This is the template for additional task topics that are needed beyond the basic tasks in the getting started index.md.  As needed, other task topics can be included, with titles such as "Configuring x", "Administering y", "Managing z", etc. This topic is a peer of the getting started index.md in the <servicename>.ditamap. This topic can have one level of children and they also can be referenced in <servicename>.ditamap -->

# Creating tables and graphs from queries in Kibana
<!-- for example, Uploading your data -->
{: #logging_kibana_tables_graphs}
<!-- Provide an appropriate ID above -->

<!-- The short description section should include a sentence describing why this task is needed. For search engine optimization, include the service long name and "Bluemix". For example: -->

Use Kibana to create graphs and tables for your queries to visualize your log data and compare results. You can access the Kibana dashboard from the **Logs** tab for your Cloud Foundry app. 
{:shortdesc}

<!-- Include a sentence to briefly introduce the steps/subtopics. Example: -->
The Kibana dashboard is laid out as a series of rows, with each row containing one or more panels. You can configure panels to display graphical representations of your data. Use queries to determine which data to display. To create a graph or table, you must first create a blank row; then, create a panel. If you access the Kibana dashboard from the **Logs** tab on your CF app, the dashboard automatically displays two panels: a histogram and a table.

Complete the following tasks to add a graph or table on the Kibana dashboard:

1. To access the **Logs** tab of your Cloud Foundry app, click the app name in the **Cloud Foundry Apps** table on the {{site.data.keyword.Bluemix_notm}} **Apps** dashboard; then, click the **Logs** tab. The logs for your app are displayed.

2. To access the Kibana dashboard display for your app, click **Advanced View** ![Advanced view link](images/logging_advanced_view.jpg). The Kibana dashboard is displayed.

3. On the Kibana dashboard, scroll to the bottom of the dashboard and click **ADD A ROW** ![Add a row icon](images/logging_add_row.jpg) to create a row for the panel you want to add. The Dashboard Settings pane is displayed. 
	
	![Dashboard settings pane](images/logging_dashboard_settings.jpg)
	
	In the Add Row pane, enter a name for your row in the **Title** field; then, click **Create Row**. A new row is added. You can adjust the order of the rows by clicking the **Up arrow** or **Down arrow** icons next to the row titles. When you have set the order of rows, click **Save**. An empty row is created on the Kibana dashboard.

4. Add a panel by clicking **Add panel to empty row**. The Row Settings pane is displayed.

    ![Row settings pane](images/logging_row_settings.jpg)
	
	You can choose different panel types such as **table**, **histogram**, or **terms** from the **Select Panel Type** drop-down list. Select **terms** to create a bar chart, pie chart, or table based on your queries. A range of configuration options are displayed in the Row Settings pane.
	
	![Adding a panel in the row settings pane](images/logging_add_panel.jpg)
	
	Configure your panel. Enter a **Title** for your graphical display. Select the **Span** of your panel from the drop-down list; the **Span** determines the width of your panel across the dashboard. In the Parameters section, delete the contents of **Field** and enter a valid log field; for example, `instance_id`. 

5. In the View Options section, select **bar**, **pie**, or **table** from the **Style** drop-down list to choose a bar chart, pie chart, or table. In the Queries section, select **selected** from the **Queries** drop-down list to use the log data from your dashboard queries. Finally, click **Save**. Your new panel is displayed on the dashboard.

	![Dashboard displaying panel containing bar chart](images/logging_bar_chart_panel.jpg)
	
6. To change this panel so that it displays a table, click the **Configure** icon ![Configure icon](images/logging_dashboard_config_panel.jpg). The Terms Settings pane is displayed. 

	![Terms Settings pane](images/logging_terms_settings.jpg)
	
	Click the **Panel** tab; then, select **table** from the **Style** drop-down list. Click **Save** to update the panel and return to the dashboard.

7. Add further rows and panels to your dashboard. When you are finished, save the changes to this dashboard by clicking the **Save** icon.

    **Note:** If you try to save a dashboard with a name containing blank spaces, it will not save. Enter a name without spaces and click the **Save** icon.

    ![Save dashboard name ](images/logging_save_dashboard.jpg).

