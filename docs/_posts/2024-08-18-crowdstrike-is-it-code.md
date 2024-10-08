---
layout: post
title: CrowdStrike - Is It Code?
author: Earl Chen
tags: software
excerpt: There has already been considerable discussion about the CrowdStrike incident on 19 July 2024. There is finger pointing by CrowdStrike customers. Finger pointing between Microsoft and CrowdStrike.... On that fateful day in July, was the update that crashed 8.5 million Windows devices content or was the update code?
---
There has already been considerable discussion about the CrowdStrike incident on 19 July 2024. There is finger pointing by CrowdStrike customers. Finger pointing between Microsoft and CrowdStrike. There is finger pointing by [governments](https://apnews.com/article/crowdstrike-tech-outage-microsoft-windows-falcon-8fe725037ab975e011b2cfad67b17c0f){:target="_blank"}{:rel="noopener noreferrer"}. Finger pointing [back](https://www.theregister.com/2024/07/22/windows_crowdstrike_kernel_eu/){:target="_blank"}{:rel="noopener noreferrer"} at governments. And sadly also finger pointing by [CrowdStrike](https://www.theverge.com/2024/8/5/24213521/crowdstrike-refutes-blame-delta-outage-litigation){:target="_blank"}{:rel="noopener noreferrer"} and [Microsoft](https://www.cnn.com/2024/08/06/business/microsoft-crowdstrike-outage-delta/index.html){:target="_blank"}{:rel="noopener noreferrer"} at their customers. Laudably CrowdStrike published a detailed [root cause analysis](https://www.crowdstrike.com/wp-content/uploads/2024/08/Channel-File-291-Incident-Root-Cause-Analysis-08.06.2024.pdf){:target="_blank"}{:rel="noopener noreferrer"} and implemented a series of changes to mitigate the impact of future issues.

[![CrowdStrike Root Cause Analysis](/assets/img/2024-08-06-crowdstrike.jpg)](https://www.crowdstrike.com/wp-content/uploads/2024/08/Channel-File-291-Incident-Root-Cause-Analysis-08.06.2024.pdf){:target="_blank"}{:rel="noopener noreferrer"}

Unfortunately, the current discourse and even Crowdstrike’s own reporting has overlooked and downplayed a fundamental issue that requires more thoughtful consideration. On that fateful day in July, was the update that crashed 8.5 million Windows devices **content** or was the update **code**?

Effectively managing software development requires formalized processes for code changes, code testing, code deployment, and code retirement. The priority and rigor of these processes must scale with the size and reach deployments. Categorizing a system artifact as code brings those formalized processes into play. Categorizing the artifact as content relaxes or even removes the required rigor.

CrowdStrike calls this type of update _Rapid Response Content._ By using content in the name CrowdStrike is categorizing the update as something other than code. CrowdStrike explicitly states “Rapid Response Content is configuration data; it is not code or a kernel driver.” Digging into the documentation we find that Rapid Response Content consists of multiple Template Instances. Template Instances consist of **regex content**. CrowdStrike even tacks the word content onto the term regex to emphasize the content over code distinction. They did not explain what the difference is between regex content and a regex so we will ignore the CrowdStrike term of art and stick with the widely used single word regex and the plural form, regexes.

[Regular expressions](https://en.wikipedia.org/wiki/Regular_expression){:target="_blank"}{:rel="noopener noreferrer"} (regexes) reside in the intersection of content and code. Like both content and code, regexes are text. Unlike some code e.g. C, C++, Swift, regexes are not compiled into an executable prior to use. However, unlike content, regexes must be interpreted by a regular expression engine that reads input and creates output based on the regex. This behavior is identical to interpreted code e.g. Java, JavaScript, Python.

Whether a regex is content or code is the fundamental issue because reclassifying code as content can be used to bypass more rigorous code pipeline controls. Reading through CrowdStrike’s mitigations:

- Add runtime input array bounds checks
- Increase test coverage
- Create additional checks
- Update content configuration test procedures
- Add additional deployment layers and acceptance checks
- Provide customer control over deployment

These are all code and code pipeline improvements. Despite what CrowdStrike has written in their documentation, these mitigations clearly indicate that _Rapid Response Content_ and more significantly the way it is used within the CrowdStrike environment are **code** not content. Thankfully now it will be treated as such, but what other instances of code masquerading as content exist in CrowdStrike's platform?