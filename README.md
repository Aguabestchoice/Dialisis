<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Plataforma de alta especialidad en Nefrología</title>
    <style>
        :root {
            --renal-dark: #0a2e52;
            --renal-blue: #1b4f72;
            --renal-light: #d4e6f1;
            --accent: #b9944d;
            --white: #ffffff;
            --text: #1c2833;
            --success: #27ae60;
            --error: #c0392b;
        }

        body {
            font-family: 'Helvetica Neue', Arial, sans-serif;
            line-height: 1.6;
            color: var(--text);
            background-color: #f2f4f4;
            margin: 0;
            padding: 0;
        }

        header {
            background: linear-gradient(135deg, var(--renal-dark), var(--renal-blue));
            color: var(--white);
            padding: 40px 20px;
            text-align: center;
            border-bottom: 4px solid var(--accent);
        }

        .main-nav {
            background: var(--white);
            padding: 15px;
            position: sticky;
            top: 0;
            display: flex;
            justify-content: center;
            gap: 25px;
            box-shadow: 0 2px 10px rgba(0,0,0,0.1);
            z-index: 1000;
        }

        .main-nav a {
            text-decoration: none;
            color: var(--renal-blue);
            font-weight: bold;
            font-size: 0.9rem;
            text-transform: uppercase;
        }

        .container {
            max-width: 1100px;
            margin: 30px auto;
            background: var(--white);
            padding: 50px;
            border-radius: 8px;
            box-shadow: 0 4px 20px rgba(0,0,0,0.08);
        }

        h2 {
            color: var(--renal-dark);
            border-left: 6px solid var(--accent);
            padding-left: 15px;
            margin-top: 45px;
            text-transform: uppercase;
        }

        .calc-box {
            background: var(--renal-light);
            padding: 25px;
            border-radius: 12px;
            margin: 30px 0;
            border: 1px solid #aed6f1;
        }

        .calc-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 20px;
        }

        input, select {
            width: 100%;
            padding: 10px;
            margin-top: 5px;
            border: 1px solid #ccc;
            border-radius: 4px;
        }

        .btn {
            background: var(--renal-dark);
            color: white;
            padding: 12px 25px;
            border: none;
            border-radius: 5px;
            cursor: pointer;
            font-weight: bold;
            transition: 0.3s;
            margin-top: 15px;
        }

        .btn:hover { background: var(--renal-blue); }

        .theory-grid {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 30px;
            margin-top: 20px;
        }

        @media (max-width: 768px) { .theory-grid { grid-template-columns: 1fr; } }

        .quiz-card {
            background: #fdfefe;
            border: 1px solid #ebedef;
            padding: 20px;
            margin-bottom: 20px;
            border-radius: 8px;
        }

        #quiz-results {
            display: none;
            padding: 30px;
            margin-top: 30px;
            border-radius: 8px;
        }

        footer {
            background: var(--renal-dark);
            color: white;
            text-align: center;
            padding: 30px;
            margin-top: 50px;
        }
    </style>
</head>
<body>

<header>
    <h1>SISTEMA INTEGRAL DE NEFROLOGÍA</h1>
    <p>Módulo de diálisis y terapias extracorpóreas avanzadas</p>
</header>

<nav class="main-nav">
    <a href="#fisiologia">Fisiología</a>
    <a href="#calculadora">Calculadora Kt/V</a>
    <a href="#hemodialisis">HD & HDF</a>
    <a href="#peritoneal">DP</a>
    <a href="#examen">Certificación</a>
</nav>

