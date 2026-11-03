# Cómo dejar funcionando el panel de Doblette (una sola vez)

La página es gratis y no usa base de datos: el menú vive en el archivo `menu.js`.
El panel (`admin.html`) edita ese archivo y lo publica en GitHub, donde se aloja la página.

## 1. Subir la página a GitHub Pages (gratis)

1. Crea una cuenta en https://github.com (o usa la tuya).
2. Crea un repositorio nuevo, por ejemplo `doblette-web`, **público**.
3. Sube todo el contenido de esta carpeta (`index.html`, `admin.html`, `menu.js`, la carpeta `img`).
4. En el repositorio: **Settings → Pages → Source: Deploy from a branch → `main` / root → Save**.
5. En 1–2 minutos la página queda en `https://jesusgarcia1371.github.io/doblette-web/`.
   El panel queda en `https://jesusgarcia1371.github.io/doblette-web/admin.html`.

## 2. Datos del panel

Ya están puestos en `admin.html`: usuario `jesusgarcia1371`, repositorio `doblette-web`, rama `main`.
Si usas otro nombre de repositorio, cámbialo en la línea `GITHUB_DEFAULT` (cerca del inicio del `<script>`).

## 3. Crear la clave de acceso para el negocio

1. En GitHub: foto de perfil → **Settings → Developer settings → Personal access tokens → Fine-grained tokens → Generate new token**.
2. Nombre: `Panel Doblette`. Caducidad: la más larga que permita (anota la fecha para renovarla).
3. **Repository access → Only select repositories →** `doblette-web`.
4. **Permissions → Repository permissions → Contents: Read and write**. Nada más.
5. Genera la clave y cópiala (empieza con `github_pat_`).

## 4. Conectar el panel en el negocio

En la computadora o celular de quien vaya a editar:
abrir el panel → **Conectar** → pegar la clave → **Conectar**. Se hace una sola vez por equipo.

Desde ahí solo usan **Guardar y publicar**.

## Bueno saber

- La clave solo sirve para cambiar esta página, nada más de tu cuenta.
- Sin la clave nadie puede publicar, aunque abra `admin.html`.
- Si la clave caduca, el panel avisa: crea una nueva (paso 3) y vuelve a conectar.
- Si la clave se pierde o alguien deja de trabajar en el negocio: bórrala en GitHub y crea otra.
- Sin conectar, el botón descarga `menu.js` para subirlo a mano al repositorio (respaldo).
