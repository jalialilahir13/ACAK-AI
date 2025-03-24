# ACAK-AI
GATAU
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Gambar Acak</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            margin: 0;
            background-color: #f0f0f0;
        }
        .container {
            text-align: center;
        }
        button {
            padding: 15px 30px;
            font-size: 16px;
            cursor: pointer;
            background-color: #4CAF50;
            color: white;
            border: none;
            border-radius: 5px;
            margin-top: 20px;
        }
        button:hover {
            background-color: #45a049;
        }
        img {
            width: 300px;
            height: 300px;
            border-radius: 10px;
            margin-top: 20px;
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>Gambar Acak Setiap Kali Kamu Klik!</h1>
        <button onclick="getRandomImage()">Tampilkan Gambar Acak</button>
        <div id="image-container">
            <!-- Gambar akan muncul di sini -->
        </div>
    </div>

    <script>
        function getRandomImage() {
            const imageUrls = [
                'https://source.unsplash.com/random/300x300?1',
                'https://source.unsplash.com/random/300x300?2',
                'https://source.unsplash.com/random/300x300?3',
                'https://source.unsplash.com/random/300x300?4',
                'https://source.unsplash.com/random/300x300?5',
            ];

            const randomIndex = Math.floor(Math.random() * imageUrls.length);
            const imageContainer = document.getElementById('image-container');

            // Hapus gambar lama
            imageContainer.innerHTML = '';

            // Buat elemen gambar baru
            const img = document.createElement('img');
            img.src = imageUrls[randomIndex];
            img.alt = 'Gambar Acak';

            // Tambahkan gambar ke container
            imageContainer.appendChild(img);
        }
    </script>
</body>
</html>
