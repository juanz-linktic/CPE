# Modelo de Atención al Cliente — CPE

Presentación web (una sola página, sin dependencias de build) del modelo de atención
de la Mesa de Ayuda de LinkTIC para Computadores Para Educar.

## Contenido

| Archivo | Descripción |
|---|---|
| `index.html` | Sitio completo: HTML, CSS, JS y los dos diagramas en SVG inline. No requiere assets externos salvo la fuente Inter (Google Fonts). |
| `vercel.json` | Configuración de despliegue (URLs limpias + cabeceras de seguridad). |

## Desplegar en Vercel

**Opción A — arrastrar y soltar (más rápido)**

1. Entrar a https://vercel.com/new
2. Arrastrar esta carpeta completa sobre el área de carga.
3. Framework Preset: **Other**. Sin build command, sin output directory.
4. Deploy.

**Opción B — desde la terminal**

```bash
npm i -g vercel
cd <esta-carpeta>
vercel          # despliegue de vista previa
vercel --prod   # despliegue a producción
```

**Opción C — desde GitHub**

1. Subir esta carpeta a un repositorio.
2. En Vercel: *Add New… → Project → Import* el repositorio.
3. Framework Preset: **Other**. Deploy.

## Dominio

En el proyecto de Vercel: *Settings → Domains* para asignar un dominio propio
(por ejemplo `modelo-cpe.linktic.com` mediante un registro CNAME).

## Notas de mantenimiento

- Todo el contenido y los estilos están en `index.html`; para cambiar textos, buscar
  la sección correspondiente (`id="compromisos"`, `id="flujo"`, etc.).
- La paleta se controla con variables CSS en `:root` (`--violet`, `--blue`, `--teal`,
  `--bg`, `--surface`…). Cambiar allí actualiza todo el sitio.
- Los diagramas son SVG inline: escalan sin pérdida y se pueden editar como texto.
- El botón "Descargar PDF" usa la impresión del navegador; hay una hoja de estilos
  `@media print` que convierte el sitio a fondo blanco, una sección por página.
