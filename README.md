# PiecesIndex

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Random Earth Facts</title>
    <style>
        body {
            font-family: 'Arial', sans-serif;
            background-color: #f0f4f8;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            margin: 0;
        }

        .container {
            text-align: center;
            background: white;
            border-radius: 10px;
            box-shadow: 0 4px 20px rgba(0, 0, 0, 0.1);
            padding: 20px;
            transition: transform 0.3s ease;
        }

        .container:hover {
            transform: scale(1.05);
        }

        h1 {
            color: #333;
        }

        #fact-display {
            font-size: 1.5em;
            margin: 20px 0;
            opacity: 0;
            transition: opacity 0.5s ease;
        }

        button {
            padding: 10px 20px;
            font-size: 1em;
            color: white;
            background-color: #007BFF;
            border: none;
            border-radius: 5px;
            cursor: pointer;
            box-shadow: 0 4px 10px rgba(0, 0, 0, 0.2);
            transition: background-color 0.3s ease, transform 0.3s ease;
        }

        button:hover {
            background-color: #0056b3;
            transform: translateY(-2px);
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>Random Earth Fact</h1>
        <p id="fact-display">Click the button to see a fact!</p>
        <button id="fact-button">Show Random Fact</button>
    </div>
    <script>
        const facts = [
            "Earth is the third planet from the Sun.",
            "Earth has a unique atmosphere composed of 78% nitrogen and 21% oxygen.",
            "Approximately 71% of Earth's surface is covered by water.",
            "Earth is about 4.5 billion years old.",
            "Earth's surface is divided into tectonic plates.",
            "Earth has a magnetic field that protects it from solar radiation.",
            "Earth is the only known planet to support life.",
            "The tilt of Earth's axis is responsible for the changing seasons.",
            "Earth has one natural satellite, the Moon.",
            "Earth hosts a wide variety of ecosystems."
        ];

        const factDisplay = document.getElementById('fact-display');
        const factButton = document.getElementById('fact-button');

        factButton.addEventListener('click', () => {
            const randomIndex = Math.floor(Math.random() * facts.length);
            factDisplay.textContent = facts[randomIndex];
            factDisplay.style.opacity = 0; // Start with opacity 0 for animation
            setTimeout(() => {
                factDisplay.style.opacity = 1; // Fade in the fact
            }, 100); // Delay to allow for the opacity reset
        });
    </script>
</body>
</html>
