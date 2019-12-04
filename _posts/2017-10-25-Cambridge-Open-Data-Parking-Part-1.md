
# Cambridge Open Data: Parking Tickets



The City of Cambridge has an open data portal, as well as a [Civic Innovation Challenge Inventory](https://data.cambridgema.gov/General-Government/Civic-Innovation-Challenge-Inventory/x96z-hdnh/data) that contains problem statements related to the open datasets. This article will be the first of a series of posts that I plan to make where I tackle and explore these challenges.

I decided to start with the ‘Cambridge Parking Tickets’ dataset, which has this problem statement:

‘ *How can you use this data to help us improve regulation of parking availability in Cambridge?* ‘

When I first moved to Cambridge, I decided to not bring my car with me, and this was mainly due to two reasons: a) Public transportation and Uber are effective for traveling to most places in Boston and Cambridge, and b) Parking is a hassle! Not only are parking spaces and permits expensive, but it is also difficult to find parking spots around the city, and so I ultimately decided that I would be better off without my car. But for those who do use their car in Cambridge, our city should do a better job of servicing their needs, and this dataset has the potential to highlight high-need areas around the city.

The dataset contains 1,027,980 rows (tickets) and 5 columns, which are described below (taken from the Cambridge Open Data website):

**Ticket Issue Date:** This is the actual calendar date when the violation was issued. Even Legal Holidays will appear on some violation data since Police will patrol the streets even on these days.

**Issue Time:** This column contains the actual time the violation was issued. The format is HH:MM and an indicator of AM or PM.

**Location:** This column contains the officer’s or issuer’s best description of where the violation occurred. Violations often need to be described only as a Street Number and Street Name. Others need to describe an intersection of two streets or that the violation was observed Opposite to Street Number and Name. Some may even describe a generic location such as a Park or Mall. An Asterisk will indicate the location is a Parking Meter at Street Number and Name.

**Violation Description:** The Violation Description is the officer’s or issuer’s best description of the actual violation or infraction and often makes reference to the posted sign or display that indicates what is wrong. No Stopping or No Parking refer to the posted sign visible to the driver that the area is restricted in some way. Expired Meter indicates the meter is flashing or displays an expired indicator. Overtime would indicate the vehicle has exceeded the allotted time allowed to park.

**Meter:** This column contains data when the violation is for an Expired Meter. It lists the actual meter number that is visible on the meter’s post or visible on a label that appears within the meter’s glass-globe.

I wondered if I could map this data, either using R visualization packages or Tableau Public, so I had to prep the data for this reason. The ‘Location’ column could be used for this, but the problem is that it’s in string format, and contains both the full street address and the latitude/longitude coordinates. A sample field looks like this:

“1100 CAMBRIDGE ST\nCambridge, MA\n(42.37304187600046, -71.09569369699966)”

So, if I want to end up with a longitude column and a latitude column, then I would have to extract these values and convert them to a numeric value. To do this, I used the gsub function (in the gsubfn package) and the str_split function (in the stringr package) and ended up with separated longitude and latitude values for each ticket.

To visualize this, I brought the data into Tableau Public and created a dashboard; sadly, WordPress doesn’t offer integration of Tableau dashboards, so I have linked it below.
[***Cambridge Parking Tickets Map***
Cambridge Parking Tickets Mappublic.tableau.com](https://public.tableau.com/views/CambridgeParkingTicketsMap/Map?:showVizHome=no&:embed=true)

But I still wanted to analyze the data further in R, so I pulled in the data and ran some quick summary statistics on various parameters. I was curious about the distribution of the violations, so I ran a query and checked:

![](https://cdn-images-1.medium.com/max/2000/0*-yUGGaEeRYD932zr)

Clearly the overwhelming majority of violations were due to expired meters (697,566), and the next highest were due to overtime (95,486) and resident permit violations (93,587).

From this initial analysis, I have identified further questions and areas of interest that I want to pursue. I will build upon the dashboard and focus on specific insights that can highlight parking deficiencies in the city.

I will be uploading my code to my Github page:

[https://github.com/vkumaresan/Cambridge-Open-Data](https://github.com/vkumaresan/Cambridge-Open-Data)

*Originally published at [http://datainallthings.wordpress.com](https://datainallthings.wordpress.com/2017/10/25/cambridge-open-data-parking-ticket-analysis/) on October 25, 2017.*
