——-
layout: post
title: “(un)Common Sense - MFA edition 
——-

#(un)Common Sense — MFA edition

Another day, another **Notice of Data Breach**. These notices are arriving with increasing frequency. However, today was a surprise. The US Postal Service delivered two incident notices: one from Ticketmaster and the other from Change Healthcare. Both provide the usual very cursory overview of the breaches and what I, as an impacted individual, can do to protect myself from improper use of the exposed data.

Fortunately, news and regulatory reporting provide insight into what caused these breaches.

Ticketmaster explains in a [notice](https://help.ticketmaster.com/hc/en-us/articles/26110487861137-Ticketmaster-Data-Security-Incident) that the data breach originated from an “isolated cloud database hosted by a third-party data services provider.” This suggests limited impact since only one database was breached. However, the [lawsuit](https://www.classaction.org/media/ryan-et-al-v-ticketmaster-llc-et-al.pdf) filed in California claims the entire database with 560 million customers was exposed.

Ticketmaster’s wording also implies a third\-party is responsible for the breach. It has been widely reported that Ticketmaster is one of several firms whose Snowflake databases were breached. Wired’s [story](https://www.wired.com/story/epam-snowflake-ticketmaster-breach-shinyhunters/) suggests that the breached account credentials were harvested from another third-party who stored the usernames and passwords insecurely. Snowflake tacitly [acknowledged](https://snowflake.discourse.group/t/detecting-and-preventing-unauthorized-user-access/8967) that a lack of multi-factor authentication on production databases caused these customer data breaches.

While leaking 560 million customer records is gigantic, the Change Healthcare data breach manifested in an even more dramatic fashion. As [reported](https://www.fiercehealthcare.com/providers/aha-94-hospitals-financially-impacted-change-healthcares-cyberattack) by Fierce Healthcare, 94% of hospitals suffered financially. The extended downtime of Change Healthcare’s payment systems pressured parent company United Health Group to advance over $6.5 billion in payments and no-interest loans to providers and forced UHG CEO, Andrew Witty, to testify before Congress. In his [written](https://s3.documentcloud.org/documents/24626988/uhgs-witty-house-testimony.pdf) and spoken testimony, Witty confessed that a “Change Healthcare Citrix portal … did not have multi-factor authentication.”

Having worked for a system vendor to UHG, I have been on the receiving end of their security requirements. Authentication and access to critical systems requires multi-factor authentication. These breaches can be prevented by using MFA. Yet implementing MFA seems to be oddly uncommon.