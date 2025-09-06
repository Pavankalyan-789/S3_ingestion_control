# S3_ingestion_control
This is a Python application that:
Fetches current weather data from the OpenWeather API.
Ensures an Amazon S3 bucket exists (creates it if not).
Saves weather data as JSON files in your S3 bucket with timestamps.
Features
Fetches live weather for one or more cities.
Stores results in Amazon S3.
Automatically creates the S3 bucket if missing.
Adds a timestamp to each file for unique storage.
Requirements
Python 3.8+
AWS Account with an IAM user that has S3 permissions.
OpenWeather API key (free signup at OpenWeather).
Setup Instructions
Make a project folder and move your script there. Example structure:
weather-app/ ├── src/ │ └── weather.py # Your Python script ├── .env # Store API keys and AWS details here └── requirements.txt # Python dependencies
Install dependencies:
Create a requirements.txt file with the following:
boto3 requests python-dotenv
Then run:
pip install -r requirements.txt
Set up environment variables
Create a .env file in the project root:
OPENWEATHER_API_KEY=your_openweather_api_key_here AWS_BUCKET_NAME=your-s3-bucket-name AWS_REGION=ap-south-1
Bucket name rules: must be all lowercase, no spaces, and globally unique (example: weather-bucket-09032025).
Configure AWS credentials Run:
aws configure
Enter your AWS Access Key, Secret Key, Region, and Output format.
Running the Application
From the root folder, run:
python src/weather.py
Example output:
  git push -u origin main
Enumerating objects: 8, done.
Counting objects: 100% (8/8), done.
Delta compression using up to 8 threads
Compressing objects: 100% (5/5), done.
Writing objects: 100% (8/8), 1.62 KiB | 208.00 KiB/s, done.
Total 8 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
To https://github.com/Pavankalyan-789/S3_ingestion_control.git
 * [new branch]      main -> main
branch 'main' set up to track 'origin/main'.
