![[Pasted image 20250821003325.png]]

Lo más importante es **seleccionar el Timeline frame rate** desde el inicio.

---

En DaVinci Resolve, las opciones de "Timeline frame rate" **determinan la velocidad de reproducción base de tu timeline (línea de tiempo) y afectan cómo se reproducen y procesan todos los clips en tu proyecto.** Aquí te explico las opciones más comunes:

**23.976 fps (23.98)**

- Estándar para cine digital y contenido cinematográfico
- Usado en producciones de películas y series de TV premium
- Ofrece esa "sensación cinematográfica" característica

**24 fps**

- Frame rate tradicional del cine en película
- Usado principalmente en producciones de cine artístico
- Muy similar al 23.976 pero técnicamente diferente

**25 fps**

- Estándar europeo (PAL)
- Común en televisión y video europeo
- Usado en muchos países fuera de América del Norte

**29.97 fps**

- Estándar americano para televisión (NTSC)
- Muy común en producciones de TV estadounidenses
- Técnicamente es 30 fps con "drop frame"

**30 fps**

- Frame rate "real" de 30 cuadros por segundo
- Común en contenido web y algunas producciones digitales
- Más fluido que 24fps pero menos "cinematográfico"

**50 fps / 59.94 fps / 60 fps**

- Frame rates altos para contenido muy fluido
- Usados en deportes, videojuegos, o contenido que requiere movimiento muy suave
- 50 fps es común en Europa, 60 fps en América

**Consideraciones importantes:**

- El frame rate del timeline debe coincidir idealmente con tu material fuente
- Si difieren, Resolve interpolará los frames (puede causar stuttering o motion blur)
- Para exportación, generalmente mantienes el mismo frame rate del timeline
- Cambiar el frame rate después puede requerir re-renderizar todo el proyecto

---

>[!info] Los clips **proxy** es un **clip de menor resolución** para trabajar más eficientemente.

---

En DaVinci Resolve, los formatos de "**Proxy media format**" en Project Settings > Optimized Media and Render Cache son **versiones de menor resolución y compresión más eficiente de tus clips originales**. Aquí están los formatos disponibles:

**ProRes Proxy**

- Codec de Apple optimizado para edición
- Excelente calidad/rendimiento balance
- Ideal para: Material 4K/8K, flujos de trabajo profesionales, sistemas Mac
- Ventaja: Mantiene buena calidad visual con archivos manejables

**DNxHR LB (Low Bandwidth)**

- Codec de Avid, muy comprimido
- Archivos muy pequeños
- Ideal para: Equipos con poco almacenamiento, material de resolución muy alta
- Ventaja: Máxima compresión manteniendo fluidez de edición

**DNxHR SQ (Standard Quality)**

- Versión de mayor calidad del DNxHR
- Balance entre calidad y tamaño
- Ideal para: Proyectos que requieren mejor preview quality
- Ventaja: Mejor calidad visual que LB sin comprometer mucho el rendimiento

**H.264**

- Formato universal muy comprimido
- Archivos pequeños pero requiere más CPU para decodificar
- Ideal para: Almacenamiento limitado, material web/móvil
- Desventaja: Puede ser lento en equipos menos potentes

**H.265 (HEVC)**

- Sucesor del H.264, mejor compresión
- Archivos aún más pequeños que H.264
- Ideal para: Material 4K+, cuando el espacio es crítico
- Requiere: Hardware relativamente moderno para decodificación fluida

**Consideraciones clave:**

- Los proxies se usan solo para edición, no afectan la exportación final
- ProRes Proxy y DNxHR son generalmente los más recomendados para edición profesional
- H.264/H.265 son buenos si el espacio de almacenamiento es limitado
- La elección depende de tu hardware, almacenamiento disponible y tipo de proyecto

**DNxHR HQ vs DNxHR HQX**

**DNxHR HQ (High Quality)**

- Submuestreo de color 4:2:2
- Profundidad de color de 8 bits
- Bitrate aproximado: 145 Mbps (1080p), 220 Mbps (4K)
- Tamaño de archivo moderado
- Ideal para: La mayoría de proyectos profesionales estándar

**DNxHR HQX (High Quality eXtended)**

- Submuestreo de color 4:2:2
- Profundidad de color de **10 bits**
- Bitrate aproximado: 185 Mbps (1080p), 285 Mbps (4K)
- Archivos ~25-30% más grandes que HQ
- Ideal para: Material HDR, gradaciones de color extensas, post-producción pesada

**Diferencias prácticas:**

**Información de color:**

- HQX preserva más información de color (10 bits vs 8 bits)
- Mejor para evitar banding en gradientes y cielos
- Más headroom para corrección de color agresiva

**Tamaño de archivo:**

- HQX genera archivos notablemente más grandes
- Requiere más espacio de almacenamiento y ancho de banda

**Casos de uso:**

- **Usa HQ si:** Trabajas con material Rec.709 estándar, espacio limitado, flujo básico de color
- **Usa HQX si:** Trabajas con Log/RAW, HDR, planeas gradación extensiva, tienes espacio suficiente

**Recomendación:** Si te sugirieron DNxHR HQ, probablemente es suficiente para tu proyecto. HQX solo vale la pena si específicamente necesitas la profundidad de 10 bits para tu flujo de trabajo de color.

# [[Color management]]