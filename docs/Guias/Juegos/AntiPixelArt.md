
# Eliminar Pixel Art [WIP]
## Instalar y usar Reshade
[Descargar](https://reshade.me/) y ejecutar el instalador de Reshade

Esperar a que cargue la lista de programas o añadir manualmente el ejecutable del programa. Clicar `Next`.

Seleccionar API gráfica [ver más abajo].  
Seleccionar `Install`.  
En la casilla de abajo sustituir `Enter ZIP download link to custom repository here` por `https://github.com/Linx-ESP/Reshade/archive/refs/heads/main.zip`

---

### Estilo de renderizado 
Básicamente hay "2" maneras de renderizar un juego pixel art.  
[Explicación, 3 min.](https://www.youtube.com/watch?v=jguyR4yJb1M)  
##### Estilo Retro:  
    - Los pixeles del juego se alinean a una cuadrícula
    - Similar a como funcionaban antiguamente  
    - Equivalente a renderizar en menor resolución y escalar*  
        - Este escalado es el que se puede interceptar para eliminar el "Pixel art"  
    - Animaciones 3D pixeladas perfectamente
##### Estilo Moderno:  
    - Los pixeles no se alinean  
    - Respetan la resolución de pantalla  
    - Movimiento suave de cámara
    - Puede ser un juego 3D simulando ser 2D

Juegos que sigan el "Estilo Retro" son los que darán mejores resultados con los filtros de escalado y CRT.  

---

### Lista de Juegos



| Juegos                | API gráfica   | Estilo    | Res. Interna**| Mult. 1440p   | Notas |
| ---                   | ---           | ---       | ---           | ---           | ---   |
| Stardew Valley        | OpenGL        | Moderno   | 360p          | x4            | |
| Celeste               | DirectX 11    | Retro     | 180p          | x8            | Contiene segmentos en 3D  |
| Hyper Light Drifter   | DirectX 10*   | Retro     | | | |
| Undertale             |               | Moderno   | | | |
| Terraria              | DirectX 9     | Moderno   | 360p          | x4            | |
| Dead Cells            | DirectX 11    | Moderno   | 360p          | x4            | |
| Enter the Gungeon     | DirectX 11    | Moderno   | 288p          | x5            | |


`*`: Juegos que no he comprobado personalmente, puede no ser correcto.  
`**`: La resolución interna se ha calculado calculando el tamaño de los pixeles del juego en una pantalla 1440p.  
    Es posible que haya juegos que mantengan el multiplicador fijo y no la "resolución" del pixel art, aunque sería raro.

Para la API gráfica de otros juegos se puede buscar en Google, en los requisitos mínimos del juegos (en [Steam](https://store.steampowered.com) a veces aparece) o en [PCGW](https://www.pcgamingwiki.com).  

Juegos retro en emuladores, por definición, usan el estilo retro y se benefician totalmente de los filtros de escalado.