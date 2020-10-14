<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>food.html</title>
    <script src="https://ajax.googleapis.com/ajax/libs/jquery/3.5.1/jquery.min.js"></script>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        #banner {
            position: relative;
            width: 700px; height: 400px;
            overflow: hidden;
        }

        #banner > .main {
            width: 700px; height: 400px;
            position: absolute;
            background: 
                url(./imageedit.gif);
            animation-iteration-count: infinite;
        }

        .title {
            position: absolute;
            right: 70px; top: 179px;
        
        }
        .btn {
            position: absolute;
            right: 300px; top: 250px;
            width: 100px; height: 40px;
            border-radius: 10px;
            font-size: large;
        }
        .btn:hover {
            background: black;
            color: white;
        }
        .fadeIn {
            animation-name: fadein;
            animation-duration: 1s;
            animation-timing-function: ease-in-out;
        }
        @keyframes fadein {
            0% {opacity: 0;}
            100% {opacity: 1;}
        }



    </style>
</head>
<body>
    <div id="banner">
        <div class="main"></div>
        <div class="fadeIn">
        <img src="./오늘 점심엔 [              ] 가자_.png" alt="" class="title">
        <button class="btn">Click!</button>
        </div>
    </div>

    <script>
        var main = document.querySelector('#banner > .main');
        var btn = document.querySelector('#banner .btn');

        btn.addEventListener('click', yogiyo);

        var r = Math.random() * 19 + 1;
        var int_r = Math.floor(r);

        function yogiyo() {
            main.style.background = "url(./" + int_r + ".jpg)";
            $('#banner .btn').remove();
        }
    </script>
</body>
</html>
