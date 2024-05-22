We get the phishing sites URLs form https://www.phishtank.com/developer_info.php that is open source service that updates hourly. That is in csv format.

We use XGBoost classifier module and get the best results, 
we also tried: Support vector machines, Decision trees but XGBoost gave us best accuracy.

This reference paper https://archive.ics.uci.edu/dataset/327/phishing+websites gave us the features that we could use to analyse if a website is phishing or not.
The features that we extract:

<img width="837" alt="Screenshot 2024-05-22 at 3 14 58 AM" src="https://github.com/kanwar280/Phishing-Website-Detector/assets/67856691/8e096fc1-0a70-4864-a807-5b4431330144">

These include 9 address bar features, 4 domain based, 4 HTML/JS based features.

All features are extracted in main.py

Here is main.py running in my local machine:

<img width="837" alt="Screenshot 2024-05-22 at 3 17 43 AM" src="https://github.com/kanwar280/Phishing-Website-Detector/assets/67856691/57340152-8309-422a-a5d9-d40ce70f24e0">

This program is easily uploadable to Amazon S3 bucket and build with codebuild, The Model can also be places inside an S3 bucket and used from there whenever needed.
