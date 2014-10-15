---
layout: default
img: capitalist-greed
caption: Exploit the masses!
title: Homework 6 | Building the database 
active_tab: homework
---


<div class="alert alert-info">
  This assignment is due before class on Wednesday, October 22nd.</div>


Building a database<span class="text-muted"> : Assignment 6</span> 
=============================================================

Okay, so we've been talking all semester about this gun violence database. And we've been making all sorts of big promises to Doug and the other epidemiologists. But, what have we gotten so far: "Here are some articles that we are about 10% confident are about guns. Also, the word "shooting" is a good feature." Not exactly anything to write home about. So time to deliver. Let's take these articles and turn it into something useful. 

We will do this using (surprise!) crowdsourcing. This week, you are going to ask Crowdflower workers to read through the articles that you all identified as gun related back in homework 5, and pull out the key facts in a principled way. Your primary goal is to design an interface that helps them do this quickly and accurately. We will walk you through some initial steps to get you started on the design, but you are welcome to go in your own direction.  

Your deliverables will be:
1. Two csv files from Crowdflower containing the information the workers extract
2. Screen shots of your two HIT designs
3. Reponses about your findings in [this questionnaire]().

You will might want to work in teams for this porject. These HITs will require more time for the crowd workers, and so should pay a bit more than the previous ones. Don't be a jerk and pay them pennies just because your account is low! Buddie up with someone, or feel free to add some funds to your account. (We didn't have a text book for this class, remember? So we've been easy on your budget so far.)

###Code, data, and signing up for more emails

1. In assignment 5, you guys had workers label your classifier's results. To give you data to work with, we've pulled together 200 of the urls your workers called "gun related." We've also written some code to do some text processing for you, which we will talk about in a few steps. You can download all the code and data [here](). 

	<pre><code>$ wget assignment6.tgz
	$ tar -xvzf assignment6.tgz
	$ ls assignment6/
	clean_and_process_data.py	convert_to_csv.py		gun-violence-urls.txt</code></pre>

2. You should see three files. <code>gun-violence-urls.txt</code> contains 198 urls that your workers labeled as gun-related in the previous assignment. <code>clean_and_process_data.py</code> is a script which will perform basic text processing to clean up your articles and help pull out some potentially useful information (like names and locations). <code>convert_to_csv.py</code> will put your data into a csv that can be uploaded to Crowdflower. 

3. In order to do the text processing, we will be using the [Alchemy API](http://www.alchemyapi.com/api/calling-the-api/). This is a super awesome professional API which does a lot of very complicated NLP for you and makes it seem easy. In order to use it, you will need to [sign up for an account](http://www.alchemyapi.com/api/register.html) and get an API key. The default account will give you 1,000 API calls a day. This is probably enough for this assignment- you will need two calls per url, so if you only mess up one and a half times, you should still be within your daily limit. However, if you want to explor it more (which you really should! its awesome!) you can sign up for an academic account, which will give you 30,000 calls a day. If you want to do this, let me know. It just requires sending an email to the sales team, and you can copy the email I used to request my academic license.

###HIT Design

As you may remember from [Doug's lecture](), there are a lot of details about gun crimes that epidemiologists are interested in. For this assignment, you are going to ask workers to try to extract the following information: 

	- Time and place
		- City
		- State
		- Additional fine-grained location information 
		- Date
		- Time of day
	- Detials about shooter(s) (may have to answer questions multiple times if multiple victims)
		- Number of shooters
		- Name
		- Gender
		- Age
		- Race
	- Detials about victim(s) (may have to answer questions multiple times if multiple victims)
		- Number of victims
		- Name
		- Gender
		- Age
		- Race
		- Killed? 
		- Injured?
		- Hospitalized? 
	- Circumstances of shooting
		- Type of gun
		- Number of shots fired
		- Was it a case of domestic violence?
		- Did the ictim and shooter know each other?
		- Was the shooting during another crime (robbery, home invasion by the shooter, etc)?
		- Was the shooter attempting to deter a home invasion?
		- Was alcohol involved?
		- Were drugs involved?
		- Suicide or suicide attempt?
		- Inadvertent discharge of a firearm? 
		- Shooting by the police?
		- Shooting of a police officer?
		- Was the gun stolen?
		- Was the gun owned by the vitim or thier family?

You will design two HITs on Crowdflower to extract this information from the articles. In the first, you will simply provide the article and ask workers to fill in the information. In the second, you will do some preprocessing to try to make the workers' job easier. 

1. First, we will design a simple HIT. You can see my simple version [here](). You do not have to follow my designs exactly, but your design should extract the same information.

2. Upload data

3. Using CML markup

4. Now, we will use Alchemy to design a nicer HIT interface, which will hopefully allow your workers to move through the articles more quickly and accurately. You can see my design [here](https://tasks.crowdflower.com/assignments/7062734c-e446-41c6-b491-90ba89165fb2). Again, you are encoraged to improve over my template! I am a god-awful web designer, so please! Make it better so we can recycle your designs for next year's students! :-P 


This assignment is due <b>Wednesday, October 22</b>. You can work in pairs, but you must declare the fact that you are working together when you turn your assignment.  