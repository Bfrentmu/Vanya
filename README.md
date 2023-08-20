<!DOCTYPE html>
<html>
<head>
    <title>Popup Sequence</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #f4f4f4;
            margin: 0;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
        }
        .popup-container {
            background-color: #fff;
            border-radius: 10px;
            box-shadow: 0 4px 10px rgba(0, 0, 0, 0.2);
            padding: 20px;
            text-align: center;
            display: none;
        }
        .popup-message {
            font-size: 18px;
            margin-bottom: 20px;
        }
        .popup-button {
            background-color: #e91e63;
            color: #fff;
            border: none;
            border-radius: 5px;
            padding: 10px 20px;
            cursor: pointer;
        }
    </style>
</head>
<body>
    <div class="popup-container" id="popup1">
        <p class="popup-message">Haloo Vanya cantikku</p>
        <button class="popup-button" onclick="showPopup('popup2')">OK</button>
    </div>

    <div class="popup-container" id="popup2">
        <p class="popup-message">Semoga harinya menyenangkan ya sayang</p>
        <button class="popup-button" onclick="showPopup('popup3')">OK</button>
    </div>

    <div class="popup-container" id="popup3">
        <p class="popup-message">I love you</p>
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
