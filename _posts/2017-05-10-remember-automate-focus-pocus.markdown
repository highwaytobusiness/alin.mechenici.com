---
title: remember - automate - focus - pocus
date: 2017-05-10 13:11:00 +03:00
categories:
- ios
- workflows
tags:
- workflow
- omnifocus
- rememberthemilk
layout: post
---

Remember the Milk is the task list software that I am came back several times after I tried many other similar (or not) solutions for activity planning and tracking. 

Omnifocus is the professional iOS app that I bought thinking that someday I will need it.  

Since I am using workflow app almost on a daily basis, I decided to use more omnifocus and to try to automate as much as possible. Let's see what I managed to do so far. 


## Siri integration
Using Siri (via Reminders app) you can add tasks to both apps (RTM and Omnifocus) Reminder not included because it will be deleted automated after RTM task is added. 

This is how you can use it:

	“Siri, remember to…” records a task to the system default Reminders list. OmniFocus grabs it from that list if it’s the one you have chosen to capture.

	“Siri, remind me to…at (date and time)” records a task to the default list, and assigns a due date.

	“Siri, remind me when I get to (or leave)…” records a task to the default list with a contact location attached. If you choose a specific location, make sure it matches an OmniFocus context location.

### Remember the milk[^1]
	In iOS 10, go to: Settings / Calendar / Accounts / Add Account / Other / Add CalDav
		In the 'Server' field, enter: www.rememberthemilk.com
		In the 'User Name' and 'Password' fields, enter your Remember The Milk details
	- Tap Next / Switch Calendars to off. / Make sure Reminders is switched on. / Tap Save.
	- You should be returned to Mail, Contacts, Calendars, with the account added.
	- Tap Settings. / Reminders / Default List / Remember The Milk (This step is very important).
- You're done! Start asking Siri to remind you about tasks. :)

### Omnifocus[^2]
	Omnifocus Settings (in the secret bar) / Capture / Reminders / Allow access to Reminders. 

## Workflow[^3]
Unfortunately RTM can't be directly integrated into workflow app (other than using some "hacks" like: [email](https://www.rememberthemilk.com/services/email/) or [IFTTT](https://ifttt.com/)).

Different way of using it can be found [here](http://workflow.is/docs), including the [URL scheme](http://workflow.is/docs/using-the-workflow-url-scheme).

### Omnifocus workflows

-[Reminders to Omnifocus](https://workflow.is/workflows/238374e399ae44d8b5579f33a317eccb)

-[Send file to omnifocus](https://workflow.is/workflows/ba19cd41b5d344cb98793bc6da490b46)

-[Omnifocus to Fantastical](https://workflow.is/workflows/4155520185af4763846452de77513e24)

-[Copy omnifocus only](https://workflow.is/workflows/e87d55ca974641cfbb4254c982b4ac3b)

-[Share article to Omnifocus](https://workflow.is/workflows/cb9b6e4d84a248148237c7751f31ffad)

-[Paste TaskPaper into Omnifocus](https://workflow.is/workflows/d7a565d37af84e428d81b23ac7163ec5)

-[Copy OmniFocus URL Schemes](https://workflow.is/workflows/f5ed09e10cc84a2e8a7f3e2dbc46df1e)

-[Clipboard to OmniFocus Task Notes](https://workflow.is/workflows/658cd8466fe74c2db0c57f612944fd39)


## Resources
[^1]: https://www.rememberthemilk.com/services/siri/

[^2]: https://support.omnigroup.com/collecting-with-siri-in-omnifocus-2/

[^3]: http://workflow.is/docs
