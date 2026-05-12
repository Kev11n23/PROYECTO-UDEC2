"# PROYECTO-UDEC2" 
# PROYECTO-UDEC
Repositorio para subir avances del proyecto relacionado con las pasantias.

📄 Sistema de Gestión de Inventario EPP - UDEC
Este sistema ha sido desarrollado para automatizar y asegurar el control de los Elementos de Protección Personal (EPP), permitiendo un seguimiento riguroso desde el ingreso al almacén hasta la entrega final al trabajador.

🚀 Características Principales
Arquitectura Modular: Separación estricta entre la Interfaz de Usuario (GUI), la Lógica de Negocio y el Acceso a Datos (DAO).
Gestión de Inventario: Control de stock en tiempo real con alertas visuales de niveles críticos.
Seguridad Avanzada: Protección de acceso y blindaje de integridad de datos.
Sistema de Backups: Generación automática de copias de seguridad de la base de datos.
Reportes Visuales: Generación de gráficas de consumo por categorías.

🛡️ Seguridad y Robustez
El software implementa estándares de seguridad modernos para garantizar la integridad de la información:

Encriptación de Credenciales: Las contraseñas no se almacenan en texto plano. Se utiliza el algoritmo SHA-256 para generar hashes irreversibles, asegurando que incluso si la base de datos es comprometida, las claves permanezcan cifradas.
Protección contra SQL Injection: Todas las consultas a la base de datos están parametrizadas. Se evita la concatenación de strings, separando el plano de datos del plano de ejecución para neutralizar ataques de inyección de código.
Persistencia Relacional: Uso de SQLite con claves foráneas para mantener la integridad referencial entre empleados, productos y entregas.
Acceso y registro de usuarios (ROOT): Por políticas de seguridad y control de auditoría, el acceso está restringido a una cuenta raíz de administración

🛠️ Tecnologías Utilizadas
Lenguaje: Python 3.x
GUI Framework: Tkinter / CustomTkinter
Base de Datos: SQLite 3
Seguridad: Hashlib (SHA-256)
Visualización: Matplotlib (Para gráficas de consumo)

Notas
¿Por qué SQLite? Es ligero, no requiere instalación de servidores externos y permite que la aplicación sea totalmente portable.

¿Por qué Modular? Facilita el mantenimiento. Si se desea cambiar la base de datos a PostgreSQL o MySQL en el futuro, solo se debe modificar la capa de database sin afectar la interfaz.

🛠️ GUÍA RÁPIDA DE INICIO
1. Preparación del Entorno
Antes de la primera ejecución, instala las librerías necesarias abriendo una terminal en la carpeta del proyecto y escribiendo: pip install -r requirements.txt

2. Configuración Inicial (Solo la primera vez)
Para crear la base de datos y el acceso de seguridad, ejecuta: python init_db.py

3. Ejecución del Sistema
Para iniciar el panel de control, lanza el archivo principal: python main_gui.py

4. Credenciales de Acceso (Default):
👤 Usuario: administrador
🔑 Clave: 123456
