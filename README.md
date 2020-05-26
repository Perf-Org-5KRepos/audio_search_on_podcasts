# Work in Progress.
# audio_search_on_podcasts

# Create a Python Flask Audio Search Application with `Watson Speech to Text` and `Watson Discovery`. 
Often while listening to a Podcast or probably listening to a course video/audio files, ...
In this code pattern, we will create an application with which you can search within the audio/video files. Natural language query search in audio files and get back with the results with the proper time frame where it is being talked 

In this example, we will use a <<<<video/audio we are using>>>> to illustrate the process. The data is provided by <<>> and includes 16 hours of medical dictation in both audio and text files.

When the reader has completed this code pattern, they will understand how to:

* Prepare audio/video data and perform chunking to break it into smaller chunks to work with.
* Work with the `Watson Speech to Text` service through API calls to convert audio/video to text.
* Work with the `Watson Discovery` service through API calls to perform search on text chunks.
* Create a python flask Application and deploy on IBM Cloud.

![architecture](doc/source/images/Architecture.png)

## Flow

1. The user uploads the video/audio file on the UI. 
1. The Audio/Video is processed with python libraries and perform chunking on them to convert it into smaller chunks to work with.
1. The user interacts with the Watson Speech to Text service via the provided application UI. The Audio chunks are converted into text chunks with Watson Speech to Text.
1. The text chunks are uploaded on Watson Discovery by calling Discovery APIs with python SDKs.
1. The user hit a search using Discovery .
1. The results are shown on the UI .

## Included components

* [IBM Watson Speech to Text](https://www.ibm.com/watson/services/speech-to-text): easily convert audio and voice into written text for quick understanding of content.
* [IBM Watson Discovery](https://developer.ibm.com/articles/introduction-watson-discovery/):  IBM Watson Discovery, you can ingest, normalize, enrich, and search your unstructured data (JSON, HTML, PDF, Word, and more) with speed and accuracy.

## Featured technologies

* [Python Flask](https://flask.palletsprojects.com/en/1.1.x/): Flask is a lightweight WSGI web application framework. It is designed to make getting started quick and easy, with the ability to scale up to complex application.
* [IBM Watson Speech to Text](https://www.ibm.com/watson/services/speech-to-text): easily convert audio and voice into written text for quick understanding of content.
* [IBM Watson Discovery](https://developer.ibm.com/articles/introduction-watson-discovery/):  IBM Watson Discovery, you can ingest, normalize, enrich, and search your unstructured data (JSON, HTML, PDF, Word, and more) with speed and accuracy.

# Watch the Video

[![video](link)

# Steps

1. [Clone the repo](#1-clone-the-repo)
1. [Create Speech to text service](#2-create-ibm-cloud-services)
1. [Create Watson Discovery](#3-create-ibm-cloud-services)
1. [Configure credentials](#4-configure-credentials)
1. [Run The Application Locally](#5-download-and-prepare-the-data)


## 1. Clone the repo

```bash
git clone https://github.com/IBM/audio_search_on_podcasts/
```

## 2. Create Watson Speech To Text

Create the service:

* [**Watson Speech To Text**](https://cloud.ibm.com/catalog/services/speech-to-text)
- Click on the Watson Speech To Text. It will take to the Catalog on IBM Cloud. Just hit the `create` button.

> Note: In order to perform customization, you will need to select the `Standard` paid plan. But for this Code Pattern, you can work with the `LITE` Plan. 

From your **Watson Speech to Text** service instance, select the `Service Credentials` tab.

* Copy the credentials to authenticate to your service instance:
* On the Manage page, click Show Credentials to view your credentials.
* Copy the API Key and URL values  as they will be needed in future steps.

If no credentials exist, select the `New Credential` button to create a new set of credentials. Then save API Key and URL values.


## 3. Create Watson Discovery
Create the service:

* [**Watson Discovery**](https://cloud.ibm.com/catalog/services/discovery)
- Click on the Watson Discovery. It will take to the Catalog on IBM Cloud. Just hit the `create` button.

> Note: For this Code Pattern, you can work with the `LITE` Plan. 

* click `Launch Watson Discovery`. 
* to Create a new data collection, click on the ``

<<<<<<<<<<<<<add_document(self, environment_id, collection_id, file=None, filename=None, file_content_type=None, metadata=None, **kwargs)>>>>>>>>>>>>>>>>>>>>>>>>>>>


## 4. Run The Application Locally



### a. Update global variables in app.py


### b. Install requirement.txt


### c. Run the flask app








# Sample output

* The main GUI screen:


# Links

* 



# Deploy on IBM Cloud

Instructions for deploying the web application on Cloud Foundry can be found [here](doc/cloud-deploy.md).

# Learn more

* **Artificial Intelligence Code Patterns**: Enjoyed this Code Pattern? Check out our other [AI Code Patterns](https://developer.ibm.com/technologies/artificial-intelligence/)
* **AI and Data Code Pattern Playlist**: Bookmark our [playlist](https://www.youtube.com/playlist?list=PLzUbsvIyrNfknNewObx5N7uGZ5FKH0Fde) with all of our Code Pattern videos
* **With Watson**: Want to take your Watson app to the next level? Looking to utilize Watson Brand assets? [Join the With Watson program](https://www.ibm.com/watson/with-watson/) to leverage exclusive brand, marketing, and tech resources to amplify and accelerate your Watson embedded commercial solution.

# License

This code pattern is licensed under the Apache Software License, Version 2.  Separate third party code objects invoked within this code pattern are licensed by their respective providers pursuant to their own separate licenses. Contributions are subject to the [Developer Certificate of Origin, Version 1.1 (DCO)](https://developercertificate.org/) and the [Apache Software License, Version 2](https://www.apache.org/licenses/LICENSE-2.0.txt).

[Apache Software License (ASL) FAQ](https://www.apache.org/foundation/license-faq.html#WhatDoesItMEAN)
