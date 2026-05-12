# Ex03 To-Do List using JavaScript
## Date:12.05.26
## Name: Vembarasi.A.R
## Reg no: 212224220120

## AIM
To create a To-do Application with all features using JavaScript.

## ALGORITHM
### STEP 1
Build the HTML structure (index.html).

### STEP 2
Style the App (style.css).

### STEP 3
Plan the features the To-Do App should have.

### STEP 4
Create a To-do application using Javascript.

### STEP 5
Add functionalities.

### STEP 6
Test the App.

### STEP 7
Open the HTML file in a browser to check layout and functionality.

### STEP 8
Fix styling issues and refine content placement.

### STEP 9
Deploy the website.

### STEP 10
Upload to GitHub Pages for free hosting.

## PROGRAM
```
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Attractive Todo App</title>

<style>
    *{
        margin:0;
        padding:0;
        box-sizing:border-box;
        font-family:Arial, sans-serif;
    }

    body{
        background: linear-gradient(135deg,#6a11cb,#2575fc);
        height:100vh;
        display:flex;
        justify-content:center;
        align-items:center;
    }

    .container{
        width:400px;
        background:white;
        padding:25px;
        border-radius:15px;
        box-shadow:0 5px 15px rgba(0,0,0,0.3);
    }

    h1{
        text-align:center;
        color:#2575fc;
        margin-bottom:20px;
    }

    .input-section{
        display:flex;
        gap:10px;
    }

    .input-section input{
        flex:1;
        padding:10px;
        border:2px solid #2575fc;
        border-radius:8px;
        outline:none;
    }

    .input-section button{
        padding:10px 15px;
        border:none;
        background:#2575fc;
        color:white;
        border-radius:8px;
        cursor:pointer;
        font-weight:bold;
    }

    .input-section button:hover{
        background:#6a11cb;
    }

    ul{
        list-style:none;
        margin-top:20px;
    }

    li{
        background:#f4f4f4;
        padding:12px;
        margin-bottom:10px;
        border-radius:8px;
        display:flex;
        justify-content:space-between;
        align-items:center;
    }

    li.completed span{
        text-decoration:line-through;
        color:gray;
    }

    .buttons button{
        margin-left:5px;
        border:none;
        padding:5px 8px;
        border-radius:5px;
        cursor:pointer;
        color:white;
    }

    .complete{
        background:green;
    }

    .delete{
        background:red;
    }

    footer{
        text-align:center;
        margin-top:20px;
        font-size:14px;
        color:#555;
    }
</style>
</head>

<body>

<div class="container">
    <h1>📝 To do Application</h1>

    <div class="input-section">
        <input type="text" id="taskInput" placeholder="Enter your task">
        <button onclick="addTask()">Add</button>
    </div>

    <ul id="taskList"></ul>

    <footer>
        <p><b>Name:</b> Vembarasi.A.R</p>
        <p><b>Register Number:</b> 212224220120</p>
    </footer>
</div>

<script>
    function addTask() {
        let taskInput = document.getElementById("taskInput");
        let taskText = taskInput.value.trim();

        if(taskText === ""){
            alert("Please enter a task");
            return;
        }

        let li = document.createElement("li");

        let span = document.createElement("span");
        span.innerText = taskText;

        let btnDiv = document.createElement("div");
        btnDiv.classList.add("buttons");

        // Complete Button
        let completeBtn = document.createElement("button");
        completeBtn.innerText = "✔";
        completeBtn.classList.add("complete");

        completeBtn.onclick = function(){
            li.classList.toggle("completed");
        };

        // Delete Button
        let deleteBtn = document.createElement("button");
        deleteBtn.innerText = "✖";
        deleteBtn.classList.add("delete");

        deleteBtn.onclick = function(){
            li.remove();
        };

        btnDiv.appendChild(completeBtn);
        btnDiv.appendChild(deleteBtn);

        li.appendChild(span);
        li.appendChild(btnDiv);

        document.getElementById("taskList").appendChild(li);

        taskInput.value = "";
    }
</script>

</body>
</html>
```

## OUTPUT
<img width="1918" height="1080" alt="image" src="https://github.com/user-attachments/assets/92a5bb4a-1fa1-49e3-ba47-01654580b6ce" />



## RESULT
The program for creating To-do list using JavaScript is executed successfully.
