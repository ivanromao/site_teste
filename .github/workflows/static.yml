<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Cadastro de Atletas - Liga de Voleibol de Jundiaí</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/5.15.3/css/all.min.css"></link>
    <link href="https://fonts.googleapis.com/css2?family=Roboto:wght@400;700&display=swap" rel="stylesheet">
</head>
<body class="bg-gray-100 font-roboto">
    <div class="container mx-auto p-4">
        <h1 class="text-2xl font-bold text-center mb-4">Cadastro de Atletas</h1>
        <div class="flex justify-center mb-4">
            <button id="inserirDadosBtn" class="bg-blue-500 text-white px-4 py-2 rounded hover:bg-blue-700">Inserir Dados de Atletas</button>
        </div>
        <div id="formContainer" class="hidden">
            <form id="atletasForm" class="bg-white p-4 rounded shadow-md">
                <div class="mb-4">
                    <label for="time" class="block text-gray-700">Selecione o Time:</label>
                    <select id="time" class="w-full p-2 border rounded">
                        <option value="timeX">Time X</option>
                        <option value="timeY">Time Y</option>
                        <option value="timeZ">Time Z</option>
                    </select>
                </div>
                <div class="mb-4">
                    <label for="set" class="block text-gray-700">Selecione o Set:</label>
                    <select id="set" class="w-full p-2 border rounded">
                        <option value="primeiroSet">Primeiro Set</option>
                        <option value="segundoSet">Segundo Set</option>
                        <option value="terceiroSet">Terceiro Set</option>
                        <option value="quartoSet">Quarto Set</option>
                        <option value="tieBreak">Tie Break</option>
                    </select>
                </div>
                <div id="atletasContainer">
                    <div class="mb-4">
                        <label for="nomeAtleta1" class="block text-gray-700">Nome do Atleta:</label>
                        <input type="text" id="nomeAtleta1" class="w-full p-2 border rounded" placeholder="Nome do Atleta">
                    </div>
                    <div class="mb-4">
                        <label for="numeroAtleta1" class="block text-gray-700">Número do Atleta:</label>
                        <input type="text" id="numeroAtleta1" class="w-full p-2 border rounded" placeholder="Número do Atleta">
                    </div>
                    <div class="mb-4">
                        <label for="posicaoAtleta1" class="block text-gray-700">Posição em Quadra:</label>
                        <input type="text" id="posicaoAtleta1" class="w-full p-2 border rounded" placeholder="Posição em Quadra">
                    </div>
                </div>
                <div class="flex justify-center mb-4">
                    <button type="button" id="adicionarAtletaBtn" class="bg-green-500 text-white px-4 py-2 rounded hover:bg-green-700">Adicionar Atleta</button>
                </div>
                <div class="flex justify-center">
                    <button type="submit" class="bg-red-500 text-white px-4 py-2 rounded hover:bg-red-700">Finalizar</button>
                </div>
            </form>
        </div>
    </div>

    <script>
        document.getElementById('inserirDadosBtn').addEventListener('click', function() {
            document.getElementById('formContainer').classList.toggle('hidden');
        });

        document.getElementById('adicionarAtletaBtn').addEventListener('click', function() {
            const atletasContainer = document.getElementById('atletasContainer');
            const atletaCount = atletasContainer.children.length / 3 + 1;

            const nomeAtletaDiv = document.createElement('div');
            nomeAtletaDiv.classList.add('mb-4');
            const nomeAtletaLabel = document.createElement('label');
            nomeAtletaLabel.setAttribute('for', `nomeAtleta${atletaCount}`);
            nomeAtletaLabel.classList.add('block', 'text-gray-700');
            nomeAtletaLabel.textContent = 'Nome do Atleta:';
            const nomeAtletaInput = document.createElement('input');
            nomeAtletaInput.setAttribute('type', 'text');
            nomeAtletaInput.setAttribute('id', `nomeAtleta${atletaCount}`);
            nomeAtletaInput.classList.add('w-full', 'p-2', 'border', 'rounded');
            nomeAtletaInput.setAttribute('placeholder', 'Nome do Atleta');
            nomeAtletaDiv.appendChild(nomeAtletaLabel);
            nomeAtletaDiv.appendChild(nomeAtletaInput);

            const numeroAtletaDiv = document.createElement('div');
            numeroAtletaDiv.classList.add('mb-4');
            const numeroAtletaLabel = document.createElement('label');
            numeroAtletaLabel.setAttribute('for', `numeroAtleta${atletaCount}`);
            numeroAtletaLabel.classList.add('block', 'text-gray-700');
            numeroAtletaLabel.textContent = 'Número do Atleta:';
            const numeroAtletaInput = document.createElement('input');
            numeroAtletaInput.setAttribute('type', 'text');
            numeroAtletaInput.setAttribute('id', `numeroAtleta${atletaCount}`);
            numeroAtletaInput.classList.add('w-full', 'p-2', 'border', 'rounded');
            numeroAtletaInput.setAttribute('placeholder', 'Número do Atleta');
            numeroAtletaDiv.appendChild(numeroAtletaLabel);
            numeroAtletaDiv.appendChild(numeroAtletaInput);

            const posicaoAtletaDiv = document.createElement('div');
            posicaoAtletaDiv.classList.add('mb-4');
            const posicaoAtletaLabel = document.createElement('label');
            posicaoAtletaLabel.setAttribute('for', `posicaoAtleta${atletaCount}`);
            posicaoAtletaLabel.classList.add('block', 'text-gray-700');
            posicaoAtletaLabel.textContent = 'Posição em Quadra:';
            const posicaoAtletaInput = document.createElement('input');
            posicaoAtletaInput.setAttribute('type', 'text');
            posicaoAtletaInput.setAttribute('id', `posicaoAtleta${atletaCount}`);
            posicaoAtletaInput.classList.add('w-full', 'p-2', 'border', 'rounded');
            posicaoAtletaInput.setAttribute('placeholder', 'Posição em Quadra');
            posicaoAtletaDiv.appendChild(posicaoAtletaLabel);
            posicaoAtletaDiv.appendChild(posicaoAtletaInput);

            atletasContainer.appendChild(nomeAtletaDiv);
            atletasContainer.appendChild(numeroAtletaDiv);
            atletasContainer.appendChild(posicaoAtletaDiv);
        });

        document.getElementById('atletasForm').addEventListener('submit', function(event) {
            event.preventDefault();

            const time = document.getElementById('time').value;
            const set = document.getElementById('set').value;
            const atletas = [];
            const atletasContainer = document.getElementById('atletasContainer');
            const atletaCount = atletasContainer.children.length / 3;

            for (let i = 1; i <= atletaCount; i++) {
                const nome = document.getElementById(`nomeAtleta${i}`).value;
                const numero = document.getElementById(`numeroAtleta${i}`).value;
                const posicao = document.getElementById(`posicaoAtleta${i}`).value;
                atletas.push({ nome, numero, posicao });
            }

            const data = {
                time,
                set,
                atletas,
                data: new Date().toLocaleString()
            };

            fetch('https://your-server-endpoint.com/send-email', {
                method: 'POST',
                headers: {
                    'Content-Type': 'application/json'
                },
                body: JSON.stringify(data)
            })
            .then(response => response.json())
            .then(data => {
                alert('Obrigado pelo registro, o set começará em breve.');
            })
            .catch(error => {
                console.error('Erro ao enviar os dados:', error);
            });
        });
    </script>
</body>
</html>
