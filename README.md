<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1" />
<title>Happy 18th Birthday, Mira! 💛</title>
<style>
  body {
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    margin: 0; padding: 0;
    color: #333;
    text-align: center;
    background: linear-gradient(135deg, #ffe6cc, #ffcc99);
    position: relative;
    overflow-x: hidden;
  }

  /* subtle noise texture overlay */
  body::before {
    content: "";
    position: fixed;
    top: 0; left: 0; right: 0; bottom: 0;
    pointer-events: none;
    background: url('https://www.transparenttextures.com/patterns/asfalt-light.png') repeat;
    opacity: 0.05;
    z-index: 0;
  }

  header, .notes, footer {
    position: relative;
    background: rgba(255, 255, 255, 0.85);
    border-radius: 15px;
    box-shadow: 0 4px 10px rgba(0,0,0,0.1);
    max-width: 900px;
    margin: 1.5rem auto;
    padding: 2rem;
    z-index: 1;
  }

  h1, h2, h3, p {
    position: relative;
    z-index: 1;
    color: #663300;
  }

  .countdown {
    font-size: 1.5rem;
    margin: 1rem 0 2rem;
    font-weight: bold;
  }

  .gallery {
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    gap: 10px;
    max-width: 900px;
    margin: 0 auto 2rem;
  }

  .gallery img {
    width: 150px;
    height: 150px;
    object-fit: cover;
    border-radius: 12px;
    box-shadow: 0 3px 6px rgba(0,0,0,0.2);
    transition: transform 0.3s ease;
    cursor: pointer;
  }

  .gallery img:hover {
    transform: scale(1.1);
  }

  .audio-section {
    margin: 2rem auto;
    max-width: 400px;
  }

  .audio-section audio {
    width: 100%;
    outline: none;
    margin-bottom: 1rem;
  }

  button {
    background: #ff9f68;
    color: #fff;
    border: none;
    border-radius: 8px;
    padding: 0.8rem 1.6rem;
    font-size: 1rem;
    cursor: pointer;
    transition: background-color 0.3s ease;
    box-shadow: 0 4px 8px rgba(255, 159, 104, 0.6);
    z-index: 1;
  }

  button:hover {
    background-color: #ff7e36;
    box-shadow: 0 6px 12px rgba(255, 126, 54, 0.8);
  }

  .quiz-result {
    margin-top: 1rem;
    font-weight: bold;
    color: #663300;
  }

  #hiddenPhotoLink {
    display: none;
  }

  #hiddenPhoto {
    max-width: 300px;
    border-radius: 12px;
    box-shadow: 0 3px 6px rgba(0,0,0,0.3);
    margin-top: 10px;
  }
</style>
</head>
<body>

<header>
  <h1>Happy 18th Birthday, Mira! 💛🎉</h1>
  <p>To my beautiful Mariana, who lights up my life since 25 March. 💛</p>
  <div class="countdown" id="countdown">Counting down to your special day... 💛</div>
</header>

<section class="gallery" id="gallery">
  <!-- Replace these with real photos -->
  <img src="https://i.ibb.co/vxGZVqnw/mari-jpgxqwk-20250325-0001.jpg" alt="mari-jpgxqwk-20250325-0001" border="0">
  <img src="https://i.ibb.co/SD2KpdSG/IMG-20250718-WA0001.jpg" alt="IMG-20250718-WA0001" border="0">
  <img src="https://i.ibb.co/zTrf9F9m/IMG-20250731-WA0000.jpg" alt="IMG-20250731-WA0000" border="0">
</section>

<section class="audio-section">
  <h2>ur cutie msgs</h2>
  <audio controls>
    <source src="https://drive.google.com/uc?export=download&id=1V-K1eUSe4FvxMHj4WdW1JrqbBJkrTzwq" type="audio/mpeg" />
    Your browser does not support the audio element.
  </audio>

  <audio controls>
    <source src="https://drive.google.com/uc?export=download&id=1OukrbMhh2Ns3V1RVDIMLZ17QsjzoWqZr" type="audio/mpeg" />
    Your browser does not support the audio element.
  </audio>
  <h8>if i didnt work js know i tried untill i got tired for the audios i passed around two hours on audios alone love yaaa </h8>
</section>

<section class="notes">
  <h2>read this bitch</h2>
  <p>u the sunshine in my darkest days amor 💛”</p>
  <p>every day with you is a makes me soo fkin happy 💛”</p>
  <p>espero que tengas un hermoso día 💛”</p>
</section>

<section class="quiz">
  <h2>who is my baby</h2>
  <button onclick="showAnswer()">clickk meeee</button>
  <div class="quiz-result" id="quiz-result"></div>
  <a href="https://ibb.co/fLpJQHt" target="_blank" id="hiddenPhotoLink">
    <img id="hiddenPhoto" src="https://i.ibb.co/hwW0CVH/image-2025-08-09-160522141.png" alt="Mira Photo" border="0" />
  </a>
</section>

<h3>Happy 18th Birthday, Mira ❤️ A year ago, we were just two voices and a couple of pixels on Discord… and somehow, you became my favorite person in the whole world. From late night talks to that beautiful little book u made me, you’ve filled my life with love, laughter, and a million reasons to be grateful. Today, mi amor, you officially become an adult but to me, you’ll always be that sweet, funny, and slightly crazy girl who stole my heart without even trying. Feliz cumpleaños, mi Mira. Here to ur dreams ur smile and to us siempre. dont drink alot hoe  </h3>

<footer>
  Made with 💛 by me for Mira.
</footer>

<script>
  // Countdown Timer to August 31, 2025 (her 18th birthday)
  const countdownEl = document.getElementById('countdown');
  const birthday = new Date('2025-08-31T00:00:00');

  function updateCountdown() {
    const now = new Date();
    const diff = birthday - now;
    if(diff <= 0) {
      countdownEl.textContent = "Happy 18th Birthday, Mira! 🎂🎉";
      clearInterval(timer);
      return;
    }
    const days = Math.floor(diff / (1000 * 60 * 60 * 24));
    const hours = Math.floor((diff / (1000 * 60 * 60)) % 24);
    const minutes = Math.floor((diff / (1000 * 60)) % 60);
    const seconds = Math.floor((diff / 1000) % 60);
    countdownEl.textContent = `Time left: ${days}d ${hours}h ${minutes}m ${seconds}s 💛`;
  }

  const timer = setInterval(updateCountdown, 1000);
  updateCountdown();

  // Show picture on button click
  function showAnswer() {
    const quizResult = document.getElementById('quiz-result');
    quizResult.textContent = ""; // clear text if any
    const photoLink = document.getElementById('hiddenPhotoLink');
    photoLink.style.display = 'inline-block'; // show the clickable image
  }
</script>

</body>
</html>
