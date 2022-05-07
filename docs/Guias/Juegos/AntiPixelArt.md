
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
##### Estilo Moderno:  
    - Los pixeles no se alinean  
    - Respetan la resolución de pantalla  

Juegos que sigan el "Estilo Retro" son los que darán mejores resultados con los filtros de escalado y CRT.  

---

### Lista de APIs gráficas y Estilos de renderizado



| Juegos                | API        | Estilo    |    
| ---                   | ---        | ---       |
| Stardew Valley        | OpenGL     | Moderno   |
| Celeste               | | Retro|
| Hyper Light Drifter| | Retro|
| Undertale| | Moderno|
| Terraria| | Moderno|

Para otros juegos se puede buscar en Google, en los requisitos mínimos del juegos (en [Steam](https://store.steampowered.com) aparece) o en [PCGW](https://www.pcgamingwiki.com).  
Juegos Retro en emuladores, por definición, usan el estilo retro y se benefician de los filtros de escalado.