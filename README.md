<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Hello Nishika!</title>
    <style>
        /* Global styling */
        body {
            margin: 0;
            padding: 0;
            font-family: Arial, sans-serif;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            color: #333;
            text-align: center;
            background: linear-gradient(120deg, #ff9a9e, #fad0c4, #fad0c4, #ff9a9e);
            background-size: 400% 400%;
            animation: backgroundAnimation 8s ease infinite;
            overflow: hidden;
        }
        
        /* Background animation */
        @keyframes backgroundAnimation {
            0% { background-position: 0% 50%; }
            50% { background-position: 100% 50%; }
            100% { background-position: 0% 50%; }
        }
        
        /* Container for all pages */
        .container {
            width: 80%;
            max-width: 600px;
            background: rgba(255, 255, 255, 0.9);
            padding: 20px;
            border-radius: 15px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.3);
            position: relative;
            display: none;
            animation: fadeIn 1.5s ease;
        }

        /* Fade-in animation */
        @keyframes fadeIn {
            from { opacity: 0; }
            to { opacity: 1; }
        }

        /* Visible class */
        .active {
            display: block;
        }

        /* Button styling */
        .nav-button {
            margin-top: 20px;
            padding: 10px 20px;
            background-color: #ff7f50;
            color: #fff;
            border: none;
            border-radius: 5px;
            cursor: pointer;
            font-size: 1rem;
            transition: transform 0.2s;
        }
        
        .nav-button:hover {
            transform: scale(1.1);
        }

        /* Monkey image styling */
        .monkey-image {
            width: 100px;
            height: auto;
            margin-bottom: 20px;
            animation: bounce 2s infinite;
        }

        /* Text animations */
        h1, p {
            margin: 0;
            padding: 0;
        }

        h1 {
            font-size: 2.5rem;
            color: #ff4500;
            animation: bounceIn 1.5s ease;
        }

        p {
            font-size: 1.2rem;
            color: #333;
            animation: slideUp 1.5s ease;
        }

        @keyframes bounce {
            0%, 100% { transform: translateY(0); }
            50% { transform: translateY(-10px); }
        }

        @keyframes slideUp {
            from { transform: translateY(20px); opacity: 0; }
            to { transform: translateY(0); opacity: 1; }
        }

        /* Page transition animation */
        @keyframes bounceIn {
            0% { transform: scale(0.5); opacity: 0; }
            50% { transform: scale(1.1); opacity: 1; }
            100% { transform: scale(1); }
        }
    </style>
</head>
<body>

    <!-- Page 1 - Main Greeting -->
    <div id="page1" class="container active">
        <img src="https://via.placeholder.com/100.png?text=Monkey" alt="Monkey" class="monkey-image">
        <h1>👋 Hello, Nishika!</h1>
        <p>Wishing you an amazing day filled with joy and smiles! 🌈✨</p>
        <button class="nav-button" onclick="showPage('page2')">Next</button>
    </div>

    <!-- Page 2 - Shayari 1 -->
    <div id="page2" class="container">
        <img src="https://via.placeholder.com/100.png?text=Monkey" alt="Monkey" class="monkey-image">
        <h1>Special Shayari 1</h1>
        <p>🌸 "Dosti woh nahi jo gam mein saath ho,<br>
           Dosti woh hai jo har pal mein saath ho." 🌸</p>
        <button class="nav-button" onclick="showPage('page3')">Next</button>
    </div>

    <!-- Page 3 - Shayari 2 -->
    <div id="page3" class="container">
        <img src="https://via.placeholder.com/100.png?text=Monkey" alt="Monkey" class="monkey-image">
        <h1>Special Shayari 2</h1>
        <p>🌟 "Zindagi mein sath chalne wala koi na mile,<br>
           Toh apne aap se dosti nibha lena." 🌟</p>
        <button class="nav-button" onclick="showPage('page4')">Next</button>
    </div>

    <!-- Page 4 - Shayari 3 -->
    <div id="page4" class="container">
        <img src="https://via.placeholder.com/100.png?text=Monkey" alt="Monkey" class="monkey-image">
        <h1>Special Shayari 3</h1>
        <p>🌼 "Dosti ki gehraiyon ko samajhna aasaan nahi,<br>
           Ye woh rishta hai jo bas itna keh sakta hai, 'Mein hoon na!' 🌼</p>
        <button class="nav-button" onclick="showPage('page1')">Back to Start</button>
    </div>

    <script>
        // JavaScript function to show the selected page
        function showPage(pageId) {
            // Hide all pages
            document.querySelectorAll('.container').forEach(page => {
                page.classList.remove('active');
            });
            // Show the selected page
            document.getElementById(pageId).classList.add('active');
        }
    </script>

</body>
</html>
