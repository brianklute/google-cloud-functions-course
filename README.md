# Google Cloud Functions Course

## Starting a project

To start a new project in google cloud we can go to the
[Firebase Console](https://console.firebase.google.com) or
create it from [Google Cloud Platform Console](https://console.cloud.google.com)

## Creating a virtual environment

first we have t install 'python3-venv' with the following command

~~~
sudo apt install python3-venv
~~~

Then, we execute execute the following command:

~~~
python3 activate gcloudcourse/
~~~

To activate the virtual environment we do

~~~
source gcloudcourse/bin/activate
~~~

In order to add new packages to our new virtual environment we create a file called 'requirements.txt' and execute the
following command:

~~~
pip install -r requirements.txt
~~~

## Deploying our function

First, we have to set our project ID with the following command:

~~~
gcloud config set project [YOUR_PROJECT_ID]
~~~

Then we deploy our function with this command:

~~~
gcloud functions deploy [FUNCTION_NAME] --runtime python311 --trigger-http
~~~

## Deploying cloud functions with environment variables and other dependencies
we have to create a '.env.yaml' file and a 'requirements.txt' in the same directory of our 'main.py' and then from the following command:
~~~
gcloud functions deploy [FUNCTION_NAME] --env-vars-file .env.yaml --runtime python311 --trigger-http
~~~

