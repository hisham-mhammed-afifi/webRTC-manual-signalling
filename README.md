# WebRTC Manual Signaling Demo

A completely serverless WebRTC video calling demonstration where signaling happens manually through copy/paste. No server required - just two browsers and any communication channel (email, chat, carrier pigeon, etc.)

## Features

- **Zero Server Dependencies** - All signaling is done manually via copy/paste
- **Video & Audio Calls** - Full WebRTC peer-to-peer media streaming
- **Audio Only Mode** - Option to disable video for voice-only calls
- **Data Channel Chat** - Text messaging over WebRTC data channels
- **ICE Candidate Management** - Manual or automatic ICE candidate exchange
- **Debug Logging** - Real-time connection state and event logging
- **Responsive Design** - Works on desktop and mobile browsers

## How to Use

### For Caller (Person A)

1. Open `index.html` in your browser
2. Click **Start Camera** to enable your camera/microphone
3. Click **Create Offer** to generate a connection offer
4. Copy the offer JSON and send it to your peer via any means
5. Wait for peer's answer, paste it in the Answer section
6. Click **Accept Answer** to complete your side of signaling
7. Exchange ICE candidates with your peer (if not using "Wait for all ICE")

### For Callee (Person B)

1. Open `index.html` in your browser
2. Click **Start Camera** to enable your camera/microphone
3. Paste the received offer in the Offer section
4. Click **Accept Offer** - this generates an answer automatically
5. Copy the generated answer and send it back to the caller
6. Exchange ICE candidates with your peer (if not using "Wait for all ICE")

### Connection Complete

- Status indicator turns green when connected
- Remote video stream appears in the right panel
- Use the chat feature to send text messages
- Click **Hang Up** to end the call and reset

## Options

- **Audio Only Mode** - Check this before starting camera to disable video
- **Wait for all ICE candidates** (recommended) - Bundles ICE candidates with offer/answer for simpler exchange

## Requirements

- A modern browser with WebRTC support (Chrome, Firefox, Safari, Edge)
- Camera and microphone permissions
- Any communication channel to exchange signaling data (email, messaging app, etc.)

## Educational Purpose

This demo is designed to help understand how WebRTC signaling works by making the process completely visible and manual. It demonstrates:

- SDP (Session Description Protocol) offer/answer exchange
- ICE (Interactive Connectivity Establishment) candidate gathering
- Peer connection state management
- Media stream handling
- Data channel communication

## License

MIT
