# Plataforma de Adopción y Voluntariado ("Encuentra a tu Compañero")

Bienvenido al repositorio oficial del proyecto **Encuentra a tu Compañero**, una plataforma web diseñada para promover e incentivar la adopción responsable, donación y voluntariado en pro del bienestar animal.

---

## 📋 Descripción del Proyecto

El proyecto consiste en una interfaz web moderna e interactiva que conecta a usuarios interesados en el cuidado animal con opciones de adopción, apoyo económico (donaciones) y participación activa (voluntariado). Incorpora animaciones mediante *sprite sheets* en CSS puro para brindar una experiencia visual dinámica e interactiva.

---

## 💡 Funcionalidades Principales

1. **Sección Hero Interactiva:**
   * Animación en bucle de la mascota (*sprite sheet* CSS) ubicada de forma destacada sobre la llamada a la acción principal (*"ENCUENTRA A TU COMPAÑERO"*).

2. **Formulario de Registro / Participación:**
   * Selección dinámica entre las modalidades de **Donación** o **Voluntariado**.
   * Registro de información de contacto y disponibilidad de tiempo.

3. **Diseño Responsivo y Atractivo:**
   * Paleta de colores cálida y accesible.
   * Elementos visuales optimizados con fondos transparentes (`PNG`).

---

## 🎨 Guía de Estilos y Animaciones CSS

### Animación del Sprite Sheet (`.sprite`)

La animación del personaje principal utiliza una tira de imágenes (*sprite sheet*) procesada frame por frame mediante CSS keyframes.

#### Fórmulas de Cálculo

* **Ancho del contenedor (`width`):** Coincide exactamente con el ancho de un solo fotograma ($W_{\text{frame}}$).
* **Desplazamiento horizontal (`background-position`):** El recorrido total de la tira en negativo ($-\text{Ancho Total}$).
* **Pasos (`steps`):** Número de fotogramas totales ($N$).

$$
\text{Ancho Total} = W_{\text{frame}} \times N
$$

#### Código CSS de Referencia

```css
/* Contenedor principal para centrado vertical y horizontal */
.hero-container {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  text-align: center;
}

/* Estructura del Sprite */
.sprite {
  width: 111px;               /* Ancho de 1 fotograma */
  height: 91px;               /* Alto del fotograma */
  background-image: url('imagenes/sprite.png');
  background-repeat: no-repeat;
  margin: 0 auto;             /* Centrado horizontal automático */
  animation: perrito 0.6s steps(6) infinite;
}

/* Animación por desplazamiento continuo */
@keyframes perrito {
  from {
    background-position: 0 0;
  }
  to {
    background-position: -666px 0; /* Ancho total de la tira de cuadros */
  }
}
```

---

## 🛠️ Estructura del Proyecto

```text
proyecto_HTML/
├── index.html              # Estructura principal y formulario
├── css/
│   └── estilos.css         # Reglas de diseño, layout Flexbox y keyframes
└── imagenes/
    ├── sprite.png          # Tira de imágenes en formato PNG transparente
    └── logo.png            # Recursos gráficos adicionales
```

---

## 🚀 Requisitos e Instalación

1. Clonar el repositorio o descargar la carpeta del proyecto.
2. Asegurarse de mantener la estructura de directorios (`imagenes/`, `css/`).
3. Abrir `index.html` en cualquier navegador web moderno (Google Chrome, Mozilla Firefox, Microsoft Edge).

---

## 👥 Contribución y Uso
Proyecto desarrollado con fines educativos y de concientización comunitaria.

## Link del wireframe: 
https://www.figma.com/proto/wxPtsQDi996fpB3j0Jpg0Z/wireframe-patitas-felices?node-id=4-6831&t=YSQFl9JSM7oKyvwz-1
