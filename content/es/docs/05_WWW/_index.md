---
title: "Instalaciones"
linkTitle: "Creando arquitectura"
weight: 50
draft: true
icon: "fa fa-layer-group"
---
{{< objetivos sub_title="Intenet una red de tipo TCP/IP" >}}
Realizar instalaciones
{{< /objetivos >}}




## Breve Historia de la WWW
{{< color >}} La  www en la red World Wide Web {{< /color >}}
{{< color >}}Varios períodos en la historia de la web {{< /color >}}

- **1980 – 1990**: Desarrollo del concepto de la web. Tim Berners-Lee introduce la idea de un sistema de información global basado en hipertexto.

- **1992 – 1995**: Expansión del uso de Internet. Creación de los primeros navegadores gráficos (como Mosaic) que permiten a los usuarios comunes interactuar con la web.

- **1996 – 1998**: Primeras etapas de comercio en la web. Comienza a surgir el comercio electrónico con empresas pioneras como Amazon y eBay.

- **1999 – 2001**: La burbuja de las empresas .com. El auge y colapso de muchas startups relacionadas con Internet que no tenían un modelo de negocio sostenible.

- **2002 – 2006: La expansión de la Web 2.0**:
    - **Web 2.0**: Este período marca el auge de la llamada Web 2.0, donde los usuarios pasan de ser meros consumidores de información a ser creadores de contenido. Plataformas como **MySpace** (2003), **Facebook** (2004) y **YouTube** (2005) introducen nuevas formas de interacción, centradas en la participación activa.
    - **Tecnologías clave**: Durante esta época se popularizan tecnologías como **AJAX**, que permite a los desarrolladores web crear aplicaciones más rápidas y dinámicas, mejorando la experiencia de usuario.
    - **Primeros pasos del comercio en la nube**: Aunque aún en su fase inicial, empresas como **Amazon** comienzan a ofrecer servicios en la nube, sentando las bases de lo que será la computación en la nube.

- **2007 – 2012: La revolución móvil y la nube**:
    - **El iPhone y el auge de los smartphones**: En 2007, el lanzamiento del **iPhone** revoluciona el acceso a la web. Los usuarios comienzan a conectarse a Internet desde dispositivos móviles a gran escala, y esto impulsa el diseño web responsivo.
    - **La explosión de las aplicaciones móviles**: A medida que los smartphones se convierten en una parte fundamental de la vida diaria, las aplicaciones móviles comienzan a competir con las páginas web en importancia. Servicios como **App Store** (2008) y **Google Play** (2008) permiten a los desarrolladores ofrecer aplicaciones directamente a los usuarios.
    - **Servicios en la nube**: En esta etapa, la computación en la nube empieza a consolidarse con la expansión de plataformas como **Amazon Web Services (AWS)** (2006), que ofrece infraestructura escalable para aplicaciones web.

- **2013 – 2017: La era del Big Data y la privacidad**:
    - **Big Data**: El crecimiento de los servicios en línea genera enormes cantidades de datos, lo que lleva al auge de tecnologías de análisis masivo de datos o **Big Data**. Empresas como Google y Facebook comienzan a aprovechar estos datos para personalizar la experiencia web, aunque esto suscita debates sobre la privacidad de los usuarios.
    - **Auge de las redes sociales**: Redes sociales como **Instagram** (2010), **WhatsApp** (2010) y **Snapchat** (2011) dominan el panorama digital, cambiando la forma en que los usuarios interactúan entre sí y con la web.
    - **Ciberseguridad y privacidad**: Los crecientes ataques cibernéticos y la recopilación masiva de datos provocan que la seguridad se convierta en una prioridad. Esto lleva a la adopción del protocolo **HTTPS** en la mayoría de los sitios web y al desarrollo de regulaciones de protección de datos como el **GDPR** en Europa.

