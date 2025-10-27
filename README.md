🌱 Farm2Fork — Backend

Marketplace Agroalimentario Full-Stack (Node + Express + MongoDB + HBS)

Farm2Fork es una aplicación web Full-Stack que facilita la venta directa de productos agrícolas y ganaderos entre productores locales y consumidores. Busca digitalizar el sector agroalimentario, ayudando a pequeños productores a ofrecer sus productos online de forma segura y accesible.

Este repositorio contiene el backend y la capa de vistas del proyecto.

🧩 Tecnologías Principales
Área	Tecnologías
Backend	Node.js + Express
Base de datos	MongoDB + Mongoose
Motor de plantillas	Handlebars (HBS)
Autenticación	Sessions + Cookies seguras (no JWT)
Password Hashing	bcrypt
Subida de imágenes	Multer + Cloudinary
Carrito & Pagos	Stripe Checkout (modo test)
Infraestructura	Docker + Fly.io ready
Logging	Morgan
Validación	Middlewares + Validación Mongoose
📂 Estructura del Proyecto
Farm2Fork/
│
├── config/                     # Configuración core
│   ├── db.config.js
│   ├── hbs.config.js
│   ├── multer.config.js
│   └── session.config.js
│
├── controllers/                # Lógica de negocio
│   ├── auth.controller.js
│   ├── cart.controller.js
│   ├── misc.controller.js
│   ├── products.controller.js
│   └── users.controller.js
│
├── middlewares/
│   └── auth.middleware.js
│
├── models/
│   ├── User.model.js
│   ├── Product.model.js
│   └── Cart.model.js
│
├── routes/
│   ├── routes.js               # auth + users + products
│   ├── cart.routes.js
│   └── payment.routes.js
│
├── views/                      # Plantillas HBS (UI en servidor)
│
├── public/                     # CSS, imágenes y JS estático
│
├── Dockerfile
├── app.js                      # Punto de entrada del servidor
└── package.json

🚀 Funcionalidades

✅ Registro / Login con sesiones y cookies seguras
✅ Gestión de productos agrícolas y ganaderos
✅ Carrito persistido en base de datos
✅ Checkout con Stripe
✅ Subida y manejo de imágenes con Cloudinary
✅ Listado y filtrado por categorías / subcategorías
✅ Perfiles de usuario con listado de productos publicados
✅ Validaciones y mensajes de error en UI
✅ Autorización de rutas (solo usuarios logueados)

🔐 Autenticación & Seguridad
Elemento	Estado
Sesiones en Mongo	✅
Cookies httpOnly	✅
Hashed passwords	✅
Roles implícitos (productor/consumidor)	✅
Protección contra rutas públicas	✅

📌 Ideal para evolucionar hacia RBAC explícito (admin / vendedor / comprador)

📦 Instalación
1️⃣ Clonar repositorio
git clone https://github.com/Albertocoge/farm2fork.git
cd farm2fork

2️⃣ Instalar dependencias
npm install

3️⃣ Variables de entorno

Crear .env:

PORT=3000
MONGODB_URI=mongodb://localhost:27017
COOKIE_SECRET=your_secret_here
CLOUDINARY_CLOUD_NAME=xxxx
CLOUDINARY_API_KEY=xxxx
CLOUDINARY_API_SECRET=xxxx
STRIPE_SECRET_KEY=sk_test_xxx
COOKIE_SECURE=false

4️⃣ Ejecutar servidor

Modo desarrollo:

npm run dev


Modo producción:

npm start


Acceder a:
👉 http://localhost:3000

💳 Pagos con Stripe

✔ Checkout nativo de Stripe
✔ Integración segura
✔ Redirección a éxito o cancelación

Se pueden realizar compras usando tarjetas de prueba (Stripe test mode ✅)

🎯 Objetivo del Proyecto

📌 Apoyar la economía local y la digitalización de productores agrícolas, facilitando un canal de venta directo con compradores.

🧑‍🤝‍🧑 Equipo
Participante	Rol	GitHub
Alberto Codoñer	Full-Stack Developer (Backend principal, sesiones, carrito, Stripe, Cloudinary)	https://github.com/Albertocoge

Michael B. Díaz B.	Full-Stack Developer (Backend principal, sesiones, carrito, Stripe, Cloudinary)	https://github.com/MikeBDiazB
🛠️ Roadmap
Idea	Estado
Gestión de pedidos tras pago	⏳
Sistema de reviews para productos	⏳
Roles explícitos: productor / consumidor / admin	✅ Pendiente
Filtro avanzado por distancia y origen	⏳
Perfil con métricas de ventas	⏳
Internacionalización (ES/EN)	⏳
🪪 Licencia

Este proyecto está bajo licencia ISC.
Puedes usarlo y modificarlo citando a los autores.

⭐ Contribuye o apoya

Si te gusta el proyecto, ¡déjanos una ⭐ en GitHub! 💚🌱
Tu apoyo impulsa el desarrollo de software libre y sostenible.
