---
layout: post
title: NIST SP800-63B and WHY! CapitalOne? 
author: earl
tags: security
excerpt: Here we are on the eve of the publication of the updated NIST Digital Identity Guidelines. This has been in progress since 2020 and will update the guidelines last published in 2017. The most recent draft was released at the end of August and the final comment period comes to a close in October. The new official version is anticapted soon after. This happens to coincide with an interesting expeirence trying to reset my credentials for online access with CapitalOne.
---
Here we are on the eve of the publication of the updated NIST Digital Identity Guidelines. This has been in progress since 2020 and will update the guidelines last published in 2017. The most recent draft was released at the end of August and the final comment period comes to a close in October. The new official version is anticapted soon after. This happens to coincide with an interesting expeirence trying to reset my credentials for online access with CapitalOne.

Why CapitalOne? This is the first question to be answered, but there is a more serious question which has a rather different emphasis: **WHY!** CapitalOne? First - Why CapitalOne? - I received a new CapitalOne credit card and discovered I could not access the online account to activate the card. In fairness it had been years since I used the card and at least that long since I accessed the account online. After such an extended period I could understand why the account would be inaccessible. After making a few attempts I finally called (877) 383-4802 which was helpfully shown on the error screen. In case a CapitalOne representative is interested in checking call logs, the call was placed at 8:37AM Eastern on Friday, September 20 and was 27 minutes in duration.

Now **WHY!** CapitalOne? During the course of the support call the agent I spoke with was very patient and helpful. He checked my identity and activated the card. We worked together to update my password and I attempted to authenticate using the new credentials. Failure. The helpful agent explained that he was seeing a message that I was inputting the incorrect password. I explained that I was using a password manager so it was unlikely that the password was entered incorrectly.

The agent told me **DO NOT** use a passowrd manager. I should create a new passowrd, **WRITE IT DOWN**, and then type it is exactly as written. I didn't respond immediatley. I let the words echo around in my head. Then the sounds of Depeche Mode's _Enjoy the Silence_ started to replace the voice of the agent: 

>Words like violence
>Break the silence
>Come crashing in
>Into my little world
>Painful to me
>Pierce right through me ...
>>[Apple Music](https://music.apple.com/us/album/enjoy-the-silence/665415936?i=665416650){:target="_blank"}{:rel="noopener noreferrer"}
>>[Spotify](https://open.spotify.com/track/6WK9dVrRABMkUXFLNlgWFh?si=lquk3k0KRPaIzNJTXihm0w){:target="_blank"}{:rel="noopener noreferrer"}

To the agent's credit, he was polite and patient. Despite my assertion that his recommendation was poor practice and against current security guidelines, he never argued and he never wavered in his position that password managers should not be used on the CapitalOne site. Unfortunately, even as I reset my password again he continued to see password entry errors and the call ended without resolving my login issue.

The NIST Guidelines have been updated to account for the proliferation of online identies, inprovements in technology, and changes to user behavior to ensure credential verifiers provide safe and secure access to important (and some not so important) digital capabilities. While there are some notable changes, much of the change is evolutionary. In particular the updates to NIST Special Publication 800-63B Authentication & Authenticator Management (SP800-63B) build upon guidelines defined in 2017 which were in turn based upon research about authentication in the aughts and early teens that provided empirical support for best practices that emerged in the 90s.

One area where there was no notable change and no evolution was regarding the use of password managers. Since 2017 the Guidelines are explicit and identical to the upcoming update:

>Verifiers (CapitalOne in this case) **SHOULD** (NIST's emphasis) permit claimants to use “paste” functionality when entering a memorized secret. This _facilitates the use of password managers,_ (my emphasis) which are widely used and in many cases increase the likelihood that users will choose stronger memorized secrets.

**_WHY! CapitalOne?_**
