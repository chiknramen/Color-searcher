# Color-searcher
A code made in html that can search for a color from typing in a specified color hex. 

<!DOCTYPE html>
<html>
<head>
    <title>Color Searcher</title>
    <style>
        body {
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            background-color: #f5f5f5;
        }
        .search-container {
            display: flex;
            flex-direction: column;
            align-items: center;
        }
        .search-input {
            width: 200px;
            padding: 10px;
            font-size: 18px;
            border: 1px solid #ddd;
            border-radius: 5px;
        }
        .color-display {
            width: 200px;
            height: 200px;
            border: 1px solid #ddd;
            border-radius: 5px;
            margin-top: 20px;
        }
    </style>
</head>
<body>
    <div class="search-container">
        <input id="search-input" class="search-input" type="text" placeholder="#000000">
        <div id="color-display" class="color-display"></div>
    </div>
    <script>
        const searchInput = document.getElementById('search-input');
        const colorDisplay = document.getElementById('color-display');

        searchInput.addEventListener('input', () => {
            const inputColor = searchInput.value;
            if (/^#[0-9A-F]{6}$/i.test(inputColor)) {
                colorDisplay.style.backgroundColor = inputColor;
            } else {
                colorDisplay.style.backgroundColor = '#ffffff';
            }
        });
    </script>
</body>
</html>
