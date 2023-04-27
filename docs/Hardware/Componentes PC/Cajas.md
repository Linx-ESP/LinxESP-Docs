# Cajas / Chasis
Distintos factores a tener en cuenta a la hora de comprar una caja/chasis para un ordenador

## Esencial:
Requisitos que has de formar antes de empezar a buscar un chasis, basado en necesidades para el resto del sistema.

### Decidir formato:

- Torre completa / Full tower / Super tower. [Ejemplo](https://www.corsair.com/es/es/obsidian-1000d-case)
- Semitorre / Mid tower. [Ejemplo](https://www.pccomponentes.com/phanteks-eclipse-p360a-argb-cristal-templado-usb-30-blanca)
- Pequeño formato / SFF (Small Form Factor). [Ejemplo](https://www.jonsbo.com/en/products/N1.html)
- Otros:
    - Rack mounted / Armario de servidor. [Ejemplo](https://www.silverstonetek.com/es/product/info/server-nas/RM400/)
    - Orientado a NAS. [Ejemplo](https://www.silverstonetek.com/es/product/info/server-nas/CS381/)

#### Cómo hacer esta decisión

``` mermaid
graph LR
  B{Uso};
  B -->|Especifico| C[NAS o Rack];
  B -->|Genérico| D{Tamaño};
  D -->|Necesito mucho espacio| E[Extendida/Supertorre]
  D --->|Me da igual| F[Estándar/Semitorre]
  D -->|Necesito que ocupe poco| G[SFF]
```


1. Rack y NAS, para usos muy específicos  
    1. Rack si es para servidor y armario  
    2. NAS si es para usar bastantes discos duros y ciertas opciones para acceso físico
        - No es exclusivo para NAS, a veces también para HTPC  
2. El estándar y con más opciones es Semitorre  
    - Suficientes opciones de expansión sin ocupar espacio innecesario  
3. Si necesitas más espacio interno 
    - Torre completas o extendidas
        - Muchas opciones y espacio para expansión
        - Altamente compatible con refrigeraciones líquidas personalizadas
        - Dos sistemas en un mismo chasis
        - Nada para el hogar *debería* requerir este tipo de chasis
4. Si necesitas que ocupe menos espacio
    - SFF
        - Limitaciones en expansión, refrigeración
        - Restricciones en componentes, tanto por tamaño como por refrigeración
        - Precio más alto tanto del chasis, como de ciertos componentes

### Otros factores esenciales 
- Compatibilidad de tamaño con:
    - Ventilador del procesador (altura)
    - Tarjeta gráfica (largo, altura solo en modelos extremadamente grandes)
    - Formato de placa base (ATX, ITX, etc...)
- Compatibilidad de expansión:
    - Discos duros / bahías de 2,5" y 3,5"
    - Radiadores para refrigeraciones líquidas

---

## Factores a tener en cuenta
Básicamente, que factores hacen que sea un "mejor" producto

1. Refrigeración [IMPORTANTE]
    - Menor temperatura = Menos ruido y/o más rendimiento.
        - Dado como funcionan componentes modernos, si tienen un margen de temperaturas rendirán mejor.
        - En casos de que se sobrecalienten reducirán MUCHO su rendimiento para evitar dañarse.
    - Paneles frontales cerrados < Paneles con rejilla (como regla general).
    - Más ventiladores incluidos no es directamente mejor.
    - Ha de tenerse en cuenta el ruido.
        - Esto impide métodos de fuerza bruta, con ventiladores que suenen como un despegue

    [Gamers Nexus](https://www.youtube.com/c/GamersNexus) (entre otros) tiene mediciones de temperaturas a un dado nivel de sonido

2. Puertos
    - Puertos delanteros, tales como USB (tipo C), Jacks de audio
        - Comprobar si es compatible con la placa base (solo necesario para USB-C)

4. Iluminación
    - Presencia de RGB
    - Controladores y conectores propietarios

3. Espacio interno
    - Espacio de cara a ordenar cables, y opciones para hacerlo como ganchos o velcros incluidos
