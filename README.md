<!DOCTYPE html>
<html>
<head>
    <title>Romantic Popup</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: rgba(240, 173, 78, 0.1);
            margin: 0;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
        }
        .popup-container {
            background-color: rgba(255, 255, 255, 0.9);
            border-radius: 10px;
            box-shadow: 0 4px 10px rgba(0, 0, 0, 0.2);
            padding: 20px;
            text-align: center;
            display: none;
            position: absolute;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            max-width: 80%;
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
    <div class="popup-container" id="popup1">
        <p class="popup-message">Halooo Selamat siang Vanya cantikku</p>
        <button class="popup-button" onclick="showPopup('popup2')">OK</button>
    </div>

    <div class="popup-container" id="popup2">
        <p class="popup-message">Semoga harinya menyenangkan ya sayaang</p>
        <button class="popup-button" onclick="showPopup('popup3')">OK</button>
    </div>

    <div class="popup-container" id="popup3">
        <p class="popup-message">I love you ❤</p>
        <button class="popup-button" onclick="closePopups()">Close</button>
    </div>

    <script>
        function showPopup(popupId) {
            document.getElementById(popupId).style.display = "block";
        }

        function closePopups() {
            const popups = document.getElementsByClassName("popup-container");
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
