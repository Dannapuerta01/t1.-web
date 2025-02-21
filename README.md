<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Interfaz con Bootstrap</title>
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/css/bootstrap.min.css" rel="stylesheet">
    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/js/bootstrap.bundle.min.js"></script>
    <style>
        .search-box {
            width: 0;
            opacity: 0;
            transition: width 0.4s ease, opacity 0.4s ease;
            overflow: hidden;
        }
        .search-box.active {
            width: 200px;
            opacity: 1;
        }
    </style>
</head>
<body class="container">
    <nav class="navbar bg-light mb-4">
        <div class="container-fluid d-flex align-items-center justify-content-end">
            <form class="d-flex">
                <input type="text" class="form-control search-box me-2" id="search-input" placeholder="Escribe aquí...">
                <button class="btn btn-danger" id="search-btn">
                    <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" fill="currentColor" class="bi bi-search-heart" viewBox="0 0 16 16">
                        <path d="M6.5 4.482c1.664-1.673 5.825 1.254 0 5.018-5.825-3.764-1.664-6.69 0-5.018"/>
                        <path d="M13 6.5a6.47 6.47 0 0 1-1.258 3.844q.06.044.115.098l3.85 3.85a1 1 0 0 1-1.414 1.415l-3.85-3.85a1 1 0 0 1-.1-.115h.002A6.5 6.5 0 1 1 13 6.5M6.5 12a5.5 5.5 0 1 0 0-11 5.5 5.5 0 0 0 0 11"/>
                    </svg>
                </button>
            </form>
        </div>
    </nav>
    
    <div class="container text-center mb-3">
        <div class="row">
            <div class="col">
                <div class="card card-body">Información sobre productos.</div>
            </div>
            <div class="col">
                <div class="card card-body">Consejos exclusivos de Luxe.</div>
            </div>
            <div class="col">
                <div class="card card-body">Acerca de Luxe.</div>
            </div>
        </div>
    </div>
    
    <div class="container text-center mt-4">
        <h2>Crema humectante Luxe Piel</h2>
        <p>Recupera con nuestra crema humectante  el nivel óptimo de humectación y suavidad en tu rostro. ¡Atrévete a probar la línea esencial de Luxe Piel que ofrece una solución para cada tipo de piel!</p>
    </div>
    
    <div class="text-center mt-4">
        <img src="https://i.pinimg.com/736x/69/0b/e4/690be43474f64383b07fd55d7a979881.jpg" class="img-thumbnail" style="width: 300px">
    </div>
    
    <footer class="text-center mt-4 py-3 bg-light">
        <p>Síguenos en:</p>
        <a href="#" class="me-3"><img src="https://cdn-icons-png.flaticon.com/512/733/733579.png" width="30" alt="TikTok"></a>
        <a href="#" class="me-3"><img src="https://cdn-icons-png.flaticon.com/512/2111/2111463.png" width="30" alt="Instagram"></a>
        <a href="#"><img src="https://cdn-icons-png.flaticon.com/512/733/733547.png" width="30" alt="Facebook"></a>
    </footer>
    
    <script>
        document.getElementById("search-btn").addEventListener("click", function() {
            let input = document.getElementById("search-input");
            input.classList.toggle("active");
            if (input.classList.contains("active")) {
                input.focus();
            } else {
                input.value = "";
            }
        });
    </script>
</body>
</html>
