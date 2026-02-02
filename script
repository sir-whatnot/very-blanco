const output = document.getElementById('output');
const randomBtn = document.getElementById('randomBtn');
const surpriseBtn = document.getElementById('surpriseBtn');

const colors = ['#ff6b6b','#ffd93d','#6be3ff','#7c3aed','#34d399','#ff7bd3'];
const emojis = ['😄','🤪','🚀','🎉','🧩','🐙','🌈','🪄','🕺','🧨'];
const messages = [
  "You found a secret massage chair!",
  "Have a cookie full of mold!",
  "Random fact: I am you.",
  "Tip: Leave.",
  "Keep exploring — AAAAAAAAAAAAA"
];

function randomFrom(arr){ return arr[Math.floor(Math.random()*arr.length)]; }

function doRandomStuff(){
  // pick a random action
  const action = Math.floor(Math.random()*4);

  switch(action){
    case 0: // change background color
      const color = randomFrom(colors);
      document.body.style.background = color;
      output.innerHTML = `<div>Background changed to <strong>${color}</strong></div>`;
      break;

    case 1: // show big emoji
      const e = randomFrom(emojis);
      output.innerHTML = `<div class="big-emoji">${e}</div>`;
      break;

    case 2: // show message
      output.textContent = randomFrom(messages);
      break;

    case 3: // flash effect + message
      output.textContent = "Surprise flash!";
      output.style.transition = 'transform .2s ease';
      output.style.transform = 'scale(1.05)';
      setTimeout(()=> output.style.transform = 'scale(1)', 180);
      break;
  }
}

function surprise(){
  // A deterministic fun combo
  const e = randomFrom(emojis);
  const m = randomFrom(messages);
  const c = randomFrom(colors);
  document.body.style.background = `linear-gradient(90deg, ${c}, #071129)`;
  output.innerHTML = `<div class="big-emoji">${e}</div><div style="margin-top:.6rem">${m}</div>`;
}

randomBtn.addEventListener('click', doRandomStuff);
surpriseBtn.addEventListener('click', surprise);

// Small keyboard shortcut: press R to do random
document.addEventListener('keydown', (ev)=>{
  if(ev.key.toLowerCase() === 'r') doRandomStuff();
});
