<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Tratado enciclopédico de Nefrología extracorpórea</title>
    <style>
        :root {
            --renal-dark: #001f3f;
            --renal-blue: #0074D9;
            --clinical-grey: #2c3e50;
            --gold-accent: #d4af37;
            --bg-light: #f4f7f6;
            --white: #ffffff;
        }

        body {
            font-family: 'Times New Roman', Times, serif; /* Estilo de libro de texto clásico */
            background-color: var(--bg-light);
            color: var(--clinical-grey);
            line-height: 1.8;
            margin: 0;
            padding: 0;
        }

        header {
            background: var(--renal-dark);
            color: var(--white);
            padding: 50px 20px;
            text-align: center;
            border-bottom: 5px solid var(--gold-accent);
        }

        .module {
            max-width: 1100px;
            margin: 40px auto;
            background: var(--white);
            padding: 40px;
            border-radius: 2px;
            box-shadow: 0 10px 30px rgba(0,0,0,0.1);
            border-top: 4px solid var(--renal-blue);
        }

        h2 {
            color: var(--renal-dark);
            text-transform: uppercase;
            letter-spacing: 2px;
            border-bottom: 1px solid #eee;
            padding-bottom: 15px;
            font-size: 1.8rem;
        }

        h3 {
            color: var(--renal-blue);
            margin-top: 30px;
            font-style: italic;
        }

        .formula-panel {
            background: #f8f9fa;
            border: 1px double var(--renal-blue);
            padding: 25px;
            margin: 20px 0;
            font-family: 'Courier New', Courier, monospace;
            font-size: 1.1rem;
        }

        .tech-detail {
            background: #eef2f7;
            padding: 20px;
            border-left: 5px solid var(--gold-accent);
            margin: 20px 0;
            font-size: 0.95rem;
        }

        table {
            width: 100%;
            border-collapse: collapse;
            margin: 25px 0;
        }

        th, td {
            border: 1px solid #ddd;
            padding: 15px;
            text-align: left;
        }

        th { background: var(--renal-dark); color: white; }

        .calc-section {
            background: #d4e6f1;
            padding: 30px;
            border-radius: 8px;
        }

        .btn-action {
            background: var(--renal-dark);
            color: white;
            padding: 15px 30px;
            border: none;
            cursor: pointer;
            font-weight: bold;
            width: 100%;
            margin-top: 20px;
        }

        #quiz-results {
            margin-top: 30px;
            padding: 20px;
            display: none;
            border: 2px solid var(--renal-blue);
        }
    </style>
</head>
<body>

<header>
    <h1>MASTERCLASS EN DIÁLISIS</h1>
    <p>Documentación técnica completa para residentes de Nefrología y Alta especialidad</p>
</header>

<div class="module">
    <h2>I. Bases biofísicas y termodinámica de membranas</h2>
    <p>El transporte de solutos en diálisis no es un evento azaroso, sino que responde a gradientes de energía potencial.</p>
    
    <h3>1.1 Difusión y Ley de Fick</h3>
    <p>El movimiento aleatorio de moléculas (Browniano) genera un flujo neto de solutos desde un compartimento de alta concentración a uno de baja.</p>
    <div class="formula-panel">
        J = -D * A * (dC / dx)<br>
        Donde:<br>
        J: Flujo de soluto.<br>
        D: Coeficiente de difusión (específico para cada soluto).<br>
        A: Superficie efectiva de la membrana.
    </div>

    <h3>1.2 Convección (Ultrafiltración)</h3>
    <p>Es el arrastre de solutos por el flujo de solvente (agua) mediante un gradiente de presión hidrostática o hidráulica. Es independiente del gradiente de concentración.</p>
    <div class="tech-detail">
        <strong>Coeficiente de Cribado (S):</strong> Determina qué tan "fácil" pasa un soluto con el agua. 
        S = 1 significa que el soluto pasa libremente; S = 0 significa que la membrana es impermeable al soluto.
    </div>

    <h3>1.3 Adsorción y Potencial Zeta</h3>
    <p>La interacción electroestática entre la membrana y las proteínas plasmáticas. Crucial en membranas de PMMA y AN69 para la remoción de citocinas proinflamatorias.</p>