<div class="container">
    
    <section id="fisiologia">
        <h2>I. Dinámica de Solutos y Membranas</h2>
        <div class="theory-grid">
            <div>
                <h3>1.1 Coeficiente KoA</h3>
                <p>El KoA (Productivity de transferencia de masa) define la eficiencia del dializador para la urea. Valores >700 mL/min se consideran de alta eficiencia.</p>
                <ul>
                    <li><strong>Bajo Flujo:</strong> KUF < 15 ml/h/mmHg</li>
                    <li><strong>Alto Flujo:</strong> KUF > 20 ml/h/mmHg</li>
                </ul>
            </div>
            <div>
                <h3>1.2 El Modelo de Tres Poros</h3>
                <p>En Diálisis Peritoneal, el transporte ocurre a través del endotelio capilar peritoneal mediante:</p>
                <ul>
                    <li><strong>Acuaporinas:</strong> Solo agua (transcelular).</li>
                    <li><strong>Poros Pequeños:</strong> Agua y solutos pequeños (difusión).</li>
                    <li><strong>Poros Grandes:</strong> Proteínas y macromoléculas.</li>
                </ul>
            </div>
        </div>
    </section>

    <section id="calculadora" class="calc-box">
        <h2>II. Calculadora de Adecuación (Daugirdas II)</h2>
        <div class="calc-grid">
            <div>
                <label>Urea Pre-Diálisis (mg/dL)</label>
                <input type="number" id="preUrea" value="150">
            </div>
            <div>
                <label>Urea Post-Diálisis (mg/dL)</label>
                <input type="number" id="postUrea" value="45">
            </div>
            <div>
                <label>Horas de Sesión (h)</label>
                <input type="number" id="timeH" value="4">
            </div>
            <div>
                <label>Peso Post-Sesión (kg)</label>
                <input type="number" id="weight" value="70">
            </div>
            <div>
                <label>Ultrafiltración (L)</label>
                <input type="number" id="uf" value="2.5">
            </div>
        </div>
        <button class="btn" onclick="calculateKTV()">Calcular Kt/V Single-Pool</button>
        <div id="ktvResult" style="margin-top:15px; font-weight:bold; font-size:1.2rem; color:var(--renal-dark);"></div>
    </section>

    <section id="hemodialisis">
        <h2>III. Prescripción en HD y HDF-OL</h2>
        <p>La <strong>Hemodiafiltración en Línea (HDF-OL)</strong> representa la frontera actual. El aclaramiento total (K) es la suma de la difusión y la convección ($K_{total} = K_{diff} + K_{conv}$).</p>
        <div style="background:#e8f8f5; padding:15px; border-left:5px solid #1abc9c;">
            <strong>Evidencia ESHOL:</strong> Se requiere un volumen de sustitución >23 L/sesión para demostrar reducción en mortalidad por todas las causas.
        </div>
    </section>

    <section id="examen">
        <h2>IV. Examen de Certificación (15 Reactivos)</h2>
        <div id="quiz-area"></div>
        <button class="btn" style="width:100%;" onclick="evaluateQuiz()">Finalizar Examen y Ver Retroalimentación</button>
        <div id="quiz-results"></div>
    </section>

</div>

<footer>
    <p>© 2026 CORTEX-200. Referencias: Guías KDIGO 2024, KDOQI 2025, ISPD 2026.</p>
</footer>

