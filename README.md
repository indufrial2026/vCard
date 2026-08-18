# Tarjeta digital — Adrián Liévano · Grupo Indufrial

Sitio de una sola página, publicado con GitHub Pages. Sin frameworks, sin build:
HTML + CSS puro. Editar y publicar es literalmente editar el archivo y hacer commit.

## Estructura

```
/
├── index.html              ← todo el contenido y los links viven aquí
├── style.css                ← todo el diseño vive aquí
├── assets/
│   ├── AdrianLievano.vcf    ← archivo de contacto (botón "Contacto")
│   ├── img/
│   │   ├── logo.png         ← logo Indufrial (header)
│   │   └── avatar.jpg       ← foto de Adrián (reemplazar cuando la tengas)
│   └── catalogos/
│       ├── refrigeracion.pdf
│       ├── congelacion.pdf
│       ├── vitrina-horizontal.pdf
│       ├── botelleros.pdf
│       ├── importados.pdf
│       ├── vending.pdf
│       ├── maquinas-cafe.pdf
│       └── one-pager-corporativo.pdf
```

## Cómo reemplazar la foto de Adrián

1. Nombra el archivo exactamente `avatar.jpg` (o cambia la extensión en `index.html`,
   línea `<img class="hero__avatar" src="assets/img/avatar.jpg" ...>`).
2. Súbelo a `assets/img/`, reemplazando el que existe.
3. Recomendado: foto cuadrada, mínimo 400×400px, buena luz, fondo simple.

## Cómo subir un catálogo nuevo

El nombre del archivo debe coincidir **exactamente** con lo que espera `index.html`.
Ver la tabla completa en la sección "Subir catálogos" más abajo.

## Cómo editar textos, teléfono o correo

Todo el contenido visible está en `index.html`. Busca el texto que quieras cambiar
y edítalo directamente — no hay ningún sistema de plantillas de por medio.

- Teléfono: aparece en varios `href="tel:..."` y `href="https://wa.me/57..."`.
  Si cambia el número, reemplázalo en los 3 lugares donde aparece
  (Llamar, WhatsApp principal, Agendar llamada) y también en `AdrianLievano.vcf`.
- Correo: aparece en `href="mailto:..."` y en `AdrianLievano.vcf`.
- Mensajes pre-cargados de WhatsApp: son la parte del link después de `?text=`.
  Está codificado en URL (los espacios son `%20`, las tildes son `%C3%A1`, etc.).
  Si quieres cambiar el mensaje, lo más fácil es escribirlo normal en
  https://www.urlencoder.org/ y pegar el resultado ahí.

## Publicación (GitHub Pages)

Ver el tutorial paso a paso completo que te compartí aparte
("Tutorial_GitHub_Pages.md"). Resumen rápido una vez el repo está creado y
conectado a Pages:

```bash
git add .
git commit -m "Actualiza catálogo de congelación"
git push
```

GitHub Pages se actualiza solo, 30–60 segundos después del push.
