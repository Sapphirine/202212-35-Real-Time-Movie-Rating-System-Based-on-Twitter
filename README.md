# 202212-35-Real-Time-Movie-Rating-System-Based-on-Twitter
## Structure
- pullMsg.py used for pulling message from Pub/sub, generating the sentiment scores and storing the scores inside the BigQuery tables. To start pulling messages, user need to specify the PUB_SUB_TOPIC, PUB_SUB_SUBSCRIPTION and TABLE inside the main part.
- sentiment.py and util.py is for generating sentiment scores using Vader sentiment analysis tool.
- stream.py used for streaming tweet data from Twitter API, to stream data, users need to specify the '_rules' and 'bearer_token' inside the main.
- front-end is the folder for html and css files used by frontend website.

## Start
First run the stream.py to get the real-time data from Twitter API and store the data into Pub/sub. And then, run pullMsg.py to pull messages from Pub/sub to BigQuery tables. After that, click the index.html inside the front-end folder to see all the score graphs for streamed movies. For here, since the GCP account limit, we just downloaded all the data in .csv file for frontend display, and the data is stored inside front-end/public/data
