# Application
## 12: Further Reading and Helpful Links

This module will introduce you to all the information that you'll need to become employer-ready. But, you can become employer-competitive by diving more deeply into the topics discussed in class. Remember that the data field is constantly changing. And as a professional, you'll be expected to stay up to date on the latest developments and conversations.

If you’re interested in learning more about a particular topic or need a refresher, use the following resources:

* [MongoDB in 30 minutes](https://www.youtube.com/watch?v=pWbMrx5rVBE)

* [Python Requests library](http://docs.python-requests.org/en/master/)

* [Tutorial: Web Scraping with Python Using Beautiful Soup](https://www.dataquest.io/blog/web-scraping-tutorial-python/)

* [Splinter documentation](https://splinter.readthedocs.io/en/latest/)

* [Flask-PyMongo](https://flask-pymongo.readthedocs.io/en/latest/)

## Module 12 Challenge

### Background

You’re now ready to take on the full web-scraping and data analysis project for the mission to Mars. You’ve learned to identify HTML elements on a page, identify their `id` and `class` attributes, and use this knowledge to extract information via both automated browsing with Splinter and HTML parsing with Beautiful Soup. You’ve also learned to scrape various types of information. These include HTML tables and recurring elements, like multiple news articles on a webpage.

As you work on this Challenge, remember that you’re strengthening the same core skills that you’ve been developing until now: collecting data, organizing and storing data, analyzing data, and then visually communicating your insights.

### What You're Creating

This new assignment consists of two technical products. You will submit the following deliverables:

* Deliverable 1: Scrape titles and preview text from Mars news articles. Optionally export the data into a JSON file or a MongoDB database.

* Deliverable 2: Scrape and analyze Mars weather data, which exists in a table.

### Deliverable 1: Scrape Titles and Preview Text from Mars News (40 points)

#### Deliverable 1 Instructions

1. Create a new Jupyter notebook named `mars_data_challenge_part_1.ipynb`.

2. Scrape the [Mars News](https://redplanetscience.com) website by using Splinter and Beautiful Soup. Specifically, scrape the title and preview text, or summary text, of each article on the landing page.

    * If you’d like a hint on identifying which elements to scrape, that’s totally okay. If not, that’s great too. You can always revisit this later if you change your mind.

      > **Hint** To identify which elements to scrape, you might want to inspect the page by using Chrome DevTools.

3. Store the scraping results in Python data structures as follows:

    * Store each title-and-preview pair in a Python dictionary. And, give each dictionary two keys: `title` and `preview`. An example is the following:

      ```python
      {'title': "Mars Rover Begins Mission!", 
            'preview': "NASA's Mars Rover begins a multiyear mission to collect data about the little-explored planet."}
      ```

    * Store all the dictionaries in a Python list.

    * Print the list in your notebook.

4. Optionally, store the scraped data in a file or database (to ease sharing the data with others). To do so, export the scraped data to either a JSON file or a MongoDB database.

#### Deliverable 1 Requirements

* Automated browsing (with Splinter) was used to visit the Mars news site, and the HTML code was extracted (with Beautiful Soup). (10 points)

* The titles and preview text of the news articles were scraped and extracted. (20 points)

* The scraped information was stored in the specified Python data structure&mdash;specifically, a list of dictionaries. (10 points)

### Deliverable 2: Scrape and Analyze Mars Weather Data (60 points)

#### Deliverable 2 Instructions

1. Create a Jupyter notebook named `mars_data_challenge_part_2.ipynb`. Import the relevant dependencies for web scraping, Pandas, and Matplotlib.

2. With your automated browser, visit the [Mars Temperature Data](https://data-class-mars-challenge.s3.amazonaws.com/Mars/index.html) site. Note that the URL is `https://data-class-mars-challenge.s3.amazonaws.com/Mars/index.html`.

3. Scrape the data in the HTML table. To do so, choose one of two ways. The first, simpler way is to use Pandas's `read_html` method. The second, slightly more challenging way is to manually scrape the data by using Splinter and Beautiful Soup. We highly encourage you to choose the latter to reinforce your scraping skills.

    * If you’d like a hint on manually scraping the data, that’s totally okay. If not, that’s great too. You can always revisit this later if you change your mind.

      > **Hint** First, use DevTools to discover whether the table contains usable classes. Second, use the Beautiful Soup `find_all` method to extract all the rows with a line of code. Third, find and extract the data from each cell in a specified row, and store the data from each row in a Python list. Fourth, use a `for` loop to add the data from each row to a list that will contain the data from all the rows.

4. Assemble the scraped data into a Pandas DataFrame. The columns should have the same headings as the table on the website. Here’s an explanation of the column headings:

    - The `id` heading: The identification number of a single transmission from the Curiosity rover.
    - The `terrestrial_date` heading: The date on Earth.
    - The `sol` heading: The number of elapsed sols (Martian days) since Curiosity landed on Mars.
    - The `ls` heading: The solar longitude.
    - The `month` heading: The Martian month.
    - The `min_temp` heading: The minimum temperature, in Celsius, of a single Martian day (sol).
    - The `pressure` heading: The atmospheric pressure at Curiosity's location.

5. Examine the data types of all the DataFrame columns. If necessary, cast (or convert) the data to the appropriate `datetime`, `int`, or `float` data types.

    * If you’d like a hint on how to convert the data, that’s totally okay. If not, that’s great too. You can always revisit this later if you change your mind.

      > **Hint** You can use the Pandas `astype` and `to_datetime` methods to accomplish this task.

6. Answer the following question: How many months exist on Mars?

7. Answer the following question: How many Martian (and not Earth) days worth of data exist in the scraped dataset?

8. Answer the following question: What are the coldest and the warmest months on Mars (at the location of Curiosity)? Get the answer by averaging the minimum daily temperature of all the months. Plot the results as a bar chart.

9. Answer the following question: Which months have the lowest and the highest atmospheric pressure on Mars? Get the answer by averaging the daily atmospheric pressure of all the months. Plot the results as a bar chart.

10. Answer the following question: About how many terrestrial (Earth) days exist in a Martian year? That is, in the time that Mars circles the Sun once, how many days elapse on Earth? Visually estimate the result by plotting the daily minimum temperature.

11. Export the DataFrame to a CSV file.


#### Deliverable 2 Requirements

* The HTML table was extracted into a Pandas DataFrame. Either Pandas or Splinter and Beautiful Soup were used to scrape the data. The columns have the correct headings and data types. (15 points)

* The data was analyzed to answer the following questions, and a data visualization was created to support each answer: (40 points)

  * How many months exist on Mars?
  * Which month, on average, has the lowest temperature? The highest?
  * Which month, on average, has the lowest atmospheric pressure? The highest?
  * How many terrestrial days exist in a Martian year? A visual estimate within 25% was made.

* The DataFrame was exported into a CSV file. (5 points)
### Submission

As a reminder, the deliverables for this Challenge are as follows:

* Deliverable 1: A Jupyter notebook containing code that scrapes the Mars news titles and preview text.

* Deliverable 2: A Jupyter notebook containing code that scrapes the Mars weather data and that cleans, visualizes, and analyzes that data.

To submit your Challenge assignment, click Submit, and then provide the URL of your GitHub repository for grading.

> **Note** You are allowed to miss up to two Challenge assignments and still earn your certificate. If you complete all Challenge assignments, your lowest two grades will be dropped. If you wish to skip this assignment, click Next, and move on to the next module.

Comments are disabled for graded submissions in Bootcamp Spot. If you have questions about your feedback, please notify your instructional staff or your Student Success Manager. If you would like to resubmit your work for an additional review, you can use the Resubmit Assignment button to upload new links. You may resubmit up to three times for a total of four submissions.

### Rubric

[Module 12 Challenge Rubric](https://docs.google.com/document/d/1H-g23PjJlx5ZsuKcEsOCkEolppWcQ5NMv8hvgbOpl9w/edit)

## 12: Career Connection

Great work this week learning how to web scrape! Now let’s discuss web scraping in the workplace. Then, we’ll cover how to tailor a resume for a particular job posting. 

Here’s the Career Connection agenda for today:

* Web Scraping in the Workplace
* Finding Your Career Fit: Tailoring a Resume for a Particular Role
* Interview Prep
* Next Steps

### Web Scraping in the Workplace

When sourcing data for a project, you have lots of options, such as using an API, accessing a database, or web scraping. Many of these options _also_ have options to choose from. If you choose to use web scraping, you can program your own scraper (as you did in this module) or use a third-party web scraper. 

As you’ve come to understand, your role as a data professional will often require you to choose the right tool for the job. This is why some data scientists use web scrapers regularly, and some use them only rarely. It all depends on the project!

So when is web scraping the right choice? One of the major enterprise applications of web scraping is collecting data to gain a competitive advantage. This can involve gathering leads, observing prices, and monitoring consumer sentiment. Another popular use case is machine learning. Web scraping helps data scientists acquire the large volume of data that it takes to improve the accuracy of machine learning algorithms. 

### Finding Your Career Fit: Tailoring a Resume for a Particular Role

![alt = ""](Images/coding-career-application-materials.jpg)

In a job description, an employer tells you exactly what skills and experience they are looking for. Your task is to show the employer that you are a match. One way to do this is to tailor your resume to the job description. 

Tailoring a resume shows your interest and ensures that recruiters can see that you are a good fit for the position. It can also help you stand out to an applicant tracking system (ATS), which often looks for keyword matches between job descriptions and resumes. 

We suggest following the following steps when tailoring your resume: 

1. **Review the job description.** Read the entire job description, and highlight any skills or experiences that you have. 

2. **Align your personal brand statement.** The personal brand statement (also known as a summary statement) is the first item that a recruiter reads on your resume. The skills, experiences, and interests that you describe should include the high-priority qualifications that you highlighted in the job description. 

3. **Move the most relevant qualifications to the top of your resume.** Which section of your resume most clearly highlights your value to the company? Is it your technical skills, experience, or projects? By moving the most relevant section to the top of your resume, you ensure that the recruiter sees it right away. 

4. **Include keywords in descriptions.** Review the descriptions of your projects and experiences. When possible, include keywords from the job description. You may also choose to reorder the information so that relevant points are near the top of a description. 

[Ladders Inc.](https://www.theladders.com/static/images/basicSite/pdfs/TheLadders-EyeTracking-StudyC2.pdf) reports that recruiters only spend 7.4 seconds (total!) looking at your resume. By tailoring your resume, you ensure that the recruiter sees your very best qualifications in those 7.4 seconds. 

> **Important** As a reminder, it’s never okay to misrepresent yourself in your application materials in order to meet the qualifications of a job description. Being honest is the best way to ensure that you find a good career match. 

> **Interview Prep**
>
> For today’s interview prep, we will look at some case-study-style interview questions. Imagine that a hiring manager presents you with the following scenarios. Read the scenarios, and then consider how you would answer the follow-up questions.
> 
> **Case Study Interview Question Number 1: Price Comparison** 
> You recently started working at a major online clothing retailer (Company A) that wants to sell at high volumes to increase profit margins. Company A sells to a niche market so it depends on its product and competitive price to reach the largest-possible audience. 
> A few months ago, a major competitor (Company B) entered the online market, and Company A wants to keep an eye on their pricing. 
>You’ve been hired to do the data analysis. Obviously, Company B won’t release all of its pricing information to you in a well-documented API. So you’ll have to scrape the data off of its pages, and maintain a database of products, prices, and price changes. 
>
> **Follow-up Questions”
> 1. Would you consider it legal to scrape data from your competitors? 
> Answer: In general, data that is publicly available and not copyrighted is legal to scrape. However, there are unique exceptions. You may want to check out these resources: 
> * The European Union’s [General Data Protection Regulation](https://ec.europa.eu/info/law/law-topic/data-protection/data-protection-eu_en)
> * [California Consumer Privacy Act](https://oag.ca.gov/privacy/ccpa)
> * [Computer Fraud and Abuse Act](https://www.nacdl.org/Landing/ComputerFraudandAbuseAct)
> 
> 2. Can you scrape data behind a login page? 
> Answer: Yes, you can; however, it is significantly more difficult. You need to provide the web application with valid credentials and then navigate to the authenticated portion of the site. In addition, you need to confirm the legality of the process. 
> 
> **Case Study Interview Question Number 2: Airline Tickets** 
> FlyCheap is a locally owned tech company with a big idea. Using its browser extension, customers can book flights to travel all over the world on any airline. However, it is facing a problem: Its major competitors change their flight prices multiple times per day. 
> You’ve been hired to improve the functionality of the browser extension by allowing it to pop up with an alert when the price of a flight has dropped. Unfortunately, the Google Flights API was recently dropped, and you can no longer just make an API request. You must get the information yourself. 
> Your first task is to write an application that scrapes data from Kayak, Google Flights, and similar companies. When a flight drops or increases in price, that information will get fed to the browser extension and then on to the end user. 
> 
> **Follow-Up Questions
>
> 1. Can you extract data from sites not written in English? 
> Answer: Yes! You can extract data in any language. Remember that the material you scrape remains in its original language. 
> 
> 2. Can you republish data and/or information that you scraped from the web? 
> Answer: This is another gray area. Watch out for policies that explicitly forbid redistribution of material, and stay vigilant about citation guidelines. You might be able to freely republish, not republish at all, or republish with limitations and credits to the authors. If you are unsure, get in touch with the owners of the site. 


###  Next Steps

* Consider adding web scraping to the technical skills section of your application materials. 


## 12: Review

### Congratulations on Completing Module 12!

After all your learning and practice in this module, you should be able to:

* Create and connect to local Mongo databases.

* Perform create, read, update, delete (CRUD) operations on Mongo documents by using the Mongo shell.

* Create simple Python applications that connect to and modify Mongo databases by using the PyMongo library.

* Scrape data from the web by using the Python Beautiful Soup library.

* Save your web scraping results into Mongo.

* Render a static HTML template with Flask. 

* Create a Flask application that renders data from a Mongo database on an HTML template.

* Create a Flask application that scrapes a webpage, stores the data in a Mongo database, and then renders the data on an HTML template.

Take a few minutes to reflect on your learning:

* What new topics did you learn in this module?

* How has your understanding changed or evolved?

* What are you wondering about?

* What questions do you have?

You will continue to build your knowledge and skills throughout the boot camp. If you have any outstanding questions about the content in this module, please reach out to your instructional team.
