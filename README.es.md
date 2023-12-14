# Traducir acción Léame

## Traducción LÉAME

-   [Inglés](README.md)
-   [Chino simplificado](README.zh-CN.md)
-   [chino tradicional](README.zh-TW.md)
-   [hindi](README.hi.md)
-   [Francésa](README.fr.md)
-   [árabe](README.ar.md)

**Acción de GitHub para traducir el Léame a cualquier idioma**

Esta es una acción de GitHub que traduce automáticamente el archivo Léame de su repositorio a un idioma específico.

_Una presentación para el[DEV: ¡Acciones de GitHub para código abierto!](https://dev.to/devteam/announcing-the-github-actions-hackathon-on-dev-3ljn) hackathon_

## Configuración

1.  **Agregar un archivo de flujo de trabajo**a su proyecto (p. ej.`.github/workflows/readme.yml`):

```yaml
name: Translate README

on:
  push:
    branches:
      - main
      - master
jobs:
  build:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v2
      - name: Setup Node.js
        uses: actions/setup-node@v1
        with:
          node-version: 12.x
      # ISO Langusge Codes: https://cloud.google.com/translate/docs/languages  
      - name: Adding README - Chinese Simplified
        uses: dephraiim/translate-readme@main
        with:
          LANG: zh-CN
      - name: Adding README - Chinese Traditional
        uses: dephraiim/translate-readme@main
        with:
          LANG: zh-TW
      - name: Adding README - Hindi
        uses: dephraiim/translate-readme@main
        with:
          LANG: hi
      - name: Adding README - Arabic
        uses: dephraiim/translate-readme@main
        with:
          LANG: ar
      - name: Adding README - French
        uses: dephraiim/translate-readme@main
        with:
          LANG: fr
```

## Configuración

### Opciones

Puede configurar la acción aún más con las siguientes opciones:

-   `LANG`: El idioma al que desea traducir su archivo Léame. El valor predeterminado es chino simplificado. (Soy ghanés) Los idiomas admitidos se pueden encontrar a continuación.
    (por defecto:`zh-CH`) (requerido:`false`)

## Idiomas admitidos

Los idiomas admitidos se pueden encontrar aquí<https://cloud.google.com/translate/docs/languages>

### Asuntos

Controlar[aquí](https://github.com/dephraiim/translate-readme/issues/1)para cuestiones relacionadas con esta acción.

### Desarrollo

¡Sugerencias y contribuciones siempre son bienvenidas!

### LICENCIA

[CON](./LICENSE)