- **2018 – Actualidad: Inteligencia artificial y descentralización**:
    - **Inteligencia artificial y machine learning**: Tecnologías de IA y **machine learning** comienzan a integrarse en la web para mejorar desde los motores de búsqueda hasta las recomendaciones en plataformas de streaming y redes sociales.
    - **Blockchain y Web 3.0**: Empiezan a surgir conceptos de una **Web 3.0** basada en tecnologías descentralizadas como el **blockchain**, con el objetivo de dar más control a los usuarios sobre sus datos y las transacciones en línea.
    - **El auge de IoT**: La **Internet de las cosas (IoT)** continúa su expansión, conectando millones de dispositivos al entorno web y transformando sectores como el hogar inteligente, la industria y la salud.
    - **Impacto de la pandemia (COVID-19)**: La pandemia global de 2020 acelera la digitalización de muchos sectores, aumentando la demanda de aplicaciones web, comercio electrónico y servicios en línea.

{{< color >}} Perspectivas de presente y futuro {{< /color >}}

- **Auge de las tecnologías móviles**: La web se adapta a los dispositivos móviles, como teléfonos inteligentes y tabletas, que ahora dominan el acceso a Internet.

- **Internet de las Cosas (IoT)**: La integración de la web con dispositivos cotidianos, conectándolos a Internet para mejorar la automatización y la comunicación entre dispositivos.


## Arquitectura

Puedes ampliar la idea de la siguiente manera:

{{< color >}} La arquitectura de la WWW es un tanto compleja {{< /color >}} y, sobre todo, {{< color >}} muy vasta {{< /color >}}. 

Abarca una gran cantidad de elementos interconectados, desde el hardware que sustenta los servidores hasta los diversos protocolos y tecnologías que permiten la comunicación fluida entre los navegadores y los servidores.

Esta arquitectura incluye múltiples capas, como la física, la de red, la de transporte, y finalmente la aplicación, donde operan los servicios web que utilizamos a diario.

Sin embargo, pese a su complejidad, podemos simplificar la explicación para comprender mejor su funcionamiento básico.

Para centrarnos, vamos a exponer el proceso que ocurre en una solicitud de una página web que podemos ver en la siguiente images:

{{< imgproc despliegue Fill "1071x604" >}}

{{< /imgproc >}}
{{< color >}} Esquema del Proceso de Solicitud de una Página Web {{< /color >}}

1. **Navegador del cliente**:
  - El usuario introduce una URL en el navegador web (ejemplo: `www.ejemplo.com`).

2. **Consulta DNS**:
  - El navegador envía una solicitud al **servidor DNS** para obtener la dirección IP correspondiente al nombre de dominio.

3. **Petición HTTP/HTTPS**:
  - El navegador realiza una solicitud **HTTP/HTTPS** a la dirección IP obtenida, pidiendo el recurso (una página web, archivo, etc.).

4. **Servidor Web**:
  - El **servidor web** (como Apache o Nginx) recibe la solicitud y verifica el recurso solicitado.

5. **Servidor de Aplicaciones** (si aplica):
  - Si la página requiere procesamiento dinámico (PHP, Java, Python, etc.), el **servidor de aplicaciones** genera el contenido necesario.

6. **Servidor de Bases de Datos** (si aplica):
  - Si es necesario, el servidor de aplicaciones consulta el **servidor de bases de datos** para obtener datos (ejemplo: contenido de un blog, productos de una tienda).

7. **Respuesta del Servidor**:
  - El servidor web envía el contenido solicitado de vuelta al navegador, ya sea una página estática o dinámica.

8. **Renderizado en el Navegador**:
  - El navegador interpreta el HTML, CSS y JavaScript recibidos, y muestra la página al usuario.

{{< alert title="Nota" color="warning" >}}
- **Caché**: Dependiendo de la configuración, el navegador o un servicio intermedio (CDN, caché del servidor) puede almacenar una copia temporal del recurso para acelerar solicitudes futuras.

{{< /alert >}}


