<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="theme-color" content="#1a73e8">
    <title>Bastón Inteligente</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, sans-serif;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            min-height: 100vh;
            padding: 20px;
            color: #333;
        }

        .container {
            max-width: 600px;
            margin: 0 auto;
        }

        .card {
            background: white;
            border-radius: 20px;
            padding: 25px;
            margin-bottom: 20px;
            box-shadow: 0 10px 30px rgba(0,0,0,0.2);
        }

        h1 {
            color: #667eea;
            text-align: center;
            margin-bottom: 10px;
            font-size: 28px;
        }

        .subtitle {
            text-align: center;
            color: #666;
            margin-bottom: 20px;
            font-size: 14px;
        }

        .badge {
            display: inline-block;
            background: #10b981;
            color: white;
            padding: 5px 12px;
            border-radius: 20px;
            font-size: 11px;
            font-weight: 600;
            margin-left: 10px;
        }

        .status {
            padding: 15px;
            border-radius: 10px;
            text-align: center;
            font-weight: 600;
            margin-bottom: 20px;
            transition: all 0.3s;
        }

        .status.disconnected {
            background: #fee;
            color: #c33;
        }

        .status.connected {
            background: #efe;
            color: #3c3;
        }

        .status.searching {
            background: #fef3cd;
            color: #856404;
        }

        button {
            width: 100%;
            padding: 15px;
            border: none;
            border-radius: 10px;
            font-size: 16px;
            font-weight: 600;
            cursor: pointer;
            transition: all 0.3s;
            margin-bottom: 10px;
        }

        button:disabled {
            opacity: 0.5;
            cursor: not-allowed;
        }

        .btn-primary {
            background: #667eea;
            color: white;
        }

        .btn-primary:hover:not(:disabled) {
            background: #5568d3;
            transform: translateY(-2px);
            box-shadow: 0 5px 15px rgba(102, 126, 234, 0.4);
        }

        .btn-danger {
            background: #ef4444;
            color: white;
        }

        .btn-danger:hover:not(:disabled) {
            background: #dc2626;
        }

        .info-box {
            background: #f8f9fa;
            border-left: 4px solid #667eea;
            padding: 15px;
            border-radius: 5px;
            margin-bottom: 15px;
        }

        .info-box strong {
            color: #667eea;
            display: block;
            margin-bottom: 5px;
        }

        .log {
            background: #f8f9fa;
            border-radius: 10px;
            padding: 15px;
            max-height: 200px;
            overflow-y: auto;
            font-family: 'Courier New', monospace;
            font-size: 12px;
            line-height: 1.6;
        }

        .log-entry {
            margin-bottom: 5px;
            padding: 5px;
            border-radius: 3px;
        }

        .log-info {
            color: #0066cc;
        }

        .log-success {
            color: #22c55e;
            font-weight: 600;
        }

        .log-error {
            color: #ef4444;
            font-weight: 600;
        }

        .spinner {
            border: 3px solid #f3f3f3;
            border-top: 3px solid #667eea;
            border-radius: 50%;
            width: 30px;
            height: 30px;
            animation: spin 1s linear infinite;
            margin: 10px auto;
            display: none;
        }

        @keyframes spin {
            0% { transform: rotate(0deg); }
            100% { transform: rotate(360deg); }
        }

        .instructions {
            background: #e0f2fe;
            border-left: 4px solid #0ea5e9;
            padding: 15px;
            border-radius: 5px;
            margin-top: 20px;
            font-size: 14px;
            line-height: 1.6;
        }

        .icon {
            font-size: 40px;
            text-align: center;
            margin-bottom: 10px;
        }

        .route-info {
            background: #f0fdf4;
            border-left: 4px solid #10b981;
            padding: 15px;
            border-radius: 5px;
            margin-bottom: 15px;
            display: none;
        }

        .route-info .stat {
            display: inline-block;
            margin-right: 20px;
            font-size: 14px;
        }

        .route-info .stat strong {
            color: #10b981;
        }

        .progress-bar {
            background: #e5e7eb;
            border-radius: 10px;
            height: 8px;
            margin: 15px 0;
            overflow: hidden;
            display: none;
        }

        .progress-fill {
            background: linear-gradient(90deg, #10b981, #059669);
            height: 100%;
            width: 0%;
            transition: width 0.3s;
        }

        .hidden {
            display: none;
        }
    </style>
</head>
<body>
    <div class="container">
        <div class="card">
            <div class="icon">🦯</div>
            <h1>Bastón Inteligente <span class="badge">GRATIS</span></h1>
            <p class="subtitle">Navegación con OpenStreetMap - Sin límites ni costes</p>
            
            <div id="status" class="status disconnected">
                ❌ Desconectado
            </div>

            <button id="connectBtn" class="btn-primary">
                📡 Conectar al Bastón
            </button>

            <button id="disconnectBtn" class="btn-danger" style="display:none;">
                🔌 Desconectar
            </button>

            <div class="spinner" id="spinner"></div>

            <div id="destinationInfo" class="info-box" style="display:none;">
                <strong>📍 Destino detectado:</strong>
                <span id="destinationText">---</span>
            </div>

            <div id="routeInfo" class="route-info">
                <strong>🗺️ Información de la ruta</strong>
                <div style="margin-top: 10px;">
                    <div class="stat">📏 <strong id="routeDistance">---</strong></div>
                    <div class="stat">⏱️ <strong id="routeDuration">---</strong></div>
                </div>
            </div>

            <div class="progress-bar" id="progressBar">
                <div class="progress-fill" id="progressFill"></div>
            </div>

            <div id="instructionsBox" class="info-box" style="display:none;">
                <strong>🧭 Instrucción actual (<span id="stepNumber">1</span>/<span id="totalSteps">0</span>):</strong>
                <div id="currentInstruction" style="margin-top: 10px; font-size: 16px;">Esperando ruta...</div>
            </div>
        </div>

        <div class="card">
            <h3 style="margin-bottom: 15px; color: #667eea;">📋 Registro de eventos</h3>
            <div id="log" class="log"></div>
        </div>

        <div class="instructions">
            <strong>📖 Instrucciones de uso:</strong><br>
            1. Haz clic en "Conectar al Bastón"<br>
            2. Selecciona "BastonInteligente" en el diálogo Bluetooth<br>
            3. Acerca una tarjeta NFC al bastón con el destino<br>
            4. El sistema buscará la ruta automáticamente<br>
            5. Escucha las instrucciones de navegación paso a paso<br>
            <br>
            <strong>✨ Sin API Keys, sin límites, totalmente gratis</strong>
        </div>
    </div>

    <script>
        // UUIDs del servicio BLE
        const SERVICE_UUID = '4fafc201-1fb5-459e-8fcc-c5c9c331914b';
        const NFC_CHAR_UUID = 'beb5483e-36e1-4688-b7f5-ea07361b26a8';
        const ROUTE_CHAR_UUID = 'd8de624e-140f-4a3e-a5f0-7de3f3f5e5e5';

        let device = null;
        let server = null;
        let service = null;
        let nfcCharacteristic = null;
        let routeCharacteristic = null;
        let currentInstructions = [];
        let instructionIndex = 0;
        let totalDistance = 0;
        let totalDuration = 0;

        // Elementos DOM
        const statusEl = document.getElementById('status');
        const connectBtn = document.getElementById('connectBtn');
        const disconnectBtn = document.getElementById('disconnectBtn');
        const logEl = document.getElementById('log');
        const spinnerEl = document.getElementById('spinner');
        const destinationInfoEl = document.getElementById('destinationInfo');
        const destinationTextEl = document.getElementById('destinationText');
        const routeInfoEl = document.getElementById('routeInfo');
        const routeDistanceEl = document.getElementById('routeDistance');
        const routeDurationEl = document.getElementById('routeDuration');
        const instructionsBoxEl = document.getElementById('instructionsBox');
        const currentInstructionEl = document.getElementById('currentInstruction');
        const stepNumberEl = document.getElementById('stepNumber');
        const totalStepsEl = document.getElementById('totalSteps');
        const progressBarEl = document.getElementById('progressBar');
        const progressFillEl = document.getElementById('progressFill');

        function log(message, type = 'info') {
            const entry = document.createElement('div');
            entry.className = `log-entry log-${type}`;
            entry.textContent = `[${new Date().toLocaleTimeString()}] ${message}`;
            logEl.insertBefore(entry, logEl.firstChild);
        }

        function updateStatus(text, state) {
            statusEl.textContent = text;
            statusEl.className = `status ${state}`;
        }

        function speak(text) {
            return new Promise((resolve) => {
                if ('speechSynthesis' in window) {
                    window.speechSynthesis.cancel(); // Cancelar speech anterior
                    const utterance = new SpeechSynthesisUtterance(text);
                    utterance.lang = 'es-ES';
                    utterance.rate = 0.85;
                    utterance.pitch = 1.0;
                    utterance.volume = 1.0;
                    utterance.onend = resolve;
                    utterance.onerror = resolve;
                    window.speechSynthesis.speak(utterance);
                } else {
                    log('❌ Text-to-Speech no disponible', 'error');
                    resolve();
                }
            });
        }

        async function connectBLE() {
            try {
                updateStatus('🔍 Buscando dispositivo...', 'searching');
                spinnerEl.style.display = 'block';
                log('Buscando dispositivo BLE...', 'info');

                device = await navigator.bluetooth.requestDevice({
                    filters: [{ name: 'BastonInteligente' }],
                    optionalServices: [SERVICE_UUID]
                });

                log(`✓ Dispositivo encontrado: ${device.name}`, 'success');
                log('Conectando...', 'info');

                server = await device.gatt.connect();
                log('✓ Conectado al servidor GATT', 'success');

                service = await server.getPrimaryService(SERVICE_UUID);
                log('✓ Servicio obtenido', 'success');

                nfcCharacteristic = await service.getCharacteristic(NFC_CHAR_UUID);
                routeCharacteristic = await service.getCharacteristic(ROUTE_CHAR_UUID);
                
                await nfcCharacteristic.startNotifications();
                nfcCharacteristic.addEventListener('characteristicvaluechanged', handleNfcData);

                updateStatus('✅ Conectado al bastón', 'connected');
                connectBtn.style.display = 'none';
                disconnectBtn.style.display = 'block';
                spinnerEl.style.display = 'none';

                log('✅ Sistema listo. Acerca una tarjeta NFC', 'success');
                await speak('Conectado. Sistema listo.');

            } catch (error) {
                log(`❌ Error: ${error.message}`, 'error');
                updateStatus('❌ Error de conexión', 'disconnected');
                spinnerEl.style.display = 'none';
                alert('Error al conectar. Asegúrate de que el Bluetooth está activo.');
            }
        }

        function handleNfcData(event) {
            const value = event.target.value;
            const decoder = new TextDecoder('utf-8');
            const destination = decoder.decode(value).replace(/\0/g, '').trim();

            log(`📡 Destino recibido: ${destination}`, 'success');
            destinationTextEl.textContent = destination;
            destinationInfoEl.style.display = 'block';

            speak(`Destino: ${destination}. Buscando ruta.`);
            searchRoute(destination);
        }

        async function searchRoute(destination) {
            try {
                spinnerEl.style.display = 'block';
                log('🔍 Buscando ruta en OpenStreetMap...', 'info');

                // Obtener ubicación actual
                const position = await new Promise((resolve, reject) => {
                    navigator.geolocation.getCurrentPosition(resolve, reject, {
                        enableHighAccuracy: true,
                        timeout: 10000
                    });
                });

                const fromLat = position.coords.latitude;
                const fromLon = position.coords.longitude;

                log(`📍 Ubicación actual: ${fromLat.toFixed(5)}, ${fromLon.toFixed(5)}`, 'info');

                // Geocodificar el destino usando Nominatim (OpenStreetMap)
                // Añadimos viewbox para priorizar resultados cercanos
                const geocodeUrl = `https://nominatim.openstreetmap.org/search?q=${encodeURIComponent(destination)}&format=json&limit=1&bounded=0&viewbox=${fromLon-0.5},${fromLat-0.5},${fromLon+0.5},${fromLat+0.5}`;
                
                const geocodeRes = await fetch(geocodeUrl, {
                    headers: {
                        'User-Agent': 'BastonInteligente/1.0'
                    }
                });
                const geocodeData = await geocodeRes.json();

                if (geocodeData.length === 0) {
                    throw new Error('Destino no encontrado');
                }

                const toLat = parseFloat(geocodeData[0].lat);
                const toLon = parseFloat(geocodeData[0].lon);

                log(`📍 Destino encontrado: ${geocodeData[0].display_name}`, 'success');
                log(`📍 Coordenadas: ${toLat.toFixed(5)}, ${toLon.toFixed(5)}`, 'info');

                // Obtener ruta usando OSRM (Open Source Routing Machine)
                const routeUrl = `https://router.project-osrm.org/route/v1/foot/${fromLon},${fromLat};${toLon},${toLat}?steps=true&overview=full&language=es`;
                
                const routeRes = await fetch(routeUrl);
                const routeData = await routeRes.json();

                if (routeData.code !== 'Ok' || !routeData.routes || routeData.routes.length === 0) {
                    throw new Error('No se pudo calcular la ruta');
                }

                const route = routeData.routes[0];
                totalDistance = route.distance;
                totalDuration = route.duration;

                log(`✓ Ruta calculada: ${(totalDistance/1000).toFixed(2)} km, ${Math.round(totalDuration/60)} minutos`, 'success');

                // Mostrar info de la ruta
                routeDistanceEl.textContent = totalDistance >= 1000 
                    ? `${(totalDistance/1000).toFixed(2)} km` 
                    : `${Math.round(totalDistance)} m`;
                routeDurationEl.textContent = totalDuration >= 60 
                    ? `${Math.round(totalDuration/60)} min` 
                    : `${Math.round(totalDuration)} seg`;
                routeInfoEl.style.display = 'block';

                // Enviar confirmación al ESP32 (1 ruta disponible)
                const encoder = new TextEncoder();
                await routeCharacteristic.writeValue(encoder.encode('1'));

                // Procesar instrucciones
                processRoute(route);

                spinnerEl.style.display = 'none';

            } catch (error) {
                log(`❌ Error: ${error.message}`, 'error');
                spinnerEl.style.display = 'none';
                speak('Error al buscar la ruta. Intenta con otro destino.');
            }
        }

        function translateDirection(text) {
            // Traducir direcciones comunes de OSRM
            const translations = {
                'turn right': 'gira a la derecha',
                'turn left': 'gira a la izquierda',
                'continue': 'continúa',
                'straight': 'recto',
                'slight right': 'ligeramente a la derecha',
                'slight left': 'ligeramente a la izquierda',
                'sharp right': 'gira bruscamente a la derecha',
                'sharp left': 'gira bruscamente a la izquierda',
                'arrive': 'has llegado',
                'destination': 'destino',
                'depart': 'sal',
                'end of road': 'fin de la calle',
                'roundabout': 'rotonda'
            };

            let translated = text.toLowerCase();
            for (const [eng, esp] of Object.entries(translations)) {
                translated = translated.replace(eng, esp);
            }
            return translated;
        }

        async function processRoute(route) {
            currentInstructions = [];

            log('📍 Procesando instrucciones de navegación...', 'info');

            // Introducción
            const distanceText = totalDistance >= 1000 
                ? `${(totalDistance/1000).toFixed(1)} kilómetros` 
                : `${Math.round(totalDistance)} metros`;
            const durationText = totalDuration >= 60 
                ? `${Math.round(totalDuration/60)} minutos` 
                : `${Math.round(totalDuration)} segundos`;

            const intro = `Ruta a pie calculada. Distancia total: ${distanceText}. Duración estimada: ${durationText}. Comenzamos.`;
            currentInstructions.push(intro);

            // Procesar cada paso
            let stepNum = 1;
            for (const leg of route.legs) {
                for (const step of leg.steps) {
                    const maneuver = step.maneuver;
                    let instruction = '';

                    // Tipo de maniobra
                    if (maneuver.type === 'depart') {
                        instruction = 'Comienza caminando';
                    } else if (maneuver.type === 'arrive') {
                        instruction = 'Has llegado a tu destino';
                    } else if (maneuver.type === 'turn') {
                        const modifier = translateDirection(maneuver.modifier || '');
                        instruction = `${modifier}`;
                    } else if (maneuver.type === 'continue') {
                        instruction = 'Continúa recto';
                    } else {
                        instruction = translateDirection(maneuver.type);
                    }

                    // Nombre de la calle si existe
                    if (step.name && step.name !== '') {
                        instruction += ` por ${step.name}`;
                    }

                    // Distancia
                    const stepDistance = step.distance >= 1000 
                        ? `${(step.distance/1000).toFixed(1)} kilómetros` 
                        : `${Math.round(step.distance)} metros`;

                    if (step.distance > 10) {
                        instruction += ` durante ${stepDistance}`;
                    }

                    currentInstructions.push(`Paso ${stepNum}. ${instruction}.`);
                    stepNum++;
                }
            }

            currentInstructions.push('Has llegado a tu destino.');

            totalStepsEl.textContent = currentInstructions.length;
            log(`✓ ${currentInstructions.length} instrucciones preparadas`, 'success');
            
            instructionsBoxEl.style.display = 'block';
            progressBarEl.style.display = 'block';

            // Comenzar navegación
            instructionIndex = 0;
            playNextInstruction();
        }

        async function playNextInstruction() {
            if (instructionIndex >= currentInstructions.length) {
                log('✅ Navegación completada', 'success');
                currentInstructionEl.textContent = '✅ Has llegado a tu destino';
                stepNumberEl.textContent = currentInstructions.length;
                progressFillEl.style.width = '100%';
                await speak('Navegación completada. Has llegado a tu destino.');
                return;
            }

            const instruction = currentInstructions[instructionIndex];
            
            // Actualizar UI
            stepNumberEl.textContent = instructionIndex + 1;
            currentInstructionEl.textContent = instruction;
            
            // Actualizar barra de progreso
            const progress = ((instructionIndex + 1) / currentInstructions.length) * 100;
            progressFillEl.style.width = `${progress}%`;

            log(`🔊 ${instruction}`, 'info');

            // Reproducir instrucción
            await speak(instruction);
            
            instructionIndex++;
            
            // Esperar 1 segundo antes de la siguiente instrucción
            setTimeout(playNextInstruction, 1000);
        }

        function disconnect() {
            if (device && device.gatt.connected) {
                device.gatt.disconnect();
                log('🔌 Desconectado', 'info');
            }
            
            updateStatus('❌ Desconectado', 'disconnected');
            connectBtn.style.display = 'block';
            disconnectBtn.style.display = 'none';
            destinationInfoEl.style.display = 'none';
            routeInfoEl.style.display = 'none';
            instructionsBoxEl.style.display = 'none';
            progressBarEl.style.display = 'none';
            
            device = null;
            server = null;
            service = null;
        }

        // Event listeners
        connectBtn.addEventListener('click', connectBLE);
        disconnectBtn.addEventListener('click', disconnect);

        log('📱 App iniciada. Sistema 100% gratuito con OpenStreetMap.', 'info');
        log('✨ Sin API keys, sin límites, sin costes.', 'success');
    </script>
</body>
</html>
