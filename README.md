# minha-rifa
site rifa
<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Rifa da Gratidão</title>
    <link href="https://fonts.googleapis.com/css2?family=Roboto:wght@400;700&display=swap" rel="stylesheet">
    <style>
        body {
            font-family: 'Roboto', sans-serif;
            background: linear-gradient(to right, #f9f9f9, #e0f7fa);
            color: #333;
            margin: 0;
            padding: 0;
        }
        header {
            background: linear-gradient(to right, #03b60c, #0288d1);
            color: white;
            padding: 15px 20px;
            text-align: center;
            font-family: 'Arial Black', sans-serif;
        }
        main {
            padding: 20px;
        }
        section {
            margin-bottom: 20px;
        }
        h2 {
            color: #1301b9;
            font-family: 'Comic Sans MS', sans-serif;
            font-size: 24px;
        }
        .prize {
            border: 1px solid #ddd;
            padding: 10px;
            margin-bottom: 10px;
            background-color: white;
            display: flex;
            align-items: center;
            border-radius: 8px;
            box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
        }
        .prize img {
            max-width: 150px;
            margin-right: 20px;
            border-radius: 8px;
            transition: transform 0.3s;
        }
        .prize img:hover {
            transform: scale(1.1);
        }
        .buy-ticket {
            text-align: center;
            margin: 20px 0;
        }
        .buy-ticket button {
            background-color: #4e004e;
            color: white;
            border: none;
            padding: 10px 20px;
            font-size: 16px;
            cursor: pointer;
            transition: background-color 0.3s;
            border-radius: 5px;
        }
        .buy-ticket button:hover {
            background-color: #360036;
        }
        .contact {
            text-align: center;
            margin-top: 20px;
        }
        .contact p {
            margin: 5px 0;
        }
        footer {
            background-color: #0f83e2;
            color: white;
            text-align: center;
            padding: 10px 20px;
            position: fixed;
            bottom: 0;
            width: 100%;
        }
        footer .social-icons {
            margin-top: 10px;
        }
        footer .social-icons a {
            color: white;
            margin: 0 5px;
            text-decoration: none;
            transition: color 0.3s;
        }
        footer .social-icons a:hover {
            color: #ddd;
        }
        form {
            max-width: 400px;
            margin: 0 auto;
            text-align: left;
        }
        form label, form input, form button {
            width: 100%;
            margin-bottom: 10px;
        }
        form input {
            padding: 8px;
            box-sizing: border-box;
        }
        .leaderboard {
            margin-top: 20px;
        }
        .leaderboard table {
            width: 100%;
            border-collapse: collapse;
            margin-bottom: 20px;
        }
        .leaderboard th, .leaderboard td {
            border: 1px solid #ddd;
            padding: 8px;
            text-align: center;
        }
        .leaderboard th {
            background-color: #f2f2f2;
        }
        .faq, .testimonials {
            background-color: white;
            padding: 20px;
            border-radius: 8px;
            box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
        }
        .faq h3, .testimonials h3 {
            color: #1301b9;
        }

        /* Estilos para telas menores que 768px */
        @media (max-width: 768px) {
            header, footer {
                text-align: center;
            }

            .prize {
                flex-direction: column;
                align-items: flex-start;
            }

            .prize img {
                max-width: 100%;
                margin-bottom: 10px;
            }

            .buy-ticket, .contact, .leaderboard, .faq, .testimonials {
                padding: 10px;
            }

            form {
                width: 90%;
                margin: 0 auto;
            }

            .leaderboard table, .leaderboard th, .leaderboard td {
                font-size: 14px;
            }

            .social-icons a {
                display: block;
                margin: 5px 0;
            }
        }
    </style>
</head>
<body>
    <header>
        <h1>Rifa da Gratidão</h1>
        <p>Participe e concorra a prêmios incríveis!</p>
    </header>
    <main>
        <section id="prizes">
            <h2>Prêmios</h2>
            <div class="prize">
                <img src="https://a-static.mlcdn.com.br/800x560/liquidificador-mondial-turbo-power-l-99-fb-preto-com-filtro-3-velocidades-500w/magazineluiza/021756700/7930dc2293281ea25af167111616abdb.jpg" alt="Liquidificador Philco">
                <div>
                    <h3>Liquidificador de 12 velocidades Philco</h3>
                    <p>Descrição: Liquidificador de alta qualidade com 12 velocidades.</p>
                </div>
            </div>
            <div class="prize">
                <h3>Prêmio em dinheiro: R$ 400</h3>
                <p>Descrição: Ganhe R$ 400 em dinheiro ou pix.</p>
            </div>
            <div class="prize">
                <h3>Prêmio em dinheiro: R$ 800</h3>
                <p>Descrição: Ganhe R$ 800 em dinheiro ou pix.</p>
            </div>
        </section>
        <section id="rules">
            <h2>Regras da Rifa</h2>
            <ul>
                <li>Valor de cada rifa: R$ 2,50.</li>
                <li>Quanto mais rifas você comprar, mais chances de ganhar você terá.</li>
                <li>Se o seu nome for sorteado duas vezes, você ganhará dois prêmios na ordem do sorteio.</li>
                <li>A pessoa que mais comprar rifas ganhará um valor maior do que gastou em PIX ou dinheiro garantido no dia do sorteio.</li>
            </ul>
        </section>
        <section id="buy">
            <h2>Comprar Rifa</h2>
            <div class="buy-ticket">
                <p>Para comprar rifas, faça o pagamento via PIX para a chave (61) 99996-4508 e envie o comprovante abaixo:</p>
                <form id="raffleForm">
                    <label for="name">Nome Completo</label>
                    <input type="text" id="name" name="name" required>
                    <label for="email">Email</label>
                    <input type="email" id="email" name="email" required>
                    <label for="tickets">Quantidade de Rifas</label>
                    <input type="number" id="tickets" name="tickets" required>
                    <label for="proof">Comprovante de Pagamento (max 5MB)</label>
                    <input type="file" id="proof" name="proof" accept="image/*,application/pdf" required>
                    <button type="submit">Enviar</button>
                </form>
            </div>
        </section>
        <section id="faq">
            <h2>Perguntas Frequentes</h2>
            <div class="faq">
                <h3>Como funciona a rifa?</h3>
                <p>Você compra quantas rifas desejar, envia o comprovante de pagamento e participa do sorteio dos prêmios.</p>
                <h3>Como faço para comprar as rifas?</h3>
                <p>Faça o pagamento via PIX para a chave fornecida e envie o comprovante usando o formulário de compra.</p>
                <h3>Quando será realizado o sorteio?</h3>
                <p>O sorteio será realizado no final do mês. Todos os participantes serão notificados por email.</p>
            </div>
        </section>
        <section id="testimonials">
            <h2>Depoimentos</h2>
            <div class="testimonials">
                <p>"Comprei várias rifas e fiquei muito satisfeito com a transparência do sorteio. Recomendo a todos!" - João Santos</p>
            </div>
        </section>
        <section id="contact">
            <h2>Contato</h2>
            <div class="contact">
                <p>WhatsApp: (61) 99996-4508</p>
                <p>Email: itauanamartinscasl0438@gmail.com</p>
            </div>
        </section>
        <section id="leaderboard" class="leaderboard">
            <h2>Maior Comprador de Rifas</h2>
            <table>
                <thead>
                    <tr>
                        <th>Posição</th>
                        <th>Nome</th>
                        <th>Quantidade de Rifas</th>
                    </tr>
                </thead>
                <tbody id="leaderboardBody">
                    <!-- Este conteúdo será preenchido dinamicamente -->
                </tbody>
            </table>
        </section>
    </main>
    <footer>
        <p>&copy; 2024 Rifa da Gratidão. Todos os direitos reservados.</p>
        <div class="social-icons">
            <a href="https://facebook.com" target="_blank">Facebook</a>
            <a href="https://instagram.com" target="_blank">Instagram</a>
            <a href="https://twitter.com" target="_blank">Twitter</a>
        </div>
    </footer>
    <script>
        document.getElementById('raffleForm').addEventListener('submit', function(event) {
            event.preventDefault();
            const name = document.getElementById('name').value.trim();
            const email = document.getElementById('email').value.trim();
            const tickets = document.getElementById('tickets').value;
            const proof = document.getElementById('proof').files[0];

            if (!name || !email || !tickets || !proof) {
                alert('Por favor, preencha todos os campos.');
                return;
            }

            if (!/^[^\s@]+@[^\s@]+\.[^\s@]+$/.test(email)) {
                alert('Por favor, insira um email válido.');
                return;
            }

            if (proof.size > 5 * 1024 * 1024) { // Limite de 5MB
                alert('O arquivo deve ter no máximo 5MB.');
                return;
            }

            alert('Compra realizada com sucesso! Você será redirecionado.');

            const formData = new FormData();
            formData.append('name', name);
            formData.append('email', email);
            formData.append('tickets', tickets);
            formData.append('proof', proof);

            fetch('/comprar-rifa', {
                method: 'POST',
                body: formData,
                headers: {
                    'CSRF-Token': 'your-csrf-token-here' // Substitua pelo token CSRF real
                }
            })
            .then(response => response.json())
            .then(data => {
                if (data.success) {
                    window.location.href = 'pagina-de-confirmacao.html';
                } else {
                    alert('Houve um problema na compra. Por favor, tente novamente.');
                }
            })
            .catch(error => {
                alert('Erro ao processar a compra. Por favor, tente novamente mais tarde.');
                console.error('Error:', error);
            });
        });

        // Carregar a leaderboard
        fetch('/leaderboard')
            .then(response => response.json())
            .then(data => {
                const leaderboardBody = document.getElementById('leaderboardBody');
                data.forEach((item, index) => {
                    const row = document.createElement('tr');
                    row.innerHTML = `
                        <td>${index + 1}</td>
                        <td>${item.name}</td>
                        <td>${item.tickets}</td>
                    `;
                    leaderboardBody.appendChild(row);
                });
            });
    </script>
</body>
</html>
