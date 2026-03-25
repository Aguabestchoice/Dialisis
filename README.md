<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Semanario de Nefrología: Compendio de Diálisis</title>
    <style>
        :root {
            --renal-blue: #1a5276;
            --soft-blue: #eaf2f8;
            --white: #ffffff;
            --text: #2c3e50;
            --accent: #d4ac0d;
        }

        body {
            font-family: 'Segoe UI', Arial, sans-serif;
            line-height: 1.6;
            color: var(--text);
            background-color: #f4f6f7;
            margin: 0;
            padding: 0;
        }

        header {
            background-color: var(--renal-blue);
            color: var(--white);
            padding: 40px 20px;
            text-align: center;
            border-bottom: 4px solid var(--accent);
        }

        .module {
            max-width: 900px;
            margin: 30px auto;
            background: var(--white);
            padding: 40px;
            border-radius: 5px;
            box-shadow: 0 4px 15px rgba(0,0,0,0.1);
        }

        h2 {
            color: var(--renal-blue);
            border-bottom: 2px solid var(--soft-blue);
            padding-bottom: 10px;
            margin-top: 0;
        }

        h3 {
            color: #2980b9;
        }

        ul {
            padding-left: 20px;
        }

        li {
            margin-bottom: 10px;
        }

        .quiz-section {
            background: var(--soft-blue);
            padding: 30px;
            border-radius: 8px;
        }

        .quiz-card {
            background: white;
            padding: 20px;
            margin-bottom: 20px;
            border-left: 5px solid var(--renal-blue);
            border-radius: 4px;
        }

        .btn {
            background: var(--renal-blue);
            color: white;
            padding: 15px 30px;
            border: none;
            border-radius: 4px;
            cursor: pointer;
            font-weight: bold;
            width: 100%;
            font-size: 1rem;
        }

        #results {
            margin-top: 20px;
            padding: 20px;
            display: none;
            border-radius: 4px;
        }

        .ref-section {
            font-size: 0.9rem;
            color: #566573;
        }

        .ref-section a {
            color: var(--renal-blue);
            text-decoration: none;
        }
    </style>
</head>
<body>

<header>
    <h1>Síntesis Técnica: Diálisis y Terapias Extracorpóreas</h1>
    <p>Nivel: Estudiante a Alta Especialidad</p>
</header>

<div class="module">
    <h2>1. Bases Biofísicas y Fisiología del Transporte</h2>
    <p>El principio fundamental es el movimiento a través de una membrana semipermeable:</p>
    <ul>
        <li><strong>Difusión:</strong> Movimiento a favor de gradiente de concentración. Elimina toxinas de bajo peso (urea, creatinina).</li>
        <li><strong>Convección (Ultrafiltración):</strong> Paso de solvente y solutos mediante gradiente de presión hidrostática. Clave para moléculas medias (β₂-microglobulina).</li>
        <li><strong>Adsorción:</strong> Adhesión de proteínas y toxinas a la superficie de la membrana.</li>
    </ul>
    
</div>

<div class="module">
    <h2>2. Hemodiálisis (HD): Acceso, Cinética y Complicaciones</h2>
    <h3>2.1 Acceso Vascular</h3>
    <ul>
        <li><strong>Fístula Arteriovenosa (FAV):</strong> Estándar de oro (radial-cefálica). Maduración: 6-8 semanas.</li>
        <li><strong>Injerto Protésico:</strong> Uso de PTFE.</li>
        <li><strong>Catéter Venoso Central (CVC):</strong> Tunelizados/no tunelizados. Riesgo: bacteriemia y estenosis.</li>
    </ul>
    
    <h3>2.2 Prescripción y Adecuación</h3>
    <p>Se mide mediante Kt/V (K: aclaramiento, t: tiempo, V: volumen de distribución). Objetivo estándar: <strong>≥ 1.2</strong> por sesión.</p>
</div>

<div class="module">
    <h2>3. Diálisis Peritoneal (DP): La Membrana Biológica</h2>
    <p>Clasificación según PET (Prueba de Equilibrio Peritoneal): rápidos, promedio y lentos.</p>
    <ul>
        <li><strong>DPCA:</strong> Intercambios manuales.</li>
        <li><strong>DPA:</strong> Cicladora nocturna.</li>
        <li><strong>Peritonitis infecciosa:</strong> Diagnóstico >100 leucocitos/µL y >50% polimorfonucleares.</li>
    </ul>
</div>

<div class="module">
    <h2>4. Terapias de Reemplazo Renal Continuo (TRRC)</h2>
    <p>Exclusivas de UCI para inestabilidad hemodinámica:</p>
    <ul>
        <li><strong>CVVH:</strong> Predomina la convección.</li>
        <li><strong>CVVHD:</strong> Predomina la difusión.</li>
        <li><strong>CVVHDF:</strong> Combinación de ambos mecanismos.</li>
    </ul>
</div>

<div class="module">
    <h2>5. Fronteras de la Subespecialidad</h2>
    <ul>
        <li><strong>HDF-OL:</strong> Hemodiafiltración de alto volumen. Reduce mortalidad cardiovascular.</li>
        <li><strong>Innovación:</strong> Riñón artificial portátil y regeneración de dializado con sorbentes (óxido de zirconio).</li>
    </ul>
</div>

<div class="module quiz-section">
    <h2>Examen de Evaluación (15 Reactivos)</h2>
    <div id="quiz-content"></div>
    <button class="btn" onclick="checkQuiz()">Calificar Examen</button>
    <div id="results"></div>
</div>

