# MusicPlatform
this is a music platform
<!DOCTYPE html>
<html>
<head>
    <title>My Music Platform</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #f0f0f0;
        }
        #music-player {
            width: 300px;
            margin: 0 auto;
            background-color: #fff;
            padding: 20px;
            border: 1px solid #ccc;
            border-radius: 5px;
        }
        h1 {
            text-align: center;
        }
        #song-title {
            font-size: 18px;
            margin: 10px 0;
        }
        #music-controls {
            display: flex;
            justify-content: center;
            align-items: center;
        }
        #play-button, #pause-button, #stop-button {
            background-color: #4CAF50;
            color: #fff;
            border: none;
            padding: 10px 20px;
            margin: 0 10px;
            border-radius: 5px;
            cursor: pointer;
        }
        #play-button:hover, #pause-button:hover, #stop-button:hover {
            background-color: #45a049;
        }
    </style>
</head>
<body>
    <div id="music-player">
        <h1>My Music Player</h1>
        <div id="song-title">Song Title</div>
        <audio id="audio" controls>
            <source src="your-music.mp3" type="audio/mpeg">
            Your browser does not support the audio element.
        </audio>
        <div id="music-controls">
            <button id="play-button">Play</button>
            <button id="pause-button">Pause</button>
            <button id="stop-button">Stop</button>
        </div>
    </div>

    <script>
        const audio = document.getElementById("audio");
        const playButton = document.getElementById("play-button");
        const pauseButton = document.getElementById("pause-button");
        const stopButton = document.getElementById("stop-button");

        playButton.addEventListener("click", function() {
            audio.play();
        });

        pauseButton.addEventListener("click", function() {
            audio.pause();
        });

        stopButton.addEventListener("click", function() {
            audio.pause();
            audio.currentTime = 0;
        });
    </script>
</body>
</html>
