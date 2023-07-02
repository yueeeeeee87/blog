---
title: "Tableau Project: Disaster Analysis"
date: 2023-2-2T11:30:03+00:00
# weight: 1
# aliases: ["/first"]
tags: ["Tableau", "BI system", 'Tableau Prep']
author: "Yueh-Huan, Ho"
# author: ["Me", "You"] # multiple authors
showToc: true
TocOpen: false
draft: false
hidemeta: true
comments: false
description: ""
canonicalURL: "https://canonical.url/to/page"
disableHLJS: true # to disable highlightjs
disableShare: false
disableHLJS: false
hideSummary: false
searchHidden: true
ShowReadingTime: true
ShowBreadCrumbs: true
ShowPostNavLinks: true
ShowWordCount: true
ShowRssButtonInSectionTermList: true
UseHugoToc: true
cover:
    image: "/Tableau Disaster/cover.png" # image path/url
    alt: "<alt text>" # alt text
    caption: "<text>" # display caption under cover
    relative: false # when using page bundles set this to true
    hidden: true # only hide on current single page
editPost:
    URL: ""
    Text: "test" # edit text
    appendFilePath: true # to append file path to Edit link
---

<div class='tableauPlaceholder' id='viz1688178741966' style='position: relative'><noscript><a href='#'><img alt='Disaster Overview Dashboard ' src='https:&#47;&#47;public.tableau.com&#47;static&#47;images&#47;Da&#47;DashboardStory_16858746438580&#47;Story1&#47;1_rss.png' style='border: none' /></a></noscript><object class='tableauViz'  style='display:none;'><param name='host_url' value='https%3A%2F%2Fpublic.tableau.com%2F' /> <param name='embed_code_version' value='3' /> <param name='site_root' value='' /><param name='name' value='DashboardStory_16858746438580&#47;Story1' /><param name='tabs' value='no' /><param name='toolbar' value='yes' /><param name='static_image' value='https:&#47;&#47;public.tableau.com&#47;static&#47;images&#47;Da&#47;DashboardStory_16858746438580&#47;Story1&#47;1.png' /> <param name='animate_transition' value='yes' /><param name='display_static_image' value='yes' /><param name='display_spinner' value='yes' /><param name='display_overlay' value='yes' /><param name='display_count' value='yes' /><param name='language' value='en-US' /><param name='filter' value='publish=yes' /></object></div>                <script type='text/javascript'>                    var divElement = document.getElementById('viz1688178741966');                    var vizElement = divElement.getElementsByTagName('object')[0];                    vizElement.style.width='100%';vizElement.style.height=(divElement.offsetWidth*0.75)+'px';                    var scriptElement = document.createElement('script');                    scriptElement.src = 'https://public.tableau.com/javascripts/api/viz_v1.js';                    vizElement.parentNode.insertBefore(scriptElement, vizElement);                </script>





## Project Goals
The goal of this project is to identify trends and patterns in the occurrence of disasters, through analyzing historical disaster data. The deliverable of this project focuses on the magnitude of  damage and the frequency of occurrence within certain time periods, and within certain regions.
 
End User
We can assume several end-users to whom we will provide this dashboard. One is NGO Organizations like Red Cross or Médecins Sans Frontières, MSF which need to allocate the staff to the specific area. Another one which we can imagine is insurance companies and policy makers in terms of demand for disaster insurance. 


## Data Sources and Prep
Data 1: 
-	Name: EM-DAT(Emergency Events Database) 
-	EM-DAT | The international disasters database (emdat.be)
-	Source: The dataset was launched in 1988 by the Centre for Research on the Epidemiology of Disasters (CRED), with support from the World Health Organisation (WHO) and the Belgian Government. The primary objective of EM-DAT is to support humanitarian action on both national and international levels. 
-	Data Size: EM-DAT holds essential core data regarding over 22,000 mass disasters worldwide, spanning from 1960 to the present day. 
-	Columns:
Data 2:
-	Name: Demographic Overview
-	International Database (census.gov)
-	Source: The dataset comes from the International Data Base (IDB)  developed by the United States Census Bureau. The IDB is an online tool that provides access to a wide range of demographic and socio-economic data for countries around the world. 
-	Data Size: The data ranges from 1950 to 2022 in time series, and records population in the specific year across 227 countries.
-	Columns: Country/Area Name; Year; Population; Annual Growth Rate %

