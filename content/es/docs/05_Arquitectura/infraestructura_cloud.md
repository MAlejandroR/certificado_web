+++
title = "Infraestructura y Cloud Computing"
weight = 20
draft= true
icon = "fa-solid fa-cloud"
+++

## ️ Infraestructura y servicios en la nube

En el despliegue moderno de aplicaciones web, los servidores y servicios pueden ejecutarse en **infraestructuras cloud** (nube).  
Esto permite escalar recursos, reducir costes y mejorar el rendimiento.

---


### Servidores web.
[En esta página de netcraft](https://www.netcraft.com/blog/january-2024-web-server-survey/),  podemos ver un análisis mensual de la cuota de mercado de servidores web, basado en el número de sitios web, dominios y computadoras activas.

Como podemos ver en la imagen, {{< color >}} en enero de 2024 {{< /color >}}, el estudio reporta cambios en la popularidad de servidores como {{< color >}} nginx (23.21% de los sitios web) y Apache (20.70%) {{< /color >}}.
También incluye información sobre el crecimiento de Cloudflare y OpenResty, así como actualizaciones sobre software relevante para servidores.
![analisis_netcraft](analisis_netcraft.png)

#### Servidor Web: Algunas Características
#### Servidor Web: Algunas Características

- **Contenido estático y dinámico**: Soporte para contenido estático (HTML) y dinámico (mediante CGI, intérpretes de PHP, Python, etc.).
- **Host virtuales**: Permite manejar varias direcciones web desde una única dirección IP.
- **Velocidad de respuesta**: Autoregulación de la velocidad de respuesta según la demanda.
- **Autenticación básica**: Integración con sistemas de autenticación para acceso restringido.
- **Soporte de SSL**: Capacidad de cifrar la comunicación mediante HTTPS.
- **Módulos**: Extensible mediante módulos para soporte de nuevas características.

---

### Servidor de Aplicaciones

- Un servidor de aplicaciones es un paquete de software que proporciona servicios a las aplicaciones, como:
    - **Seguridad**
    - **Balanceo de carga**
    - **Gestión de sistemas distribuidos**

- Inicialmente, estos servidores aparecieron en la plataforma **Java**, pero hoy en día se usan para todo tipo de tecnologías.
- Los servidores web y de aplicaciones suelen trabajar juntos, aunque son diferentes. Un servidor de aplicaciones necesita de un servidor web para funcionar.
  {{< imgproc servidor_aplicaciones Fill "770x491" >}}

{{< /imgproc >}}
---

### Servidor de Bases de Datos

- **Tipos de bases de datos**:
    - **Relacionales**: MySQL, Oracle, SQLServer, MariaDB
    - **No relacionales**: MongoDB

---

### Servidores Complementarios

- **Correo**:
    - Servidores como **Postfix** o **Sendmail**.
    - Extensiones como **SPF** para verificación y control de SPAM.
    - Generalmente se delega al proveedor del servicio.

- **DNS**:
    - Servidores como **Bind** gestionan la resolución de nombres en Internet.
    - También puede ser gestionado por el proveedor.

---

### Servidores Complementarios: Proxies

- Un **proxy** actúa como intermediario entre el cliente y el servidor web.

    - **Proxy directo**:
        - Mejora la eficiencia y seguridad al controlar el acceso a redes externas.
        - Ofrece funcionalidades de caché y autenticación.

    - **Proxy inverso**:
        - Se coloca entre el cliente y los servidores internos.
        - Permite balancear la carga entre varios servidores.
        - Mejora el rendimiento al ofrecer caché.
        - Un proxy inverso puede servir múltiples servidores desde la misma URI.

---

### Infraestructura Hardware

- **Cloud Computing**:
    - Se basa en la provisión de servicios informáticos a través de la nube, sin depender de dispositivos específicos.
    - Ventajas:
        - **Agilidad**: Mejores recursos para el usuario.
        - **Coste**: Reducidos en comparación con infraestructura física.
        - **Escalabilidad**: Ajuste de recursos según demanda.
        - **Rendimiento mejorado**.

    - Desventajas:
        - Dependencia de la conexión a Internet.
        - Los datos sensibles pueden no estar completamente bajo el control de la empresa.
        - Curvas de aprendizaje elevadas debido a cambios continuos en la tecnología.

---

### Modelos de Servicios Cloud

- **IaaS (Infrastructure as a Service)**:
    - Provisión de recursos físicos y virtuales, como máquinas virtuales, almacenamiento, y balanceadores de carga.
    - Se usan hipervisores como **Xen**, **KVM**, **VMware ESX/ESXi** o **Hyper-V**.
    - Ejemplos: **Amazon EC2**, **Azure VM**, **OpenStack**.

- **PaaS (Platform as a Service)**:
    - Permite desarrollar, ejecutar y gestionar aplicaciones sin preocuparse por la infraestructura.
    - Se puede ejecutar sobre IaaS, máquinas físicas o contenedores.
    - Ejemplos: **Google App Engine**, **OpenShift**, **Heroku**.

- **SaaS (Software as a Service)**:
    - Aplicaciones disponibles a través de Internet.
    - Ejemplos: **Google Docs**, **Dropbox**, **Twitter**, **Netflix**.

- **CaaS (Container as a Service)**:
    - Nuevo concepto entre IaaS y PaaS, basado en el uso de contenedores.
    - Permite desplegar aplicaciones sin necesidad de virtualización completa.
    - Ejemplos: **Docker**, **OpenStack Magnum**, **Kubernetes**, **Rancher**:

        - **Docker**: Es una plataforma de contenedores que permite empaquetar aplicaciones y todas sus dependencias en contenedores ligeros. Facilita la portabilidad entre entornos y el despliegue rápido de aplicaciones, tanto en desarrollo como en producción.

        - **Kubernetes**: Es una plataforma de orquestación de contenedores que automatiza el despliegue, escalado y operación de aplicaciones en contenedores. Facilita la gestión de múltiples contenedores en clústeres, distribuyendo la carga y asegurando alta disponibilidad.

        - **OpenStack Magnum**: Es una solución de OpenStack para gestionar contenedores mediante orquestadores como Kubernetes o Docker Swarm, integrándose en infraestructuras OpenStack.

        - **Rancher**: Es una plataforma que simplifica la gestión de Kubernetes y contenedores, ofreciendo una interfaz intuitiva para gestionar clústeres Kubernetes en múltiples entornos (nubes, servidores físicos).


###  Servidores web

[Netcraft](https://www.netcraft.com/blog/january-2024-web-server-survey/) publica estudios mensuales sobre el uso de servidores web.

En **enero de 2024**, reportaba:
- **nginx** → 23,21% de los sitios web
- **Apache** → 20,70%
- Crecimiento de **Cloudflare** y **OpenResty**.

![analisis_netcraft](analisis_netcraft.png)

#### Características comunes

- Soporte para contenido **estático y dinámico**
- **Hosts virtuales** (varios dominios en una misma IP)
- **Autenticación y SSL/HTTPS**
- **Módulos** extensibles
- **Gestión de rendimiento y caché**

---

### ️ Servidores de aplicaciones

Un **servidor de aplicaciones** ofrece servicios intermedios a las aplicaciones, como:

- Seguridad
- Balanceo de carga
- Gestión de sesiones y recursos distribuidos

Se usa en muchos lenguajes (Java, PHP, Node.js…).  
Trabaja junto al servidor web, pero su función es diferente.

{{< imgproc servidor_aplicaciones Fill "770x491" >}}
Esquema básico de un servidor de aplicaciones.
{{< /imgproc >}}

---

###  Servidores de bases de datos

Tipos principales:

- **Relacionales** → MySQL, PostgreSQL, Oracle, MariaDB
- **No relacionales (NoSQL)** → MongoDB, Redis, Cassandra

---

### 🧱 Servidores complementarios

#### 📬 Correo
- Postfix, Sendmail
- Uso de SPF, DKIM, antispam
- A menudo gestionados por el proveedor de hosting.

#### 🌐 DNS
- Servidores como **Bind** gestionan la resolución de nombres.

####  Proxies
- **Proxy directo:** mejora seguridad, caché y filtrado.
- **Proxy inverso:** balancea carga y mejora rendimiento.  
  _Ejemplo: Nginx o Cloudflare como proxy inverso._

---

## ️ Cloud Computing

La **computación en la nube** permite disponer de servicios sin depender de dispositivos físicos.

### Ventajas
- Escalabilidad y flexibilidad
- Reducción de costes
- Acceso desde cualquier lugar
- Mejor rendimiento

### Desventajas
- Dependencia de conexión a Internet
- Datos en servidores externos
- Curva de aprendizaje continua

---

## ☁️ Modelos de servicio en la nube

| Modelo | Significado | Ejemplo |
|:--|:--|:--|
| **IaaS** | Infraestructura como servicio | Amazon EC2, Azure VM |
| **PaaS** | Plataforma como servicio | Google App Engine, Heroku |
| **SaaS** | Software como servicio | Google Docs, Dropbox, Netflix |
| **CaaS** | Contenedores como servicio | Docker, Kubernetes, Rancher |

---

###  Tecnologías de contenedores

#### Docker
Plataforma que permite empaquetar aplicaciones y dependencias en **contenedores ligeros**.  
Facilita el despliegue rápido y la portabilidad entre entornos.

#### Kubernetes
Sistema de **orquestación** que automatiza el despliegue y gestión de contenedores.  
Ofrece alta disponibilidad y escalado automático.

#### OpenStack Magnum
Herramienta para gestionar contenedores dentro de infraestructuras **OpenStack**.

#### Rancher
Plataforma que simplifica la administración de clústeres **Kubernetes** en entornos híbridos o multi-nube.

---

{{< alert title="En resumen" color="success" >}}
Los servicios cloud permiten ejecutar y escalar aplicaciones web sin preocuparse por la infraestructura física.  
Son el presente del **despliegue y mantenimiento de aplicaciones web modernas**.
{{< /alert >}}
