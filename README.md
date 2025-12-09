# Weather Dashboard

A weather data collection system using AWS S3 and OpenWeather API

## Project Overview
This project demonstrates core DevOps principles by combining:
- External API Integration (OpenWeather API)
- Cloud Storage (AWS S3)
- Version Control (Git)
- Python Development
- Error Handling
- Environment Management

## Features
- Fetches real-time weather data for multiple cities
- Displays temperature (°F), humidity, and weather conditions
- Automatically stores weather data in AWS S3
- Supports multiple cities tracking
- Timestamps all data for historical tracking

## Technical Architecture
- **Language:** Python 3.x
- **Cloud Provider:** AWS (S3)
- **External API:** OpenWeather API
- **Dependencies:** 
  - boto3 (AWS SDK)
  - python-dotenv
  - requests

## Project Structure
```
weather-dashboard/
├── src/
│   ├── __init__.py
│   └── weather_dashboard.py
├── tests/
├── data/
├── .env
├── .gitignore
└── requirements.txt
```

## Setup Instructions

1. Clone the repository:
```bash
git clone https://github.com/gus-hub-tech/weather-dashboard.git
cd weather-dashboard
```

2. Create a virtual environment:
```bash
python3 -m venv venv
```

3. Activate the virtual environment:
```bash
# On Linux/macOS:
source venv/bin/activate

# On Windows:
venv\Scripts\activate
```

4. Install dependencies:
```bash
pip install -r requirements.txt
```

5. Create and configure the .env file:
```bash
# Create .env file in the project root
touch .env
```

Add the following variables to your .env file:
```
# OpenWeather API Configuration
OPENWEATHER_API_KEY=your_openweather_api_key_here

# AWS S3 Configuration
AWS_BUCKET_NAME=your_s3_bucket_name_here
```

To get your OpenWeather API key:
- Sign up at https://openweathermap.org/api
- Navigate to API keys section
- Copy your API key

6. Configure AWS credentials:
```bash
aws configure
```
Provide your:
- AWS Access Key ID
- AWS Secret Access Key
- Default region (e.g., us-east-1)
- Default output format (json)

7. Run the application:
```bash
python src/weather_dashboard.py
```

8. Deactivate the virtual environment (when finished):
```bash
deactivate
```

## Uninstall

To uninstall all project dependencies:
```bash
pip uninstall -r requirements.txt -y
```

## What I Learned

- AWS S3 bucket creation and management
- Environment variable management for secure API keys
- Python best practices for API integration
- Git workflow for project development
- Error handling in distributed systems
- Cloud resource management

## Future Enhancements

- Add weather forecasting
- Implement data visualization
- Add more cities
- Create automated testing
- Set up CI/CD pipeline