Data Preparation:
1.	Load EMDAT data
2.	Correct wrong data information in EMDAT data, including country names, and date
3.	Load World Census data
4.	Joining EMDAT data with world census data on country name and year
5.	Remove duplicates after first join 
6.	Remove columns with too many missing values
7.	Output final dataset for the dashboard
 

## Dashboard Interactions and Findings 

I.	Dashboard1: Disaster Overview
This dashboard gives an overview of disaster occurrences within a certain year. Users can look into data for specific continent/ country/year with three filter options on the top of the dashboard. In order to make the plots more intuitive and easy to understand, we ask the user to choose only one year at a time.
We create a new calculated field called per capita loss, representing the total damages in dollar amount divided by population in that country. The higher the value, the larger the per-capita disaster damage in that country. This is useful when comparing the level of damage in countries with very different population sizes.

1.	Disaster Map: a map colored by the average of ‘Total Death’ in each disaster
2.	Number of Deaths by Disaster’s Type: a pie chart showing the proportion of ‘Total Death’ from each kind of disaster, colored by the disaster type
3.	Disaster Frequency: a treemap showing the frequency of each type of disaster, and highlighting the most frequent disaster type and how often it happens
4.	Loss per capita: a bubble plot showing the average dollar amount of damage per capita in the selected countries in a certain year. Each bubble represents a country. The larger the bubble, the more severe dollar amount damage that country suffered.

II.	Dashboard2: Disaster Insights
This dashboard gives a more detailed view of damage happening within a certain range of time. In this dashboard, users can still narrow down the countries or continents through adjusting the filters. In addition, users can choose the time range specific to dates. The two heatmaps in the dashboard display the number of human casualties and the amount of damage loss provides information on country-specific disasters in chronological order.

1.	Country Total Death: a symbol map showing circles for each selected country, while the size of circle indicating the sum of ‘Total Death’ within the time range.
2.	Total Death by Disaster Type: a heatmap showing the sum of ‘Total Death’ caused by each type of disaster in each year. A darker color indicates that type of disaster killed more people in that year.
3.	Loss Per Capita by Disaster Type: a heatmap showing the sum of ‘Per capita loss’ caused by each type of disaster in each year. A darker color indicates that type of disaster caused more economic loss in that year.

III.	Dashboard3: Disaster Insured Damage $
This dashboard provides a view of how much damage in dollar amount is insured. In this dashboard, we allow users to select one year at a time. Through selecting the country in the pie chart, users can narrow down to see in a country what type of disaster occurred and how much of the damages are covered by the insurance. This dashboard serves global insurance companies who are seeking opportunities/ demands. It also serves policy makers to show the disaster risk within their country and to suggest a proper amount of national budgets for insurance.
One new calculated field is created to filter out the data with insurance information only. This filter is applied when comparing the total of insured damage dollar amount and the total damage amount.

1.	Total Insured Damage $: a pie chart showing proportions of total insured damage amount for each country.
2.	Insured Damage v.s. Total Damage: a bar chart comparing the insured damage amount versus the total damage amount for each disaster type
3.	Insured Damage $ for each Disaster Type: a bar chart showing the total insured damage amount by each disaster type, in a descending order
4.	Disaster Map: a map indicating the total insured damage amount of each country in a certain year. The darker the color on the map, the higher the total insured amount in that country.
	

BI Document 
Group member: Shunsuke Iwata, YuehHuan Ho, Jiahui Zhang