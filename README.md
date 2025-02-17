<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Flower Fun Fact Generator</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background: linear-gradient(135deg, #f6d365 0%, #fda085 100%);
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            margin: 0;
            overflow: hidden;
        }

        .container {
            text-align: center;
            background: white;
            padding: 20px;
            border-radius: 10px;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
            animation: fadeIn 2s ease-in-out;
        }

        h1 {
            color: #333;
        }

        button {
            background-color: #ff6f61;
            color: white;
            border: none;
            padding: 10px 20px;
            font-size: 16px;
            cursor: pointer;
            border-radius: 5px;
            transition: background-color 0.3s ease;
        }

        button:hover {
            background-color: #ff3b2f;
        }

        .fact-display {
            margin-top: 20px;
            font-size: 18px;
            color: #555;
            animation: slideIn 1s ease-out;
        }

        @keyframes fadeIn {
            from { opacity: 0; }
            to { opacity: 1; }
        }

        @keyframes slideIn {
            from { transform: translateY(20px); opacity: 0; }
            to { transform: translateY(0); opacity: 1; }
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>Flower Fun Fact Generator</h1>
        <button id="generateFactBtn">Generate Fun Fact</button>
        <div id="factDisplay" class="fact-display"></div>
    </div>
    <script>
        const facts = [
            "Sunflowers can grow up to 12 feet tall.",
            "Tulips were once more valuable than gold in Holland.",
            "The largest flower in the world is the Rafflesia arnoldii.",
            "Dandelions are completely edible, from root to flower.",
            "The smell of roses can help you relax and reduce stress."
        ];

        document.getElementById('generateFactBtn').addEventListener('click', function() {
            const randomIndex = Math.floor(Math.random() * facts.length);
            const factDisplay = document.getElementById('factDisplay');
            factDisplay.textContent = facts[randomIndex];
        });
    </script>
</body>
</html>
