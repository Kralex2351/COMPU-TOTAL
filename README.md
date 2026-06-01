# TechStore — Tienda de Tecnología

Tienda web estática para GitHub Pages. Paleta rojo, negro y blanco.

## 🚀 Cómo publicar en GitHub Pages

1. Crea un repositorio en GitHub (ej: `mi-tienda-tech`)
2. Sube todos los archivos de esta carpeta al repositorio
3. Ve a **Settings → Pages**
4. En **Source**, selecciona `main` branch y carpeta `/ (root)`
5. Guarda — en ~1 minuto tu tienda estará en:
   `https://TU_USUARIO.github.io/mi-tienda-tech`

---

## 📁 Estructura de archivos

```
tienda/
├── index.html          ← Página principal (no tocar)
├── css/
│   └── styles.css      ← Estilos (no tocar)
├── js/
│   ├── productos.js    ← ⭐ EDITA AQUÍ los productos
│   └── app.js          ← Lógica (no tocar)
└── images/
    └── logo.png        ← Sube tu logo aquí
```

---

## ✏️ Cómo editar productos (archivo `js/productos.js`)

### Agregar un producto nuevo

Copia este bloque y pégalo dentro del array `PRODUCTOS`:

```javascript
{
  id: "cat-999",              // ID único (no repetir)
  nombre: "Nombre del Producto",
  categoria: "procesadores",  // Ver lista de categorías abajo
  precio: 99.99,
  precioOriginal: 129.99,     // null si no hay descuento
  stock: 10,                  // 0 = agotado
  imagen: "images/foto.jpg",  // o URL externa
  descripcion: "Descripción corta del producto",
  promocion: false,           // true = aparece en Ofertas Flash
},
```

### Eliminar un producto

Borra el bloque completo `{ ... },` del producto.

### Cambiar precio / stock / imagen

Solo edita el valor del campo que quieras cambiar.

---

## 📂 Categorías disponibles

| Clave            | Nombre mostrado       |
|------------------|-----------------------|
| `procesadores`   | Procesadores          |
| `teclados`       | Teclados              |
| `impresoras`     | Impresoras            |
| `mouse`          | Mouse                 |
| `audifonos`      | Audífonos             |
| `camaras_cctv`   | Cámaras CCTV          |
| `dvr`            | DVR                   |
| `webcam`         | Webcam                |
| `almacenamiento_cctv` | Almacenamiento CCTV |
| `almacenamiento` | Almacenamiento        |
| `suministros`    | Suministros           |
| `adaptadores`    | Adaptadores           |
| `slot1`–`slot20` | (para categorías nuevas) |

### Agregar una nueva categoría (slots adicionales)

En `js/productos.js`, descomenta la línea del slot y cámbiale el nombre:

```javascript
// Antes:
// slot1: "Categoría 1",

// Después:
slot1: "Monitores",
```

Luego agrega productos con `categoria: "slot1"`.

---

## ⏰ Cambiar fecha de fin de promociones

En `js/productos.js`, busca:

```javascript
fechaFin: "2025-07-01T23:59:59",
```

Cambia la fecha al formato `"YYYY-MM-DDTHH:MM:SS"`.

---

## 🖼️ Subir logo

1. Guarda tu logo como `images/logo.png`
2. Sube el archivo al repositorio
3. ¡Listo! Aparecerá automáticamente en el header

---

## 📱 WhatsApp

El link de WhatsApp está configurado en `js/productos.js`:

```javascript
const WHATSAPP_LINK = "https://wa.link/lunypx";
```

Cada botón "Comprar" envía automáticamente el nombre y precio del producto al chat.
