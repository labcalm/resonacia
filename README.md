# Resonancia Somática | Laboratorio de Calma

Intervención digital interactiva de código abierto (**210 segundos**) diseñada para la desescalada de picos agudos de ansiedad, hiperactivación autonómica y rumiación verbal mediante mecanismos psicofisiológicos *bottom-up* y carga ejecutiva visoespacial controlada.

🔗 **Demo en vivo:** archivo.labcalm.lat
🧠 **Autor:** Psic. Héctor López ([Laboratorio de Calma](https://labcalm.lat))

\---

## Fundamento Neurobiológico y Clínico

Cuando un individuo atraviesa un pico de ansiedad aguda, la hiperreactividad de la amígdala basolateral y la liberación de catecolaminas comprometen funcionalmente la corteza prefrontal dorsolateral (dlPFC) y ventromedial (vmPFC), haciendo que las intervenciones puramente verbales (*top-down*) fracasen al inicio.

Este micro-juego opera en 4 fases cronometradas para restaurar el tono vagal y la receptividad cognitiva sin requerir esfuerzo analítico inicial:

1. **Fase 1 (`00:00 – 00:36` · Descarga Vagal Aguda):** 3 ciclos de *Suspiro Fisiológico* (3.5s inhalación primaria + 1.5s inhalación secundaria de reapertura alveolar + 7.0s exhalación prolongada) acoplados a tensión isométrica suave (*Hold \& Release*), activando el reflejo de alivio del complejo pre-Bötzinger.
2. **Fase 2 (`00:36 – 01:30` · Arrastre Cardiorrespiratorio y Seguimiento Bilateral):** Rampa adaptativa de desaceleración progresiva (de 6.5s a 10.0s por ciclo) para evitar hambre de aire (*air hunger*) e hipocapnia, combinada con oscilación horizontal a **0.60 Hz** (seguimiento ocular suave / estimulación del colículo superior).
3. **Fase 3 (`01:30 – 03:00` · Flujo Visoespacial *Zero-Fail* a 0.10 Hz):** Sincronización barorrefleja a frecuencia de resonancia cardiovascular (**0.10 Hz** / 6 respiraciones por minuto: 4s inhalación, 6s exhalación) mientras se manipulan **3 nodos rotacionales simultáneos** (Límite de Cowan) a 0.78 rad/s. Recluta la dlPFC derecha para bloquear el bucle fonológico rumiativo sin inducir Negatividad Relacionada con el Error (ERN) en el córtex cingulado anterior dorsal (dACC).
4. **Fase 4 (`03:00 – 03:30` · Ventana de Receptividad JITAI y Defusión ACT):** Aprovecha la restauración del acoplamiento vmPFC-amígdala tras 180 segundos para presentar una micro-cápsula diegética de defusión cognitiva que se disuelve físicamente durante la exhalación.

## Arquitectura Técnica y Psicoacústica (`Web Audio API` + `Canvas 2D`)

* **Cero dependencias externas / Local-First:** Monolito en HTML5, CSS y Vanilla JS (< 30 KB). Sin rastreadores, sin telemetría y sin archivos de audio externos pesados.
* **Síntesis de Ruido Marrón ($1/f^2$):** Integración estocástica en tiempo real (-6 dB/octava) con filtrado de paso bajo dinámico (`BiquadFilterNode`, $f\_c = 240\\text{–}680\\text{ Hz}$, $Q = 0.707$).
* **Prevención del Reflejo de Sobresalto Acústico (ASR):** Todas las envolventes ADSR respetan tiempos de ataque $\\ge 250\\text{ ms}$ en notas pentatónicas interactivas y $2000\\text{ ms}$ en el bordón grave ($C\_2 = 65.41\\text{ Hz}$, $G\_2 = 98.00\\text{ Hz}$).
* **Física Amortiguada Anti-Brusquedad:** El puntero opera bajo un oscilador armónico amortiguado ($\\zeta \\approx 0.82$, fricción $0.89$ a 60 FPS). Movimientos erráticos ($> 550\\text{ px/s}$) atenúan suavemente el filtro acústico hacia 220 Hz, moldeando la desaceleración motora por retroalimentación somática.

## Uso Local

Clona este repositorio o descarga `index.html` y ábrelo directamente en cualquier navegador moderno.

