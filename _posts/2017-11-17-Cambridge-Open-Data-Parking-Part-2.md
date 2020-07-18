---
layout: post
title: 'Cambridge Open Data: Parking Tickets Part 2'
subtitle: A tale of five squares.
tags: [Analysis]
comments: true
---

This article is the continuation of my Open Data series (You can read the first part here).

Cambridge is unique because there are several hubs around the city, and these hubs are usually referred to as squares. Since these squares usually have the most housing, shopping, and dining establishments, parking here is probably more of a concern. Thus, I decided to perform an analysis of tickets in the various squares using long-lat ranges.

(From lat-long.com)

Harvard: 42.3737, -71.1194971

Central: 42.3653,-71.1047745

Porter: 42.3899,-71.121164

Kendall: 42.3629, -71.0901

Davis: 42.3967, -71.1223

The ranges were approximately deduced by using a 1 degree range (ex. (long > 42.37 & long < 42.38) & (lat > -71.12 & lat < -71.11)). Ideally, I would set a radius for each square and pull all tickets in that range, so that will be something that I will look into for the future.

Based off the subsetting, I’ve listed the ticket tables for each of the squares below. Since a meter violation is the most common type for every square, I’ve listed the second most common violation and the least common violation for each square. There were also some repeated violation types and some ‘no violation’ types, so these were disregarded in this most/least listing as well.

## Harvard Square

![Photo: [https://www.robertpaul.com/real-estate/1170-massachusetts-ave-2-cambridge-ma-02138/72318589/55373411](https://www.robertpaul.com/real-estate/1170-massachusetts-ave-2-cambridge-ma-02138/72318589/55373411)](https://cdn-images-1.medium.com/max/2000/0*3EY66We4NDmPo3YH)*Photo: [https://www.robertpaul.com/real-estate/1170-massachusetts-ave-2-cambridge-ma-02138/72318589/55373411](https://www.robertpaul.com/real-estate/1170-massachusetts-ave-2-cambridge-ma-02138/72318589/55373411)*

![](https://cdn-images-1.medium.com/max/2000/0*xEX-DO5ooiBCDa7n)

Most relevant common violation: Overtime (19399)

Harvard Square is one of the most popular tourist spots in Cambridge, so this violation count makes sense. Drivers from out of town might not know the local time rules for the meters, and local drivers might be caught up in a restaurant or campus tour/event and not remember to update their parking payment.

Least relevant common violation: Fire Lane (11)

## Central Square

![Photo: [https://cambridgehistory.org/Central-Square/Central%20Square%207.html](https://cambridgehistory.org/Central-Square/Central%20Square%207.html)](https://cdn-images-1.medium.com/max/2000/1*ePwC5SdnGfN7C0gfh4FlyQ.jpeg)*Photo: [https://cambridgehistory.org/Central-Square/Central%20Square%207.html](https://cambridgehistory.org/Central-Square/Central%20Square%207.html)*

![](https://cdn-images-1.medium.com/max/2000/0*muy-lgBXcBjBovlx)

Most relevant common violation: Resident Permit Only (1123)

Central Square is a popular residential area, especially for those who work in Kendall or Boston, so the number of resident permit spots are probably higher than in other areas. There are also some popular establishments (Toscanini’s Ice Cream, The Middle East, Central Square Theater) that bring in residents from other areas, so this could cause the high number of resident permit violations.

Least relevant common violation: Fire Lane (1)/Within Intersect(1)

## Porter Square

![Photo: [https://www.cambridgebikesafety.org/2018/01/18/porter-square-intersection/](https://www.cambridgebikesafety.org/2018/01/18/porter-square-intersection/)](https://cdn-images-1.medium.com/max/2000/0*xdAO6OQFjP8o1SLl)*Photo: [https://www.cambridgebikesafety.org/2018/01/18/porter-square-intersection/](https://www.cambridgebikesafety.org/2018/01/18/porter-square-intersection/)*

![](https://cdn-images-1.medium.com/max/2000/0*4TX6coqSFLtDUL-c)

Most relevant common violation: Resident Permit Only (5582)

Porter Square is a predominantly residential square, so most of these violations are probably incurred by visitors to the houses in the area. The residential permit violation count is almost as high as the expired meter violation count, which shows the overwhelming nature of the resident permit regulation.

Least relevant common violation: Taxi Cab Stand (2)

## Kendall Square

![Photo: [https://www.glassdoor.com/Photos/InterSystems-Office-Photos-IMG208751.htm](https://www.glassdoor.com/Photos/InterSystems-Office-Photos-IMG208751.htm)](https://cdn-images-1.medium.com/max/2000/0*IWyjaNaU5TqR3IpY)*Photo: [https://www.glassdoor.com/Photos/InterSystems-Office-Photos-IMG208751.htm](https://www.glassdoor.com/Photos/InterSystems-Office-Photos-IMG208751.htm)*

![](https://cdn-images-1.medium.com/max/2000/0*UFSqCb7b1Mvnb-bl)

Most relevant common violation: Overtime (6892)

Kendall Square is a hub of technology and biological companies, so most of these overtime violations are most likely from workers who were not able to update their parking payment due to work obligations. Resident permit violations are also high, and this is probably due to the recent increase in luxury apartment development in the area.

Least relevant common violation: Bus Stopping Other T (2)

## Davis Square

![Photo: [https://thesomervillenewsweekly.blog/2018/07/23/somerville-davis-square-planning-meeting-%E2%80%AAjuly-31%E2%80%AC/](https://thesomervillenewsweekly.blog/2018/07/23/somerville-davis-square-planning-meeting-%E2%80%AAjuly-31%E2%80%AC/)](https://cdn-images-1.medium.com/max/2000/0*O41eBfl8fv64aBwg)*Photo: [https://thesomervillenewsweekly.blog/2018/07/23/somerville-davis-square-planning-meeting-%E2%80%AAjuly-31%E2%80%AC/](https://thesomervillenewsweekly.blog/2018/07/23/somerville-davis-square-planning-meeting-%E2%80%AAjuly-31%E2%80%AC/)*

![](https://cdn-images-1.medium.com/max/2000/0*WlIP8vpVBQNI61gL)

Most relevant common violation: Resident Permit Only (2404)

Davis Square is another primarily residential area, similar to Porter Square. The overall number of violations is relatively low as well, which could be due to a number of reasons: lower regulation and enforcement, lower overall parking traffic, etc.

Least relevant common violation: No Standing Area (2)/ Taxi Cab Stand (2)

This quick analysis was able to show how data can paint a picture about the geographic diversity in a city like Cambridge. Further analysis on this data could help police departments and city planners to modify current parking arrangements, ensuring that responsible parking is balanced and maintained.

As always, my code will be on my [Github repo](https://github.com/vkumaresan/Open-Data). This will conclude my blog series on the Parking Tickets dataset, although I will probably continue my analysis separately. My next Open Data series will be on the Residential Report dataset.

*Originally published at [http://datainallthings.wordpress.com](https://datainallthings.wordpress.com/2017/11/17/cambridge-open-data-parking-tickets-part-2/) on November 17, 2017.*
