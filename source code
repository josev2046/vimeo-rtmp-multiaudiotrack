├── index.html
└── script.js

**index.html**

<!DOCTYPE html>
<html>
<head>
  <title>Multi-Language Live Stream</title>
  <style>
    body {
      display: flex;
      align-items: flex-start;
      justify-content: center;
      height: 100vh;
      margin: 0;
      background-color: #f0f0f0;
      padding: 10px;
      box-sizing: border-box;
    }

    .container {
      display: flex;
      gap: 20px;
      width: 95%; 
      max-width: 1400px; 
    }

    .video-container, .qa-container {
      position: relative;
      padding-top: 56.25%; 
      overflow: hidden;
      flex: 1;
    }

    .video-container iframe, .qa-container iframe {
      position: absolute;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      border: none;
    }

    select {
      padding: 10px;
      font-size: 16px;
    }
  </style>
</head>
<body>

  <div class="container">
    <select onchange="changeStream(this.value)">
      <option value="0">Language #1</option>
      <option value="1">Language #2</option>
      <option value="2">Language #3</option>
    </select>

    <div class="video-container" id="video-container">
    </div>

    <div class="qa-container" id="qa-container"></div> 
  </div>

  <script src="script.js"></script>

</body>
</html>

**script.js**

const videoIds = [
  'ID#1', 
  'ID#2', 
  'ID#3', 
];

function changeStream(index) {
  const videoContainer = document.getElementById('video-container');
  const qaContainer = document.getElementById('qa-container');

  videoContainer.innerHTML = '';
  qaContainer.innerHTML = '';

  const videoIframe = document.createElement('iframe');
  videoIframe.src = `https://vimeo.com/event/${videoIds[index]}/embed?autoplay=1`;
  videoIframe.frameBorder = '0';
  videoIframe.allow = 'autoplay; fullscreen; picture-in-picture';
  videoIframe.allowFullscreen = true;
  videoContainer.appendChild(videoIframe);

  const qaIframe = document.createElement('iframe');
  qaIframe.src = `https://vimeo.com/live/interaction_tools/live_event/${videoIds[index]}?module=auto&amp;theme=light`;
  qaIframe.frameBorder = '0';
  qaIframe.allow = 'autoplay; fullscreen; picture-in-picture';
  qaIframe.allowFullscreen = true;
  qaContainer.appendChild(qaIframe);
}

changeStream(0);
