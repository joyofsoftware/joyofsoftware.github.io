---
layout: post
title: Common (non)Sense - Ticketmaster & Change Healthcare
author: earl
tags: security
excerpt: Another day, another Notice of Data Breach. Though these notices are arriving with increasing frequency.... These breaches can be prevented by using multi-factor authentication. Yet organizations continue to subject us to this all too common nonsense.
---
Another day, another _Notice of Data Breach_. Though these notices are arriving with increasing frequency, today was a surprise. The US Postal Service delivered two incident notices: one from Ticketmaster and the other from Change Healthcare. Both provide the usual very cursory overview of the breaches. Fortunately, news and regulatory reporting provide insight into the impacts and underlying cause.

![Ticketmaster Notice of Data Breach](/assets/img/2024-07-17-ticketmaster.jpg)
![Change Healthcare Notice of Data Breach](/assets/img/2024-07-29-changehealthcare.jpg)

Ticketmaster explains in their [help center](https://help.ticketmaster.com/hc/en-us/articles/26110487861137-Ticketmaster-Data-Security-Incident){:target="_blank"}{:rel="noopener noreferrer"} that the data breach originated from an “isolated cloud database hosted by a third-party data services provider.” This suggests limited impact since only one database was breached. However, the [lawsuit](https://www.classaction.org/media/ryan-et-al-v-ticketmaster-llc-et-al.pdf){:target="_blank"}{:rel="noopener noreferrer"} filed in California claims that the database was exceptionally large with data of 560 million customers.

Ticketmaster’s wording also implies a third\-party is responsible for the breach. It has been widely reported that Ticketmaster is one of several firms whose Snowflake databases were compromised. Wired’s [story](https://www.wired.com/story/epam-snowflake-ticketmaster-breach-shinyhunters/){:target="_blank"}{:rel="noopener noreferrer"} suggests that account credentials were harvested from another third-party who stored the usernames and passwords insecurely. Snowflake [blames](https://snowflake.discourse.group/t/detecting-and-preventing-unauthorized-user-access/8967){:target="_blank"}{:rel="noopener noreferrer"} the **lack of multi-factor authentication** on production databases for these customer data breaches.

While leaking 560 million customer records is gigantic, the Change Healthcare data breach manifested in an even more dramatic fashion. As [reported](https://www.fiercehealthcare.com/providers/aha-94-hospitals-financially-impacted-change-healthcares-cyberattack){:target="_blank"}{:rel="noopener noreferrer"} by Fierce Healthcare, 94% of hospitals suffered financially. The extended downtime of Change Healthcare’s payment systems pressured parent company United Health Group to advance over $6.5 billion in payments and no-interest loans to providers and forced UHG CEO, Andrew Witty, to testify before Congress. In his [written](https://s3.documentcloud.org/documents/24626988/uhgs-witty-house-testimony.pdf){:target="_blank"}{:rel="noopener noreferrer"} and spoken testimony, Witty confessed that a “Change Healthcare Citrix portal … **did not have multi-factor authentication**.”

Having been a vendor to UHG, I have been on the receiving end of their security requirements which include multi-factor authentication for access to critical systems. These breaches can be prevented by using multi-factor authentication. Good security practices dictate the use of multi-factor authentication. Yet organizations continue to subject us to this all too common nonsense.