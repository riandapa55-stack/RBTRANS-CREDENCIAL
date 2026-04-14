[sitecompleto.txt](https://github.com/user-attachments/files/26719561/sitecompleto.txt)
<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <title>Credencial de Transporte</title>
    <style>
        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background: linear-gradient(135deg, #004e92, #000428);
            color: #fff;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            margin: 0;
        }
        .card {
            background: rgba(255, 255, 255, 0.1);
            backdrop-filter: blur(10px);
            border-radius: 15px;
            padding: 30px;
            width: 420px;
            box-shadow: 0 8px 20px rgba(0,0,0,0.5);
            animation: fadeIn 1.2s ease-in-out;
        }
        h2 {
            text-align: center;
            margin-bottom: 20px;
            font-size: 22px;
            letter-spacing: 2px;
            text-transform: uppercase;
            border-bottom: 2px solid #fff;
            padding-bottom: 10px;
        }
        .photo {
            width: 100px;
            height: 130px;
            border: 2px solid #fff;
            margin: 20px auto;
            background-color: #ccc;
            border-radius: 5px;
            overflow: hidden;
            display: flex;
            justify-content: center;
            align-items: center;
            color: #000;
            font-weight: bold;
        }
        .info {
            margin: 12px 0;
            font-size: 16px;
        }
        .info strong {
            color: #ffd700;
        }
        @keyframes fadeIn {
            from {opacity: 0; transform: translateY(-20px);}
            to {opacity: 1; transform: translateY(0);}
        }
    </style>
</head>
<body>
    <div class="card">
        <h2>CREDENCIAL DE TRANSPORTE</h2>
        
        <div class="photo" id="photo">
            Foto 3x4
        </div>
        
        <div class="info"><strong>Nome:</strong> <span id="nome"></span></div>
        <div class="info"><strong>CPF:</strong> <span id="cpf"></span></div>
        <div class="info"><strong>Placa:</strong> <span id="placa"></span></div>
        <div class="info"><strong>Situação Cadastral:</strong> <span id="situacao"></span></div>
        <div class="info"><strong>Data de Validade:</strong> <span id="validade"></span></div>
    </div>

    <script>
        // Dados da credencial
        const credencial = {
            nome: "Francisco Pereira de Rocha",
            cpf: "018.546.987-91",
            placa: "NZR9A58",
            situacao: "Regular",
            validade: "30/09/2027",
            foto: "https://via.placeholder.com/100x130" // substitua pelo link da foto real
        };

        // Preenche os campos automaticamente
        document.getElementById("nome").textContent = credencial.nome;
        document.getElementById("cpf").textContent = credencial.cpf;
        document.getElementById("placa").textContent = credencial.placa;
        document.getElementById("situacao").textContent = credencial.situacao;
        document.getElementById("validade").textContent = credencial.validade;

        // Adiciona a foto dinamicamente
        const fotoDiv = document.getElementById("photo");
        const img = document.createElement("img");
        img.src = credencial.foto;
        img.alt = "Foto do usuário";
        img.style.width = "100%";
        img.style.height = "100%";
        fotoDiv.innerHTML = "";
        fotoDiv.appendChild(img);
    </script>
</body>
</html>
