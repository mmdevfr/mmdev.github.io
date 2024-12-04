<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>my websitel</title>
    <style>
        /* Reset default margins and paddings */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        /* Basic Styling */
        body {
            font-family: 'Arial', sans-serif;
            background-color: #f0f0f0;
            color: #333;
            height: 100vh;
            display: flex;
            justify-content: center;
            align-items: center;
            overflow: hidden;
            position: relative;
        }

        .content {
            text-align: center;
            padding: 40px;
            background-color: white;
            border-radius: 8px;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
        }

        h1 {
            font-size: 2.5rem;
            margin-bottom: 20px;
        }

        p {
            font-size: 1rem;
            color: #666;
        }

        /* Snowfall Effect */
        .snowflake {
            position: absolute;
            top: -10px;
            pointer-events: none;
            user-select: none;
            color: #ffffff;
            font-size: 24px;
            animation: fall linear infinite;
        }

        @keyframes fall {
            to {
                transform: translateY(100vh);
            }
        }
    </style>
</head>
<body>
    <div class="content">
        <h1>https://fbi.bio/mmdev</h1>
        <p>i will make the website better when i learn more html def not chatgpt.</p>
    </div>

    <script>
        // Snowfall effect
        const snowflakes = ['❄', '❅', '❆']; // Snowflake characters

        function createSnowflake() {
            const snowflake = document.createElement('span');
            snowflake.classList.add('snowflake');
            snowflake.textContent = snowflakes[Math.floor(Math.random() * snowflakes.length)];

            // Random position and animation delay
            snowflake.style.left = `${Math.random() * 100}vw`;
            snowflake.style.animationDuration = `${Math.random() * 5 + 5}s`;  // Random duration between 5 and 10 seconds
            snowflake.style.fontSize = `${Math.random() * 10 + 20}px`; // Random size

            document.body.appendChild(snowflake);

            // Remove snowflake after it falls to the bottom
            setTimeout(() => {
                snowflake.remove();
            }, 10000);  // Match with animation duration
        }

        // Generate snowflakes continuously
        setInterval(createSnowflake, 200); // Create a snowflake every 200ms
    </script>
</body>
</html>
