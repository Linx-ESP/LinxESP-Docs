# Eliminar Pixel Art
## Reshade
Reshade es una herramienta que permite aplicar filtros de postprocesado, o incluso efectos si puede usar el búfer de profundidad.  
En el caso de juegos Pixel Art, 2DSCale es un filtro de escalado que permite mezclar los pixeles manteniendo el estilo artístico.  

Otros filtros similares incluyen ScaleFX (RetroArch) o HQ4x (peor resultado).  

Como alternativa, este estilo se beneficia infinitamente de una pantalla CRT... O un filtro que lo imite.  


[Ver ejemplos](/Demos/PixelArt/#stardew-valley){ .md-button }

=== "Instalar"
    - [Descarga](https://reshade.me/) y ejecuta el instalador de Reshade
    - Busca el juego o añadelo manualmente. Haz click en `Next`.
    - Selecciona la API gráfica que corresponda, [Ver aquí](#lista-de-juegos).  
    - Selecciona `Install`.
    - [Opcional] Marca `RSRetroArch by Matsilagi` si quieres usar el filtro de CRT.
    - En la casilla de abajo sustituye `Enter ZIP download link to custom repository here` por `https://github.com/Linx-ESP/Reshade/archive/refs/heads/main.zip` y haz clock en `Add`. Asegúrate que `main.zip` está marcado en la lista.
    - Haz click en `Next` para continuar y `Finish` para acabar.  

=== "Usar"
    - Pulsa la tecla `Home` desplegar el overlay de Reshade.
    - Selecciona `Continue` si quieres ver el tutorial (5 pasos), `Skip the tutorial` si no.  
    === "[Recomendado] 2D Scaler"
        - Activa `TWO_D_SCALER_LEVEL2`
            - En los ajustes de la parte inferior:
                - `Filter Width`: 1. Parece que cualquier otra cantidad es peor
                - `Deblur`: 5. Parece que más es mejor
        - [Opcional] Activa `BUMPMAPPING` y asegúrate que esté debajo de `TWO_D_SCALER_LEVEL2`
        !!! check "Listo para jugar"
            2D Scaler debería no debería generar artefactos debido a que no usa una cuadrícula fija para escalar
    === "xBRZ"
        - Activa `xBRZx4`
        - En la parte inferior, `Strength` equivale al multiplicador de escalado.
            - Multiplicador = Resolución vertical del monitor / Resolución del pixel art
            - Ejemplo: Monitor 2560x1440p en Celeste sería:
                - 1440p (Res. Vertical) / 180p (Res. Celeste) = **x8**
        !!! warning "Calidad variable"
            xBRZ usa una cuadrícula fija para escalar, lo que hace que funcione bien prácticamente solo en juegos de [estilo retro](#lista-de-juegos), y no siempre, debido a que la cuadrícula del juego puede moverse respecto a la pantalla
    === "CRT"
        - Activa `Advanced CRT`
        - En los ajustes de la parte inferior:
            - `Amount`: A gusto
            - [Opcional] `Resolution`: Multiplicador (Resolución de pantalla / Resolución del pixel art).
        !!! question "¿CRT y xBRZ / 2D Scaler?"
            Debido al efecto que generan ambos filtros no parece que haya beneficio por usar ambos a la vez, pero siéntete libre de probar.  


---
# Información adicional (Info opcional)  
## Estilo de renderizado 
Básicamente hay "2" maneras de renderizar un juego pixel art.  
[Explicación, 3 min.](https://www.youtube.com/watch?v=jguyR4yJb1M)  
=== "Estilo Retro"  
    - Todos los pixeles del juego se alinean en una sola cuadrícula.
    - Similar a como funcion juegos viejos.
    - Equivalente a renderizar en menor resolución y **escalar**  .
        - Este escalado es el que se puede usar para eliminar el "Pixel art" en el filtro xBRZ .
    - Pixela automáticamente modelos en 3D para mantener la estética.
    !!! success "Mejores resultados"
        Juegos que sigan el "Estilo Retro" son los que darán mejores resultados con los filtros de escalado.   
=== "Estilo Moderno"  
    - Los pixeles no se alinean una cuadrícula .
    - Respeta la resolución de pantalla.
        - Con lo que un filtro de escalado como xBRZ no podrá funcionar correctamente.  
    - Movimiento suave de cámara.
    - Usar filtros de escalado puede no ser eficaz o generar artefactos en movimiento.
    !!! warning "Calidad imprevisible"
        Juegos con este método puede no ser buenos candidatos a usar xBRZ o filtro de CRT, pudiendo generar parpadeo o artefactos en movimiento o quedando "desenfocados". El filtro 2DScaler debería no tener problemas como este.

#### Antialiasing y Pixel Art (Info opcional)  

![](/assets/AA_y_escalado.webp)

Al usar resoluciones que no sean múltiplos del Pixel Art del juego ocurrir dos cosas
=== "Con antialiasing"
    - Bordes difuminados  
    - Los pixeles no están definidos, afectando a los filtros como xBRZ
=== "Sin antialiasing"
    - Bordes pixelados  
    - Produce píxeles de distinto tamaño, lo cuál impide usar filtros de escalado correctamente
!!! info "Resolución proporcional"
    Para usar un filtro como xBRZ o CRT es recomendable configurar el juego para que use una resolución que sea múltiplo del Pixel Art.  
    En caso de que tu pantalla no lo sea, prueba a seleccionar una resolución inferior en el juego y comprueba los resultados:  
        - En Hyper Light Drifter, en vez de x2,6667 @ 1440p, prueba x2 @ 1080p.



---

## Lista de Juegos


| Juegos                | API gráfica   | Estilo    | Res. Pixel Art   | Notas |
| ---                   | ---           | ---       | ---               | ---   |
| Celeste               | DirectX 11    | Retro     | 180p      | Contiene segmentos en 3D  |
| Hyper Light Drifter   | DirectX 9     | Retro*    | 540p      |
| Stardew Valley        | OpenGL        | Moderno   | ---p      | Zoom hace variar |
| Undertale             | DirectX 9     | Moderno   | 240p      |
| Terraria              | DirectX 9     | Moderno   | 360p      |
| Dead Cells            | DirectX 11    | Moderno   | 360p      |
| Enter the Gungeon     | DirectX 11    | Moderno   | 288p      |
| Wildfire              | DirectX 9     | Moderno   | 540p      |
| Moonlighter           | DirectX 11    | Moderno   | 720p      |
| Children of Morta     | DirectX 11    | Retro*    | 720p      |

`*`: Puede no ser correcto.  
!!! info "Encontrar la API gráfica"
    Para la API gráfica de otros juegos se puede buscar en Google, en los requisitos mínimos del juegos (en [Steam](https://store.steampowered.com) a veces aparece) o en [PCGW](https://www.pcgamingwiki.com).  
    Otra opción más avanzada es usar el overlay de MSI Afterburner / HWinfo64 y mostrar la API
!!! tip "Emuladores"
    Juegos retro en emuladores, por definición, usan el estilo retro y se benefician totalmente de los filtros de escalado.