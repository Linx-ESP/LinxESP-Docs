# Salida de video, color y estándares

Importante mencionar que apenas toco lo que tenga que ver con el buffer y gestión interna de la Wii
- [Gist útil sobre ello](https://gist.github.com/vaguerant/eb9c7fba35f118ccb32c5df22b2b0f35)

!!! info "Wii Mini y vWii (Wii U)"
    La Wii Mini tiene limitaciones artificiales que no tengo en cuenta.
    El modo Wii de la Wii U tiene alguna cosa en particular, pero en general todo es aplicable.
!!! failure "Confusiones habituales"
    Mucha gente, por no decir la totalidad de usuarios de Wii y otras consolas, usan incorrectamente términos que se refieren a modos de video, conectores, espacios de color y de todo.  
    Por ejemplo: Componente (Conector) vs. YPbPr (Espacio de color).

## Especificaciones de la Wii

### Resoluciones
| Nombre en Wii | Resolución | Compatbilidad |
| ---           | ---        | ---   |
| ``480i``      | 640×480@60Hz Interlazado  | Todas las consolas
| ``576i``      | 640×576@50Hz Interlazado  | Stock Software: Solo EU. Mods en software: Todas (no hay diferencia de hardware en las consolas)
| ``EDTV``      | 640x480@60Hz Progresivo   | Todas las consolas
| -             | 640×576@50Hz Progresivo   | Fisicamente imposible en Wii. Se puede forzar en vWii (Wii U) mediante mods.

### Conexiones
| Conector | Uso en Wii / "Especificación"  | Compatibilidad    | Notas |
| ---      | ---                            | ---               | ---   |
| Compuesto/composite | 480i/576i, YUV, 1 canal     | Todas las consolas | No es S-VIDEO
| Componente          | EDTV, YUV, 3 canales        | Todas las consolas, requiere cable adicional |
| SCART               | 480i/576i, RGB, 3 canales   | Solo consolas europeas, requiere cable adicional | Puede forzarse 480p en USB loaders sin problemas aparentemente

!!! info "YUV vs RGB"
    Más adelante lo explico algo más, pero en la Wii, ninguno es mejor. Son matemáticamente intercambiables si no se usa "Chroma subsampling".

## Especificaciones de Video (independiente de la Wii, pero se aplica)

### Estándares de emisión
- ``PAL``: Phase Analogue Line
    - Es un estándar de codificación de color para emisión en televisión.
    - El estándar no define una resolución ni herzios.
    - La especificación define que el color se codifique en un formato YUV en una sola señal.
- ``NTSC``: National Television System Committee
    - Es un comité regulatorio, aunque generalmente se usa para referirse a los estándares de TV que creó.
    - NTSC estándar de emisión de televisión analógica.
    - Define codificación de color en YIQ. Rl espacio de color cambia en las revisiones del estándar.
    - Define 29.97 fotogramas interlazados, con una señal visible de 480 lineas. (Distintas revisiones alternan 486 lineas y 30 fotogramas, no es relevante).

### Codificación del color y "chroma subsampling"
El color, como luz, se puede representar como una frecuencia. Excepto que eso da igual para una consola. Ahí es donde entra la codificación del color.
    - Por ejemplo, el ojo humano "codifica" el color según la señal que recibe cada uno de los conos fotorreceptores del ojo.

- ``RGB``
    - Divide el color en 3 canales: Rojo, Verde, Azul (Red, Green, Blue)
- ``YUV``
    - Divide el color en 3 canales: Luminancia (Luma), Proyección Azul (Luminancia - Azul), Proyección Roja (Luminancia - Rojo)
- ``YIQ``
    - Mismo sistema que YUV: 3 canales, 1 luminancia y 2 de cromacidad
    - En vez de azul y rojo, considera un azul verdoso y un rojo tirando a morado.
    - En uan representación 2D del color, sería colora los ejes ligeramente rotados.

Son matemáticamente intercambiable entre si. Imagínalo como ``1 + 2 + 3 = __ vs. 1 + __ + 3 = 6``.

El porqué de esto es que nuestros ojos son más sensibles a cambios de luminancia que de cromacidad (cromacidad ≠ color).
Con tal de ahorrar ancho de banda en las conexiones, los colores codificados en YUV sufren ``chroma subsampling`` (lo habrás visto como 4:2:2, 4:2:0, ...):  

- Muy simplificado: en vez de mandar una imagen 1080p de Luma, otra 1080p de U y otra 1080p de V; mandas Luma en 1080p, y UV en 540p cada una.  
- Chroma subsampling no es reversible, conlleva pérdidas.  
- La Wii no usa chroma subsampling, es decir, RGB y YUV conservan la misma calidad de color.  
- Televsiores modernos son capaces de aceptar e intercambiar las dos, otra cosa es que lo muestren exactamente igual (piensa en YUV vs YIQ). Anteriormente esto no era así por ser analógicos y no digitales.  

### Espacios de color
Ok, ahora sabes que tu imagen te la envían en tres paquetes: rojo, verde y azul... ¿De qué rojo estamos hablando? ¿Cómo de azul?  
Los espacios de color son los que definen y calibran los colores de pantallas frente a la vida real. Establecen limites del espacio de color, gamma objetivo, luminancia considerada, temperatura del punto blanco... (Varía según la especificación)

Para todo, lo mejor es tener una pantalla calibrada al contenido que se va a consumir, excepto gamma (muy dependiente de las condiciones de visionado).

- [sRGB](https://www.color.org/chardata/rgb/srgb.xalter): Considerado el estándar de internet. Desde webs hasta interfaces.
- [AdobeRGB 1998](https://www.color.org/chardata/rgb/adobergb.xalter): Creado para facilitar la impresión de elementos digitales.
- [BT.2020](https://www.color.org/chardata/rgb/BT2020.xalter): Presentado como el sucesor de bt.601 y bt.709 y preparado para contenido en HDR.
- [DCI-P3](https://www.color.org/chardata/rgb/DCIP3.xalter): Al parecer BT.2020 era demasiado optimista con cómo de buenas serían las pantallas en 2020.
- [BT.709](https://www.color.org/chardata/rgb/BT709.xalter): Espacio de color usado actualmente para emisiones televisión.
- [BT.601](https://www.color.org/chardata/rgb/BT601.xalter): Espacio de color usado anteriormente para emisiones de televisión.
- YPbPr: Buena suerte con la especificación original. Parece que se basa en YUV en vez de RGB y estuvo orientado a emisiones analógicas.
- YCbCr: Buena suerte con la especificación original. Se basa en YUV y es un espacio de color más extenso que YCbCr dadas las mejoras técnológicas (de ahí que se relacione con dispositivos digitales)

!!! info "El espacio de color en software, hardware"
    El espacio de color no lo define el dispositivo, si no el contenido: En mi ordenador puedo ver una serie que seguramente esté calibrada en BT.709 y luego editar fotos en DCI-P3.  

    Esto es lo que causa tener que usar distintos perfiles de calibración en cada aplicación y pantalla en entornos profesionales.  

!!! success "Espacio de color de la Wii"
    Sin saber que hizo cada estudio y desarrolladora (o documentación de Nintendo), se puede estimar que trabajaban con la referencia de BT.601 en la Wii (basado en el resultado final y las fechas).  

    La WiiU en cambio es principalmente BT.709 (lo que causa resultados de calibración distintos al usar vWii)