# Build a chatbot using Rasa

***Problem Brief:*** Build a chatbot using [Rasa](https://rasa.com/) to converse with job seekers and provide them with relevant jobs. A lot more functionality is required in the backend for the chatbot to become useful, some of which has been discussed below. However, let your imagination run wild and think of various ways in which you could make this chatbot more useful and lifelike.  

## What are the problems and how to tackle them? 
The final goal is to build a chatbot that can: 

- Understand the **intent** in the Job seeker's question and come up with a response. Ex: "Hey, how are you doing?", our bot should recognise the input as `greet` and respond with, "Hey {name}, I'm good. How can I help you today?" (Hint: this can be done using Rasa NLU)

- repeatedly ask for missing information to create a profile of a job seeker so that it can then show relevant jobs. Ex: If our bot needs the job title and the location to search for relevant jobs and only job title is provided then it should ask for location too. (Hint: this can be done using Rasa forms)

Bot: "What job are you looking for?"   
JS:  "I'm looking for a python developer job"   
Bot: "Which location would you like to find jobs in?"   
JS:  "I want to search for jobs in Hyderabad"   
Bot: "Okay, here are python developer jobs in Hyderabad"

Lucky for us Rasa is capable of doing most of this already. Test out the [Rasa playground](https://rasa.com/docs/rasa/playground) to get a clearer understanding. 

### But how do I make the bot respond with jobs? 
For this you'll first need to scrape data from an active job board with thousands of jobs, however, for the sake of simplicity we will confine ourselves to ~35 job descriptions from the ONET database [here](https://www.onetonline.org/find/family?f=15&g=Go).

> ONET is an open database with standardised job descriptions. In our case we are using it instead of an active job board. 

What information we will scrape from the database will be dependent on the information we are planning to ask the job seeker through our chatbot. For example, if we only plan on asking the job seeker for their technical skills, then, scraping just the technical skills would be enough. 

> Technologies you could use for scraping: Selenium, Beautiful Soup, etc. 

### Where will you store all the scraped data? 
For the sake of our chatbot an excel sheet would do, however, that wouldn't be a great idea due to speed, extendability, etc. For this purpose using a database such as MySQL would be a good choice. 

**Extra:** You could also use mongoDB. Check out the mongoDB for developers course [here](https://university.mongodb.com/courses/M220P/about) if you're interested. 

Further, This will help us store job seeker profiles as and when provided through a rasa form as discussed above.

### Retrieving data and showing it to the job seeker
To code logic such as this we'll need to use [custom actions](https://rasa.com/docs/rasa/actions/) in Rasa. Finding the most relevant job and retrieving it can be done in multiple ways and it depends on the data we are taking from the job seeker (check advanced functionalities). 

## Recap

**Functionalities expected:** 
- Converse and capture details about the job seeker
- Create and store a profile of each job seeker and remember them when they come back and mention their name/phone number, etc. 
- Intelligently provide the most relevant job from the ONET database [here](https://www.onetonline.org/find/family?f=15&g=Go)
- Take and store feedback from the job seeker about the recommendation

**Advanced Functionalities (optional):**
- Instead of asking for the job seeker's skills, ask for previous projects and map them to the jobs based on that.

## What are we looking for in the submission? 
Through this assessment we are trying to simulate a work environment where you are approached with a problem and a rough idea on what to do to solve it. The rest is up to you. You'll have to:

- Research about the problem and arrive at a theoretical solution 
- Go back to the whiteboard and sketch the architecture - define classes, functionalities, interconnections etc
- Convert your idea into code 
- Validate your solution and explain why it did or didn't do well and the challenges faced

We understand that this is a tough challenge, so don't worry if you're not able to complete it in time. The purpose of the assessment is to understand your learning speed and style, thought process, execution quality and clarity.   

If you have any doubts, queries or concerns feel free to reach out to me at `rana@maprecruit.ai`. 

Happy Coding!
