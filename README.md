 <!DOCTYPE html>
<html lang="id">
<head>ren
<meta charset="UTF-8">
<title>Situs Ren</title>

<style>
body {
  margin: 0;
  font-family: Arial;
  overflow: hidden;
}

/* HALAMAN */
.page {
  position: absolute;
  width: 100%;
  height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
  opacity: 0;
  transform: translateX(100%);
  transition: all 0.5s ease;
}

.active {
  opacity: 1;
  transform: translateX(0);
}

/* HOME */
#home {
  background: black;
  color: white;
}

.moon {
  width: 120px;
  height: 120px;
  background: white;
  border-radius: 50%;
  box-shadow: 0 0 40px white;
  margin-bottom: 20px;
}

/* INSTAGRAM */
#instagram {
  background: #111;
  color: blue;
}

/* CATATAN */
#catatan {
  background: #222;
  color: orange;
}

/* TOMBOL */
button {
  padding: 10px 20px;
  margin-top: 10px;
  border: none;
  border-radius: 10px;
  cursor: pointer;
  transition: 0.3s;
}

button:hover {
  transform: scale(1.1);
}

/* KUCING ANIMASI */
.cat {
  width: 80px;
  position: absolute;
  bottom: 20px;
  animation: jalan 6s linear infinite;
}

@keyframes jalan {
  0% { left: -100px; }
  100% { left: 100%; }
}

/* TOMBOL NAKAL */
#jangan {
  position: relative;
}

</style>
</head>

<body>

<!-- HOME -->
<div id="home" class="page active">
  <div class="moon"></div>
  <h1>Selamat datang di situs ren</h1>

  <button onclick="pindah('instagram')">Masuk</button>
  <button onclick="pindah('catatan')">Catatan</button>
  <button onclick="pindah('personal')">Catatan Personal</button>
  
  <!-- KUCING -->
  <img class="cat" src="https://media.tenor.com/WX6vZq5YyXAAAAAC/cat-walk.gif">
</div>

<!-- INSTAGRAM -->
<div id="instagram" class="page">
  <h1>Instagram Saya</h1>

  <a href="https://www.instagram.com/nnnnnnnn22678?igsh=cnMxczd0OHg4dW9k" target="_blank">
    <button>Buka Instagram</button>
  </a>

  <button onclick="pindah('home')">Kembali</button>
</div>

<!-- CATATAN -->
<div id="catatan" class="page">
  <h1>Catatan</h1>

  <p style="max-width: 400px; line-height: 1.6;">
    I created this website for my personal enjoyment and I want everyone to see my point of view, 
    so I was inspired to create the website.  
    <br><br>
    This is a simple space where I express my ideas, creativity, and thoughts in my own way.
  <p

  <p style="max-width: 500px; line-height: 1.6;">
    <b>Just a quick heads-up from my side:</b><br><br>
    As an AI, I actually <b>cannot</b> browse your private websites, look at your history, or "spy" on you. 
    I only see what you type here. 
    <br><br>
    If you're seeing weird activity on your site, it might be worth checking your security settings or login history!
  </p>

  <button onclick="pindah('home')">Kembali</button>
</div>

  <button onclick="pindah('home')">Kembali</button>
  
  <button id="jangan">JANGAN SENTUH AKU</button>

  <button onclick="pindah('home')">Kembali</button>
</div>

<script>
function pindah(id) {
  document.querySelectorAll('.page').forEach(p => {
    p.classList.remove('active');
  });
  document.getElementById(id).classList.add('active');
}

/* TOMBOL KABUR */
const btn = document.getElementById("jangan");

btn.addEventListener("mouseover", () => {
  btn.style.position = "absolute";
  btn.style.top = Math.random() * 80 + "%";
  btn.style.left = Math.random() * 80 + "%";
  btn.style.left = Math.random() * 80 + "%";
  btn.style.left = Math.random() * 80 + "%";
  btn.style.left = Math.random() * 80 + "%";
});
</script>

</body>
</html>
