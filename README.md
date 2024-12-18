# Google Sheets to HubSpot Integration

This project provides an integration between **Google Sheets** and **HubSpot** using **Google Apps Script**. It automates the process of adding or updating HubSpot contacts and creating associated deals from Google Sheets data.

## Features

- **Contact Lookup**: Searches for an existing HubSpot contact based on the email address.
- **Create/Update Contact**: If the contact exists, the script updates it; if not, it creates a new contact.
- **Deal Creation**: Automatically creates a deal for the contact with details like project type or message.
- **Custom Deal Description**: The deal description is populated with a custom message or project type from the Google Sheet.

## How It Works

1. **Google Sheets** stores form submission data (e.g., first name, last name, email, project type, etc.).
2. **Google Apps Script** checks for new rows in the Google Sheet and performs the following:
   - Searches for a contact in HubSpot using the email.
   - If the contact exists, creates or updates a deal.
   - If the contact does not exist, creates both a new contact and a new deal in HubSpot.
3. **HubSpot API** is used to perform contact and deal creation using the provided HubSpot API token.

## Prerequisites

- **HubSpot Account** with API access and a valid **API token**.
- **Google Sheet** to store data submitted via a form.
- **Google Apps Script** bound to the Google Sheet to manage integration logic.

## Setup Instructions

1. Open your Google Sheet and go to **Extensions > Apps Script**.
2. Copy and paste the provided Apps Script code into the script editor.
3. Insert your **HubSpot API Token** in the designated variable in the script.
4. Set up triggers in Google Apps Script to run the script automatically when new rows are added.

## Deployment

To deploy the integration:

1. Authorize the script with your Google account.
2. Create a trigger to run the script on a schedule (e.g., every minute) or on form submission.
