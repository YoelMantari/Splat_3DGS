# Instrucciones para ejecutar el visor `splat` localmente

Este visor permite visualizar escenas 3D generadas mediante Gaussian Splatting directamente en tu navegador usando WebGL.

## ✅ Requisitos

- Navegador moderno (preferiblemente **Google Chrome** o **Edge**)
- Servidor local (puede ser Python, Node.js o cualquier servidor estático)

## 🚀 Pasos para ejecutar localmente

1. **Clona el repositorio**

```bash
git clone https://github.com/antimatter15/splat.git
cd splat
```

2. **Inicia un servidor local**

### Opción 1: Usando Python (recomendado)

```bash
# Python 3.x
python3 -m http.server 8000
```

### Opción 2: Usando Node.js con `http-server`

```bash
npm install -g http-server
http-server -p 8000
```

3. **Abre el visor en tu navegador**

Abre tu navegador y accede a:

```
http://localhost:8000
```

4. **Carga archivos**

- Arrastra y suelta un archivo `.ply` procesado con Gaussian Splatting.
- (Opcional) Arrastra un archivo `cameras.json` para cargar vistas predefinidas.

## 🎮 Controles

| Acción                  | Teclas                         |
|-------------------------|--------------------------------|
| Mover (adelante/atrás)  | Flechas ↑ ↓                   |
| Strafe (izquierda/derecha) | Flechas ← →                |
| Girar cámara            | `a`/`d` (horizontal), `w`/`s` (vertical) |
| Rotar cámara            | `q` / `e`                     |
| Orbitar                 | `i`, `k`, `j`, `l`             |
| Cambiar cámara          | `0`-`9`, `+`, `-`              |
| Guardar vista a URL     | `v`                            |

## 🌐 Cargar archivo .splat por URL

También puedes cargar archivos `.splat` remotos usando:

```
http://localhost:8000/?url=archivo.splat
```

Asegúrate de que el archivo esté accesible públicamente con CORS habilitado.

## 📝 Notas

- El visor está hecho en **JavaScript** con **WebGL 1.0**, sin dependencias externas.
- La conversión de `.ply` a `.splat` se realiza automáticamente al arrastrar el archivo.

---

© Proyecto original por [antimatter15](https://github.com/antimatter15/splat)