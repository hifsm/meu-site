# meu-site
<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Desafio GitHub</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #f4f4f9;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            margin: 0;
        }

        .content {
            text-align: center;
            background-color: #fff;
            padding: 20px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
        }

        h1 {
            color: #333;
        }

        .hint {
            margin-top: 20px;
            color: #777;
        }

        .hint a {
            color: #007BFF;
            text-decoration: none;
        }

        .hint a:hover {
            text-decoration: underline;
        }
    </style>
</head>
<body>
    <div class="content">
        <h1>Bem-vindo ao Desafio!</h1>
        <p>Procure pela dica que irá te ajudar a encontrar a resposta!</p>
        <p class="hint">Dica: Veja com atenção o código-fonte da página...</p>
    </div>

    <!-- A flag está escondida aqui! -->
    <!-- flag{BFG} -->

    <script>
        // Alguma interação simples para dar a sensação de desafio
        setTimeout(function() {
            alert("Você encontrou a dica! Explore o código-fonte!");
        }, 2000);
    </script>
</body>
</html>
