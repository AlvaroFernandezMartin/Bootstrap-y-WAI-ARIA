# Mejora de accesibilidad con WAI-ARIA en elementos Bootstrap

## 1. Botón (Button)

### Original
```html
<button class="btn btn-primary">Botón</button>
```

### Mejorado
```html
<button class="btn btn-primary" aria-label="Enviar formulario">Botón</button>
```

### Mejora
Se agregó el atributo `aria-label="Enviar formulario"` para proporcionar un contexto adicional sobre la acción que realiza el botón, especialmente útil para usuarios con lectores de pantalla.

---

## 2. Modal

### Original
```html
<div class="modal" tabindex="-1">
  <!-- contenido -->
</div>
```

### Mejorado
```html
<div class="modal" tabindex="-1" role="dialog" aria-labelledby="modalTitle" aria-describedby="modalDescription">
  <div class="modal-dialog" role="document">
    <!-- contenido -->
  </div>
</div>
```

### Mejora
- `role="dialog"`: Identifica el elemento como un cuadro de diálogo.
- `aria-labelledby`: Indica el título del modal para los lectores de pantalla.
- `aria-describedby`: Proporciona una descripción del contenido del modal.

---

## 3. Menú desplegable (Dropdown)

### Original
```html
<button class="btn btn-secondary dropdown-toggle" type="button" data-bs-toggle="dropdown">
  Menú desplegable
</button>
```

### Mejorado
```html
<button class="btn btn-secondary dropdown-toggle" type="button" data-bs-toggle="dropdown" aria-expanded="false" aria-haspopup="true" aria-controls="dropdownMenu">
  Menú desplegable
</button>
```

### Mejora
- `aria-expanded`: Indica si el menú está abierto o cerrado.
- `aria-haspopup`: Declara que el botón activa un menú.
- `aria-controls`: Relaciona el botón con el elemento del menú desplegable.

---

## 4. Alerta (Alert)

### Original
```html
<div class="alert alert-warning" role="alert">
  Este es un mensaje de alerta.
</div>
```

### Mejorado
```html
<div class="alert alert-warning" role="alert" aria-live="assertive" aria-atomic="true">
  Este es un mensaje de alerta.
</div>
```

### Mejora
- `aria-live="assertive"`: Informa inmediatamente a los usuarios de cambios en el contenido.
- `aria-atomic="true"`: Garantiza que el mensaje se lea completo y no fragmentado.

---

## 5. Pestañas (Tabs)

### Original
```html
<ul class="nav nav-tabs" id="myTab" role="tablist">
  <li class="nav-item" role="presentation">
    <button class="nav-link active" id="home-tab" data-bs-toggle="tab" data-bs-target="#home" type="button" role="tab" aria-controls="home" aria-selected="true">Inicio</button>
  </li>
</ul>
```

### Mejorado
```html
<ul class="nav nav-tabs" id="myImprovedTab" role="tablist">
  <li class="nav-item" role="presentation">
    <button class="nav-link active" id="home-tab-improved" data-bs-toggle="tab" data-bs-target="#home-improved" type="button" role="tab" aria-controls="home-improved" aria-selected="true" tabindex="0">Inicio</button>
  </li>
</ul>
```

### Mejora
- `aria-controls`: Relaciona cada pestaña con su contenido.
- `tabindex`: Permite un mejor control del orden de navegación.

---



