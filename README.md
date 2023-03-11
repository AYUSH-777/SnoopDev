# SnoopDev
Snoop Deep Web to crawl a website and get its html and screenshot using stormcrawler running in local mode in Apache Storm.

Here are the brief steps for executing the task with code snippets in Java:

Step 1: Setting up the Environment

Install and configure Apache Storm and Selenium in your system
Created a new Java project and add dependencies for Storm and Selenium

Step 2: Crawling the Websites

Created a new Spout for reading seed URLs from a JSON file
Created a new Bolt for fetching HTML and image data using Selenium
Defined a Topology that connects the Spout and Bolt and submit it to Storm

Step 3: Stored the Data in the Database

Used a database library such as JDBC to connect to your chosen backend (MySQL, PostgreSQL, or MongoDB)
Created a new Bolt for storing the extracted data in the database
Added the Bolt to your Topology to store the data as it is crawled


Step 4: Creating the Result JSON

Once I have stored the HTML data and images in the database, I  created the result JSON file. The result should contain the following information for each seed URL:

Seed URL
Current URL visited by the crawler
HTML source code of the current URL
Base64 image of the complete 1080p viewport (full screen) webpage



Step 5: Deployment

I completed the above steps, I can deploy the service. Here are the steps for deployment:

Setting up a server to run Apache Storm and your chosen backend (MySQL, PostgreSQL, or MongoDB).
Cloning the repository containing your code onto the server.
Installed all the required dependencies (Apache Storm, Selenium, etc.).
Settted up your backend (create the required tables, set up authentication, etc.).
Runnned the stormcrawler command to start crawling the seed URLs.
Monitored the logs to ensure that the crawling process is running smoothly.
Once the crawling process is complete, extracted the data from the database and create the result JSON file.
Made the result JSON file accessible to the user.

Step 6: Key Takeaway

One key takeaway from this exercise is the importance of using a distributed system like Apache Storm to handle large-scale web crawling. Apache Storm allows you to distribute the crawling process across multiple nodes, making it faster and more efficient. Additionally, the use of Selenium allows for the extraction of full-page screenshots, which can be useful for certain applications. Overall, this exercise demonstrates the power and potential of distributed systems and web crawling for data acquisition and analysis.
