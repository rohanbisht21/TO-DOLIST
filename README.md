the code -
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>TO_DO</title>

    <style>
body{
    background-color: beige;
}
        .done{

            text-decoration: line-through;
        }
   
        
     
       
    </style>
</head>
<body>
    
<div>

    <input type="text" class="write" >
<ul class="todo-list"
style="list-style-type: none;">


</ul>


</div>



    <script>

let write =document.querySelector(".write");
let toDoList =document.querySelector(".todo-list");

write.addEventListener("keyup",function(e){
    
if(e.key == "Enter"){
    addTodo(this.value);
    this.value='';
}
})




function addTodo(val){
    var list = document.createElement("li");
    list.innerHTML= `${val}`;
    toDoList.appendChild(list)
    console.log(val)



list.addEventListener("click",function (){
    this.classList.toggle('done');
})
}





  </script>
</body>
</html>
