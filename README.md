# Event Announcement System (AWS Serverless)

A serverless event notification system built with AWS that publishes event announcements via API Gateway, processes them with Lambda, and distributes notifications using SNS email subscriptions.


## Architecture

This project follows a serverless event-driven architecture on AWS:
User - API Gateway - AWS Lambda - Amazon SNS - Email Subcribers

##Tech Stack

- AWS Lambda (serverless compute)
- Amazon API Gateway (REST API management)
- Amazon SNS (event distribution / email notifications)
- Python (backend logic)
- IAM (permissions and security)


### System Flow

1. User sends a POST request with event details
2. API Gateway receives the request
3. AWS Lambda processes and formats the event data
4. Amazon SNS publishes the message
5. Subscribers receive email notifications


## Example Request

**POST /announce**

```json
{
  "title": "AWS Cybersecurity Workshop",
  "date": "May 10, 2026",
  "location": "Charlotte"
}

## Example Output

New Event: AWS Cybersecurity Workshop  
Date: May 10, 2026  
Location: Charlotte
