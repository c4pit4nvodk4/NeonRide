
⚡ NEON RIDE — Velocímetro GPS para moto eléctrica
NEON RIDE es un tablero web para acompañar recorridos en moto eléctrica, especialmente útil en repartos de corta distancia. Incluye velocímetro GPS, mapa con ruta, métricas del trayecto y contador de pedidos, con una interfaz negra y verde neón, animaciones y diseño adaptable a celular y escritorio.

Importante: La velocidad y posición dependen del GPS del dispositivo y pueden variar según la señal. Esta aplicación es una herramienta de consulta, no reemplaza el velocímetro ni los instrumentos de seguridad de la moto. Consulta la pantalla únicamente cuando estés detenido.

✨ Características
🏍️ Velocidad actual en km/h, con velocímetro animado.
📈 Velocidad máxima y promedio de la sesión.
🗺️ Mapa interactivo con ubicación y trazado de ruta.
📍 Información GPS, como coordenadas, precisión y rumbo cuando estén disponibles.
📏 Distancia recorrida en kilómetros.
⏱️ Tiempo de ruta y reloj.
📦 Contador de entregas con botones + y −.
🔋 Porcentaje de batería manual (no consulta la batería real de la moto).
▶️ Iniciar, pausar y reiniciar el recorrido.
📤 Exportar ruta en formato GPX para abrirla en aplicaciones compatibles.
📱 Diseño responsive y opción de pantalla completa (si el navegador la admite).
💾 Guardado local del contador de entregas y el porcentaje de batería mediante localStorage.
🛠️ Tecnologías
HTML5, CSS3 y JavaScript sin frameworks de aplicación.
Geolocation API del navegador para obtener posición y velocidad.
Leaflet 1.9.4 para el mapa interactivo.
Mapas base de CARTO, con atribución a OpenStreetMap.
Google Fonts: Barlow Condensed y DM Sans.
Screen Wake Lock API, cuando el navegador la permite, para intentar mantener la pantalla encendida durante la ruta.
No necesita instalación de dependencias, compilación ni backend. Las bibliotecas, fuentes y teselas del mapa se descargan desde servicios externos, por lo que el mapa y los estilos externos requieren conexión a internet.

🚀 Instalación y uso local
Descarga o clona el repositorio.
Abre moto_neon_gps.html en tu navegador para visualizar el tablero.
Para usar el GPS, sirve el archivo mediante localhost o publícalo con HTTPS. Abrir un archivo local directamente (file://) no es una opción fiable para esta función.
Para probar con un servidor local, desde la carpeta del proyecto ejecuta:

python -m http.server 8000
Después visita http://localhost:8000/moto_neon_gps.html en el mismo dispositivo. En Windows, si python no funciona, prueba py -m http.server 8000.

🌐 Publicar gratis en GitHub Pages
Crea un repositorio nuevo en GitHub (por ejemplo, neon-ride).
Renombra moto_neon_gps.html a index.html antes de subirlo, para que la página abra desde la raíz.
Sube index.html y este README.md a la rama principal (main).
En tu repositorio ve a Settings → Pages.
En Build and deployment, selecciona Deploy from a branch.
Selecciona la rama main y la carpeta / (root), y guarda los cambios.
Cuando termine la publicación, abre la URL que GitHub Pages muestre. Normalmente será:
[https://c4pit4nvodk4.github.io/neon-ride/](https://c4pit4nvodk4.github.io/NeonRide/)
Reemplaza TU-USUARIO y neon-ride por los nombres reales de tu cuenta y repositorio. GitHub Pages utiliza HTTPS, necesario para solicitar permisos de ubicación en navegadores modernos.

📱 Cómo usarlo en tu moto
Abre la página publicada en tu celular.
Habilita la ubicación del teléfono y concede permiso de ubicación al navegador.
Pulsa INICIAR RUTA y espera a que el GPS consiga señal.
Consulta velocidad, tiempo, distancia y mapa durante tus paradas.
Cada vez que completes un pedido, pulsa + en el contador de entregas.
Ajusta manualmente el porcentaje de batería cuando lo necesites.
Usa PAUSAR para detener el registro y GPX para descargar la ruta registrada.
Usa REINICIAR para borrar las métricas de la sesión; el contador de entregas y la batería se conservan.
Consejo: Para mejorar la lectura del GPS, utiliza el dispositivo al aire libre con ubicación de alta precisión activada. La velocidad puede tardar en actualizarse o fluctuar cuando la señal es débil.

🔒 Privacidad y almacenamiento
La página solicita ubicación solo al iniciar el recorrido.
No incorpora una cuenta de usuario ni un servidor propio para guardar viajes.
El contador de entregas y el porcentaje de batería se guardan en localStorage del navegador.
Los puntos de la ruta y las métricas de recorrido viven en la memoria de la pestaña: recargar o cerrar la página puede hacer que se pierdan. Exporta el GPX antes de cerrar si quieres conservar tu ruta.
El mapa descarga contenido desde proveedores externos. Revisa sus políticas de privacidad si necesitas más información sobre esas solicitudes.
⚠️ Limitaciones
No mide la batería real: el control de batería es manual; no hay conexión Bluetooth ni integración con el controlador de la moto.
No incluye navegación paso a paso ni cálculo de rutas hacia destinos.
El GPS debe ser compatible con el dispositivo y estar autorizado; en interiores, con ahorro de batería o baja señal puede presentar errores.
El seguimiento en segundo plano no está garantizado: el navegador o el sistema operativo pueden suspender la página al bloquear el teléfono o cambiar de aplicación.
No es una app offline completa: el mapa depende de recursos externos.
📁 Estructura del proyecto
Para publicar mediante GitHub Pages:

neon-ride/
├── index.html      # Aplicación web (archivo HTML renombrado)
└── README.md       # Documentación
🎨 Personalización
Los colores principales están definidos en las variables CSS :root del archivo HTML:

--bg: #050907;       /* Fondo oscuro */
--lime: #baff37;     /* Verde neón principal */
--mint: #52f7ab;     /* Verde secundario */
--text: #f3fff2;     /* Texto */
Puedes editar estos valores para cambiar el estilo visual.

📄 Licencia
Aún no se ha incluido un archivo de licencia en el proyecto. Si deseas permitir reutilización, modificación o distribución bajo términos específicos, agrega un archivo LICENSE al repositorio con la licencia que elijas.

NEON RIDE — Un tablero GPS para acompañar tus recorridos y entregas. 🏍️⚡

