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
            background: radial-gradient(circle, #ff0000, #660000);
            color: white;
            height: 100vh;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
        }

        h1 {
            max-width: 80%;
            font-size: 24px;
        }

        #yes, #no {
            font-size: 20px;
            padding: 10px 20px;
            border: none;
            cursor: pointer;
            transition: transform 0.3s, left 0.3s, top 0.3s;
            position: absolute;
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
    <h1>If someone asked me to define love, I might stumble over the words, but one thing I know for sure is that what we have is real, pure, and absolutely magical ✨❤️.<br>
    Every moment with you feels like a beautiful story unfolding, and I wouldn’t trade it for anything.<br>
    So, here’s the much-anticipated question... will you make me the happiest person alive by being my girlfriend? 🥰💍💕</h1>

    <button id="yes">Yes</button>
    <button id="no">No</button>

    <script>
        let yesButton = document.getElementById("yes");
        let noButton = document.getElementById("no");
        let moves = 0;

        function moveNoButton() {
            if (moves < 6) {
                let randomX = Math.random() * (window.innerWidth - 100);
                let randomY = Math.random() * (window.innerHeight - 100);
                noButton.style.left = `${randomX}px`;
                noButton.style.top = `${randomY}px`;
                moves++;
            } else {
                noButton.style.display = "none";
            }

            let currentSize = parseInt(window.getComputedStyle(yesButton).fontSize);
            yesButton.style.fontSize = (currentSize + 5) + "px";
        }

        noButton.addEventListener("click", moveNoButton);

        yesButton.addEventListener("click", function() {
            alert("Mwangi says: Now I'm yours for life ❤️");
            window.open('https://open.spotify.com/track/7wfDCDfhVe2tFxIkQEJp35', '_blank');
        });

        // Set initial button positions
        yesButton.style.position = "absolute";
        yesButton.style.left = "45%";
        yesButton.style.top = "60%";

        noButton.style.position = "absolute";
        noButton.style.left = "55%";
        noButton.style.top = "60%";
    </script>
</body>
</html>
