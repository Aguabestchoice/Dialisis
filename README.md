<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Masterclass en Diálisis</title>
    <link href="https://fonts.googleapis.com/css2?family=Segoe+UI:wght@300;400;600;700&display=swap" rel="stylesheet">
    <style>
        :root {
            --renal-blue: #004a99;
            --clinical-white: #ffffff;
            --soft-grey: #f4f7f6;
            --border-color: #d1d9e6;
            --accent-red: #b00020;
            --success-green: #2e7d32;
        }

        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            line-height: 1.6;
            color: #333;
            background-color: var(--soft-grey);
            margin: 0;
            padding: 0;
        }

        header {
            background-color: var(--renal-blue);
            color: white;
            padding: 2rem 1rem;
            text-align: center;
            border-bottom: 5px solid #003366;
        }

        nav {
            background: #fff;
            padding: 10px;
            position: sticky;
            top: 0;
            display: flex;
            justify-content: center;
            gap: 20px;
            box-shadow: 0 2px 5px rgba(0,0,0,0.1);
            z-index: 1000;
        }

        nav a {
            text-decoration: none;
            color: var(--renal-blue);
            font-weight: 600;
            font-size: 0.9rem;
        }

        .container {
            max-width: 900px;
            margin: 20px auto;
            background: white;
            padding: 40px;
            box-shadow: 0 4px 15px rgba(0,0,0,0.05);
            border-radius: 8px;
        }

        h2 {
            color: var(--renal-blue);
            border-left: 5px solid var(--renal-blue);
            padding-left: 15px;
            margin-top: 40px;
        }

        .formula-box {
            background: #eef2f7;
            padding: 20px;
            border-radius: 5px;
            font-family: "Courier New", Courier, monospace;
            border: 1px solid var(--border-color);
            margin: 20px 0;
        }

        .quiz-container {
            background: #fff;
            border: 2px solid var(--renal-blue);
            padding: 25px;
            border-radius: 10px;
            margin-top: 50px;
        }

        .question {
            margin-bottom: 25px;
            padding-bottom: 15px;
            border-bottom: 1px dotted #ccc;
        }

        .options label {
            display: block;
            margin: 10px 0;
            padding: 10px;
            background: #f9f9f9;
            border-radius: 5px;
            cursor: pointer;
            transition: 0.3s;
        }

        .options label:hover {
            background: #f0f4f8;
        }

        button {
            background: var(--renal-blue);
            color: white;
            border: none;
            padding: 15px 30px;
            border-radius: 5px;
            cursor: pointer;
            font-size: 1rem;
            font-weight: bold;
        }

        #resultArea {
            margin-top: 20px;
            display: none;
            padding: 20px;
            border-radius: 5px;
        }

        footer {
            text-align: center;
            padding: 20px;
            font-size: 0.8rem;
            color: #777;
        }
    </style>
</head>
<body>

<header>
    <h1>Compendio de terapias de reemplazo renal</h1>
    <p>Nivel: Grado médico a subespecialidad en Nefrología</p>
</header>

<nav>
    <a href="#teoria">Fundamentos</a>
    <a href="#hemodialisis">Hemodiálisis</a>
    <a href="#peritoneal">Diálisis peritoneal</a>
    <a href="#examen">Autoevaluación</a>
</nav>

<div class="container">
    <section id="teoria">
        <h2>1. Fisiología y biofísica</h2>
        <p>La diálisis se rige por leyes físicas de transferencia de masa. La eficacia depende de la permeabilidad de la membrana (coeficiente KoA) y el gradiente de presión.</p>
        <ul>
            <li><strong>Difusión:</strong> Eliminación de moléculas pequeñas (Urea: 60 Da).</li>
            <li><strong>Convección:</strong> Eliminación de moléculas medias (β2-m: 11,800 Da).</li>
        </ul>
        <div class="formula-box">
            Dosis de Diálisis (Kt/V):<br>
            Donde K = Aclaramiento, t = tiempo, V = Volumen de distribución (Agua corporal total).
        </div>
    </section>

    <section id="hemodialisis">
        <h2>2. Hemodiálisis y HDF-OL</h2>
        <p>La Hemodiafiltración en línea (HDF-OL) combina difusión y convección masiva mediante el uso de agua ultrapura como líquido de sustitución.</p>
        <p><strong>Acceso Vascular:</strong> El estándar es la FAV nativa (Regla de los 6 para maduración: 6mm de diámetro, 6mm de profundidad, flujo >600ml/min).</p>
    </section>

    <section id="peritoneal">
        <h2>3. Diálisis Peritoneal (DP)</h2>
        <p>Basada en la membrana peritoneal. El transporte se define por el <strong>PET (Peritoneal Equilibrium Test)</strong>.</p>
        <ul>
            <li><strong>Transportadores Rápidos:</strong> Pierden ultrafiltración rápido (usar ciclos cortos).</li>
            <li><strong>Transportadores Lentos:</strong> Aclaran urea lento (usar permanencias largas).</li>
        </ul>
    </section>

    <section id="examen" class="quiz-container">
        <h2>Examen de Certificación Médica</h2>
        <div id="quizContent">
            <div class="question">
                <p><strong>1. ¿Qué mecanismo es superior para aclarar moléculas de 12,000 Daltons en diálisis?</strong></p>
                <div class="options">
                    <label><input type="radio" name="p1" value="0"> Difusión pasiva</label>
                    <label><input type="radio" name="p1" value="1"> Convección (Arrastre de solvente)</label>
                    <label><input type="radio" name="p1" value="0"> Adsorción proteica</label>
                </div>
            </div>

            <div class="question">
                <p><strong>2. ¿Por qué ocurre el edema cerebral en el Síndrome de Desequilibrio?</strong></p>
                <div class="options">
                    <label><input type="radio" name="p2" value="1"> Gradiente osmótico inverso por urea atrapada en el SNC</label>
                    <label><input type="radio" name="p2" value="0"> Hipernatremia post-diálisis</label>
                    <label><input type="radio" name="p2" value="0"> Hipotensión súbita durante la ultrafiltración</label>
                </div>
            </div>

            <div class="question">
                <p><strong>3. En un paciente "Transportador Rápido" en DP, ¿qué sucede con la glucosa?</strong></p>
                <div class="options">
                    <label><input type="radio" name="p3" value="0"> Se mantiene en la cavidad por más de 12 horas</label>
                    <label><input type="radio" name="p3" value="0"> No atraviesa la membrana peritoneal</label>
                    <label><input type="radio" name="p3" value="1"> Se absorbe rápidamente hacia la sangre, perdiendo poder osmótico</label>
                </div>
            </div>
        </div>

        <button onclick="checkQuiz()">Calificar Examen</button>

        <div id="resultArea"></div>
    </section>
</div>

<footer>
    <p>Basado en guías KDIGO y KDOQI 2026. Formato APA 7ma edición.</p>
</footer>

<script>
    function checkQuiz() {
        let score = 0;
        let total = 3;
        const q1 = document.querySelector('input[name="p1"]:checked');
        const q2 = document.querySelector('input[name="p2"]:checked');
        const q3 = document.querySelector('input[name="p3"]:checked');

        if (!q1 || !q2 || !q3) {
            alert("Por favor, responde todas las preguntas del examen.");
            return;
        }

        score = parseInt(q1.value) + parseInt(q2.value) + parseInt(q3.value);
        
        const resultArea = document.getElementById('resultArea');
        resultArea.style.display = 'block';
        
        let feedback = "";
        if(score === 3) {
            resultArea.style.backgroundColor = "#e8f5e9";
            feedback = "<strong>Fortaleza:</strong> Dominio excelente
