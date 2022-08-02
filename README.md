# Docker Arduino Project

Project to learn Rust and Next.js.  
Arduino and API are both written in Rust, they communicate with a simple protocol and handshake to set up communication.

The Arduino will listen to actions such as displaying a message and switching the LED, but also serves DHT measurements.
The API uses threading and a mutex to make sure the Arduino only processes one request at a time, while the rest of the API is not blocked.

The frontend in Next.js provides the actions of the API. It uses static props to revalidate the DHT measurements with SSR.

## Running the project

### Arduino

First make sure the Rust Arduino project is flashed.

### Init repos

Make sure submodules for the API and frontend are pulled.
Front-end requires setup of `.env.local`.
Check the README.md of both repos.

### Docker compose

Then run the project with `docker compose up -d`.
