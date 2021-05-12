# AZ-900 Azure Fundamentals
Resumen de los contenidos para la certificación AZ-900.

# Parte 1 - Aspectos básicos de Azure

Azure es una plataforma de informática en la nube → Desde hosting básico hasta soluciones de software personalizadas (IaaS/ PaaS/ SaaS).

- Almacenamiento remoto
- Hospedaje de bases de datos
- Administración centralizada de cuentas
- IA + IoT

### Nube

Es la entrega de servicios informáticos a través de Internet (servidores, almacenamiento, bases de datos, redes, software, análisis e inteligencia.).

Es mas barato porque te permite:

- Reducir los costos operativos.
- Ejecutar la infraestructura de forma más eficaz.
- Escalar a medida que cambien las necesidades empresariales.

### **Ventajas**

 Confiabilidad, Escalabilidad (vertical y horizontalmente), Elasticidad, Agilidad, Distribución geográfica, recuperación ante desastres.

### Modelos de servicio

- **Infraestructura como servicio (IaaS)** - Un proveedor de servicios en la nube mantiene actualizado el hardware, pero el mantenimiento del sistema operativo y la configuración de red es responsabilidad del inquilino de nube.
- **Plataforma como serivico (Sass)** - El proveedor de servicios en la nube administra las máquinas virtuales y los recursos de red, y el inquilino de nube implementa sus aplicaciones en el entorno de hospedaje administrado (Azure App Services).
- **Software como servicio (SaaS)** - el proveedor de servicios en la nube administra todos los aspectos del entorno de la aplicación, como las máquinas virtuales, los recursos de red, el almacenamiento de datos y las aplicaciones (Office 365)

### Serverless

En las aplicaciones sin servidor, el proveedor de servicios en la nube aprovisiona, escala y administra automáticamente la infraestructura necesaria para ejecutar el código.

### Tipos de nube

- Nube pública - disponibles para cualquiera que quiera comprarlos.
- Nube privada - uso exclusivo de los usuarios de una empresa u organización.
- Nube híbrida - combina una nube pública y una nube privada (Azure).

### Azure portal

Es una consola unificada basada en web que proporciona una alternativa a las herramientas de línea de comandos.

**Azure marketplace**: proveedores de software independientes y nuevas empresas que ofrecen sus soluciones y servicios, optimizados para ejecutarse en Azure.

### Servicios de Azure

**Servicios de infraestructura**

1. **Procesos** (compute services) - máquinas virtuales, contenedores y Kubernetes, Azure functions (serverless y microservicios).
2. **Redes** (Networking) - vpn, load balancer, dns, traffic manager, app gateways, express route, DDoS Protection.
3. **Almacenamiento** (cloud storage) - Archivos (servidor de archivos), discos, Table (almacenamiento NoSQL para datos no estructurados), Queue storage (colas para mensaje entre apps), blob (objetos grandes como videos).

**Servicio de plataforma**

1. **Movil** (app hosting) - servicios de back-end móviles para aplicaciones iOS, Android y Windows
2. **Bases de datos** (app hosting) - bases de datos relacionales como Postgres, MySQL, SQL Server, Maria DB, etc.
3. **Web** (app hosting) - compilar y hospedar aplicaciones web y servicios web basados en HTTP.
4. **IoT** (Internet of things) - supervisión y la administración de los recursos de IoT a escala (Hubs, dashboards, apps).
5. **Macrodatos** (Big Data) - Synapse Analytics (almacenamiento y consulta), HDInsight (procesamiento Hadoop) y Databricks (análisis colaborativo Apache Spark).
6. **IA** (Artificial Intelligence) - Machine Learning Service (desarrollar y entrenar modelos), ML Studio (área visual con algoritmos predefinidos) y Cognitive Services (API precompiladas de vision, vpz, pln, bing search y asignación de conocimiento).
7. **Devops** (Integration) - automatización de la entrega de software (pruebas, integración continua, etc)
8. **Seguridad** (Security) - Security center, active directory, key vault, multifactor authentication.

Todos estos incluyen durabilidad, seguridad, escalabilidad, administración y accesibilidad.

## Componentes principales de la arquitectura de Azure

La estructura organizativa de los recursos de Azure consta de cuatro niveles: 

- **Grupos de administración** - administrar el acceso, las directivas y el cumplimiento de varias suscripciones.
- **Suscripciones** - agrupa las cuentas de usuario y los recursos que han creado esas cuentas de usuario.
- **Grupos de recursos** - contenedor lógico en el que se implementan y administran recursos (flexible).
- **Recursos** - instancias de servicios.

### Suscripciones

Una suscripción de Azure es una unidad lógica de servicios de Azure que está vinculada a una cuenta de Azure, que es una identidad en Azure Active Directory y definir límites en torno a los productos, servicios y recursos de Azure.

- Límite de facturación
- Límite de control de acceso

Se pueden crear distintas suscripciones para separa entornos, estructuras organizativas y facturación.

### Grupos de administración

Los grupos de administración de Azure ofrecen un nivel de ámbito que está por encima de las suscripciones. Las suscripciones se organizan en contenedores llamados grupos de administración y las condiciones de gobernanza se aplican a los grupos de administración.

- Se admiten 10 000 grupos de administración en un único directorio.
- Un árbol de grupo de administración puede admitir hasta seis niveles de profundidad. Este límite no incluye el nivel raíz ni el nivel de suscripción.
- Cada grupo de administración y suscripción solo puede admitir un elemento primario.
- Cada grupo de administración puede tener muchos elementos secundarios.
- Todas las suscripciones y grupos de administración están dentro de una única jerarquía en cada directorio.

### Grupo de recursos

Los grupos de recursos existen para ayudar a administrar y organizar los recursos de Azure. Al colocar recursos de uso, tipo o ubicación similar en un grupo de recursos, puede proporcionar orden y organización a los recursos que cree en Azure.

- **Ciclo de vida** - Si elimina un grupo de recursos, también se eliminarán todos los recursos que contenga.
- **Autorización** - se pueden aplicar permisos de control de acceso basado en roles (RBAC).

### Azure Resource Manager

Proporciona una capa de administración que le permite crear, actualizar y eliminar recursos de la cuenta de Azure.

Todas las funcionalidades que están disponibles en Azure Portal también lo están a través de PowerShell, la CLI de Azure, las API REST y los SDK de cliente.

 

### Regiones y zonas

Las zonas de disponibilidad son centros de datos separados físicamente dentro de una región de Azure.

- **Servicios de zona**: ancle el recurso a una zona específica (por ejemplo, máquinas virtuales, discos administrados, direcciones IP).
- **Servicios de redundancia de zona**: la plataforma se replica automáticamente entre zonas (por ejemplo, almacenamiento con redundancia de zona, SQL Database).

**Pares de regiones:** Cada región de Azure se empareja siempre con otra región de la misma zona geográfica (por ejemplo, EE. UU., Europa o Asia) que se encuentre como mínimo a 500 km de distancia.

### Conceptos de Azure

**App Service** es un servicio basado en HTTP que permite crear y hospedar muchos tipos de soluciones basadas en la Web sin necesidad de administrar la infraestructura.

**Azure Marketplace** es una tienda en línea que hospeda aplicaciones certificadas y optimizadas para ejecutarse en Azure.

