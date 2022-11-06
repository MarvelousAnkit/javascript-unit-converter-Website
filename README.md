# javascript-unit-converter-Website
Source Code 
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Unit Converter</title>
    <style>
        * {
            margin: 0;
            padding: 0;
        }

        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }

        .heading1 {
            text-align: center;
            margin-top: 40px;
        }

        #container {
            margin: 15px auto 0px auto;
            width: 90%;
            text-align: center;
            background-color: aquamarine;
            border-radius: 10px;
            padding: 20px;
        }

        .input-div{display: inline-block;}
        .heading2{display: inline-block;}
    </style>
</head>

<body>
    <h1 class="heading1"> Unit Converter </h1>
    <div id="container">
        <div class="input-div">
            <label for="feet">Feet</label>
            <input type="number" name="no-backend-use" id="feet" value="0" class="input">
        </div>

        <h1 class="heading2" >=</h1>
        
        <div class="input-div">
            <label for="feet">Inches</label>
            <input type="number" name="no-backend-use" id="inch" value="0" class="input">
        </div>
    </div>
<script>
    let feet = document.getElementById("feet");
    let inch = document.getElementById("inch");

    feet.addEventListener('input' , function() {
         let f = this.value;
         let i = f*12
         inch.value=i
         
           
         
    })

    inch.addEventListener('input' , function(){
        let a = this.value
        let b = a/12
        
        if (!Number.isInteger(b)) {
            b = b.toFixed(2);
            
        }
        feet.value = b
            
    })
</script>
</body>

</html>