<div class="module ref-section">
    <h2>Referencias Bibliográficas (APA 7ma Edición)</h2>
    <ul>
        <li>Daugirdas, J. T., Blake, P. G., & Ing, T. S. (2015). <i>Manual de diálisis</i> (5ta ed.). Wolters Kluwer. <a href="https://www.wolterskluwer.com/es-es/solutions/lippincott/manual-de-dialisis" target="_blank">Enlace</a></li>
        <li>Himmelfarb, J., & Sayegh, M. H. (2019). <i>Chronic Kidney Disease, Dialysis, and Transplantation</i> (4th ed.). Elsevier. <a href="https://www.elsevier.com/books/chronic-kidney-disease-dialysis-and-transplantation/himmelfarb/978-0-323-52978-5" target="_blank">Enlace</a></li>
        <li>Kovesdy, C. P. (2022). Epidemiology of chronic kidney disease: an update 2022. <i>Kidney International Supplements</i>. <a href="https://doi.org/10.1016/j.kisu.2021.11.003" target="_blank">Enlace</a></li>
        <li>Levy, J., Brown, E., & Lawrence, A. (2016). <i>Oxford Handbook of Dialysis</i> (4th ed.). <a href="https://academic.oup.com/book/26233" target="_blank">Enlace</a></li>
        <li>Ronco, C., Bellomo, R., & Kellum, J. A. (2018). <i>Critical Care Nephrology</i> (3rd ed.). <a href="https://www.elsevier.com/books/critical-care-nephrology/ronco/978-0-323-44942-7" target="_blank">Enlace</a></li>
    </ul>
</div>

<script>
    const quizData = [
        { q: "¿Qué mecanismo elimina principalmente urea y creatinina?", a: ["Difusión", "Convección", "Adsorción"], c: 0 },
        { q: "La eliminación de β₂-microglobulina depende primordialmente de:", a: ["Difusión", "Convección", "Ósmosis"], c: 1 },
        { q: "Estándar de oro para acceso vascular en hemodiálisis:", a: ["Injerto PTFE", "Catéter tunelizado", "Fístula Arteriovenosa"], c: 2 },
        { q: "¿Cuánto tiempo de maduración requiere una FAV?", a: ["1-2 semanas", "6-8 semanas", "3 meses"], c: 1 },
        { q: "Material utilizado en injertos protésicos:", a: ["Silicona", "Óxido de zirconio", "PTFE"], c: 2 },
        { q: "Riesgo principal asociado al uso de Catéter Venoso Central:", a: ["Estenosis venosa y bacteriemia", "Maduración lenta", "Pérdida de convección"], c: 0 },
        { q: "En la fórmula Kt/V, ¿qué representa la 'V'?", a: ["Velocidad de flujo", "Volumen de distribución", "Variación de urea"], c: 1 },
        { q: "Objetivo estándar de Kt/V por sesión:", a: ["≥ 0.8", "≥ 1.0", "≥ 1.2"], c: 2 },
        { q: "La Prueba de Equilibrio Peritoneal (PET) clasifica a los pacientes según:", a: ["Tasa de transporte", "Riesgo de infección", "Volumen de urea"], c: 0 },
        { q: "Tipo de diálisis peritoneal que usa cicladora nocturna:", a: ["DPCA", "DPA", "HDF-OL"], c: 1 },
        { q: "Criterio diagnóstico de peritonitis (leucocitos en efluente):", a: [">10 cel/µL", ">100 cel/µL", ">500 cel/µL"], c: 1 },
        { q: "Técnica de TRRC donde predomina la difusión:", a: ["CVVH", "CVVHD", "CVVHDF"], c: 1 },
        { q: "La CVVHDF se caracteriza por:", a: ["Solo difusión", "Solo convección", "Combinar ambos mecanismos"], c: 2 },
        { q: "Ventaja demostrada de la HDF-OL de alto volumen:", a: ["Reducción de mortalidad CV", "Menor costo", "Evita el acceso vascular"], c: 0 },
        { q: "Sustancia investigada para la regeneración del dializado:", a: ["PTFE", "Beta-2 microglobulina", "Óxido de zirconio"], c: 2 }
    ];

    const quizContent = document.getElementById('quiz-content');
    quizData.forEach((item, i) => {
        quizContent.innerHTML += `
            <div class="quiz-card">
                <p><strong>${i+1}. ${item.q}</strong></p>
                ${item.a.map((opt, idx) => `
                    <label style="display:block; margin:5px 0;">
                        <input type="radio" name="q${i}" value="${idx}"> ${opt}
                    </label>
                `).join('')}
            </div>
        `;
    });

    function checkQuiz() {
        let score = 0;
        let missed = [];
        quizData.forEach((item, i) => {
            const sel = document.querySelector(`input[name="q${i}"]:checked`);
            if(sel && parseInt(sel.value) === item.c) score++;
            else missed.push(i+1);
        });

        const res = document.getElementById('results');
        res.style.display = 'block';
        res.style.backgroundColor = score >= 12 ? "#d4efdf" : "#f9ebea";
        res.innerHTML = `
            <h3>Resultado: ${score}/15</h3>
            <p><strong>Fallos en reactivos:</strong> ${missed.length ? missed.join(', ') : 'Ninguno'}</p>
            <p><strong>Fortalezas:</strong> ${score >= 12 ? 'Dominio sólido de los bloques técnicos.' : 'Conocimiento de bases generales.'}</p>
            <p><strong>Oportunidades:</strong> ${score < 15 ? 'Repasar detalles sobre accesos vasculares y tipos de TRRC.' : 'Nivel de excelencia alcanzado.'}</p>
        `;
    }
</script>

</body>
</html>
