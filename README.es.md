[English](README.md) · **Español** · [Français](README.fr.md) · [Deutsch](README.de.md) · [日本語](README.ja.md) · [中文](README.zh.md) · [हिन्दी](README.hi.md)

# U-MA Escalas

Un laboratorio de escalas de piano: elegís una tónica y cualquiera de las **61 escalas**, y la app te muestra sus notas e intervalos, cómo digitarla con las dos manos, sus arpegios, los acordes que viven adentro, y te deja encadenar esos acordes en una progresión que suena con buena conducción de voces.

**▶ Abrir la app:** https://buenosairesfront.github.io/escalas/

No hay que instalar nada. La interfaz está en castellano.

## Cómo funciona

La página es una hoja técnica en cinco secciones numeradas, con un **monitor** arriba (un teclado que enciende lo que suena, más lecturas de escala, nota, grado y acorde) y una **barra de transporte** fija abajo.

### 01 · Escala
- **Tónica:** las 12 notas (las teclas negras muestran las dos grafías, por ejemplo Do♯ / Re♭).
- **Familia:** mayor y sus modos, menor melódica, menor armónica, mayor armónica, pentatónicas y blues, simétricas, bebop y del mundo. O escribí en **Buscar escala**. Cada tarjeta muestra la forma de la escala como 12 puntos.
- **Resumen:** el nombre grande, cada nota bien escrita con su grado (1, ♭3, ♯4…), una barra de colores con los pasos entre notas (S semitono, T tono, 1½ tono y medio, 2T dos tonos), **la escala en partitura** y un **reloj** con su forma en el círculo de 12 notas.

### 02 · Teclado y digitación
La escala en un teclado grande con un círculo de color y el número de dedo en cada tecla (pulgar, índice, medio, anular, meñique), para la mano derecha, la izquierda o las dos. La vista cambia entre **Teclado** y **Pentagrama**. Abajo, una tabla con cada nota y su dedo. Las escalas mayores y menores usan la digitación **tradicional**; para el resto la app **calcula** una (busca la que tiene menos estiramientos incómodos y menos pulgares en teclas negras) y la marca como calculada.

### 03 · Arpegios
Elegís el **grado**, el **tipo** (tríada, con 7ª o por cuartas) y la **inversión**. Aparece el arpegio en dos octavas con su digitación, también tradicional o calculada.

### 04 · Armonización
La escala **apilada** en tríadas o cuatríadas: una tarjeta por grado con su número romano, nombre, calidad (mayor, menor, disminuido, aumentado…), la cadena de intervalos, un mini teclado y su función (T tónica, SD subdominante, D dominante) cuando la escala es mayor o menor. Cada tarjeta tiene **▶** para escucharla y **+ PROG** para sumarla a la progresión.

### 05 · Progresión
Hasta 16 acordes, un compás de 4/4 cada uno. Cargá una armada (I–IV–V–I, ii–V–I, I–vi–IV–V, I–V–vi–IV, vi–IV–I–V, I–vi–ii–V, andaluza, círculo de 5ª, todos los grados) o armá la tuya. Las voces **se mueven a la inversión más cercana**, como lo haría un pianista, y mientras suena un visor grande muestra el acorde actual y el compás.

### Transporte (barra de abajo)
- **Qué suena:** Escala, Arpegio, Armonizada (los acordes de la escala) o Progresión.
- **▶ / ■** y **loop**, tempo y metrónomo con luces de pulso.
- **Manos:** ambas, MD o MI. **Dirección:** ↑ o ↑↓. **Octavas:** 1 o 2.
- **Sonido:** Piano, EP (piano eléctrico) o Pad.

En la cabecera se cambian los nombres de nota (**Do Re Mi** o **C D E**) y el tema claro / oscuro. Todo lo que elegís queda recordado en el navegador.

## Por dentro

Un solo `index.html` sin dependencias. Cada escala está escrita como una fórmula de grados (`1 2 ♭3 4 5 6 ♭7`), así que cada nota sale con la letra correcta para la tónica elegida; los nombres de acordes y los números romanos se deducen de los intervalos reales. Las digitaciones calculadas salen de una búsqueda por programación dinámica sobre los cinco dedos de cada mano. Los dibujos son `<canvas>` y SVG; los tres sonidos se sintetizan en vivo con Web Audio (sin samples).

## Correr en local

Bajá `index.html` y abrilo, o serví la carpeta:

```
python3 -m http.server 8000
```

<!-- u-ma:more -->
**Más de U-MA:** todos los instrumentos y herramientas en un solo lugar → [muestrario U-MA](https://github.com/buenosairesfront/U-ma/blob/main/README.es.md)
<!-- /u-ma:more -->

## Créditos

Digitaciones tradicionales de escalas y arpegios, como se enseñan en los métodos de piano. App de U-MA サウンド · [Buenos Aires Front](https://www.instagram.com/buenos.aires.front/).
