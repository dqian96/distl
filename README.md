# distl

HTML/CSS/JS Frontend:

* Beautifully designed
* Filters out ads from relevant article text
* Sends text to backend
* Recieves and displays summarized text and sentiment analysis
* Sends user ratings on text analysis to backend

Node.js Backend:

* Recieves source text from frontend and caches it
* Performs text summarization using a Node.js plugin
* Sends text to Google Natural Language API for sentiment analysis
* Aggregates results and sends analysis back to frontend
* Recieves user rating on analysis and sends the cached sourced text to Google Storage

Google Cloud Platform:

* Hosts the Node.js backend using Google App Engine
* A VM created by Google Compute Engine uses CRON to schedule PySpark jobs on a Google Hadoop cluster
* Spark apps analyze a day's worth of source text and user ratings (stored in Google Storage) for patterns (i.e. most frequently visited site, number of of dislike v.s. likes for a particular site, etc.)

