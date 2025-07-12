# 🎼 Creador de Pistas Musicales Fáciles

> Genera melodías rápidamente con un piano virtual, selección de instrumento y guardado/carga en JSON.

![Vista previa](Captura%20de%20pantalla%202025-07-12%20142522.png)

## Tabla de contenidos

1. [Características](#características)
2. [Instalación](#instalación)
3. [Uso](#uso)
4. [Estructura del proyecto](#estructura-del-proyecto)
5. [Tecnologías](#tecnologías)
6. [Contribuciones](#contribuciones)
7. [Créditos](#créditos)
8. [Licencia](#licencia)

---

## Características

* **Piano virtual** de dos octavas (C4–B5) con teclas blancas y negras.
* **Selector de instrumento**: flauta, piano, violín, clarinete, guitarra, trompeta y saxofón.
* **Control de duración** de notas (16ª, 8ª, negra, negra puntillo, blanca, blanca puntillo).
* **Silencios** y cambio rápido de duración con un clic en la secuencia.
* **Reproducción** con animación de la nota actual.
* **Guardar** melodías en un archivo JSON y **cargar** melodías previamente guardadas.
* **Prueba instantánea** de una nota dentro de la secuencia antes de agregarla.
* **Responsivo** y sin dependencias de *build*: basta con un servidor estático.

## Instalación

1. **Clona** el repositorio:

```bash
git clone https://github.com/leonardos4enz/creadora-pistas-musicales-faciles.git
cd creadora-pistas-musicales-faciles
```

2. Abre la carpeta en tu editor/IDE favorito y lanza un servidor local con la extensión **Live Server** (VS Code) o cualquier servidor HTTP ligero.

> Con Live Server simplemente haz clic derecho sobre `index.html` y elige **Open with Live Server**. Cuando guardes cambios el navegador se recargará automáticamente.
>
> También puedes abrir `index.html` directamente, pero algunos navegadores bloquean la carga de los *soundfonts* remotos por CORS; usar Live Server evita ese problema.

¡Listo! Visita la URL que te indique Live Server (normalmente [http://127.0.0.1:5500](http://127.0.0.1:5500)) y empieza a crear melodías.

## Uso

1. Selecciona la **duración** deseada en el desplegable.
2. Toca una nota en el piano virtual para **añadirla** a la secuencia o presiona *Añadir silencio* para agregar una pausa.
3. Cambia la **duración** de una nota existente haciendo clic sobre ella.
4. Usa **Reproducir** para escuchar tu melodía y **Detener** para parar.
5. **Guardar** descargará un archivo `.json` con la secuencia. Después podrás **Cargar** para restaurarla.
6. Cambia de **instrumento** cuando quieras; el botón *Reproducir* se habilita una vez cargado el soundfont.

## Estructura del proyecto

```
├── index.html       # Archivo principal (HTML, CSS y JS en un solo documento)
├── README.md        # Este archivo
└── ...              # Otros assets (capturas, melodías .json, etc.)
```

> El proyecto es deliberadamente *self‑contained*: basta con `index.html` para trabajar o hacer un fork y personalizar.

## Tecnologías

* **[Tone.js](https://tonejs.github.io/)** – Motor de audio y secuenciación Web Audio API.
* **[FluidR3\_GM SoundFonts](https://github.com/gleitz/midi-js-soundfonts)** – Muestras de instrumentos en formato *mp3*.
* **HTML5 + CSS3 + JavaScript (ES6)** – Sin frameworks de front‑end ni bundlers.
* **Live Server** – Servidor local conveniente (o cualquier servidor estático equivalente).

## Contribuciones

¡Las *pull requests* son bienvenidas! Para cambios sustanciales, abre primero un *issue* y discute qué te gustaría mejorar.

1. Haz un *fork* del proyecto.
2. Crea tu rama de características: `git checkout -b mi-feature`.
3. Haz *commit* de tus cambios: `git commit -m "Añadir nueva característica"`.
4. Sube la rama: `git push origin mi-feature`.
5. Abre un *Pull Request*.

## Créditos

* **[@leonardos4enz](https://github.com/leonardos4enz)** – Creación y mantenimiento principal.
* Sonidos cortesía de **FluidR3\_GM** SoundFont (licencia MIT).
* Iconos *emoji* de Twemoji.

## Licencia

Distribuido bajo la licencia **MIT**. Consulta `LICENSE` para más información.
