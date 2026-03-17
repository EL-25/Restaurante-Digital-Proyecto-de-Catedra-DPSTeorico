# Restaurante-Digital-Proyecto-de-Catedra-DPSTeorico
Enlace Trello: https://trello.com/invite/b/69b8a172ddbce1671e34755a/ATTI578335f2112471151b212d9e1b68cf33C7E714C7/gestion-del-proyecto-fase-1

Tipo de Licencia Creative Commons implementada:
pideYcome © 2026 by Cesar Lara is licensed under CC BY-NC-ND 4.0. To view a copy of this license, visit https://creativecommons.org/licenses/by-nc-nd/4.0/
# Sistema de Gestión de Restaurante (PideyCome)

## 📋 Descripción General

Sistema completo de gestión de restaurante desarrollado como mockup de prueba con múltiples roles de usuario. Permite la gestión integral de órdenes, cocina, pagos e inventario con actualizaciones en tiempo real.

---

## 👥 Roles de Usuario

### 1. **Mesero**
- Crea órdenes para llevar o comer en el lugar
- Asigna mesas a las órdenes
- Agrega nombre del cliente
- Recibe notificaciones en tiempo real del estado de órdenes
- Ve campanita de notificaciones con contador de pendientes
- Filtra órdenes por mesa
- Selecciona productos del menú (los agotados aparecen deshabilitados)

### 2. **Cocina**
- Ve todas las órdenes en tiempo real
- Estados: Pendiente → Recibida → Preparando → Despachada
- Filtra por estado de orden
- Filtra por mesa o "para llevar"
- Ve ID de mesa o identificador para llevar
- Ve nombre del cliente en cada orden
- Actualiza el estado de las órdenes

### 3. **Cajera**
- Ve recuento automático de órdenes
- Calcula totales automáticamente
- Agrupa órdenes por mesa
- Imprime tickets o facturas
- Simulación de POS
- Envío de comprobantes por correo
- Gestiona pagos y marca órdenes como pagadas
- Ve ingresos del día y estadísticas

### 4. **Administrador**
- Gestiona productos, precios e inventario
- Ve todos los movimientos del restaurante
- Crea nuevos usuarios (mesero, cocina, cajera)
- Agrega nuevos productos al inventario
- Actualiza stock de productos
- Modifica precios y categorías
- Panel de estadísticas general

---

## 🔐 Usuarios de Prueba
(Los datos de prueba no estan insertados en nignuna base de datos)

| Rol | Usuario | Contraseña |
|-----|---------|------------|
| **Mesero** | mesero1 | 1234 |
| **Cocina** | cocina1 | 1234 |
| **Cajera** | cajera1 | 1234 |
| **Administrador** | admin | admin |

---

## 📊 Flujo de Estados de Órdenes

```
Ordenada → Recibida por Cocina → Preparando → Despachada
```

### Estados Detallados:
1. **Ordenada** (Amarillo) - El mesero crea la orden
2. **Recibida por Cocina** (Azul) - La cocina confirma recepción
3. **Preparando** (Naranja) - La orden está en preparación
4. **Despachada** (Verde) - La orden está lista para entregar

---

## ✨ Funcionalidades Principales

### Sistema de Órdenes
- ✅ Creación de órdenes con nombre de cliente
- ✅ Asignación de mesa o "para llevar"
- ✅ Carrito de compras con cantidades ajustables
- ✅ Cálculo automático de totales
- ✅ Actualización en tiempo real de estados
- ✅ Notificaciones push para meseros
- ✅ Filtrado por mesa y estado
- ✅ Historial completo de órdenes

### Gestión de Productos
- ✅ Catálogo de productos por categorías
- ✅ Control de stock en tiempo real
- ✅ Productos agotados visibles pero deshabilitados
- ✅ Indicador de stock bajo (menos de 10 unidades)
- ✅ Agregar nuevos productos desde admin
- ✅ Modificación de precios e inventario
- ✅ Imágenes de productos

