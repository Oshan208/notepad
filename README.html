<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Notepad</title>
    <style>
        /* Your existing CSS styles here */
        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            margin: 0;
            padding: 0;
            background-image: url('https://vauclusespring.com/wp-content/uploads/2016/12/hiking-in-northern-va.jpg');
            background-size: cover;
            background-position: center;
            display: flex;
            justify-content: center;
            align-items: center;
            min-height: 100vh;
        }

        .container {
            max-width: 600px;
            padding: 30px;
            background-color: rgba(255, 255, 255, 0.9);
            border-radius: 10px;
            box-shadow: 0px 0px 20px rgba(0, 0, 0, 0.2);
        }

        h2 {
            text-align: center;
            color: #333;
            margin-bottom: 20px;
        }

        textarea {
            width: 100%;
            height: 200px;
            padding: 10px;
            border: 1px solid #ccc;
            border-radius: 5px;
            resize: vertical;
            margin-bottom: 20px;
            font-size: 16px;
            color: #333;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background-color: rgba(255, 255, 255, 0.7); /* Modified background color */
        }

        .button-container {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .button-container button {
            padding: 10px 20px;
            background-color: #007bff;
            color: #fff;
            border: none;
            border-radius: 5px;
            cursor: pointer;
            transition: background-color 0.3s;
        }

        .button-container button:hover {
            background-color: #0056b3;
        }

        .file-list {
            margin-top: 20px;
        }

        .file-list h3 {
            color: #333;
            font-size: 18px;
            margin-bottom: 10px;
        }

        .file-list ul {
            padding: 0;
            margin: 0;
            list-style-type: none;
        }

        .file-list-item {
            cursor: pointer;
            margin-bottom: 5px;
            color: #007bff;
            font-size: 14px;
            transition: color 0.3s;
        }

        .file-list-item:hover {
            text-decoration: underline;
            color: #0056b3;
        }

        .error-message {
            color: red;
            font-size: 14px;
            margin-top: 5px;
        }

        label {
            font-size: 16px;
            color: #333;
            margin-right: 10px;
        }

        select, input[type="color"], input[type="number"] {
            font-size: 16px;
            padding: 8px;
            border: 1px solid #ccc;
            border-radius: 5px;
        }

        .file-container {
            margin-top: 20px;
            border: 1px solid #ccc;
            padding: 10px;
            border-radius: 5px;
            background-color: #f9f9f9;
            position: relative;
        }

        .file-container h3 {
            color: #333;
            margin-bottom: 10px;
        }

        .file-content {
            white-space: pre-wrap;
        }

        .remove-button {
            background-color: #dc3545;
            color: #fff;
            border: none;
            padding: 5px 10px;
            border-radius: 5px;
            cursor: pointer;
            position: absolute;
            top: 10px;
            right: 10px;
        }

        .remove-button:hover {
            background-color: #c82333;
        }
    </style>
</head>
<body>
<div class="container">
    <h2>Notepad</h2>
    <form id="noteForm">
        <textarea id="noteText" placeholder="Enter your note here"></textarea>
        <div id="errorMessage" class="error-message" style="display: none;">Please Type Anything to Save !</div>
        <div class="button-container">
            <label for="fileInput" class="button">Open</label>
            <input type="file" id="fileInput" accept=".txt" multiple onchange="handleFileSelect(event)">
            <button type="button" onclick="saveNote()">Save Note</button>
        </div>
        <div class="file-list">
            <h3>Last 10 Files</h3>
            <ul id="lastFilesList"></ul>
        </div>
        <button type="button" onclick="clearData()" style="margin-top: 20px;">Clear Data</button>
    </form>
    <div>
        <label for="colorSelect">Text Color:</label>
        <input type="color" id="colorSelect" onchange="changeColor()">
    </div>
    <div>
        <label for="fontSelect">Font Family:</label>
        <select id="fontSelect" onchange="changeFont()">
            <option value="'Segoe UI', Tahoma, Geneva, Verdana, sans-serif">Segoe UI</option>
            <option value="Arial, sans-serif">Arial</option>
            <option value="Verdana, sans-serif">Verdana</option>
            <option value="Georgia, serif">Georgia</option>
        </select>
    </div>
    <div>
        <label for="sizeSelect">Font Size:</label>
        <input type="number" id="sizeSelect" min="8" max="72" value="16" onchange="changeSize()">
    </div>
</div>

<script>
    let openedFiles = {};

    function changeColor() {
        var color = document.getElementById("colorSelect").value;
        document.getElementById("noteText").style.color = color;
    }

    function changeFont() {
        var font = document.getElementById("fontSelect").value;
        document.getElementById("noteText").style.fontFamily = font;
    }

    function changeSize() {
        var size = document.getElementById("sizeSelect").value + "px";
        document.getElementById("noteText").style.fontSize = size;
    }

    function handleFileSelect(event) {
        const files = event.target.files;

        for (let i = 0; i < files.length; i++) {
            const file = files[i];
            const reader = new FileReader();

            reader.onload = function(e) {
                const fileContent = e.target.result;
                openedFiles[file.name] = fileContent;
                updateLastFilesList(file.name);
                if (i === files.length - 1) {
                    document.getElementById("noteText").value = fileContent;
                }
            };

            reader.readAsText(file);
        }
    }

    function saveNote() {
        const noteText = document.getElementById("noteText").value.trim();

        if (noteText === "") {
            document.getElementById("errorMessage").style.display = "block";
            return;
        }

        const blob = new Blob([noteText], { type: "text/plain;charset=utf-8" });
        saveAs(blob, "NOTEFILE.txt");
        document.getElementById("errorMessage").style.display = "none";
    }

    function updateLastFilesList(fileName) {
        const lastFilesList = document.getElementById("lastFilesList");
        const listItem = document.createElement("li");
        listItem.textContent = fileName;
        listItem.addEventListener("click", function() {
            document.getElementById("noteText").value = openedFiles[fileName];
        });
        lastFilesList.appendChild(listItem);

        if (lastFilesList.children.length > 10) {
            lastFilesList.removeChild(lastFilesList.children[0]);
        }
    }

    function clearData() {
        document.getElementById("noteText").value = "";
        document.getElementById("lastFilesList").innerHTML = "";
    }
</script>
</body>
</html>
