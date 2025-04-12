<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Calculator</title>
    <style>
        *{
            margin:0;
            padding:0;
            text-align: center;
        }
        body{
            background-color:#203a43;
        }
        .claculator{
            width:360px;
            height:460px;
            background-color:black;
            padding:30px;
            margin: auto;
            padding-bottom:70px;
            border-radius:20px;
            margin-top:75px;
            box-shadow:10px 10px 20px rgba(255,255,255,0.5);
        }
        button{
            border-radius:50%;
            background-color:rgba(128, 128, 128,0.8);
            color:white;
            margin:10px 12px;
            border:1px solid white;
            height:58px;
            width:58px;
            font-size:20px;
            cursor: pointer;
        }
        input{
            width:98%;
            height:60px;
            padding-left:10px;
            text-align: left;
            border-radius:10px;
            margin-bottom:30px;
            font-size:25px;
            font-weight:600;
            border:none;

        }
    
    </style>
</head>
<body>
    <div class="claculator">
            <input type="text" class="input" value="0">
            <button class="btn" style="background-color: orange;">AC</button>
            <button class="btn" style="background-color: orange;">DEL</button>
            <button class="btn" style="background-color: orange;">%</button>
            <button class="btn" style="background-color: orange;">/</button>
            <button class="btn">7</button>
            <button class="btn">8</button>
            <button class="btn">9</button>
            <button class="btn" style="background-color: orange;">*</button>
            <button class="btn">4</button>
            <button class="btn">5</button>
            <button class="btn">6</button>
            <button class="btn" style="background-color: orange;">-</button>
            <button class="btn">1</button>
            <button class="btn">2</button>
            <button class="btn">3</button>
            <button class="btn" style="background-color: orange;">+</button>
            <button class="btn" style="background-color: orange;">00</button>
            <button class="btn">0</button>
            <button class="btn" style="background-color: orange;">.</button>
            <button class="btn" style="background-color: orange;">=</button>


    </div>
    <script>
        let input=document.querySelector("input");
        let buttons=document.querySelectorAll("button");
        let arr=Array.from(buttons);
        arr.forEach(button =>{
            button.addEventListener("click",(event)=>{
                if(event.target.innerHTML=="="){
                    input.value=eval(input.value);
                }
              else if(event.target.innerHTML=="AC"){
                    input.value="";
                }
              else if(event.target.innerHTML == "DEL"){
                   input.value=input.value.substring(0,input.value.length-1);
             }
                else{
                input.value=input.value+event.target.innerHTML;}

            });
        });
       
    </script>
</body>
</html>