</div>

<div class="module">
    <h2>II. Hemodiálisis y hemodiafiltración (HDF-OL)</h2>
    
    <h3>2.1 Cinética de la Urea: Modelo de Dos Compartimentos</h3>
    <p>La urea no se distribuye uniformemente de forma instantánea. Existe una resistencia al flujo de urea entre el líquido intracelular (LIC) y el líquido extracelular (LEC).</p>
    <div class="formula-panel">
        Kt/V eq = Kt/V sp * [1 - (0.6 / t)] + 0.03<br>
        (Ecuación de Tattersall para el Kt/V equilibrado)
    </div>

    <h3>2.2 Hemodiafiltración en Línea (HDF-OL)</h3>
    <p>Combina lo mejor de dos mundos. Se infunden grandes volúmenes de líquido ultrapuro (sustitución) para maximizar la convección.</p>
    <table>
        <tr>
            <th>Factor</th>
            <th>Impacto Clínico</th>
        </tr>
        <tr>
            <td>Volumen de Convección</td>
            <td>Meta >23 L por sesión para reducir mortalidad cardiovascular.</td>
        </tr>
        <tr>
            <td>Aclaramiento β2-m</td>
            <td>Reducción del riesgo de Amiloidosis asociada a diálisis.</td>
        </tr>
        <tr>
            <td>Estabilidad Hemodinámica</td>
            <td>Mejorada por el enfriamiento del dializado y balance de sodio.</td>
        </tr>
    </table>
</div>

<div class="module">
    <h2>III. Diálisis peritoneal: fisiología y adecuación</h2>
    
    <h3>3.1 El Modelo de los Tres Poros (Rippe)</h3>
    <p>El peritoneo actúa como una barrera compleja con tres tipos de canales:</p>
    <ul>
        <li><strong>Acuaporinas-1 (Ultraporos):</strong> Responsables del 50% de la ultrafiltración inicial bajo gradiente de glucosa.</li>
        <li><strong>Poros Pequeños:</strong> Intercambio de urea, creatinina y electrolitos.</li>
        <li><strong>Poros Grandes:</strong> Pérdida de proteínas (Albúmina e IgG).</li>
    </ul>

    <h3>3.2 Prueba de Equilibrio Peritoneal (PET)</h3>
    <p>Clasifica a los pacientes según la velocidad de transporte de creatinina (D/P) y glucosa (D/D0).</p>
    <div class="tech-detail">
        <strong>Transportador Rápido (D/P > 0.81):</strong> Requiere ciclos cortos (DPA) para evitar la absorción de glucosa y pérdida de UF.
    </div>
</div>

<div class="module calc-section">
    <h2>IV. Herramienta de cálculo: Kt/V de Daugirdas II</h2>
    <div style="display:grid; grid-template-columns: 1fr 1fr; gap:20px;">
        <input type="number" id="preU" placeholder="Urea Pre (mg/dL)">
        <input type="number" id="postU" placeholder="Urea Post (mg/dL)">
        <input type="number" id="time" placeholder="Tiempo (Horas)">
        <input type="number" id="weight" placeholder="Peso Post (kg)">
        <input type="number" id="uf" placeholder="Ultrafiltración (Litros)">
    </div>
    <button class="btn-action" onclick="calcKTV()">Ejecutar Algoritmo de Adecuación</button>
    <div id="ktvRes" style="margin-top:20px; font-weight:bold; font-size:1.5rem; text-align:center;"></div>
</div>

<div class="module">
    <h2>V. Evaluación (15 Reactivos)</h2>
    <div id="quiz-box"></div>
    <button class="btn-action" onclick="evalQuiz()">Finalizar y Generar Retroalimentación Técnica</button>
    <div id="quiz-results"></div>
</div>

