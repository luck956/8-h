<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Biography</title>
    <style>
        /* Basic reset */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        /* Black background */
        body {
            color: #fff;
            font-family: Arial, sans-serif;
            height: 100vh;
            display: flex;
            justify-content: center;
            align-items: center;
            padding: 20px;
            background: #000; /* Solid black background */
            overflow: hidden;
        }

        .container {
            position: relative;
            width: 100%;
            height: 100%;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
        }

        .biography {
            max-width: 800px;
            background-color: #1c1c1c;
            padding: 20px;
            border-radius: 10px;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
            opacity: 0;
            transform: translateX(100%);
            transition: opacity 0.5s ease, transform 0.5s ease;
        }

        .biography.active {
            opacity: 1;
            transform: translateX(0);
        }

        .biography h1 {
            font-size: 3em;
            color: white;
            text-shadow: 2px 2px 10px rgba(0, 0, 0, 0.7);
            margin-bottom: 20px;
            text-align: center;
        }

        .biography p {
            font-size: 1.2em;
            line-height: 1.6;
            color: #dcdcdc;
            margin-bottom: 20px;
        }

        .image {
            text-align: center;
            margin-bottom: 20px;
        }

        .image img {
            max-width: 100%;
            height: auto;
            border-radius: 8px;
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
        }

        .navigation {
            position: absolute;
            bottom: 20px;
            display: flex;
            gap: 20px;
        }

        .nav-button {
            padding: 10px 20px;
            background-color: #34495e;
            color: white;
            border: none;
            border-radius: 5px;
            cursor: pointer;
            font-size: 1em;
            transition: background-color 0.3s ease;
        }

        .nav-button:hover {
            background-color: #2c3e50;
        }
    </style>
</head>
<body>
    <div class="container">
        <div class="biography" id="apry-bio">
            <div class="image">
                <img src="apry.jpeg" alt="Image of Apry">
            </div>
            <h1>Apry Malla</h1>
            <p>Apry Malla, born on April 24, 2011, is known for their unique style and love for comfort, often seen in a hoodie and baggy jeans. A devoted dog lover, Apry finds joy in the company of their furry friends. They are deeply inspired by the balance of light and shadow in life, much like the concept of "Ghaam Chaya." Fictional worlds and characters hold a special place in Apry’s heart, showcasing their vivid imagination and creative spirit.</p>
            <p>Apry’s close friend circle includes cherished friends such as Garima, Prasiddhi Shistata, and Zade as favorate person, who share a bond of mutual respect and understanding. Together, they form a tapestry of stories and shared memories, each thread as vibrant and meaningful as the last.</p>
        </div>

        <div class="biography" id="garima-bio">
            <div class="image">
                <img src="garima.jpeg" alt="Image of Garima">
            </div>
            <h1>Garima Shrestha</h1>
            <p>Garima Shrestha, born on March 2, 2011, has a love for comfortable attire, often opting for hoodies that match her casual and relaxed personality. A passionate dog lover, Garima’s days are brightened by her furry companions. She finds joy and energy in the music of BLACKPINK, which fuels her creativity and zest for life.</p>
            <p>Garima also has a deep appreciation for fictional characters and stories, which provide her with an escape into worlds filled with endless possibilities. She shares her journey with close friends like Apry, Prasiddhi Shistata, and Zade, making every moment an adventure worth cherishing.</p>
        </div>

        <div class="navigation">
            <button class="nav-button" onclick="showBiography('apry-bio')">Apry</button>
            <button class="nav-button" onclick="showBiography('garima-bio')">Garima</button>
        </div>
    </div>

    <script>
        function showBiography(id) {
            const bios = document.querySelectorAll('.biography');
            bios.forEach(bio => bio.classList.remove('active'));
            document.getElementById(id).classList.add('active');
        }

        // Default to showing Apry's bio
        showBiography('apry-bio');
    </script>
</body>
</html>

