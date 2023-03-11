# SnoopDev
Snoop Deep Web to crawl a website and get its html and screenshot using stormcrawler running in local mode in Apache Storm.

Here are the brief steps which I followed for executing the task in Java:

Step 1: Setting up the Environment

Installed and configured the Apache Storm and Selenium in my system
Created a new Java project and added new dependencies for Storm and Selenium

Step 2: Crawling the Websites

Created a new Spout for reading seed URLs from a JSON file
Created a new Bolt for fetching HTML and image data using Selenium
Defined a Topology that connects the Spout and Bolt and submit it to Storm

Step 3: Stored the Data in the Database

Used a database library such as JDBC to connect to my chosen backend MySQL
Created a new Bolt for storing the extracted data in the database
Added the Bolt to my Topology to store the data as it is crawled


Step 4: Creating the Result JSON

Once I stored the HTML data and images in the database, I  created the result JSON file. 

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

One key takeaway from this exercise is the importance of using a distributed system like Apache Storm to handle large-scale web crawling. Apache Storm allows us to distribute the crawling process across multiple nodes, making it faster and more efficient. Additionally, the use of Selenium allows for the extraction of full-page screenshots, which can be useful for certain applications. Overall, this exercise demonstrates the power and potential of distributed systems and web crawling for data acquisition and analysis.
