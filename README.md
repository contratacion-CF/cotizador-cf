# Cotizaciones CF (sin servidor)

Esta es una aplicación **100% estática** (HTML/CSS/JS) que funciona en el navegador y guarda la información localmente (IndexedDB).

## Qué conserva del Excel
Tu archivo tiene estas hojas y lógica:
- **Formato**: plantilla con campos (fecha, número de cotización, cliente) y una tabla de ítems.
- **Clientes**: tabla con columnas *Numero, Nombre, Direccion, Rfc*.
- **Productos**: tabla con columnas *Codigo, Descripcion, Precio de venta*.

El Excel autocompleta con **VLOOKUP**:
- Cliente por *Numero* → Nombre / Dirección / RFC.
- Producto por *Código* → Descripción / Precio.
- Importe por línea = Cantidad × Precio.

La web reproduce exactamente esto con autocompletado y cálculo automático.

## Cómo usar
1. Abre `index.html` en tu navegador (Chrome/Edge recomendado).
2. Inicia sesión con **admin / admin** (por defecto).
3. En **Config**, define prefijo, longitud de ceros, consecutivo e IVA.
4. Importa tus datos desde Excel: botón **Importar Clientes/Productos desde Excel**.
5. Crea una nueva cotización y guarda.
6. Imprime para generar PDF (usa “Guardar como PDF” en el diálogo de impresión).

## Hospedaje gratuito (opcional)
- GitHub Pages
- Netlify
- Cloudflare Pages

> Importante: el hospedaje no cambia que los datos se guardan localmente por usuario/navegador.

## Respaldo
- Exportar respaldo (.json)
- Importar respaldo (admin)

