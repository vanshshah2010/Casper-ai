<!DOCTYPE html>
<html>
<head>
<title>Casper AI</title>
<style>
body {
    background: #00ff88;
    font-family: Arial;
    text-align: center;
    padding-top: 50px;
}

h1 {
    font-size: 40px;
    color: black;
}

#chatbox {
    width: 80%;
    height: 300px;
    border: 2px solid black;
    background: white;
    margin: auto;
    padding: 10px;
    overflow-y: scroll;
}

input {
    width: 60%;
    padding: 10px;
    font-size: 16px;
}

button {
    padding: 10px 20px;
    font-size: 16px;
    background: black;
    color: white;
    border: none;
}
</style>
</head>

<body>

<h1>Casper.ai</h1>

<div id="chatbox"></div>
<br>

<input id="userInput" placeholder="Ask Casper..." />
<button onclick="sendMessage()">Send</button>

<script>
function sendMessage() {
    let input = document.getElementById("userInput").value;
    let chatbox = document.getElementById("chatbox");

    if(input === "") return;

    // Show user message
    chatbox.innerHTML += "<p><b>You:</b> " + input + "</p>";

    // Basic AI replies
    let reply = "I am Casper AI. I am still learning.";

    if(input.toLowerCase().includes("hello")) reply = "Hello! How can I help you?";
    if(input.toLowerCase().includes("your name")) reply = "My name is Casper AI.";
    if(input.toLowerCase().includes("who made you")) reply = "Vansh created me 😎";

    chatbox.innerHTML += "<p><b>Casper:</b> " + reply + "</p>";
    document.getElementById("userInput").value = "";
}
</script>

</body>
</html>
