## Fruit.ai Project by Aman Rana

## Table of Contents

- [Features](#features)
- [Requirements](#requirements)
- [Setup](#setup)
- [Running the Application](#running-the-application)
- [API Endpoints](#api-endpoints)
- [Example JSON](#example-json-for-creating-a-new-faq)
- [Error Handling](#error-handling)
- [FAQ Model](#faq-model)
- [Frontend Overview](#frontend-overview)
- [Routes](#routes-in-the-application)
- [Responsive Design](#responsive-design)

## Features

- **Retrieve All FAQs:** Fetch a complete list of FAQs.
- **Get FAQ by ID:** Obtain specific details for any FAQ using its ID.
- **Create FAQ:** Add new FAQs to the system.
- **Update FAQ:** Edit existing FAQ content.
- **Delete FAQ:** Remove an FAQ from the database.

## Requirements

- Python 3.9+
- Django 3.2+
- Django REST Framework
- React.js

## Setup

### Backend Setup

1. Clone the repository:
   \`\`\`bash
   git clone https://github.com/MrFranklink/Fruit.ai.git
   \`\`\`

2. Move to the backend folder:
   \`\`\`bash
   cd server
   \`\`\`

3. Install the necessary dependencies:
   \`\`\`bash
   pip install -r requirements.txt
   \`\`\`

4. Apply database migrations:
   \`\`\`bash
   python manage.py migrate
   \`\`\`

5. Start the backend server:
   \`\`\`bash
   python manage.py runserver
   \`\`\`

### Frontend Setup

1. Go to the frontend directory:
   \`\`\`bash
   cd frontend
   \`\`\`

2. Install frontend dependencies:
   \`\`\`bash
   npm install
   \`\`\`

3. Set up environment variables by creating a \`.env\` file in the root directory:
   \`\`\`bash
   REACT_APP_API_URL=http://localhost:8000/api
   \`\`\`

4. Start the frontend server:
   \`\`\`bash
   npm start
   \`\`\`

## Running the Application

Ensure both frontend and backend servers are running simultaneously. The frontend will connect with the backend API to display the FAQ content.

## API Endpoints

- **GET** \`/faqs/\` - Retrieve all FAQs.
- **GET** \`/faqs/<id>/\` - Retrieve a specific FAQ by its ID.
- **POST** \`/faqs/\` - Create a new FAQ.
- **PUT** \`/faqs/<id>/\` - Update an existing FAQ.
- **DELETE** \`/faqs/<id>/\` - Delete an FAQ.

## Example JSON for Creating a New FAQ

\`\`\`json
{
"name": "John Doe",
"title": "How to reset password?",
"description": "You can reset your password by clicking on 'Forgot Password' on the login page.",
"image_url": "https://example.com/image.png"
}
\`\`\`

## Error Handling

- **404 Not Found:** Returned when the FAQ is not found.
- **400 Bad Request:** Returned when there is an issue with the request data, such as missing fields or invalid values.

## FAQ Model

The \`Faq\` model contains the following attributes:

- \`faqs_id\`: A unique ID for each FAQ.
- \`name\`: Name of the person submitting the FAQ (up to 50 characters).
- \`title\`: A short title for the FAQ (up to 50 characters).
- \`description\`: Detailed response to the FAQ.
- \`image_url\`: Optional field for an image URL related to the FAQ.

## Frontend Overview

### Login Page

- You can log in using any username and password (dummy credentials).
- After logging in, you’ll be redirected to the homepage.

### Homepage

The homepage has buttons that lead to different sections:

- **Chat Button:** Takes you to a brief splash screen before loading the ChatApp page.
- **Translate Button:** Redirects to a translation page (placeholder functionality).
- **FAQs Button:** Displays all FAQs from the backend API. Ensure the backend is running to access the data.
- **About Button:** Provides details about the app.

## Routes in the Application

- **/**: Displays the login page.
- **/home**: Homepage after login.
- **/translate**: Translation page.
- **/splash**: Brief splash screen before loading ChatApp.
- **/chatapp**: Main chat application page.
- **/about**: About the application.
- **/faq**: List of FAQs.

## Responsive Design

The application is optimized for various device resolutions, including:

- iPhone 14 Pro Max (430x932)
- iPhone XR (414x896)
- iPhone SE (375x667)
- Google Pixel 7 (412x915)
- Samsung Galaxy S20 (412x915)

EOL
