<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Casa do Pet</title>
    <link rel="stylesheet" href="style.css">
    <style>
        /* Estilos CSS para o carrossel */
        .carousel-container {
            width: 100%;
            margin-bottom: 20px;
            overflow: hidden;
            position: relative;
        }

        .carousel-slide {
            display: flex;
            transition: transform 0.5s ease;
        }

        .carousel-image {
            width: 100%;
            height: auto;
        }

        .prev-btn, .next-btn {
            position: absolute;
            top: 50%;
            transform: translateY(-50%);
            cursor: pointer;
            padding: 10px;
            background: rgba(0, 0, 0, 0.5);
            color: white;
            border: none;
            outline: none;
        }

        .prev-btn {
            left: 0;
        }

        .next-btn {
            right: 0;
        }
    </style>
</head>
<body>
    <header>
        <div class="logo">
            <img src="https://github.com/guilherme-rigel/CasaDoPet/blob/main/logo%20casa%20do%20pet.png?raw=true" alt="Logo Casa do Pet" width="200" height="200">
        </div>
        <nav>
            <ul>
                <li><a href="#">Home</a></li>
                <li><a href="#">Produtos</a></li>
                <li><a href="#">Banho e Tosa</a></li>
                <li><a href="#">Atendimento</a></li>
                <li><a href="#">Contato</a></li>
            </ul>
        </nav>
        <div class="login-cadastro">
            <a href="#">Entrar</a>
            <a href="#">Cadastrar</a>
        </div>
    </header>
    <main>
        <!-- Carrossel de Imagens -->
        <div class="carousel-container">
            <div class="carousel-slide">
                <img class="carousel-image" src="banner1.jpg" alt="Banner 1">
                <img class="carousel-image" src="banner2.jpg" alt="Banner 2">
                <img class="carousel-image" src="banner3.jpg" alt="Banner 3">
            </div>
            <button class="prev-btn">&#10094;</button>
            <button class="next-btn">&#10095;</button>
        </div>

        <!-- Restante do conteúdo -->
        <section class="promocao">
            <h2>TODO SITE 15% OFF</h2>
            <p>Aproveite nossa promoção e economize em compras para o seu pet!</p>
            <a href="#">Saiba Mais</a>
        </section>
        <section class="produtos-em-destaque">
            <!-- Produtos em Destaque -->
            <!-- Seu código de produtos em destaque aqui -->
        </section>
        <section class="servicos">
            <!-- Seus serviços aqui -->
        </section>
        <section class="newsletter">
            <!-- Seção de Newsletter -->
        </section>
    </main>
    <footer>
        <!-- Seu rodapé aqui -->
    </footer>

    <!-- Script do carrossel -->
    <script>
        const prevBtn = document.querySelector('.prev-btn');
        const nextBtn = document.querySelector('.next-btn');
        const slide = document.querySelector('.carousel-slide');

        let counter = 0;
        const size = slide.children[0].offsetWidth;

        nextBtn.addEventListener('click', () => {
            if (counter >= slide.children.length - 1) return;
            counter++;
            slide.style.transform = `translateX(${-size * counter}px)`;
        });

        prevBtn.addEventListener('click', () => {
            if (counter <= 0) return;
            counter--;
            slide.style.transform = `translateX(${-size * counter}px)`;
        });
    </script>
</body>
</html>
