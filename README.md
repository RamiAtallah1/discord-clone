# Discord Clone

This is a Discord clone project that replicates the popular communication platform's features using Next.js 13, React, <span style="display: inline">Socket.io</span>, Prisma, Tailwind CSS, and MySQL.

## Table of Contents

- [Introduction](#introduction)
- [Features](#features)
- [Installation](#installation)
- [Usage](#usage)
- [Environment Variables](#environment-variables)

## Introduction

Discord Clone is a real-time communication platform designed to facilitate text, voice, and video communication among users. It offers features similar to Discord, allowing users to create servers, join channels, engage in conversations, and manage their communities.

## Features

- **Real-time Messaging**: Utilize <span style="display: inline">Socket.io</span> for seamless real-time messaging between users.
- **Attachment Support**: Send attachments as messages using UploadThing.
- **Message Management**: Users can delete and edit messages in real-time.
- **Voice and Video Channels**: Create text, audio, and video call channels for interactive communication.
- **1:1 Conversations**: Members can engage in private one-on-one conversations.
- **1:1 Video Calls**: Initiate video calls between members for face-to-face communication.
- **Member Management**: Ability to manage members, including kicking and changing roles (guest/moderator).
- **Invite System**: Generate unique invite links and implement a fully functional invite system.
- **Infinite Message Loading**: Implement infinite loading for messages in batches of 10 for smooth user experience.
- **Server Customization**: Create servers and customize them according to preferences.
- **User Interface**: Beautiful UI crafted with TailwindCSS and ShadcnUI, ensuring an engaging visual experience.
- **Responsive Design**: Full responsivity and mobile-friendly UI for accessibility across devices.
- **Dark Mode**: Support for light and dark modes to cater to user preferences.
- **Websocket Fallback**: Automatic fallback to polling with alerts in case of websocket issues.
- **ORM with Prisma**: Utilize Prisma for object-relational mapping for efficient database interactions.
- **MySQL Database**: Utilize Planetscale for a robust MySQL database backend.
- **Authentication**: Implement secure authentication using Clerk for user management.

## Installation

To run the Discord clone locally, follow these steps:

1. Clone the repository to your local machine:

```bash
git clone https://github.com/RamiAtallah1/discord-clone.git
```

2. Navigate to the project directory:

```bash
cd discord-clone
```

3. Install dependencies using npm or yarn:

```bash
npm install
# or
yarn install
```

4. Set up the MySQL database:

   - Create a MySQL database for the project.
   - Update the database configuration in `.env` file with your MySQL connection details.

5. Run the database migrations:

```bash
npx prisma migrate dev
```

6. Start the development server:

```bash
npm run dev
# or
yarn dev
```

This will start the development server and you can access the Discord clone in your web browser at `http://localhost:3000`.

## Usage

Once the development server is running, you can sign up, log in, create servers, join servers, and start chatting with other users in real-time.

## Environment Variables

The project uses environment variables to manage sensitive information and configuration. You should create a `.env` file in the root directory of the project and add the following variables:

- **NEXT_PUBLIC_CLERK_PUBLISHABLE_KEY**: Clerk Publishable Key for authentication.
- **CLERK_SECRET_KEY**: Clerk Secret Key for authentication.
- **NEXT_PUBLIC_CLERK_SIGN_IN_URL**: URL for signing in with Clerk.
- **NEXT_PUBLIC_CLERK_SIGN_UP_URL**: URL for signing up with Clerk.
- **NEXT_PUBLIC_CLERK_AFTER_SIGN_IN_URL**: URL to redirect to after signing in with Clerk.
- **NEXT_PUBLIC_CLERK_AFTER_SIGN_UP_URL**: URL to redirect to after signing up with Clerk.
- **DATABASE_URL**: MySQL database connection URL.
- **UPLOADTHING_SECRET**: Secret key for UploadThing service.
- **UPLOADTHING_APP_ID**: App ID for UploadThing service.
- **LIVEKIT_API_KEY**: API key for LiveKit integration.
- **LIVEKIT_API_SECRET**: API secret for LiveKit integration.
- **NEXT_PUBLIC_LIVEKIT_URL**: URL for LiveKit service.
- **NEXT_PUBLIC_SITE_URL**: URL for the site.
