<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Checkout - Seven7</title>
    <style>
        body {
            background-color: black;
            color: white;
            font-family: Arial, sans-serif;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            margin: 0;
            flex-direction: column;
        }

        .checkout-container {
            background-color: #222;
            padding: 30px;
            border-radius: 8px;
            box-shadow: 0 4px 10px rgba(0, 0, 0, 0.5);
            width: 400px;
            margin-top: 30px;
        }

        h1 {
            text-align: center;
            font-size: 24px;
        }

        .product-info {
            margin-bottom: 20px;
        }

        .product-info p {
            font-size: 18px;
        }

        .form-group {
            margin-bottom: 15px;
        }

        label {
            display: block;
            font-size: 16px;
        }

        input[type="text"],
        input[type="email"],
        input[type="number"],
        input[type="submit"] {
            width: 100%;
            padding: 10px;
            margin-top: 5px;
            border: 1px solid #444;
            background-color: #333;
            color: white;
            border-radius: 4px;
        }

        input[type="submit"] {
            background-color: #28a745;
            cursor: pointer;
        }

        input[type="submit"]:hover {
            background-color: #218838;
        }

        .footer {
            margin-top: 20px;
            font-size: 14px;
            color: #aaa;
            text-align: center;
        }

        .testimonials {
            margin-top: 30px;
            padding: 20px;
            background-color: #333;
            border-radius: 8px;
            width: 400px;
        }

        .testimonial {
            margin-bottom: 15px;
            font-style: italic;
            color: #ddd;
        }

        .testimonial p {
            margin: 0;
        }

        .testimonial strong {
            display: block;
            margin-top: 5px;
            color: #28a745;
        }

        /* Timer de Oferta */
        .offer-timer {
            background-color: #ff3333;
            color: white;
            padding: 20px;
            text-align: center;
            margin-top: 30px;
            border-radius: 8px;
            font-size: 20px;
        }

        .offer-timer span {
            font-size: 30px;
            font-weight: bold;
        }
    </style>
</head>
<body>

    <!-- Timer de Oferta Imperdível -->
    <div class="offer-timer">
        <p>Oferta Imperdível: De R$ 1599,99 por apenas R$ 19,99!</p>
        <p>Corra, a oferta acaba em:</p>
        <p><span id="timer">10:00</span></p>
    </div>

    <div class="checkout-container">
        <h1>Checkout - Seven7</h1>
        
        <div class="product-info">
            <p>Produto: <strong>Seven7</strong></p>
            <p>Preço Original: <strong>R$ 1599,99</strong></p>
            <p><strong>Preço com Oferta: R$ 19,99</strong></p>
            <p><strong>Pagamento vitalício</strong></p>
            <p><strong>Garantia de 7 dias</strong></p>
        </div>

        <form action="#" method="post">
            <div class="form-group">
                <label for="nome">Nome Completo:</label>
                <input type="text" id="nome" name="nome" required>
            </div>
            
            <div class="form-group">
                <label for="email">E-mail:</label>
                <input type="email" id="email" name="email" required>
            </div>
            
            <div class="form-group">
                <label for="cartao">Número do Cartão:</label>
                <input type="number" id="cartao" name="cartao" required>
            </div>
            
            <div class="form-group">
                <label for="cpf">CPF:</label>
                <input type="text" id="cpf" name="cpf" required>
            </div>
            
            <input type="submit" value="Finalizar Compra">
        </form>

        <div class="footer">
            <p>Pagamentos seguros. Garantia de 7 dias para reembolso.</p>
        </div>
    </div>

    <!-- Depoimentos -->
    <div class="testimonials">
        <h2>O que nossos clientes dizem:</h2>
        <div class="testimonial">
            <p>"O Seven7 mudou completamente a minha rotina! Um excelente produto por um preço acessível e com garantia de 7 dias. Super recomendo!"</p>
            <strong>- João Silva</strong>
        </div>
        <div class="testimonial">
            <p>"Muito satisfeito com o Seven7! A compra foi rápida e o atendimento impecável. Além disso, o pagamento vitalício é um ótimo benefício!"</p>
            <strong>- Maria Oliveira</strong>
        </div>
        <div class="testimonial">
            <p>"Nunca mais vou ficar sem o Seven7! A garantia de 7 dias me deixou tranquilo e o produto entregou tudo o que prometeu!"</p>
            <strong>- Carlos Costa</strong>
        </div>
    </div>

    <script>
        // Timer de Oferta
        var countdown = 600; // 10 minutos em segundos
        var timerElement = document.getElementById("timer");

        function updateTimer() {
            var minutes = Math.floor(countdown / 60);
            var seconds = countdown % 60;
            if (seconds < 10) seconds = "0" + seconds;
            timerElement.textContent = minutes + ":" + seconds;
            countdown--;

            if (countdown < 0) {
                clearInterval(timerInterval);
                timerElement.textContent = "Oferta Expirada!";
            }
        }

        var timerInterval = setInterval(updateTimer, 1000);
    </script>

</body>
</html>
