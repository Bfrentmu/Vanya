<html>
<head>
    <title>For My Beloved Vanya</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-image: url('background.jpg');
            background-size: cover;
            background-position: center;
            margin: 0;
            padding: 0;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
        }
        .container {
            background-color: rgba(255, 255, 255, 0.9);
            border-radius: 10px;
            padding: 30px;
            text-align: center;
            max-width: 500px;
            box-shadow: 0 4px 10px rgba(0, 0, 0, 0.2);
        }
        h1 {
            color: #e91e63;
            font-size: 36px;
            margin-bottom: 20px;
        }
        p {
            font-size: 18px;
            line-height: 1.6;
        }
        .popup {
            display: none;
            position: fixed;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            padding: 20px;
            background-color: rgba(255, 255, 255, 0.9);
            border-radius: 10px;
            box-shadow: 0 4px 10px rgba(0, 0, 0, 0.2);
            z-index: 1000;
            text-align: center;
        }
        .popup-message {
            font-size: 20px;
            margin-bottom: 20px;
            line-height: 1.5;
        }
        .popup-button {
            background-color: #e91e63;
            color: #fff;
            border: none;
            border-radius: 5px;
            padding: 10px 20px;
            cursor: pointer;
            font-size: 16px;
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>For My Beloved Vanya</h1>
        <p>Dear Vanya,</p>
        <p>halo cantikku, kamu hari ini sibuk gasih??? ya kalo sibukpun gapapa</p>
        <p>i know beberapa hari ini mood kamu lagi kurang bagus, but i can't do anything so i just sending you this</p>
        <p>jangan skip makan ya cantikk, semoga acara hari ini lancar</p>
        <p>semangattttt</p>
    <img src="https://github.com/Bfrentmu/Vanya/blob/2a27bbbb9afa1acdd70ac2d1b0c84b8b64e719da/giphy%20(1).gif" alt="error">
    </div>

    <div class="popup" id="popup1">
        <p class="popup-message">Hallooo Vanya cantikku</p>
        <button class="popup-button" onclick="showPopup('popup2')">Close</button>
    </div>

    <div class="popup" id="popup2">
        <p class="popup-message">Semoga harinya menyenangkan yaaaa</p>
        <button class="popup-button" onclick="showPopup('popup3')">Close</button>
    </div>

    <div class="popup" id="popup3">
        <p class="popup-message">I love you ❤</p>
        <button class="popup-button" onclick="closePopups()">Close</button>
    </div>

    <script>
        function showPopup(popupId) {
            document.getElementById(popupId).style.display = "block";
        }

        function closePopups() {
            const popups = document.getElementsByClassName("popup");
            for (let i = 0; i < popups.length; i++) {
                popups[i].style.display = "none";
            }
        }

        // Show the first popup when the page loads
        window.onload = function() {
            showPopup("popup1");
        };
    </script>
</body>
</html>
