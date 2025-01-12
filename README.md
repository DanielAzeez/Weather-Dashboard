# Weather Dashboard  

## Overview  
The **Weather Dashboard** is a scalable weather data collection and storage system. This project integrates the **OpenWeather API** with **AWS S3**, showcasing foundational DevOps principles such as automation, cloud resource management, and real-time data integration.  

---

## Features  
- Fetches real-time weather data for multiple cities.  
- Displays temperature (°F), humidity, and weather conditions.  
- Dynamically generates globally unique AWS S3 bucket names for secure and scalable storage.  
- Automatically stores weather data in JSON format.  
- Supports tracking for multiple cities.  

---

## Technologies Used  
- **Programming Language**: Python 3.x  
- **Cloud Provider**: AWS (S3)  
- **External API**: OpenWeather API  

---

## Dependencies  
The following Python libraries are required to run the project:  
- **`boto3`**: AWS SDK for Python, enabling interactions with AWS S3.  
- **`python-dotenv`**: Manages environment variables securely.  
- **`requests`**: Facilitates API calls to fetch data from the OpenWeather API.  

---

## Prerequisites  
### Environment Setup  
1. Install Python 3.8 or higher on your system.  
2. Configure the AWS CLI with access credentials to manage S3 buckets.  

### API Key  
- Obtain an API key from [OpenWeather](https://openweathermap.org/api).  

---

## Installation  
### 1️⃣ Clone the Repository  
```bash  
git clone https://github.com/DanielAzeez/Weather-Dashboard.git  
cd Weather-Dashboard  
```  

### 2️⃣ Install Dependencies  
Install the required libraries using `pip`:  
```bash  
pip install -r requirements.txt  
```  

### 3️⃣ Configure Environment Variables  
Create a `.env` file in the project directory and add the following:  
```dotenv  
OPENWEATHER_API_KEY=your_api_key_here
AWS_BUCKET_NAME=weather-dashboard-${RANDOM}
```  

---

## Usage  
### Run the Application  
Execute the script to fetch and store weather data:  
```bash  
python weather_dashboard.py  
```  

### Data Storage  
- Weather data is automatically stored in AWS S3 buckets in JSON format.  
- Each entry is timestamped for historical tracking.  

---

## Project Structure  
```
Weather-Dashboard/  
├── data/                   # Folder for storing local data (if applicable)  
├── test/                   # Folder for test scripts  
├── src/                    # Source code directory  
│   ├── __init__.py         # Package initialization file  
│   ├── weather_dashboard.py # Main script for fetching and storing weather data
├── .env                    # Environment variables file  
├── .gitignore              # Git ignore file  
├── README.md               # Project documentation  
├── requirements.txt        # List of dependencies  
```  

---


## Acknowledgements  
- **OpenWeather**: For providing reliable weather data.  
- **AWS S3**: For seamless and scalable cloud storage services.  