### Sistema de Notificaciones
- ✅ Campanita de notificaciones para meseros
- ✅ Contador de órdenes pendientes
- ✅ Actualización en tiempo real
- ✅ Indicador visual con badge rojo
- ✅ Lista desplegable de notificaciones recientes

### Punto de Venta (POS)
- ✅ Agrupación de órdenes por mesa
- ✅ Cálculo automático de totales
- ✅ Opciones de pago: Efectivo, Tarjeta
- ✅ Generación de tickets y facturas
- ✅ Envío por correo electrónico
- ✅ Simulación de impresión
- ✅ Marcado de órdenes como pagadas

### Panel Administrativo
- ✅ Gestión completa de usuarios
- ✅ Creación de nuevos usuarios (sin rol admin)
- ✅ Gestión de inventario expandible
- ✅ Actualización de precios y stock
- ✅ Estadísticas de ventas
- ✅ Historial de movimientos
- ✅ Panel de control general

### Recuperación del Sistema
- ✅ Persistencia de datos en localStorage
- ✅ Recuperación automática al recargar
- ✅ Manejo de errores y estados vacíos
- ✅ Validaciones de formularios

---

## 🎨 Diseño UX/UI

### Paleta de Colores

#### Color Principal - Naranja 🟠
- **Primario**: `orange-500` (#f97316)
- **Hover**: `orange-600` (#ea580c)
- **Degradados**: `from-orange-50 to-orange-100`
- **Uso**: Botones principales, iconos de navegación, precios, elementos destacados

#### Colores de Estado de Órdenes 🚦
- **Amarillo** (`yellow-500`) - Estado "Ordenada"
- **Azul** (`blue-500/600`) - Estado "Recibida por Cocina"
- **Naranja** (`orange-500/600`) - Estado "Preparando"
- **Verde** (`green-500/600`) - Estado "Despachada"

#### Colores por Rol 👥
- **Mesero**: Naranja (`orange-500`)
- **Cocina**: Naranja (`orange-500`)
- **Caja**: Verde (`green-500/600`)
- **Admin**: Sistema por defecto

#### Colores de Información 📊
- **Verde** (`green-600`) - Ingresos, órdenes pagadas, confirmaciones
- **Azul** (`blue-600`) - Contador de tickets, información general
- **Naranja** (`orange-600`) - Órdenes pendientes de pago, alertas
- **Rojo** (`red-500`) - Notificaciones urgentes, contador de pendientes

#### Colores de Base (Sistema de Diseño) ⚙️
- **Background**: `#ffffff` (blanco)
- **Foreground**: `oklch(0.145 0 0)` (negro azulado)
- **Primary**: `#030213` (negro azulado)
- **Destructive**: `#d4183d` (rojo)
- **Muted**: `#ececf0` (gris claro)
- **Border**: `rgba(0, 0, 0, 0.1)` (gris transparente)

#### Colores Neutros ⚪
- `gray-50` - Fondos de secciones
- `gray-100` - Placeholders y estados deshabilitados
- `gray-500` - Estados por defecto

---

### Iconografía

La aplicación utiliza iconos de **lucide-react** de manera consistente:

#### Navegación Principal
- `UtensilsCrossed` - Logo del sistema
- `ShoppingCart` - Carrito de compras
- `ChefHat` - Panel de cocina
- `CreditCard` - Panel de caja
- `Settings` - Panel de administración
- `LogOut` - Cerrar sesión

#### Acciones y Estados
- `Plus` / `Minus` - Ajustar cantidades
- `Trash2` - Eliminar items
- `Check` / `CheckCircle` - Confirmaciones
- `X` - Cerrar/Cancelar
- `Bell` - Notificaciones
- `Filter` - Filtros
- `Search` - Búsqueda

#### Información
- `DollarSign` - Precios e ingresos
- `Receipt` - Tickets y comprobantes
- `Printer` - Imprimir
- `Mail` - Envío por correo
- `FileText` - Facturas
- `Smartphone` - Acciones móviles

#### Usuarios y Gestión
- `Users` - Gestión de usuarios
- `Package` - Productos e inventario
- `ClipboardList` - Órdenes
- `TrendingUp` - Estadísticas

---

### Tipografía

El sistema utiliza las fuentes por defecto del navegador con la siguiente jerarquía:

#### Tamaños de Texto
- **Títulos H1**: `text-2xl` (1.5rem) - Títulos principales de página
- **Títulos H2**: `text-xl` (1.25rem) - Subtítulos de secciones
- **Títulos H3**: `text-lg` (1.125rem) - Encabezados de tarjetas
- **Texto Base**: `text-base` (1rem) - Texto principal
- **Texto Pequeño**: `text-sm` (0.875rem) - Información secundaria
- **Texto Muy Pequeño**: `text-xs` (0.75rem) - Etiquetas y badges

#### Pesos de Fuente
- **Normal**: `font-normal` (400) - Texto general
- **Medium**: `font-medium` (500) - Labels y botones
- **Bold**: `font-bold` (700) - Precios y totales destacados

#### Altura de Línea
- **Base**: `leading-normal` (1.5) - Lectura cómoda
- **Ajustada**: `leading-tight` - Títulos compactos

---

### Navegación Web

#### Estructura de Navegación
El sistema utiliza **React Router** con navegación basada en roles:

1. **Login** (`/`) - Pantalla de autenticación
2. **Mesero** (`/mesero`) - Dashboard de mesero
3. **Cocina** (`/cocina`) - Dashboard de cocina
4. **Caja** (`/caja`) - Dashboard de caja
5. **Admin** (`/admin`) - Dashboard de administrador

#### Patrón de Navegación
- **Redirección automática**: Al iniciar sesión, cada usuario ve su panel correspondiente
- **Header persistente**: Navegación superior con logo, título del rol y botón de logout
- **Layout responsivo**: Adaptable a móvil, tablet y desktop
- **Navegación contextual**: Tabs y filtros dentro de cada vista

---

### Diseño de Pantallas

#### Pantalla de Login
- Degradado de fondo naranja suave
- Card centrado con logo circular
- Formulario simple con usuario y contraseña
- Botón naranja principal
- Tarjetas de ayuda con credenciales de prueba

#### Dashboard de Mesero
- **Tab 1 - Nueva Orden**:
  - Formulario de mesa y nombre de cliente
  - Selector de categorías
  - Grid de productos con precios
  - Badge de stock bajo
  - Productos agotados deshabilitados
  - Carrito lateral con resumen
  - Total destacado en naranja
  - Botón "Crear Orden"

- **Tab 2 - Mis Órdenes**:
  - Filtro por mesa
  - Campanita de notificaciones con contador
  - Lista de órdenes con estados de color
  - Información de mesa y cliente
  - Detalle de productos
  - Total por orden
  - Badge "PAGADA" en verde

#### Dashboard de Cocina
- Header con icono de chef
- Filtros por estado y mesa
- Grid de tarjetas de órdenes
- Código de colores por estado
- Identificador de mesa o "para llevar"
- Nombre del cliente destacado
- Lista de productos con cantidades
- Botones de acción por estado:
  - Azul: "Recibir Orden"
  - Naranja: "Comenzar Preparación"
  - Verde: "Marcar como Despachada"

#### Dashboard de Caja
- Header con icono de tarjeta
- **Estadísticas del día**:
  - Ingresos totales (verde)
  - Total de tickets (azul)
  - Pendientes de pago (naranja)
- **Órdenes agrupadas por mesa**:
  - Card por mesa con múltiples órdenes
  - Lista de productos consolidada
  - Total calculado automáticamente
  - Checkbox de selección
  - Métodos de pago
  - Opciones de impresión
  - Envío por email
  - Botón "Procesar Pago"

#### Dashboard de Administrador
- **Tab 1 - Productos**:
  - Lista de productos con imagen
  - Precio, categoría y stock
  - Botón de edición por producto
  - Botón "Agregar Producto"
  - Modal de edición/creación

- **Tab 2 - Usuarios**:
  - Tabla de usuarios
  - Roles asignados
  - Botón "Crear Usuario"
  - Modal de creación (sin rol admin)

- **Tab 3 - Estadísticas**:
  - Métricas generales
  - Historial de movimientos
  - Gráficos y reportes

#### Diseño Responsivo Multiplataforma

**Desktop (lg: 1024px+)**:
- Grid de 3 columnas para productos y órdenes
- Sidebar visible
- Tabs horizontales
- Modales amplios

**Tablet (md: 768px - 1023px)**:
- Grid de 2 columnas
- Tabs compactos
- Modales de tamaño medio

**Mobile (< 768px)**:
- Grid de 1 columna
- Navegación adaptada
- Botones de tamaño completo
- Modales fullscreen
- Touch-friendly (botones grandes)

---

## 🛠️ Tecnologías Utilizadas
(Tecnologias temporales ya que usaremos JavaScript en remplazo de TypeScript)

### Frontend
- **React** - Biblioteca de UI
- **TypeScript** - Tipado estático
- **React Router** - Navegación y routing
- **Tailwind CSS v4** - Framework de estilos
- **Lucide React** - Iconografía

### Componentes UI
- Custom UI components basados en Radix UI
- Card, Button, Input, Select, Checkbox
- Dialog, Tabs, Badge, Label
- Sheet (drawer mobile)

### Gestión de Estado
- **React Context API** - Estado global compartido
- **localStorage** - Persistencia de datos local (Mientras se conecta a una base de datos real)

### Estructura del Proyecto
La estructura del proyecto puede cambiar con el nombre de las variables cuando se realize el sistema, dado que se ha realizado en figma y para poder pasarse a React Native.
```
src/
├── app/
│   ├── components/
│   │   ├── ui/              # Componentes reutilizables
│   │   ├── Layout.tsx       # Layout principal
│   │   └── figma/           # Componentes de Figma
│   ├── contexts/
│   │   └── RestaurantContext.tsx  # Estado global
│   ├── pages/
│   │   ├── Login.tsx        # Pantalla de login
│   │   ├── Mesero.tsx       # Dashboard mesero
│   │   ├── Cocina.tsx       # Dashboard cocina
│   │   ├── Caja.tsx         # Dashboard caja
│   │   └── Admin.tsx        # Dashboard admin
│   ├── App.tsx              # Componente principal
│   ├── routes.tsx           # Configuración de rutas
│   └── types.ts             # Tipos TypeScript
├── styles/
│   ├── theme.css            # Variables de diseño
│   ├── tailwind.css         # Configuración Tailwind
│   └── index.css            # Estilos globales
└── main.tsx                 # Punto de entrada
```

---

## 📦 Datos del Sistema

### Productos de Ejemplo
El sistema incluye productos de ejemplo en las siguientes categorías:
- **Entradas**: Nachos, Alitas, Quesadillas, etc.
- **Platos Principales**: Hamburguesas, Pizzas, Tacos, Burritos, etc.
- **Bebidas**: Refrescos, Agua, Cerveza, Jugos, etc.
- **Postres**: Helado, Brownie, Cheesecake, Flan, etc.

Cada producto incluye:
- Nombre
- Precio
- Categoría
- Stock disponible
- ID único

### Usuarios Predefinidos
4 usuarios de prueba (ver sección de Usuarios de Prueba)

### Órdenes
Las órdenes se generan dinámicamente y persisten en localStorage con:
- ID único
- Fecha y hora de creación
- Mesero responsable
- Mesa o tipo "para llevar"
- Nombre del cliente
- Items con cantidades
- Total calculado
- Estado actual
- Estado de pago

---

## 🚀 Flujo Completo de Uso

### 1. Inicio de Sesión
Usuario inicia sesión con credenciales → Redirección automática a su panel dependiendo a su rol

### 2. Creación de Orden (Mesero)
1. Selecciona mesa o "para llevar"
2. Ingresa nombre del cliente
3. Navega por categorías de productos
4. Agrega productos al carrito
5. Ajusta cantidades
6. Revisa total
7. Crea la orden

### 3. Procesamiento en Cocina
1. La orden aparece automáticamente en pantalla de cocina
2. Cocina confirma recepción (Estado: Recibida)
3. Inicia preparación (Estado: Preparando)
4. Finaliza y despacha (Estado: Despachada)
5. Mesero recibe notificación de cada cambio

### 4. Cobro en Caja
1. Cajera ve órdenes despachadas
2. Agrupa órdenes por mesa
3. Revisa total automático
4. Selecciona método de pago
5. Elige tipo de comprobante (ticket/factura)
6. Opcionalmente envía por correo
7. Procesa el pago
8. Orden marcada como PAGADA

### 5. Administración
1. Admin gestiona inventario
2. Actualiza stock de productos
3. Modifica precios
4. Crea nuevos usuarios
5. Agrega nuevos productos
6. Revisa estadísticas generales

---

## 🔄 Actualizaciones en Tiempo Real

El sistema simula actualizaciones en tiempo real mediante:
- Context API compartido entre todos los componentes
- Actualización inmediata del estado global
- Re-renderizado automático de componentes afectados
- Persistencia en localStorage

### Notificaciones Push
- El mesero recibe notificaciones cuando una orden cambia de estado
- Contador visible en campanita
- Badge rojo con número de pendientes
- Lista desplegable de notificaciones recientes

---

## 💾 Persistencia de Datos

### localStorage
Todos los datos se guardan en localStorage:
- `restaurant-orders` - Órdenes del sistema
- `restaurant-users` - Usuarios registrados
- `restaurant-products` - Inventario de productos
- `restaurant-notifications` - Notificaciones del mesero

### Recuperación
Al recargar la página:
- Se restauran todas las órdenes
- Se mantiene el estado de productos
- Se conservan los usuarios creados
- Se recuperan las notificaciones

---

## 📱 Compatibilidad

### Navegadores
- ✅ Chrome/Edge (Chromium)
- ✅ Firefox
- ✅ Safari

### Dispositivos
- ✅ Desktop (1024px+)
- ✅ Tablet (768px - 1023px)
- ✅ Mobile (320px - 767px)

---

## ⚠️ Notas Importantes

### Mockup de Prueba
Este sistema es un **mockup de demostración** y no lo utilizaremos en el desarrollo del software real:
- Los datos se almacenan localmente en el navegador
- No hay autenticación real ni seguridad
- No hay conexión a base de datos
- Las contraseñas son de ejemplo
- La impresión y envío de correos son simulados

### Limitaciones
- Sin backend real
- Sin base de datos persistente
- Sin autenticación segura
- Sin procesamiento de pagos real
- Sin integración con impresoras térmicas
- Sin envío real de correos electrónicos

### Uso Recomendado
Este sistema es ideal para:
- Demostraciones de concepto
- Prototipos de UI/UX
- Presentaciones a clientes
- Pruebas de flujo de trabajo
- Capacitación de personal
- Mockups de diseño

---

## 📄 Licencia

Proyecto de demostración y prueba. Uso educativo y de prototipado.

---

## 🎯 Próximas Mejoras Potenciales

- [ ] Integración con backend real como (Java Spring Boot)
- [ ] Base de datos MySQL
- [ ] Autenticación JWT
- [ ] WebSockets para tiempo real verdadero
- [ ] Muestra simulación de una ticketera
- [ ] Pasarela de pagos (simuladas)
- [ ] Reportes y gráficos avanzados
- [ ] App móvil nativa

---

## Link para ver la pagina web simulada sin backend solo diseño pero funcional con localstorage
https://stew-lapis-76991141.figma.site/  
Figma nos da esta herramienta para subir nuestros prototipos y ver como interactuarán cuando ya la programemos y se lleve a producción.

---

**Desarrollado como sistema mockup de gestión de restaurante (PideyCome)** | Grupo 2 DPS 01T 2026
# README
