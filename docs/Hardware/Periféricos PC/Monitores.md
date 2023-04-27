# Monitores
Esto es muy general por ahora, es WIP al fin y al cabo.

## Esencial
Aspectos a considerar antes de buscar una pantalla:

1. Resolución, relación de aspecto y frecuencia
    - Deberían considerarse en conjunto, sobre todo porque por ser quienes van a dictaminar el precio principalmente.
    1. Relación de aspecto
        - ``16:9``: estándar.
        - ``21:9`` y `32:9`: ultrawide.
            - Mayor espacio en el escritorio para ventanas simultáneas.
            - Mayor inmersión en juegos por mayor campo de visión .
            - Mayor espacio físico requerido.
    2. Frecuencia de actualiación o refresco / refresh rate
        - `60Hz`: estándar
        - `144Hz` / `240Hz` / `360Hz`: alto refresco / high refresh rate
            - Movimientos mucho más fluidos.
            - Latencia menor.
            - Prioridad si es para videojuegos.
            - En tareas de ofimática ofrece mayor claridad en movimientos de ventana, animaciones y similar.
    3. Resolución
        - `1080p` o ``FullHD``
        - `1440p` o ``QHD`` (incorrectamente 2K)
        - `2560p` o ``UHD``
        - Resoluciones más altas ofrecen mayor densidad de píxeles por tamaño.
        - Pueden dar más espacio de pantalla útil debido a poder hacer más pequeño aspectos de interfaces.
2. Especificaciones del ordenador
    1. Salidas de vídeo que soporten resolución y frecuencia
        - Monitores `4K 144Hz` requieren o bien `Display Port 1.4` (común) o `HDMI 2.1` (poco común)
        - En caso de no cumplir con el requisito se tendrá que usar a menor frecuencia o resolución
    2. Potencia para 3D
        - Solo afecta a videojuegos
        - Aumentar resolución y frecuencia de refresco aumentan los requisitos del sistema
            - No escala linealmente, normalmente a menos:
                - *2 resolución =/= *2 rendimiento, sino *1.x
3. HDR
    1. `OLED` o `Full Array Local Diming` es lo único con verdadero HDR.
    2. Certificaciones `VESA HDR` (como `HDR 400`) no significan nada útil.
## Factores a tener en cuenta
Básicamente, que aspectos del producto lo hacen "mejor"

### Tipo de panel
1. ``IPS`` (Recomendación)
    - Mejor tiempo de respuesta.
    - Mejor color.
    - Mejores ángulos de visión.
2. ``VA``
    - Más baratos que ``IPS``.
    - Tiempor de respuesta potencialmente horribles en transiciones entre colores oscuros.
3. ``OLED``
    - Alto riesgo de Burn-in, esperar a ``QD-OLED``.
    - Mínima latencia.
    - Amplio rango de color.
    - HDR perfecto.
    - Brillo inferior.
    - Muy caros.
4. ``TN`` EVITAR
    - Anteriormente se beneficiaban de buenos tiempos de respuesta, ya no es notable.
    - Colores y ángulos de visión pésimos

### Frecuencia de refresco variable / VRR (Variable Refresh Rate)
En juegos, no siempre se muestra la misma cantidad de fotogramas, lo cuál causa problemas (ver Tearing, Stutter).  
Adaptar la frecuencia del monitor a los fotogramas renderizados soluciona estos problemas.  

- `VESA Adaptative Sync` es el estándar principal.
    - `Nvidia G-Sync Compatible` se vasa en el de VESA, exclusivo de Display Port.
    - `AMD Freesync` es una modificación para hacerlo funcionar con HDMI.
        - Esto hace que no todos los monitores Freesync sean `G-Sync capable / compatible`, pero por regla general lo son.
    - Todo el mundo se refiere a ello como Freesync.
- `Nvidia G-Sync Ultimate`
    - Es literalmente un chip en el monitor, permite funciones adicionales pero siendo mucho más caro.
- `HDMI VRR`
    - A partir de HDMI 2.1, `Variable Refresh Rate` está incluido en el estándar.

### Tiempo de respuesta
[Hardware Unboxed](https://www.youtube.com/c/Hardwareunboxednow), [RTINGS](https://www.rtings.com/monitor), entre otros, lo miden.  

- Indica el tiempo que tarda un píxel en cambiar de color.
  - Menos es mejor = más rápido es mejor
- Varía según que brillo transicione a que brillo (oscuro a oscuro, brillante a oscuro, etc...).
- ES NECESARIO que sea como poco suficiente para su frecuencia:
    - `144Hz` = 144 imagenes por segundo => Píxel tiene (1/144) segundos para cambiar de color.

#### Overdrive
Básicamente, no hay panel (salvo OLED) que pueda tener un tiempo de respuesta óptima.  
Overdrive es un empujón extra para alcanzarlo, pero según puede pasarse, causando artefactos (ghosting).  

- Un modo de overdrive para `144Hz` puede no ser óptimo para `60Hz` o `100Hz`
    - Si el monitor es `G-Sync Ultimate` puede variar overdrive según necesite, otros sin `G-Sync Ultimate` también lo soportan, pero muy pocos
### Espacio de color y calibración
- Los espacios de color se usan para estandarizar que colores han de mostrarse
    - Más % de un espacio de color, mejor
    - Los principales son ``sRGB`` para contenido SDR y ``DCI-P3`` para HDR
        - Por algún motivo para TV son ``Rec.601`` para SDR y ``Rec.709`` para HDR
- Calibración significa como de cerca está de mostrar el color correcto
    - Menor delta = Mejor (menor diferencia del color objetivo)
    - Debido a defectos en fabricación, un mismo modelo de monitor puede variar entre unidades
    - Lo más común es rojos o verdes sobresaturados, lo cual hace perder detalle entre medias
    - Se calibra respecto a un espacio de color, de normal debería ser ``sRGB``
    - Se puede calibrar por software, aunque requiere hardware adicional para hacer un perfil perfecto
        - Normalmente la mayor parte de los errores de calibración se puede solucionar de manera suficiente con un perfil ICC normal, ver Patreon de Hardware Unboxed.

### Conectividad
- Puertos de vídeo
    - Display Port es preferencia en PC
    - HDMI puede no cumplir con los requisitos en resoluciones y frecuencias de refresco altas
- Otros puertos
    - USBs
        - KVM o USB switch, que permite usar un set de dispositivos conectados y alternarlos entre varios ordenadores
    - Audio
        - Salidas de jack es lo más normal
### Adicional