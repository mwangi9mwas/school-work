<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Will You Be My Girlfriend?</title>
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Pacifico&display=swap');
        body {
            text-align: center;
            font-family: 'Pacifico', cursive;
            margin-top: 100px;
            background: linear-gradient(rgba(0, 0, 0, 0.5), rgba(0, 0, 0, 0.5)), url('https://source.unsplash.com/1600x900/?love,romantic') no-repeat center center fixed; background-color: #ff6699;
            background-size: cover;
            color: white;
            height: 100vh;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
        }
        #yes, #no {
            font-size: 20px;
            padding: 10px 20px;
            border: none;
            cursor: pointer;
            transition: transform 0.3s;
        }
        #yes {
            background-color: #28a745;
            color: white;
        }
        #no {
            background-color: #dc3545;
            color: white;
        }
        #yes:hover, #no:hover {
            transform: scale(1.1);
        }
    </style>
</head>
<body>
    <h1>If someone asked me to define love, I might stumble over the words, but one thing I know for sure is that what we have is real, pure, and absolutely magical ✨❤️.<br>Every moment with you feels like a beautiful story unfolding, and I wouldn’t trade it for anything.<br>So, here’s the much-anticipated question... will you make me the happiest man alive by being my girlfriend? 🥰💍💕</h1>
    <button id="yes">Yes</button>
    <button id="no">No</button>

    <script src="https://cdn.jsdelivr.net/npm/canvas-confetti@1.5.1/dist/confetti.browser.min.js"></script>
    <script>
        let yesButton = document.getElementById("yes");
        let noButton = document.getElementById("no");

        noButton.addEventListener("click", function() {
            let currentSize = parseInt(window.getComputedStyle(yesButton).fontSize);
            yesButton.style.fontSize = (currentSize + 5) + "px";
        });

        yesButton.addEventListener("click", function() {
            confetti({
                particleCount: 500,
                spread: 150,
                origin: { y: 0.6 }
            });
            alert("Now I'm yours for life ❤️");
        });
    </script>
<button id="spotify-link" style="display: none;">Listen on Spotify</button>
    <script>
        yesButton.addEventListener("click", function() {
            window.open('https://open.spotify.com/track/7wfDCDfhVe2tFxIkQEJp35', '_blank');
        });
    </script>
</body>
</html>
