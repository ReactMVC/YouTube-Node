# YouTube API

This is a fast and modern API for downloading videos, audios, thumbnails, and getting video information from YouTube. It's built with Node.js and uses the `ytdl-core` library to interact with YouTube.

## Installation

To install and run this project, follow these steps:

1. Clone the repository:

```bash
git clone https://github.com/ReactMVC/YouTube-Node.git
```

2. Navigate into the project directory:

```bash
cd YouTube-Node
```

3. Install the dependencies:

```bash
npm install
```

4. Start the server:

```bash
npm start
```

The server will start running on port 3000.

## Usage

This API provides two endpoints, both of which accept a YouTube URL and return information about the video.

### GET Request

To send a GET request, use the `/api` endpoint and include the YouTube URL as a query parameter:

```javascript
fetch('http://localhost:3000/api?url=YOUR_YOUTUBE_URL')
  .then(response => response.json())
  .then(data => console.log(data));
```

### POST Request with Fetch

```javascript
fetch('http://localhost:3000/api', {
  method: 'POST',
  headers: {
    'Content-Type': 'application/json',
  },
  body: JSON.stringify({ url: 'YOUR_YOUTUBE_URL' }),
})
  .then(response => response.json())
  .then(data => console.log(data));
```

### POST Request with Axios

```javascript
const axios = require('axios');

axios.post('http://localhost:3000/api', {
  url: 'YOUR_YOUTUBE_URL'
})
.then(function (response) {
  console.log(response.data);
})
.catch(function (error) {
  console.error(error);
});
```

### cURL Command for POST Request

You can also use cURL to send a POST request:

```bash
curl -X POST -H "Content-Type: application/json" -d '{"url":"YOUR_YOUTUBE_URL"}' http://localhost:3000/api
```

## Response

The API will return a JSON object containing information about the video, including the title, description, view count, channel details, publish date, update date, embed details, thumbnails, and available formats.

## Demo

You can try out the API at the following demo URL:

[https://youtube.reactmvc.repl.co/api?url=YOUR_YOUTUBE_URL](https://youtube.reactmvc.repl.co/api?url=YOUR_YOUTUBE_URL)

Please replace `youtube.reactmvc.repl.co` with the actual URL where your API is hosted, and replace `YOUR_YOUTUBE_URL` with the URL of the YouTube video you want to get information about.

For example, if your API is hosted at `api.example.com` and you want to get information about the video at `https://www.youtube.com/watch?v=dQw4w9WgXcQ`, you would use the following URL:

```bash
http://api.example.com/api?url=https://www.youtube.com/watch?v=dQw4w9WgXcQ
```

## Developer Contact

For any queries or suggestions, you can reach out to the developer:

- Name: Hossein Pira
- Email: h3dev.pira@gmail.com
- Telegram: [@h3dev](https://t.me/h3dev)

## License

This project is licensed under the MIT License.
