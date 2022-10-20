# san_minetest_cabeca_3d_html
cabeca 3d san minetest 
<!--code by joseanastacio (josegamestest)-->
<html>
<head>
    <meta charset="UTF-8">
    <title>San</title>
    <style>
          @keyframes turn {
          from { transform: rotate3d(0,0,0,); }
          to { transform: rotate3d(.3, 1, 0, 360deg); }
          }

          .container {
            width: 16px;
            height: 16px;
            perspective: 500px;
            margin: 10px;
          }

          .cube {
            position: relative;
            width: 16px;
            height: 16px;
            transform-style: preserve-3d;
            animation: turn 5s linear infinite;
          }

          .face {
            width: 20px;
            height: 20px;
            background: skyblue;
            border: 0px solid black;
            position: absolute;
            opacity: 1;
            display: flex;
            align-items: center;
            justify-content: center;
            font-family: Arial, sans-serif;
            font-size: 2rem;
            transition: transform 500ms;
          }
              
          .front {transform: translateZ(10px);}
          .back {transform: translateZ(-10px) rotateY(180deg);}
          .left {transform: translateX(-10px) rotateY(-90deg);}
          .right {transform: translateX(10px) rotateY(90deg);}
          .top {transform: translateY(-10px) rotateX(90deg);}
          .bottom {transform: translateY(10px) rotateX(-90deg);}

          @media (prefers-reduced-motion: reduce) {
            .cube {animation: none;transform: rotate3d(1, 1, 0, 45deg);}
          }
          img{ width: 100%;}

      </style>
</head>
<body>
  <div class="cube">
    <div class="face top">    <img src="top.png?raw=true"/></div>
    <div class="face bottom"> <img src="botton.png?raw=true"/></div>
    <div class="face left">   <img src="left.png?raw=true"/></div>
    <div class="face right">  <img src="right.png?raw=true"/></div>
    <div class="face front">  <img src="front.png?raw=true"/></div>
    <div class="face back">   <img src="back.png?raw=true"/></div>
  </div>
</body>
</html>
