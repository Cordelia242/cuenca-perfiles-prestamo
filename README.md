# Perfiles de préstamo para Cuenca

Catálogo público de perfiles de préstamo consumido por la app Cuenca.

Cada perfil vive en su propia carpeta:

```
perfiles/<id>/perfil.json      # condiciones del perfil
perfiles/<id>/descripcion.md   # descripción en Markdown (obligatoria, no vacía)
```

- `<id>` usa solo minúsculas, dígitos y guiones, y coincide con el campo `id` de `perfil.json`.
- `perfil.json` incluye `version` (entero positivo), `id`, `nombre`, `categoria`, `tags`, `moneda`, `familiaId`, `padre` y `contrato`.
- Los IDs no pueden repetirse entre carpetas y el linaje (`padre`) no puede formar ciclos.

La app lista `perfiles/` con la API de contenidos de GitHub y descarga ambos archivos de cada carpeta desde la rama `main`.
