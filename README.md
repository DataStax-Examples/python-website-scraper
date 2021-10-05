<!--- STARTEXCLUDE --->
# Build a Website Scraper with Astra DB + Python
*180 minutes, Advanced, [Start Building](https://github.com/DataStax-Examples/python-website-scraper/blob/master/README.md)*

Learn how to scrape websites with Astra DB, Python, Selenium, Requests HTML, Celery, & FastAPI by following along with CodingEntrepreneurs' video, located [here](https://youtu.be/NyDT3KkscSk).
<!--- ENDEXCLUDE --->

![image](https://raw.githubusercontent.com/DataStax-Examples/python-website-scraper/master/hero.jpeg)

## Quick Start
<!--- STARTEXCLUDE --->
* [Signup for DataStax Astra](https://dtsx.io/3ogyCAI), or login to your already existing account. 
* [Create an Astra DB Database](https://github.com/DataStax-Examples/sample-app-template/blob/master/GETTING_STARTED.md#create-an-astra-db) if you don't already have one.
<!--- ENDEXCLUDE --->
* [Create an Astra DB Keyspace](https://github.com/DataStax-Examples/sample-app-template/blob/master/GETTING_STARTED.md#create-an-astra-db-keyspace) called `sag_nuxtjs_fullstack` in your database.
* [Generate an Application Token](https://github.com/DataStax-Examples/sample-app-template/blob/master/GETTING_STARTED.md#create-an-application-token) with the role of `Database Administrator` for the Organization that your Astra DB is in.
* Get your [secure connect bundle](https://github.com/DataStax-Examples/sample-app-template/blob/master/GETTING_STARTED.md#get-an-astra-db-secure-connect-bundle) from the connect page of your database and save it to your project folder. Rename it to `bundle.zip`

* Setup your system: Below is a preflight checklist to ensure you system is fully setup to work with this course. All guides and setup can be found in the [setup](https://github.com/DataStax-Examples/python-website-scraper/tree/master/setup) directory of this repo.
  * Install Selenium & Chromedriver - [setup guide](https://github.com/DataStax-Examples/python-website-scraper/tree/master/setup/Install%20Selenium%20%26%20Chromedriver%20on%20your%20System.md)
  * Install Redis  - [setup guide](https://github.com/DataStax-Examples/python-website-scraper/tree/master/setup/Setup%20Redis.md)
  * Create a virtual environment & install dependencies
  * Setup an account with DataStax
  * Create your first AstraDB and get API credentials
  * Use `cassandra-driver` to verify your connection to AstraDB


  
## How this works
Follow along in this video tutorial: [https://youtu.be/NyDT3KkscSk](https://youtu.be/NyDT3KkscSk).

This series is broken up into 4 parts:
- **Scraping** How to scrape and parse data from nearly any website with Selenium & Requests HTML. 
- **Data models** how to store and validate data with `cassandra-driver`, `pydantic`, and **AstraDB**.
- **Worker & Scheduling** how to schedule periodic tasks (ie scraping) integrated with Redis & AstraDB
- **Presentation** How to combine the above steps in as robust web application service

Here's what each tool is used for:
- **Python 3.9** [download](https://www.python.org/download/) - programming the logic.
- **AstraDB** [sign up](https://dtsx.io/3ogyCAI) - highly perfomant and scalable database service by DataStax. AstraDB is a Cassandra NoSQL Database. [Cassandra](https://cassandra.apache.org/_/index.html) is used by Netflix, Discord, Apple, and many others to handle astonding amounts of data.
- **Selenium** [docs](https://selenium-python.readthedocs.io/) - an automated web browsing experience that allows:
  - Run all web-browser actions through code
  - Loads JavaScript heavy websites
  - Can perform standard user interaction like clicks, form submits, logins, etc.
- **Requests HTML** [docs](https://docs.python-requests.org/) - we're going to use this to parse an HTML document extracted from Selenium
- **Celery** [docs](https://docs.celeryproject.org/) - Celery providers worker processes that will allow us to schedule when we need to scrape websites. We'll be using [redis](https://redis.io/) as our task queue.
- **FastAPI** [docs](https://fastapi.tiangolo.com/) - as a web application framework to Display and monitor web scraping results from anywhere
