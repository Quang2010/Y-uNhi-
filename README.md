<!DOCTYPE html>
<html lang="vi">
<head>
    <meta charset="UTF-8">
    <title>Gửi đến Nhi yêu dấu</title>
    <style>
        body {
            background: linear-gradient(to right, #ffdde1, #ee9ca7);
            font-family: 'Segoe UI', sans-serif;
            color: #4a1c40;
            text-align: center;
            padding: 50px;
            overflow: hidden;
        }

        h1 {
            font-size: 3em;
            margin-bottom: 0.5em;
        }

        .heart {
            font-size: 5em;
            color: red;
            animation: beat 1s infinite;
        }

        @keyframes beat {
            0%, 100% {
                transform: scale(1);
            }
            50% {
                transform: scale(1.2);
            }
        }

        .message {
            font-size: 1.2em;
            text-align: left;
            max-width: 700px;
            margin: 0 auto;
            background-color: #fff0f5;
            padding: 30px;
            border-radius: 15px;
            box-shadow: 0 0 15px rgba(0,0,0,0.1);
            line-height: 1.6em;
        }

        /* Trái tim rơi */
        .falling {
            position: fixed;
            top: -10px;
            animation: fall linear infinite;
            opacity: 0.7;
            z-index: 9999;
        }

        @keyframes fall {
            to {
                transform: translateY(100vh);
            }
        }
    </style>
</head>
<body>

    <!-- Nhạc nền -->
    <audio autoplay loop>
        <source src="https://cdn.pixabay.com/download/audio/2022/03/23/audio_3cfd0f90f6.mp3?filename=love-110344.mp3" type="audio/mpeg">
    </audio>

    <div class="heart">❤️</div>
    <h1>Gửi đến Nhi của anh</h1>

    <div class="message">
        <p>Anh xin lỗi vì tất cả những điều mà anh đã làm với em, khiến cho tâm trạng và cảm xúc của em không tốt. Anh biết rằng dù có nói thế nào đi chăng nữa cũng không thể hoàn toàn làm dịu cơn giận của em.</p>

        <p>Anh sợ lắm… sợ em buồn. Dù là anh có nói như thế mà bản thân anh lại làm hoàn toàn ngược lại, chỉ khiến em không tin anh, thất vọng về anh. Không sao cả ạ, em đã cho anh thấy tầm sự nghiêm trọng của vấn đề mà anh đã mắc phải.</p>

        <p>Anh yêu em chưa được hoàn hảo với những suy nghĩ khác nhau. Anh đang cố nhìn lại bản thân mình, nhìn lại cách anh thất hứa hết lần này đến lần khác. Anh không chắc… Anh chỉ cảm thấy rằng đã có những lúc em không đặt anh vào tương lai của em. Anh chỉ thắc mắc rằng liệu em đã từng nghĩ đến anh và nghĩ rằng sẽ yêu anh lâu dài, thành chồng của em?</p>

        <p>Anh biết là điều đó rất xa vời… nhưng anh hy vọng điều đó rất nhiều.</p>

        <p>Anh mong rằng sẽ không còn những xung đột khiến cả anh và em mệt mỏi như thế này nữa. Anh mong mình có thể bình tĩnh nhìn lại vấn đề rồi nói chuyện với nhau một cách nhẹ nhàng.</p>

        <p>Trang web nhỏ này là để nói rằng... Anh yêu em, rất nhiều. Thực sự rất rất nhiều. 💖</p>
    </div>

    <!-- Trái tim rơi -->
    <script>
        function createHeart() {
            const heart = document.createElement("div");
            heart.innerHTML = "❤️";
            heart.classList.add("falling");
            heart.style.left = Math.random() * 100 + "vw";
            heart.style.animationDuration = (3 + Math.random() * 2) + "s";
            heart.style.fontSize = (16 + Math.random() * 24) + "px";
            document.body.appendChild(heart);
            setTimeout(() => {
                heart.remove();
            }, 5000);
        }
        setInterval(createHeart, 400);
    </script>

</body>
</html>
