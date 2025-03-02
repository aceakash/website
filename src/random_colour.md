---
title: Random colour
layout: base.njk
---
<h1 id="message" style="text-align: center; font-size: 4em">Hello there!</h1>

<script>
function getRandomColor() {
  const letters = '0123456789ABCDEF';
  let color = '#';
  for (let i = 0; i < 6; i++) {
    color += letters[Math.floor(Math.random() * 16)];
  }
  return color;
}

function changeColors() {
    document.getElementById('message').style.color = getRandomColor();
    document.body.style.backgroundColor = getRandomColor();
}

window.setInterval(changeColors, 3000)

</script>