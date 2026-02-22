let score = 0;
// Note: Sound might not play on GitHub until the user interacts with the page
const munchSound = new Audio('https://assets.mixkit.co/active_storage/sfx/2301/2301-preview.mp3');

function catchFly() {
  const frog = document.getElementById('frog');
  const tongue = document.getElementById('tongue');
  const fly = document.getElementById('fly');
  const garden = document.getElementById('garden');
  const counter = document.getElementById('counter');

  if (frog.classList.contains('jump')) return;

  munchSound.currentTime = 0;
  munchSound.play();
  
  frog.classList.add('jump');
  tongue.classList.add('shoot-tongue');
  fly.style.visibility = 'hidden';

  score++;
  counter.innerText = "Flies: " + score;

  if (score % 3 === 0) {
    const flowers = ['🌸', '🌻', '🌷', '🌼', '🌹'];
    const randomFlower = flowers[Math.floor(Math.random() * flowers.length)];
    const newFlower = document.createElement('span');
    newFlower.className = 'flower';
    newFlower.innerText = randomFlower;
    garden.appendChild(newFlower);
  }

  setTimeout(() => {
    frog.classList.remove('jump');
    tongue.classList.remove('shoot-tongue');
    fly.style.visibility = 'visible';
  }, 400);
}