<script>
    function calcKTV() {
        const Cpre = parseFloat(document.getElementById('preU').value);
        const Cpost = parseFloat(document.getElementById('postU').value);
        const t = parseFloat(document.getElementById('time').value);
        const w = parseFloat(document.getElementById('weight').value);
        const uf = parseFloat(document.getElementById('uf').value);

        if (!Cpre || !Cpost) return;

        const R = Cpost / Cpre;
        const ktv = -Math.log(R - 0.008 * t) + (4 - 3.5 * R) * (uf / w);
        
        document.getElementById('ktvRes').innerHTML = `Kt/V calculado: ${ktv.toFixed(2)}`;
    }

    const questions = [
        { q: "¿Cuál es el motor principal del aclaramiento de moléculas medias en HDF-OL?", a: ["Difusión", "Convección", "Adsorción"], c: 1 },
        { q: "En el PET, un cociente D/P de creatinina elevado indica:", a: ["Fibrosis peritoneal", "Membrana hiperpermeable", "Disfunción de acuaporinas"], c: 1 },
        { q: "El 'Cribado de Sodio' (Sodium Sieving) es mediado por:", a: ["Poros pequeños", "Acuaporinas-1", "Poros grandes"], c: 1 },
        { q: "Dosis mínima recomendada de Kt/V para HD 3 veces/semana:", a: ["1.0", "1.2", "1.4"], c: 1 },
        { q: "Complicación neurológica por corrección rápida de urea:", a: ["Mielinolisis", "Síndrome de Desequilibrio", "Encefalopatía de Wernicke"], c: 1 },
        { q: "¿Qué membrana es mejor para adsorción de citocinas?", a: ["Polisulfona", "PMMA", "Acetato de celulosa"], c: 1 },
        { q: "Factor de riesgo principal para Peritonitis Esclerosante:", a: ["S. Aureus", "Años en DP (>5-8 años)", "Uso de Heparina"], c: 1 },
        { q: "El rebote de urea post-diálisis ocurre típicamente a los:", a: ["10 min", "30-60 min", "4 horas"], c: 1 },
        { q: "¿Qué electrolito del dializado previene la inestabilidad hemodinámica?", a: ["Calcio alto", "Sodio (138-142 mEq/L)", "Potasio bajo"], c: 1 },
        { q: "La Icodextrina genera ultrafiltración por:", a: ["Ósmosis cristaloide", "Ósmosis coloide", "Presión hidrostática"], c: 1 },
        { q: "En TRRC, el 'Sieving Coefficient' de la Albúmina es cercano a:", a: ["1.0", "0.5", "0.0"], c: 2 },
        { q: "Meta de saturación de transferrina en pacientes en diálisis:", a: [">10%", ">20%", ">50%"], c: 1 },
        { q: "Anticoagulación de elección en TRRC con falla hepática:", a: ["Citrato", "Heparina sódica", "Argatroban"], c: 1 },
        { q: "Signo radiológico de catéter de DP migrado:", a: ["Punta en pelvis menor", "Punta en hipocondrio", "Presencia de fibrina"], c: 1 },
        { q: "La urea se distribuye en:", a: ["Espacio plasmático", "Agua Corporal Total", "Tejido adiposo"], c: 1 }
    ];

    const box = document.getElementById('quiz-box');
    questions.forEach((item, i) => {
        box.innerHTML += `<div style="margin-bottom:20px;"><strong>${i+1}. ${item.q}</strong><br>` + 
            item.a.map((opt, idx) => `<label><input type="radio" name="q${i}" value="${idx}"> ${opt}</label>`).join('<br>') + `</div>`;
    });

    function evalQuiz() {
        let score = 0;
        questions.forEach((item, i) => {
            const sel = document.querySelector(`input[name="q${i}"]:checked`);
            if(sel && parseInt(sel.value) === item.c) score++;
        });
        const res = document.getElementById('quiz-results');
        res.style.display = 'block';
        res.innerHTML = `<h3>Resultado: ${score}/15</h3><p>Áreas a reforzar: ${score < 12 ? 'Cinética de transporte y biocompatibilidad' : 'Ninguna, excelente nivel.'}</p>`;
    }
</script>

</body>
</html>
