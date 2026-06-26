const taskInput = document.getElementById("task-input");
const addBtn = document.getElementById("add-btn");
const taskList = document.getElementById("task-list");

document.addEventListener("DOMContentLoaded", loadTasks);

addBtn.addEventListener("click", () => {
    const taskText = taskInput.value.trim();

    if (taskText === "") {
        alert("Please enter a task first!");
        return;
    }

    createTaskElement(taskText);
    saveTaskToLocal(taskText); // 
    taskInput.value = "";
});

function createTaskElement(taskText) {
    const li = document.createElement("li");
    li.innerText = taskText;

    const deleteBtn = document.createElement("button");
    deleteBtn.innerText = "Delete";
    deleteBtn.classList.add("delete-btn");

    deleteBtn.addEventListener("click", () => {
        li.remove();
        removeTaskFromLocal(taskText); 
    });

    li.appendChild(deleteBtn);
    taskList.appendChild(li);
}


function saveTaskToLocal(task) {
    let tasks = localStorage.getItem("tasks") ? JSON.parse(localStorage.getItem("tasks")) : [];
    tasks.push(task);
    localStorage.setItem("tasks", JSON.stringify(tasks));
}

function loadTasks() {
    let tasks = localStorage.getItem("tasks") ? JSON.parse(localStorage.getItem("tasks")) : [];
    tasks.forEach(task => createTaskElement(task));
}
function removeTaskFromLocal(taskToRemove) {
    let tasks = JSON.parse(localStorage.getItem("tasks"));
    tasks = tasks.filter(task => task !== taskToRemove);
    localStorage.setItem("tasks", JSON.stringify(tasks));
}
