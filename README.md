<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Minha Loja Virtual</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <header>
        <h1>Minha Loja Virtual</h1>
        <nav>
            <ul>
                <li><a href="#">Home</a></li>
                <li><a href="#">Produtos</a></li>
                <li><a href="#">Contato</a></li>
            </ul>
        </nav>
    </header>

    <section class="banner">
        <h2>Bem-vindo à Minha Loja Virtual</h2>
        <p>Encontre os melhores produtos com os melhores preços!</p>
        <a href="#" class="btn">Ver Produtos</a>
    </section>

    <section class="produtos">
        <h2>Nossos Produtos</h2>
        <div class="produto">
            <img src="produto1.jpg" alt="Produto 1">
            <h3>Produto 1</h3>
            <p>R$ 99,99</p>
            <button class="btn-adicionar" data-produto="Produto 1" data-preco="99.99">Adicionar ao Carrinho</button>
        </div>
        <div class="produto">
            <img src="produto2.jpg" alt="Produto 2">
            <h3>Produto 2</h3>
            <p>R$ 149,99</p>
            <button class="btn-adicionar" data-produto="Produto 2" data-preco="149.99">Adicionar ao Carrinho</button>
        </div>
        <div class="produto">
            <img src="produto3.jpg" alt="Produto 3">
            <h3>Produto 3</h3>
            <p>R$ 199,99</p>
            <button class="btn-adicionar" data-produto="Produto 3" data-preco="199.99">Adicionar ao Carrinho</button>
        </div>
    </section>

    <footer>
        <p>&copy; 2024 Minha Loja Virtual. Todos os direitos reservados.</p>
    </footer>

    <script>
        // Adicionar ao carrinho
        document.addEventListener('DOMContentLoaded', function() {
            const btnsAdicionar = document.querySelectorAll('.btn-adicionar');

            btnsAdicionar.forEach(btn => {
                btn.addEventListener('click', function() {
                    const produto = this.getAttribute('data-produto');
                    const preco = parseFloat(this.getAttribute('data-preco'));
                    
                    // Aqui você pode adicionar a lógica para adicionar o produto ao carrinho
                    console.log(`Produto "${produto}" adicionado ao carrinho por R$ ${preco.toFixed(2)}`);
                });
            });
        });
    </script>
</body>
</html>