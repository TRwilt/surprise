#surprise
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Happy Birthday Julia!</title>
</head>
<style>
    body {
    margin: 0;
    padding: 0;
    font-family: Arial, sans-serif;
    display: flex;
    justify-content: center;
    align-items: center;
    height: 100vh;
    background: linear-gradient(to bottom, #ff9a9e, #fad0c4);
    color: #fff;
    overflow: hidden;
}

.container {
    text-align: center;
    z-index: 10;
    position: relative;
    background: rgba(0, 0, 0, 0.5);
    padding: 20px;
    border-radius: 15px;
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
}

h1 {
    font-size: 2.5rem;
    opacity: 0;
    transition: opacity 2s ease-in-out;
}

.note {
    margin-top: 15px;
    font-size: 1.2rem;
    color: #ffedd5;
}

button {
    background-color: #ff6f61;
    color: white;
    border: none;
    padding: 10px 20px;
    font-size: 1rem;
    border-radius: 5px;
    cursor: pointer;
    transition: background-color 0.3s ease;
    margin-top: 20px;
}

button:hover {
    background-color: #ff3d2e;
}

#heart {
    position: absolute;
    top: 50%;
    left: 50%;
    width: 0;
    height: 0;
    background-color: transparent;
    transform: translate(-50%, -50%);
    opacity: 0;
    transition: all 2s ease-in-out;
}

#heart::before,
#heart::after {
    content: "";
    position: absolute;
    width: 200px;
    height: 200px;
    background-color: red;
    border-radius: 50%;
    transform: rotate(45deg);
    top: -100px;
    left: 0;
}

#heart::after {
    left: 100px;
    top: 0;
}

.hidden {
    display: none;
}

.visible {
    display: block;
    width: 400px;
    height: 400px;
    opacity: 1;
}



</style>
<body>
    <div class="container">
        <h1 id="message"></h1>
        <button id="revealButton">Click to Reveal</button>
        <div id="heart" class="hidden"></div>
        <p class="note">Happy Birthday, Julia! ^_^ (: I am very sorry for my small mistakes:)</p>
    </div>
    <script>
        document.getElementById("revealButton").addEventListener("click", () => {
   
  const messageElement = document.getElementById("message");
  const message =`Dear Julia,
   Every moment with you is magical.
   You light up my world, today and always.
   Happy Birthday, my love! ❤️ `;
  messageElement.textContent = message;
  messageElement.style.opacity = 1;

    
  const heartElement = document.getElementById("heart");
  heartElement.classList.remove("hidden");
  heartElement.classList.add("visible");

    
  const button = document.getElementById("revealButton");
  button.disabled = true;
  button.textContent = "Message Revealed!";
});
</script>
</body>
</html>
