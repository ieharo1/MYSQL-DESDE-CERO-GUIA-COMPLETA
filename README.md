# 🐬 MYSQL DESDE CERO - GUÍA COMPLETA

**MySQL desde Cero** es un sitio educativo completo diseñado para enseñar MySQL desde los fundamentos hasta conceptos avanzados, con explicaciones claras, ejemplos prácticos y código listo para usar.

> *"MySQL es el sistema de gestión de bases de datos de código abierto más popular del mundo."*

---

## 🎯 ¿Qué es este Proyecto?

Este proyecto proporciona un recurso educativo gratuito para aprender MySQL, incluyendo:

- **Documentación completa** de cada tema
- **Ejemplos de código** listos para ejecutar
- **Ejercicios prácticos** para reforzar el aprendizaje
- **Sitio web educativo** con navegación intuitiva

---

## 📚 Contenido del Curso

### Módulo 1: Fundamentos

1. **Introducción**
   - ¿Qué es MySQL?
   - Historia y evolución
   - Casos de uso en la industria

2. **Instalación**
   - MySQL Server en Windows
   - MySQL Server en Linux
   - MySQL Workbench
   - Configuración inicial

3. **Conceptos básicos**
   - Creación de bases de datos
   - Tipos de datos MySQL
   - Restricciones (constraints)
   - Claves primarias y foráneas

### Módulo 2: Intermedio

4. **Ejemplos prácticos**
   - Consultas SELECT
   - JOINs (INNER, LEFT, RIGHT)
   - Subconsultas
   - Funciones de agregación

5. **Buenas prácticas**
   - Normalización de bases de datos
   - Indexación estratégica
   - EXPLAIN para optimización
   - Diseño de esquemas eficientes

### Módulo 3: Avanzado

6. **Casos reales**
   - Replicación maestro-esclavo
   - Backup y recuperación
   - Implementación en producción

7. **Proyecto final**
   - Base de datos para e-commerce
   - Aplicación completa con MySQL

---

## 🗂️ Estructura del Proyecto

```
Practica-Nro11/
├── index.html          # Página principal
├── css/
│   └── styles.css      # Estilos del sitio
├── js/
│   └── main.js         # JavaScript del sitio
└── README.md
```

---

## 🚀 Cómo Usar este Proyecto

### Opción 1: Navegar el Sitio Web

1. Abre `index.html` en tu navegador
2. Navega por las secciones del curso
3. Haz clic en los temas para ver la documentación detallada

### Opción 2: Ejecutar los Ejemplos SQL

1. Abre MySQL Workbench o MySQL CLI
2. Conéctate a tu instancia de MySQL
3. Ejecuta los scripts SQL de ejemplo

### Requisitos

- **MySQL 8.0** o superior
- **MySQL Workbench** o cliente MySQL
- Navegador web moderno (Chrome, Firefox, Edge)

---

## 📝 Ejemplos Rápidos

### Crear Base de Datos

```sql
CREATE DATABASE IF NOT EXISTS mi_tienda;
USE mi_tienda;
```

### Crear Tabla

```sql
CREATE TABLE productos (
    id INT AUTO_INCREMENT PRIMARY KEY,
    nombre VARCHAR(100) NOT NULL,
    precio DECIMAL(10,2) NOT NULL,
    stock INT DEFAULT 0,
    fecha_creacion TIMESTAMP DEFAULT CURRENT_TIMESTAMP
) ENGINE=InnoDB;
```

### Consulta con JOIN

```sql
SELECT p.nombre, c.nombre AS categoria
FROM productos p
INNER JOIN categorias c ON p.categoria_id = c.id
WHERE p.stock > 0
ORDER BY p.precio DESC;
```

### Stored Procedure

```sql
DELIMITER //
CREATE PROCEDURE ObtenerProductos()
BEGIN
    SELECT * FROM productos;
END //
DELIMITER ;
```

---

## 🎓 Metodología de Aprendizaje

