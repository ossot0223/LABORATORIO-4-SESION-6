# LABORATORIO-4-SESION-6
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.0.2/dist/css/bootstrap.min.css" rel="stylesheet" integrity="sha384-EVSTQN3/azprG1Anm3QDgpJLIm9Nao0Yz1ztcQTwFspd3yD65VohhpuuCOmLASjC" crossorigin="anonymous">
    <link rel="stylesheet" href="bootstrap.css">

    <title>Mi primera web</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            background-color: #f9f9f9;
            color: #333;
            line-height: 1.6;
        }

        .container {
            max-width: 800px;
            margin: 20px auto;
            padding: 20px;
            background-color: #f4f4f4;
            border-radius: 8px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
        }

        h1, h2 {
            color: #007bff;
            text-align: center;
            margin-bottom: 20px;
            text-shadow: 1px 1px 2px rgba(0,0,0,0.1);
        }

        p {
            color: #666;
            text-align: center;
            margin-bottom: 20px;
        }

        table {
            width: 100%;
            border-collapse: collapse;
            margin-top: 20px;
            display: none; /* Hide the table by default */
        }

        th, td {
            padding: 12px;
            text-align: left;
            border-bottom: 1px solid #ddd;
        }

        th {
            background-color: #f2f2f2;
            color: #333;
            font-weight: bold;
        }

        img {
            max-width: 80px;
            height: auto;
            display: block;
            margin: 0 auto;
            transition: transform 0.3s ease;
        }

        img:hover {
            transform: scale(1.1);
        }

        hr {
            border: none;
            height: 1px;
            background-color: #ddd;
            margin: 20px 0;
        }

        .button {
            display: block;
            width: 100%;
            max-width: 200px;
            margin: 20px auto;
            padding: 12px 24px;
            text-align: center;
            background-color: #007bff;
            color: #fff;
            border: none;
            border-radius: 4px;
            cursor: pointer;
            text-decoration: none;
            transition: background-color 0.3s ease;
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
        }

        .button:hover {
            background-color: #0056b3;
        }

        .hidden {
            display: none; /* Hide rows with 'hidden' class */
        }

        .buy-button {
            display: none; /* Hide the buy button initially */
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>CERTUS CLASE 2</h1>
        <h2>LABORATORIO 4</h2>
        <p>OSCAR SOTELO</p>
        <hr>
        <h1>OFERTAS</h1>
        <table id="productTable">
            <tr>
                <th>Código</th>
                <th>Producto</th>
                <th>Precio</th>
                <th>Imagen</th>
                <th>Comprar</th>
            </tr>
            <tr>
                <td>001</td>
                <td>Televisor</td>
                <td>1500 soles</td>
                <td><img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcS441HsMyz-0yZdzJx3lqC4O81OZaJzzqqzphA8HKLoTA&s" alt="Televisor"></td>
                <td><button class="buy-button">Comprar</button></td>
            </tr>
            <tr>
                <td>002</td>
                <td>Microondas</td>
                <td>650 soles</td>
                <td><img src="https://www.lg.com/content/dam/channel/wcms/pe/images/microondas/mh7032jas_bbkglpr_espr_pe_c/Basic-450.jpg" alt="Microondas"></td>
                <td><button class="buy-button">Comprar</button></td>
            </tr>
            <tr>
                <td>003</td>
                <td>Refrigerador</td>
                <td>1000 soles</td>
                <td><img src="https://cdn11.bigcommerce.com/s-dj46qhetxl/images/stencil/1280x1280/products/137849/386895/irdrotqaqdqdnbj7lqkq__78811.1692328643.jpg?c=1" alt="Refrigerador"></td>
                <td><button class="buy-button">Comprar</button></td>
            </tr>
        </table>
        <a href="#" class="button" id="showMoreBtn">Ver más</a>
    </div>
    
    <!-- Optional JavaScript; choose one of the two! -->

    <!-- Option 1: Bootstrap Bundle with Popper -->
    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.0.2/dist/js/bootstrap.bundle.min.js" integrity="sha384-MrcW6ZMFYlzcLA8Nl+NtUVF0sA7MsXsP1UyJoMp4YLEuNSfAP+JcXn/tWtIaxVXM" crossorigin="anonymous"></script>

    <!-- Option 2: Separate Popper and Bootstrap JS -->
    <!--
    <script src="https://cdn.jsdelivr.net/npm/@popperjs/core@2.9.3/dist/umd/popper.min.js" integrity="sha384-m/4mDo1XC+L2SuHNZ5I6LZP3D7R4iLbdTn2Z6f4HCp2s9CQnK+NyMvvkR1rHk4fo" crossorigin="anonymous"></script>
    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.0.2/dist/js/bootstrap.min.js" integrity="sha384-ZAxOYkoqfzijqB82kEBG2HRcStG5uZoaox9V3OX6o3OBt1qJ/3qM3fPjFLBLou1p" crossorigin="anonymous"></script>
    -->

    <script>
        document.getElementById('showMoreBtn').addEventListener('click', function() {
            var table = document.getElementById('productTable');
            if (table.style.display === 'none') {
                table.style.display = 'table'; // Show the table
                document.getElementById('showMoreBtn').innerText = 'Ver menos';
                var buyButtons = document.querySelectorAll('.buy-button');
                buyButtons.forEach(function(button) {
                    button.style.display = 'inline-block'; // Show the buy buttons
                });
            } else {
                table.style.display = 'none'; // Hide the table
                document.getElementById('showMoreBtn').innerText = 'Ver más';
                var buyButtons = document.querySelectorAll('.buy-button');
                buyButtons.forEach(function(button) {
                    button.style.display = 'none'; // Hide the buy buttons
                });
            }
        });
    </script>
</body>
</html>
