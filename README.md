<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="stylesheet" href="style.css">
    <style>
        *{
    margin: 0;
    padding:0;
    box-sizing: border-box;
}
body{
    width: 100%;
    height: 100vh;
    display: flex;
    align-items: center;
    justify-content: center;
    background-image: linear-gradient(135deg, #a5fafa 10%, #32c2bb 100%);
    animation: backGround 3s ease-in-out infinite alternate;
}

@keyframes backGround{
    0%{
        box-shadow: inset 100px 300px 20em 2em #50acd6;
    }

    60%{
        box-shadow: inset 100px -300px 20em 2em #13a795;
    }
 
    100%{
        box-shadow: inset -100px 300px 20em 2em #5999b3;
    }
}


.rod{
    width: 20rem;
    height: 20rem;
    border-top:1.5rem solid #032520;
    border-top-left-radius:10px;
    border-top-right-radius:10px;
    display: flex;
    gap: 2.9rem;
    justify-content: center;
    
}

.rod div{
    width: .2rem;
    height: 11rem;
    top: -1px;
    transform-origin: top right;
    background:#032520;
    box-shadow: 1.9px 1px 30px 2px rgb(4, 53, 68);
    position: relative;
}
.rod div::after{
    content: " ";
    width:3rem;
    aspect-ratio: 1;
    bottom: 0;
    left: -1.5rem;
    border-radius: 50%;
    position: absolute;
    background: #011f0e;
    box-shadow: 1.9px 10px 20px 2px black;
}



.rod div:first-child{
    animation: left-ball 1s ease-in infinite;
}

@keyframes left-ball{
    0%{
        rotate: -1.5deg;
    }
    25%{
        rotate: 35deg;
    }
    50%{
        rotate: 0deg;
    }
    100%{
        rotate: -1.5deg;
    }
}



.rod div:not(div:first-child,div:last-child,div:nth-child(3)){
    animation: center-ball 1s ease-in infinite reverse;
}

@keyframes center-ball{
    0%{
        rotate: 0deg;
    }
    50%{
        rotate:-1.5deg;
    }
    70%{
        rotate: 0deg;
    }
    100%{
        rotate: 1.5deg;
    }
}



.rod div:last-child{
    animation: right-ball 1s ease-in 0.5s infinite;   
}

@keyframes right-ball{
    0%{
        rotate: 0deg;
    }
    25%{
        rotate: -35deg;
    }
    50%{
        rotate: 0deg;
    }
    100%{
        rotate: 0deg;
    }
}
    </style>
    <title>Pendulum</title>
</head>
<body>
<div class="rod">
    <div></div>
    <div></div>
    <div></div>
    <div></div>
    <div></div>
</div> 
</body>
</html>
