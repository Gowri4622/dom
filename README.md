### EX NO: 10

# <p align="center">DOM Manipulation using js</P>

## Aim:
To implement the Dom-Manipulation for Color-picker

## Algorithm:

Step 1: Import the required packages

Step 2: Create the assets folder in that create css and js file folder

Step 3: By using some functions “less and greater selector function”

Step 4: Callback the function

Step 5: Run the program.
  


## Program

### index.html
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="stylesheet" href="assets/css/style.css">
    <title>Document</title>
</head>
<body>
    <div class="picker">
    <input id="picker1" type="color">
    <input id="picker2" type="color">
    <input id="picker3" type="color">
    <button id="less">&lt</button>
    <button id="great">&gt</button>
</div>
    <script src="assets/js/script.js"></script>
</body>
</html>


```

### script.js
```js
const cp1 = document.getElementById('picker1')
const cp2 = document.getElementById('picker2')
const cp3 = document.getElementById('picker3')
const less =  document.getElementById('less')
const great =  document.getElementById('great')
var pos = 0

var colorsSet = [
    {
        selector:"cp1",
        selectedColor:"#ffffff"
    },
    {   selector:"cp2",
        selectedColor:"#ffffff"
    },
    {   selector:"cp3",
        selectedColor:"#ffffff"
    }


]
// console.log(cp1);
cp2.style.display = 'none';
cp3.style.display = 'none';

less.addEventListener("click",()=>{
     if(pos===0)
         pos = 2
    else if(pos==1 || pos==2)
        pos = pos-1
    const lessSelectorFunc = (pos)=>{
        const currSelector = colorsSet[pos].selector;
        const currColor = colorsSet[pos].selectedColor;
        switch(currSelector){
            case 'cp1':
                cp1.style.display = 'block'
                cp2.style.display = 'none'
                cp3.style.display = 'none'
                document.body.style.backgroundColor = currColor;
                break;
            case 'cp2':
                cp2.style.display = 'block'
                cp1.style.display = 'none'
                cp3.style.display = 'none'
                document.body.style.backgroundColor = currColor;
                break;
            case 'cp3':
                cp3.style.display = 'block'
                cp1.style.display = 'none'
                cp2.style.display = 'none'
                document.body.style.backgroundColor = currColor;
                break;
        }
        // currSelector.style.display='block';
        
        

    }
    lessSelectorFunc(pos);
    
})

great.addEventListener("click",()=>{
    if(pos===2)
        pos = 0
    else if(pos===0 || pos===1)
        pos = pos+1        
        const greatSelectorFunc = (pos)=>{
            const currSelector = colorsSet[pos].selector;
            const currColor = colorsSet[pos].selectedColor;
            switch(currSelector){
                case 'cp1':
                    cp1.style.display = 'block'
                    cp2.style.display = 'none'
                    cp3.style.display = 'none'
                    document.body.style.backgroundColor = currColor;
                    break;
                case 'cp2':
                    cp2.style.display = 'block'
                    cp1.style.display = 'none'
                    cp3.style.display = 'none'
                    document.body.style.backgroundColor = currColor;
                    break;
                case 'cp3':
                    cp3.style.display = 'block'
                    cp1.style.display = 'none'
                    cp2.style.display = 'none'
                    document.body.style.backgroundColor = currColor;
                    break;
            }
}
greatSelectorFunc(pos);

})

console.log(colorsSet);


cp1.addEventListener("change",(e)=>{
     const color = e.target.value
     //colorsSet.cp1 = color;
     if(colorsSet[0]){
        colorsSet[0].selectedColor = color;
     }
     console.log(colorsSet);
     document.body.style.backgroundColor=color;

})
cp2.addEventListener("change",(e)=>{
    const color = e.target.value
    if(colorsSet[1]){
        colorsSet[1].selectedColor = color;
     }
   
    console.log(colorsSet);
    document.body.style.backgroundColor=color;
})
cp3.addEventListener("change",(e)=>{
    const color = e.target.value
    colorsSet.cp3 = color;
    if(colorsSet[2]){
        colorsSet[2].selectedColor = color;
     }
    console.log(colorsSet);
    document.body.style.backgroundColor=color;
})
```

## Output

![Screenshot 2023-06-04 182312](https://github.com/Gowri4622/dom/assets/75235455/e2c7537e-e4ae-4384-aff2-8fb0459b616a)

![Screenshot 2023-06-04 182808](https://github.com/Gowri4622/dom/assets/75235455/7d352b69-ce0f-48c6-b6dd-c2c0932b8745)

![Screenshot 2023-06-04 182345](https://github.com/Gowri4622/dom/assets/75235455/f50ec7cf-e1fb-46f7-a09b-e3e8f440a781)


## Result
Hence the implementation of color -picker in dom-manipulation
