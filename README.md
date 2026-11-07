# 🎧 DJ Bryan — tu celular es la consola, tu laptop es el equipo de sonido

DJ Bryan es un DJ con inteligencia artificial que funciona en el navegador:

- **Laptop (`index.html`)**: reproduce la música, mezcla y muestra en grande qué hacer (Vista guía).
- **Celular (`control.html`)**: es tu consola táctil, con platos para scratch, pads, crossfader, mixer, efectos y tu música.

Los dos quedan **sincronizados en tiempo real y en ambos sentidos**: lo que mueves en el celular cambia en la laptop, y lo que cambia en la laptop (la IA, el teclado o el mouse) se ve al instante en el celular.

---

## 1. Publicarlo en GitHub Pages (una sola vez, ~5 minutos)

1. Entra a <https://github.com> e inicia sesión (o crea una cuenta gratis).
2. Arriba a la derecha: **+ → New repository**.
   - Nombre: `dj-bryan`
   - Marca **Public**
   - Clic en **Create repository**.
3. En el repositorio nuevo, clic en **uploading an existing file** (o **Add file → Upload files**).
4. Arrastra **todos** los archivos de esta carpeta: `index.html`, `control.html`, `manifest.webmanifest`, `icon.svg`, `README.md` y `.nojekyll` (si no ves `.nojekyll`, no pasa nada).
5. Clic en **Commit changes**.
6. Ve a **Settings → Pages**.
   - En **Source** elige **Deploy from a branch**.
   - En **Branch** elige **main** y **/(root)**, luego **Save**.
7. Espera 1–2 minutos y recarga la página. Arriba aparecerá tu dirección, por ejemplo:
   **`https://TU-USUARIO.github.io/dj-bryan/`**

> Para actualizarlo más adelante, sube los archivos nuevos al mismo repositorio (reemplazan a los anteriores).

---

## 2. Usarlo en la fiesta

1. **Laptop:** abre `https://TU-USUARIO.github.io/dj-bryan/` en **Chrome o Edge**.
2. Carga tus canciones con **📂 Elegir archivos** o **🗂 Elegir carpeta**. La música **no se sube a internet**: se queda en tu laptop.
3. Presiona **📱 Celular**. Aparece un **código QR** y un **código de 6 letras**.
4. **Celular:** escanea el QR con la cámara. Se abre la consola y se conecta sola. (También puedes abrir `.../dj-bryan/control.html` y escribir el código.)
5. En la laptop se activa la **🖥 Vista guía**: instrucciones grandes, ondas, pulso y cuenta regresiva.
6. Desde el celular, ve a **🎉 Fiesta → ▶ Empezar fiesta**.

**Tip:** en el celular, usa *Agregar a la pantalla de inicio* para abrirlo como app a pantalla completa.

### ¿Qué necesito?

- **Internet en los dos equipos.** Pueden estar en redes distintas (por ejemplo, el celular con datos y la laptop con Wi-Fi).
- **Nada de cable ni Bluetooth.** El servidor gratuito de PeerJS solo sirve para presentar los dos equipos; luego la conexión va directo entre ellos (WebRTC) y solo viajan órdenes, nunca la música.
- **En la misma Wi-Fi responde más rápido** (normalmente entre 20 y 80 ms). La latencia se ve arriba en el celular.
- **Haz un clic en la laptop** al menos una vez para activar el sonido (los navegadores lo exigen). El celular te avisa si falta.

### Funciones del celular

| Pestaña | Qué tiene |
|---|---|
| 🎚 **Decks** | Plato (scratch con VINILO, empujar sin VINILO), PLAY, CUE, SYNC, 8 pads (HOT CUE / LOOP / ROLL / SALTO), loops IN/OUT/½/×2, ECO, REVERSA, FRENO, GIRO. Puedes ver Deck A, Deck B o **A + B** (mejor con el celular horizontal). |
| 🎛 **Mixer** | Ganancia, agudos, medios, graves, filtro, tempo, empujar, volumen, 🎧 pre-escucha, TAP, /2, ×2 y cuadrícula. Doble toque en un control lo regresa al centro. |
| ✨ **FX** | Bocina, sirena, subida, boom, eco, grito, láser, palmas, scratch IA, y los efectos de cada deck. |
| 🎵 **Música** | Tus canciones, ordenadas de la que mejor encaja con lo que suena a la que menos. ⭐ marca la que la IA pondrá después. Botones A, B y + Cola. |
| 🎉 **Fiesta** | Empezar/pausar, modo (Piloto / Copiloto / Manual), momento de la fiesta, salvar la pista, grabar, largo de canciones, trucos IA y pre-escucha. |

Abajo siempre tienes el **crossfader** y el botón **⇄ Mezclar**.

**En modo 🎓 Copiloto:**
- Arriba en el celular aparece qué hacer y una cuenta regresiva.
- El control que debes tocar **se ilumina en verde**, y la app **cambia sola a la pestaña correcta**.
- En Android el celular vibra cuando toca un paso nuevo.
- Si no llegas a tiempo, la IA lo hace por ti (si tienes activada la red de seguridad).

**Dos celulares:** puedes conectar más de uno con el mismo código, por ejemplo uno para cada deck.

---

## 3. Problemas comunes

- **El celular dice “La laptop no responde”:** en la laptop presiona **📱 Celular** y revisa que tenga internet. El celular reintenta solo.
- **No aparece el QR:** escribe el código de 6 letras en el celular.
- **“Ese código ya está en uso”:** tienes DJ Bryan abierto en otra pestaña. Ciérrala o usa **🔄 Nuevo código**.
- **No conecta en la red del trabajo o la universidad:** algunas redes bloquean WebRTC. Prueba con los datos del celular o un hotspot.
- **No suena:** haz un clic en la pantalla de la laptop.
- **Abrí `index.html` con doble clic y no conecta:** desde un archivo local el celular no puede llegar. Usa la dirección de GitHub Pages.

---

Hecho con Web Audio API (motor propio con AudioWorklet) y PeerJS (WebRTC). Sin instalaciones.
