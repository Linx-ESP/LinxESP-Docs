# Esenciales de Windows
    - Está página tiene que ser reformateada y actualizada, no seguir ciegamente
# Ajustes
- Asociar tu claves de Windows a tu cuenta de Microsoft | Seguridad y comodidad a cambio de algo de privacidad. [Ver](https://www.microsoft.com/security/blog/2021/09/15/the-passwordless-future-is-here-for-your-microsoft-account/)
    - Da igual como esté activado Windows, mientras lo esté
    - Configuración de activación > Agregar una cuenta
        - Como te pedirá la contraseña para iniciar sesión a Windows mi recomendación es poner un PIN
        - Este PIN permite iniciar sesión con la cuenta de microsoft en el navegador, solo afecta a ese PC 
- Cambios en Windows Update
    - Ajustes > Actualización y Seguridad > Opciones avanzadas
        - Reinicia este dispotivo lo antes posible: "Desactivado"
    - Actualización y seguridad > Opciones avanzadas > Optimización de distribución
        - Permitir descargas de otros equipos: "Desactivado"
    - Optimización de distribución > Opciones Avanzadas
        - Ancho de banda absoluto: Configúralo a gusto
- Administrador de tareas completo
    - Admin. de tareas > Más detalles
    - Rendimiento > CPU > Clic derecho en la gráfica > Cambiar a > Procesadores Lógicos
    - Opciones (Barra de arriba) > Siempre Visible: "Sí"
- Mejores capturas de pantalla
    - Ajustes > Accesibilidad > Teclado > Utilizar el botón Impr Pant para abrir recorte de pantalla: "Activado"
- Mejor portapapeles (Win + V) 
    - Ajustes >  Sistema > Portapapeles > Historial del portapapeles
- Mejor precisión de ratón
    - Ajustes > Dispositivos > Mouse > Opciones de mouse adicionales (derecha) > Opciones del puntero
    - Velocidad del puntero: A gusto
    - Mejorar la preciosión del puntero: "No"
    - Entrada directa en juegos se salta este ajuste
- Limpiar el menú de inicio
    - Puedes ajustar el menú de inicio como solo la barra de apps
    - Ajustes > personalización > Inicio
        - Aplicaciones más usadas y agregadas recientemente: "No" (a gusto)
        - Mostrar sugerencias ocasionalmente en inicio: "No"  
- Limpiar la barra de tareas
    - Clic derecho en la barra de tareas >
        - Barra de herramientas: "Ninguna"
        - Búsqueda: "Oculto" (puedes escribir directamente en el menú de inicio)
        - Mostrar Botón de Vista de Tareas y Contactos: "No"
- Configurar conexión como red privada (SÓLO SI EN LA RED DE CASA)
    - Estado de red > (tu conexión) > Propiedades > Perfil de red: Privado 
- Cambiar DNS's (no afecta al ping en juegos, solo a resolver urls a IPs númericas, [test por Battle (non)sense](https://www.youtube.com/watch?v=cWBrZKvYUuw))
    - Estado de Red > (red actual) Propiedades > Configuración de IP (Editar) > Manual
    - IPv4 Activado
    - DNS preferido: 1.1.1.1 [Cloudflare]
    - DNS alternativo: 1.0.0.1
        - IBM Quad9: 9.9.9.9 | 149.112.112.112
        - Cisco OpenDNS / Umbrella: 208.67.222.222 | 208.67.220.220
- Mejor indexación de archivos
    - Ajustes > Buscar > En Windows > Mejorado
        - CPUs modernas y SSD no tienen problemas de rendimiento con esto
- Evitar que programas se inicien con el PC
    - Administrador de Tareas > Inicio (Nada de ahí es necesario)
    - msconfig > Servicios > Ocultar todos los servicios de Microsoft > Ir probando cuales
        - Para cosas que se puedan necesitar pero no según se inicia: Servicios > (servicio a modificar) > Inicio Manual
- Evitar que el menú de inicio busque en internet también (No todas las versiones de Win10/11)
    - Regedit / Editor del registro > Equipo\HKEY_CURRENT_USER\SOFTWARE\Microsoft\Windows\CurrentVersion\Search
        - Clic derecho > Nuevo > DWORD 32 bits > BingSearchEnabled -> Valor = 0
# Navegador
Huir de Chrome    

- Edge tiene opción para inicio instantáneo y sigue los materiales/Fluent Design de Windows, pero telemetría de Microsoft  
- Firefox (único no basado en chromium)  
- Brave incorpora alguna función no deseada, aunque opcional, no parece mantener el rendimiento 
- Opera y GX desde que fueron comprados tiene demasiada telemetría y anuncios integrados  
- Vivaldi, del equipo original de Opera, es la mayor cantidad posible de personalización, pero por defecto puede no ser tan bueno  
- [Ungoogle Chromium](https://ungoogled-software.github.io/ungoogled-chromium-binaries/) e Iridium: Chrome sin servicios de Google, pegas para usar pero máxima privacidad  
### Extensiones
- uBlock Origin - Mejor bloqueador de anuncios y ligero
- [Privacy Badger by EFF](https://privacybadger.org/) - Opciones de privacidad y [Global Privacy Control](https://globalprivacycontrol.org/)
- [Fast Forward](https://chrome.google.com/webstore/detail/fastforward/icallnadddjmdinamnolclfjanhfoafe) - Salta links intermedios automáticamente
- SponsorBlock - Bloquea sponsors, promociones, "sub y dale a like" y demás en yt, configurable
- [Return Dislike Button](https://chrome.google.com/webstore/detail/return-youtube-dislike/gebbhagfogifgggkldgodflihgfeippi) - Gracias Youtube por quitar el botón de dislike
- ViolentMonkey - Permite cargar script para funciones en web, código abierto. Ver Greasy Fork
- Stylus - permite encontrar y usar temas para webs
- Bitwarden o cualquier otro gestor de contraseñas
# Apps
Mejora la experiencia manteniendo la esencia básica de Windows, nada extravagante:   

- [EarTrumpet](https://www.microsoft.com/es-es/p/eartrumpet/9nblggh516xp?activetab=pivot:overviewtab) - Mejor control de audio de Windows  
- [Rainmeter](https://www.rainmeter.net) - Personalización con "widget-like", se pueden conseguir en otras [webs](https://www.deviantart.com/search?q=rainmeter)  
- [Taskbar X](https://chrisandriessen.nl/taskbarx) - Centrar y transparencia de la barra de tareas. Windows 11 incorpora la opción para centrar  
- [Wallpaper Engine](https://store.steampowered.com/app/431960/Wallpaper_Engine/) - Fondos animados e interactivos. Ver [Lively Wallpaper](https://rocksdanister.github.io/lively/) también  
- [NanaZip](https://apps.microsoft.com/store/detail/nanazip/9N8G7TSCL18R?hl=es-es&gl=ES) - Alternativa a WinRAR y 7zip (basado en 7zip)  
- [PowerToys](https://github.com/microsoft/PowerToys) - Añade distintas funciones a Windows  

# Otros
- [Breeze Mouse Cursors](https://www.deviantart.com/niivu/art/Breeze-Cursors-784566911) Punteros alternativos, sacados de KDE/Gnome Linux  
- [HEVC Códec](ms-windows-store://pdp/?ProductId=9n4wgh0z6vhq) Debido a licencias relacionadas con HEVC, este producto está oculto en MS Store, en su lugar parece que ha de instalarse la versión de pago.