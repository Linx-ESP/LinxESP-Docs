
# Eliminar Pixel Art [WIP]
## Instalar y usar Reshade
- [Descarga](https://reshade.me/) y ejecuta el instalador de Reshade
- Busca el juego o añadelo manualmente. Haz click en `Next`.
- Selecciona la API gráfica que corresponda [ver más abajo].  
- Selecciona `Install`.  
- En la casilla de abajo sustituye `Enter ZIP download link to custom repository here` por `https://github.com/Linx-ESP/Reshade/archive/refs/heads/main.zip` y haz clock en `Add`. Asegúrate que `main.zip` está marcado en la lista.
- Haz click en `Next` para continuar y `Finish` para acabar.  

### Una vez en el juego:  
 - Pulsa la tecla `Home` desplegar el overlay de Reshade.
 - Selecciona `Continue` si quieres ver el tutorial (5 pasos), `Skip the tutorial` si no.
 - Activa `xBRZx4`
 - En la parte inferior, `Strength` equivale al multiplicador de escalado.
    - Multiplicador = Resolución vertical del monitor / Resolución de la cuadrícula del pixel art
    - Ejemplo: Monitor 2560x1440p en Celeste sería  
        - 1440p (Res. Vertical) / 180p (Res. Celeste) = **x8** 

---

## Estilo de renderizado 
Básicamente hay "2" maneras de renderizar un juego pixel art.  
[Explicación, 3 min.](https://www.youtube.com/watch?v=jguyR4yJb1M)  
=== "Estilo Retro"  
    - Todos los pixeles del juego se alinean en una sola cuadrícula
    - Similar a como funcion juegos viejos 
    - Equivalente a renderizar en menor resolución y **escalar**  
        - Este escalado es el que se puede usar para eliminar el "Pixel art"  
    - Pixela automáticamente modelos en 3D para mantener la estética
    - Juegos que sigan el "Estilo Retro" son los que darán mejores resultados con los filtros de escalado.   
=== "Estilo Moderno"  
    - Los pixeles no se alinean una cuadrícula 
    - Respetan la resolución de pantalla  
    - Movimiento suave de cámara
    -  Usar filtros de escalado puede no ser eficaz o generar artefactos en movimiento.

#### Antialiasing y Pixel Art  

![Test](assets/AA_y_escalado.webp)


Al usar resoluciones que no sean múltiplos del Pixel Art del juego ocurrir dos cosas
=== "Con antialias"
    Suaviza los bordes
=== "Sin antialiasing"
    Bordes pixelados  
    Produce píxeles de distinto tamaño, lo cuál impide usar filtros de escalado correctamente
- Para usar un filtro como xBRZ es altamente recomendable configurar el juego para que use una resolución que sea múltiplo  



---

## Lista de Juegos


| Juegos                | API gráfica   | Estilo    | Res. Cuadrícula   | Notas |
| ---                   | ---           | ---       | ---               |  ---   |
| Celeste               | DirectX 11    | Retro             | 180p       | Contiene segmentos en 3D  |
| Hyper Light Drifter   | DirectX 9     | Retro             | 540p      |
| Stardew Valley        | OpenGL        | Moderno           | 360p      |
| Undertale             | DirectX 9     | Moderno           | 240p      |
| Terraria              | DirectX 9     | Moderno           | 360p      |
| Dead Cells            | DirectX 11    | Moderno           | 360p      |
| Enter the Gungeon     | DirectX 11    | Moderno           | 288p      |
| Wildfire              | DirectX 9     | Moderno / No AA   | 540p      |
| Moonlighter           | DirectX 11    | Moderno / No AA   | 720p      |
| Children of Morta     | DirectX 11    | Retro*  / No AA   | 720p      |

`*`: Puede no ser correcto.  

Para la API gráfica de otros juegos se puede buscar en Google, en los requisitos mínimos del juegos (en [Steam](https://store.steampowered.com) a veces aparece) o en [PCGW](https://www.pcgamingwiki.com).  

Juegos retro en emuladores, por definición, usan el estilo retro y se benefician totalmente de los filtros de escalado.