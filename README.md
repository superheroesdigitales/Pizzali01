<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <title>WebControl-IA: Sensor Global de Temperatura</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      line-height: 1.6;
      margin: 0;
      padding: 20px;
      background: #f9f9f9;
      color: #333;
    }
    header {
      text-align: center;
      background-color: #004080;
      color: white;
      padding: 40px 20px;
      border-radius: 12px;
    }
    header h1 {
      font-size: 2.5em;
      margin-bottom: 10px;
    }
    section {
      background: white;
      margin-top: 20px;
      padding: 20px;
      border-radius: 12px;
      box-shadow: 0 0 8px rgba(0,0,0,0.1);
    }
    h2 {
      color: #004080;
    }
    code {
      background-color: #eee;
      padding: 2px 6px;
      border-radius: 4px;
    }
    .flujo {
      background-color: #f0f8ff;
      padding: 10px;
      border-left: 6px solid #004080;
      font-family: monospace;
    }
    footer {
      text-align: center;
      margin-top: 40px;
      font-size: 0.9em;
      color: #666;
    }
  </style>
</head>
<body>

<header>
  <h1>WebControl-IA: Sensor Global de Temperatura</h1>
  <p>Proyecto educativo de la Escuela de Superhéroes Digitales</p>
</header>

<section>
  <h2>🔍 Descripción General</h2>
  <p>Este proyecto permite leer la temperatura desde cualquier parte del mundo con una placa <strong>ESP8266</strong> y enviarla a un <strong>servidor web central</strong> ubicado en tu casa, al cual se podrá acceder desde cualquier lugar del planeta. No utiliza la nube tradicional ni plataformas IoT: ¡usa páginas web inteligentes que se comunican como héroes digitales!</p>
</section>

<section>
  <h2>📦 Componentes del Sistema</h2>
  <ul>
    <li><strong>ESP8266</strong> (NodeMCU o Wemos D1 Mini)</li>
    <li><strong>Sensor de temperatura</strong> (DHT11 o DHT22)</li>
    <li><strong>Servidor web</strong> casero (Raspberry Pi o PC)</li>
    <li><strong>Red WiFi</strong> con acceso a internet</li>
    <li><strong>Router con puertos abiertos</strong> o servicio No-IP</li>
  </ul>
</section>

<section>
  <h2>🧱 Estructura del Sistema</h2>
  <h3>1. Nodo WebSensor (Cliente Web Inteligente)</h3>
  <p>El ESP8266 actúa como una <strong>página web inteligente</strong>. Lee la temperatura y la envía mediante <code>HTTP POST</code> a un servidor central.</p>
  <p>Este "cliente web" puede tener incluso una interfaz accesible desde un navegador.</p>

  <h3>2. Servidor Maestro WebControl-IA</h3>
  <p>Servidor ubicado en tu casa que recibe los datos enviados por cada sensor remoto. Tiene funciones como:</p>
  <ul>
    <li>Recibir y almacenar datos (JSON, SQLite o MySQL)</li>
    <li>Mostrar temperatura actual e historial</li>
    <li>Dashboard web accesible globalmente</li>
  </ul>

  <h3>3. Visualización Global</h3>
  <p>Desde cualquier lugar del mundo, un usuario puede ingresar a la página del servidor maestro y ver:</p>
  <ul>
    <li>Temperatura en tiempo real</li>
    <li>Fecha y hora del último registro</li>
    <li>Gráficas con historial (Chart.js)</li>
  </ul>

  <h3>4. Expansión entre Servidores (Avanzado)</h3>
  <p>Los sensores también pueden comportarse como pequeños servidores que comparten datos entre sí, creando una <strong>red de nodos inteligentes descentralizados</strong>.</p>
</section>

<section>
  <h2>📡 Flujo del Sistema</h2>
  <div class="flujo">
    [ESP8266 + Sensor + Página web] → (POST con datos) → [Servidor WebControl-IA en casa] → (Visualización) → [Usuarios en cualquier parte del mundo]
  </div>
</section>

<section>
  <h2>🧠 Módulos del Proyecto</h2>
  <ul>
    <li><strong>WebSensorClient:</strong> Código en ESP8266 que actúa como página web y cliente de envío</li>
    <li><strong>WebServerReceptor:</strong> Backend que recibe y guarda datos</li>
    <li><strong>VisualizadorGlobal:</strong> Página con tabla, gráficos y datos en tiempo real</li>
    <li><strong>Seguridad:</strong> Login básico y protección con HTTPS</li>
  </ul>
</section>

<footer>
  Proyecto creado por Prof. Ing. Víctor – Escuela de Superhéroes Digitales 🌱⚡
</footer>

</body>
</html>
