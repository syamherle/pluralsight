# Pluralsight Challenge
## Required modules to run
+ Pandas
+ Numpy
+ Flask
+ sqlite3 (For Backend)

## Steps to run the api locally
+ Note for running on local
  + Download user_similarity folder from github adb unzip
  + Keep the folder structure in same way, have deleted database (since it was large)
  
+ Run db_data_loader.py, this loads all .csv files and feature_space model into SQL Database, the database will be created in db/ folder.
+ Run app.py, usually the application will run on 9090 port or http://127.0.0.1:9090/
+ Or once the app.py is compiled, web server port will be displayed in console.

## Written response for interview challenge

### What similarity metric and why?

+ I have choosen cosine simillarity as similarity metric, the feature space was very high dimension and it was contructed from sparse features, other metrics are dependent on magnitude, wherease the cosine similarity is based on direction. And also, cosine similarity is easy to calculate for high dimension data, as it is dot product of normalized vectors, beacuse of this I used to calculate it and get top users when user enters user_handle.

### What if data was large?

+ When the data is huge, we can do the following aproaches,
  + Working with smaller samples, and trying to generalize the final model on the whole data.
  + Making use of Apache Sparks's RDD's parallel processing or python's parallel processing. 
  + Progressively loading data, like the one available in keras.
  + Processing the data in chunks.

### Context assumption?

+ The context which I can assume is, this API can be extended further for recommendation engine, like for course-course recommendation for which additional data about courses might have been required like, cost of the course, rating given by the user for specific courses, review written by users for course specific, duration of videos of the course (week) etc. User-User based comparing could have been done more efficiently if personal information of users like demography,education, profession, experience in other courses,reviews written by the user from which sentiment analysis can be done, currently enrolleed courses per user, etc.
 
 