<script>
    // Lógica de la Calculadora
    function calculateKTV() {
        const pre = parseFloat(document.getElementById('preUrea').value);
        const post = parseFloat(document.getElementById('postUrea').value);
        const t = parseFloat(document.getElementById('timeH').value);
        const w = parseFloat(document.getElementById('weight').value);
        const uf = parseFloat(document.getElementById('uf').value);

        const R = post / pre;
        // Fórmula de Daugirdas II: Kt/V = -ln(R - 0.008*t) + (4 - 3.5*R) * (UF/W)
        const ktv = -Math.log(R - (0.008 * t)) + (4 - (3.5 * R)) * (uf / w);
        
        const status = ktv >= 1.2 ? "ADECUADO" : "SUB-ÓPTIMO";
        document.getElementById('ktvResult').innerHTML = `Kt/V Estimado: ${ktv.toFixed(2)} (${status})`;
    }

    // Lógica del Examen
    const questions = [
        { q: "¿Cuál es el cofactor necesario para que el Citrato actúe como anticoagulante?", a: ["Magnesio", "Calcio", "Vitamina K"], c: 1 },
        { q: "El fenómeno de 'Cribado de Sodio' se evidencia por:", a: ["Hipernatremia", "Hiponatremia en el efluente inicial", "Acidosis metabólica"], c: 1 },
        { q: "En HDF-OL, ¿qué parámetro limita el volumen de sustitución?", a: ["Flujo de dializado", "Hemoconcentración (Fracción de Filtración)", "Presión arterial media"], c: 1 },
        { q: "¿Qué complicación se asocia a la pérdida de biocompatibilidad en membranas de celulosa?", a: ["Leucopenia precoz", "Hiperpotasemia", "Hiperglucemia"], c: 0 },
        { q: "Un transporte peritoneal 'Rápido' se asocia a:", a: ["Alta ultrafiltración", "Baja ultrafiltración por absorción de glucosa", "Bajo aclaramiento de urea"], c: 1 },
        { q: "El modelo cinético de urea postula que 'V' es equivalente a:", a: ["Volumen plasmático", "Agua Corporal Total", "Espacio extracelular"], c: 1 },
        { q: "La principal ventaja de la Icodextrina es su transporte vía:", a: ["Poros pequeños", "Difusión facilitada", "Presión coloidosmótica (Intercambios largos)"], c: 2 },
        { q: "Meta de Hemoglobina en ERC G5D según KDIGO:", a: ["12-14 g/dL", "10-11.5 g/dL", ">13 g/dL"], c: 1 },
        { q: "Indicación absoluta de inicio de diálisis de urgencia:", a: ["Creatinina > 10", "Pericarditis urémica", "Anemia grado IV"], c: 1 },
        { q: "El aclaramiento de moléculas medias (>10,000 Da) es nulo en:", a: ["Hemodiálisis de bajo flujo", "Hemodiafiltración", "Diálisis Peritoneal"], c: 0 },
        { q: "En la TRRC, la pre-dilución ayuda a:", a: ["Aumentar la urea", "Disminuir la coagulación del filtro", "Eliminar potasio más rápido"], c: 1 },
        { q: "¿Qué mide el PET (Prueba de Equilibrio Peritoneal)?", a: ["Función renal residual", "Permeabilidad de la membrana peritoneal", "Gasto cardíaco"], c: 1 },
        { q: "Causa más frecuente de peritonitis en DP:", a: ["S. epidermidis / S. aureus", "E. coli", "Cándida"], c: 0 },
        { q: "El 'Rebote de Urea' se debe a:", a: ["Falla del dializador", "Cinética multicompartimental", "Ingesta excesiva de proteínas"], c: 1 },
        { q: "La toxina urémica considerada prototipo de moléculas medias es:", a: ["Urea", "Creatinina", "B2-microglobulina"], c: 2 }
    ];

    const quizArea = document.getElementById('quiz-area');
    questions.forEach((item, index) => {
        quizArea.innerHTML += `
            <div class="quiz-card">
                <p><strong>${index + 1}. ${item.q}</strong></p>
                ${item.a.map((opt, i) => `
                    <label style="display:block; margin:5px 0;">
                        <input type="radio" name="q${index}" value="${i}"> ${opt}
                    </label>
                `).join('')}
            </div>
        `;
    });

    function evaluateQuiz() {
        let score = 0;
        let incorrectas = [];
        questions.forEach((item, index) => {
            const sel = document.querySelector(`input[name="q${index}"]:checked`);
            if(sel && parseInt(sel.value) === item.c) score++;
            else incorrectas.push(index + 1);
        });

        const res = document.getElementById('quiz-results');
        res.style.display = 'block';
        res.style.backgroundColor = score > 12 ? "#e8f8f5" : "#fdedec";
        res.innerHTML = `
            <h3>Calificación Final: ${score}/15 (${((score/15)*100).toFixed(1)}%)</h3>
            <p><strong>Preguntas fallidas:</strong> ${incorrectas.length ? incorrectas.join(', ') : 'Ninguna'}</p>
            <div style="margin-top:20px;">
                <strong>Retroalimentación:</strong><br>
                ${score > 12 ? 'Excelente. Estás listo para el examen de subespecialidad.' : 'Recomendamos repasar la biofísica de membranas y guías de adecuación.'}
            </div>
        `;
    }
</script>

</body>
</html>
