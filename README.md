html
<!DOCTYPE html>
<html>
<head>
<title>Meu Site</title>
<style>
body {
font-family: Arial, sans-serif;
text-align: center;
padding: 10%;
animation: shake 0.82s cubic-bezier(.36,.07,.19,.97) both;
transform: translate3d(0, 0, 0);
backface-visibility: hidden;
perspective: 1000px;
display: flex;
flex-direction: column;
justify-content: center;
align-items: center;
height: 100vh;
}
#noBtn {
animation: none;
}
#noBtn.active {
animation: shake 0.82s cubic-bezier(.36,.07,.19,.97) both infinite;
}
@keyframes shake {
10%, 90% {
transform: translate3d(-1px, 0, 0);
}
20%, 80% {
transform: translate3d(2px, 0, 0);
}
30%, 50%, 70% {
transform: translate3d(-4px, 0, 0);
}
40%, 60% {
transform: translate3d(4px, 0, 0);
}
}
button {
margin: 2em;
padding: 1em 2em;
font-size: 1em;
}
</style>
</head>
<body>
<h1 id="text">Eu te amo Malu, você me ama?</h1>
<button type="button" id="yesBtn" onclick="yesResponse()">Sim</button>
<button type="button" id="noBtn" onmouseover="noResponse()">Não</button>
<script>
function yesResponse() {
document.getElementById('text').textContent = 'Te Jaime ❤️';
document.getElementById('yesBtn').style.display = 'none';
document.getElementById('noBtn').style.display = 'none';
}

function noResponse() {
document.getElementById('noBtn').classList.add('active');
}
</script>
</body>
</html>