### 1. Leer la Teoría
Cada tema comienza con una explicación clara del concepto.

### 2. Ver Ejemplos
Los ejemplos de código muestran la aplicación práctica.

### 3. Practicar
Los ejercicios te permiten aplicar lo aprendido.

### 4. Experimentar
Modifica los ejemplos para entender cómo funcionan.

---

## 🔧 Comandos Esenciales

### Gestión de Bases de Datos

```sql
-- Listar bases de datos
SHOW DATABASES;

-- Usar una base de datos
USE nombre_base_datos;

-- Eliminar base de datos
DROP DATABASE IF EXISTS nombre_base_datos;
```

### Gestión de Tablas

```sql
-- Listar tablas
SHOW TABLES;

-- Ver estructura de tabla
DESCRIBE nombre_tabla;

-- Eliminar tabla
DROP TABLE IF EXISTS nombre_tabla;
```

### Consultas Comunes

```sql
-- Contar registros
SELECT COUNT(*) FROM nombre_tabla;

-- Ver primeros registros
SELECT * FROM nombre_tabla LIMIT 10;

-- Buscar datos
SELECT * FROM nombre_tabla WHERE columna LIKE '%valor%';
```

---

## 📖 Recursos Adicionales

### Documentación Oficial

- [MySQL Documentation](https://dev.mysql.com/doc/)
- [MySQL Tutorial](https://www.mysqltutorial.org/)
- [MySQL Blog](https://mysqlserverteam.com/)

### Herramientas Recomendadas

- **MySQL Workbench** - IDE oficial gratuito
- **phpMyAdmin** - Administración web
- **MySQL Shell** - Línea de comandos moderna

### Comunidades

- [MySQL Community](https://dev.mysql.com/community/)
- [Stack Overflow - MySQL](https://stackoverflow.com/questions/tagged/mysql)
- [Reddit r/MySQL](https://www.reddit.com/r/MySQL/)

---

## 💡 Consejos para Principiantes

1. **Practica regularmente**: La consistencia es clave para aprender SQL.
2. **Comienza simple**: Domina SELECT antes de avanzar a conceptos complejos.
3. **Entiende los JOINs**: Son fundamentales para consultas relacionales.
4. **Usa InnoDB**: Para transacciones y foreign keys.
5. **Aprende EXPLAIN**: Te ayudará a optimizar consultas.

---

## ⚠️ Mejores Prácticas

### Seguridad

- Nunca uses `SELECT *` en producción
- Usa prepared statements para prevenir SQL Injection
- Valida siempre los datos de entrada

### Rendimiento

- Indexa columnas usadas en WHERE y JOIN
- Usa EXPLAIN para analizar consultas
- Evita SELECT * en producción

### Código

- Usa nombres descriptivos para tablas y columnas
- Comenta tu código SQL
- Mantén un formato consistente

---

## 🧪 Ejercicios Prácticos

### Nivel Básico

1. Crea una base de datos llamada `Biblioteca`
2. Crea tablas para `Libros`, `Socios` y `Prestamos`
3. Inserta al menos 5 registros en cada tabla
4. Consulta todos los libros disponibles

### Nivel Intermedio

1. Crea un stored procedure para registrar préstamos
2. Usa JOIN para mostrar libros con sus categorías
3. Crea una vista con el resumen de préstamos por socio

### Nivel Avanzado

1. Implementa un trigger para actualizar stock automáticamente
2. Crea índices para optimizar consultas frecuentes
3. Configura replicación maestro-esclavo

---

## 👨‍💻 Desarrollado por Isaac Esteban Haro Torres

**Ingeniero en Sistemas · Full Stack · Automatización · Data**

- 📧 Email: zackharo1@gmail.com
- 📱 WhatsApp: 098805517
- 💻 GitHub: https://github.com/ieharo1
- 🌐 Portafolio: https://ieharo1.github.io/portafolio-isaac.haro/

---

© 2026 Isaac Esteban Haro Torres - Todos los derechos reservados.
