<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Valentine's Day</title>
    <style>
        body {
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            margin: 0;
            background-color: pink;
            font-family: 'Arial', sans-serif;
            text-align: center;
        }

        .container {
            text-align: center;
        }

        h1 {
            color: red;
            font-size: 3em;
        }

        .buttons {
            margin-top: 20px;
        }

        .buttons button {
            padding: 15px 30px;
            font-size: 1.5em;
            margin: 10px;
            cursor: pointer;
            border: none;
            border-radius: 10px;
            transition: all 0.3s ease;
        }

        #yesButton {
            background-color: green;
            color: white;
        }

        #noButton {
            background-color: red;
            color: white;
        }

        #message {
            margin-top: 20px;
            font-size: 2em;
            color: red;
            display: none; /* Hidden by default */
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>Will you be my Valentine?</h1>
        <div class="buttons">
            <button id="yesButton">Yes</button>
            <button id="noButton">No</button>
        </div>
        <div id="message">Yay! I knew you'd say yes! 💖 You make me the happiest person in the world! 😘</div>
    </div>

    <script>
        const yesButton = document.getElementById('yesButton');
        const noButton = document.getElementById('noButton');
        const message = document.getElementById('message');

        let scale = 1; // Initial scale of the "Yes" button

        noButton.addEventListener('click', () => {
            scale += 0.5; // Increase the scale by 0.5 every time "No" is clicked
            yesButton.style.transform = `scale(${scale})`; // Apply the new scale
        });

        yesButton.addEventListener('click', () => {
            message.style.display = 'block'; // Show the cute message
            yesButton.style.display = 'none'; // Hide the "Yes" button
            noButton.style.display = 'none'; // Hide the "No" button
        });
    </script>
</body>
</html>

