<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>About Me</title>
    <style>
        body {
            margin: 0;
            padding: 0;
            font-family: Arial, sans-serif;
            color: white;
            text-align: center;
            overflow: hidden;
        }
        .background {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            overflow: hidden;
            z-index: -1;
        }
        .background video {
            width: 100%;
            height: 100%;
            object-fit: cover;
            position: absolute;
            top: 0;
            left: 0;
        }
        .overlay {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(0, 0, 0, 0.6);
            backdrop-filter: blur(5px);
            z-index: 0;
        }
        .content {
            position: absolute;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            width: 350px;
            padding: 20px;
            background: rgba(0, 0, 0, 0.7);
            border-radius: 10px;
            box-shadow: 0 4px 10px rgba(0, 0, 0, 0.5);
        }
        .scrollable {
            max-height: 200px;
            overflow-y: auto;
            scrollbar-width: thin;
            scrollbar-color: #888 #333;
        }
        .scrollable::-webkit-scrollbar {
            width: 8px;
        }
        .scrollable::-webkit-scrollbar-thumb {
            background: #888;
            border-radius: 4px;
        }
        .profile-img {
            width: 100px;
            height: 100px;
            border-radius: 50%;
            margin-bottom: 10px;
        }
        .username {
            font-size: 24px;
            font-weight: bold;
            background-image: linear-gradient(90deg, red, orange, yellow, green, blue, indigo, violet);
            background-clip: text;
            -webkit-background-clip: text;
            color: transparent;
            animation: rainbow 3s linear infinite;
        }
        @keyframes rainbow {
            0% { background-position: 0%; }
            100% { background-position: 100%; }
        }
        .discord-link {
            color: #7289da;
            text-decoration: none;
            font-size: 14px;
        }
        .discord-link:hover {
            text-decoration: underline;
        }
    </style>
</head>
<body>
    <div class="background">
        <video autoplay loop muted>
            <source src="https://res.cloudinary.com/djkug0a3i/video/upload/v1740638266/y2mate.com_-_puppy_Dangrangto_Wrong_Times_ft_FOWLEX_Snowz_OFFICIAL_LYRICS_VIDEO_dfgsaz.mp3" type="video/mp3">
        </video>
    </div>
    <audio id="background-music" autoplay loop>
        <source src="https://res.cloudinary.com/djkug0a3i/video/upload/v1740638266/y2mate.com_-_puppy_Dangrangto_Wrong_Times_ft_FOWLEX_Snowz_OFFICIAL_LYRICS_VIDEO_dfgsaz.mp3" type="audio/mpeg">
    </audio>
    <script>
        document.addEventListener('click', function() {
            const music = document.getElementById('background-music');
            if (music.paused) {
                music.play().catch(error => console.log("Autoplay prevented:", error));
            }
        });
    </script>
    <div class="overlay"></div>
    <div class="content">
        <img src="https://res.cloudinary.com/djkug0a3i/image/upload/v1740637031/3fb7b2c09846169939f571a56b088d23_fh0r6t.jpg" alt="Profile Picture" class="profile-img">
        <div class="username">Shinichi</div>
        <p>📍 Location:Quang Binh Province, VietNam</p>
        <p>🏫 Schools: Cisvn <a href="Truong THPT Hoang Hoa Tham" target="_blank">Truong THPT Hoang Hoa Tham</a></p>
        <p>💬 Name: Nguyen Phuc Sinh [Shinichi]</p>
        <p>🎵 Favorite Music: Dung Lam Trai Tim Anh Dau (Son Tung MTP)</p>
        <p>👑 Favorite Sports: Play Football, Volleyball</p>
        <p>🎮 Favorite Game: Roblox</p>
        <p>🍕 Favorite Food: Spicy Noodles, Ramen</p>
        <p> 🖥 Skill: Skider: Java, Python, HTML, Lua</p>
        <a href="https://discord.gg/wWX6EAYzrA" target="_blank" class="discord-link">Join my Discord Server</a>
    </div>
</body>
</html>
