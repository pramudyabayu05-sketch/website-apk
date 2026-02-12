# website-apk
<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <title>Deskripsi Spesial ✨</title>

    <style>
        body {
            margin: 0;
            font-family: 'Segoe UI', sans-serif;
            background: linear-gradient(to right, #fbc2eb, #a6c1ee);
            height: 100vh;
            display: flex;
            justify-content: center;
            align-items: center;
        }

        .container {
            background: white;
            width: 90%;
            max-width: 400px;
            padding: 30px;
            border-radius: 20px;
            box-shadow: 0 10px 25px rgba(0,0,0,0.2);
            text-align: center;
        }

        h1 {
            color: #e84393;
        }

        input {
            width: 90%;
            padding: 10px;
            margin: 10px 0;
            border-radius: 10px;
            border: 1px solid #ccc;
            font-size: 16px;
        }

        button {
            background: #e84393;
            color: white;
            border: none;
            padding: 12px 25px;
            border-radius: 25px;
            font-size: 16px;
            cursor: pointer;
            margin-top: 15px;
        }

        button:hover {
            background: #d63031;
        }

        .slide {
            display: none;
        }

        .active {
            display: block;
        }

        p {
            font-size: 17px;
            color: #444;
            line-height: 1.6;
        }

        .highlight {
            color: #e84393;
            font-weight: bold;
        }
    </style>
</head>

<body>

<div class="container">

    <!-- SLIDE 1 -->
    <div class="slide active" id="slide1">
        <h1>Kenalan Dulu ✨</h1>

        <input type="text" id="nama" placeholder="Masukkan Nama">
        <input type="number" id="umur" placeholder="Masukkan Umur">

        <button onclick="nextSlide()">Lanjut ➡️</button>
    </div>

    <!-- SLIDE 2 -->
    <div class="slide" id="slide2">
        <h1>Bintang Istimewa 🌟</h1>

        <p id="deskripsi"></p>

        <button onclick="backSlide()">⬅️ Kembali</button>
    </div>

</div>

<script>

function nextSlide() {

    let nama = document.getElementById("nama").value;
    let umur = document.getElementById("umur").value;

    if (nama === "" || umur === "") {
        alert("Nama dan umur harus diisi ya 😊");
        return;
    }

    // Ganti slide
    document.getElementById("slide1").classList.remove("active");
    document.getElementById("slide2").classList.add("active");

    // Isi deskripsi
    let teks = `
    <span class="highlight">${nama}</span> adalah sosok perempuan yang
    bagaikan bintang di langit malam ✨<br><br>

    Di usianya yang ke-${umur} tahun, 
    dia tumbuh menjadi pribadi yang:<br><br>

    💖 Cantik luar dan dalam<br>
    🌸 Berhati baik dan tulus<br>
    📚 Cerdas dan penuh wawasan<br>
    💪 Rajin dan bertanggung jawab<br>
    🌟 Mandiri dan tidak mudah menyerah<br>
    🔥 Penuh semangat dalam mengejar mimpi<br><br>

    Keberadaannya mampu membawa
    kebahagiaan bagi orang di sekitarnya.
    Senyumnya seperti cahaya,
    sikapnya seperti ketenangan,
    dan semangatnya seperti api yang
    menginspirasi 🔥<br><br>

    Dia bukan hanya istimewa,
    tapi juga pantas mendapatkan
    yang terbaik di dunia 💕
    `;

    document.getElementById("deskripsi").innerHTML = teks;
}

function backSlide() {
    document.getElementById("slide2").classList.remove("active");
    document.getElementById("slide1").classList.add("active");
}

</script>

</body>
</html>
