# c221 — Video Chat App with Email Invites

A real-time video chat application with room-based URLs, PeerJS video calls, text chat, and email invitations via Nodemailer.

## Features
- Random room URLs (`/:uuid`) to join a video room.
- Peer-to-peer video/audio calls using PeerJS.
- Real-time text chat within a room via Socket.IO.
- Mute/unmute and camera on/off controls.
- Email invitations with a join link (Nodemailer/SMTP).

## Tech Stack
- Node.js, Express, EJS
- Socket.IO, PeerJS, UUID
- Nodemailer (Gmail SMTP)

## Project Structure
```
├── server.js          # Express + Socket.IO + PeerServer + mail route
├── package.json
├── views/index.ejs    # room UI
└── public/            # style.css, script.js
```

## Installation
```bash
npm install
# configure SMTP credentials in server.js before sending mail
```

## Usage
```bash
node server.js   # listens on :3030
```
- Visiting `/` redirects to a fresh `/roomId`; share the URL with others.
- Use the on-screen controls to mute, stop video, send chat, or email an invite.