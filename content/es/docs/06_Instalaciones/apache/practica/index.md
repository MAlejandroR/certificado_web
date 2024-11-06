+++
title = 'practicando'
date = 2024-10-15T07:04:49+02:00
draft = false
icon = "fas fa-chalkboard-teacher"
weight = 10
+++
 
{{% pageinfo %}}

#### Practicando 

Creamos en nuestro servidor web, dos sitios virtuales o virtual host, llamados www.informatica.com y www.musica.com
Cada uno de ellos van a tener esta peculiaridad de comportameiento y es que informatica.com va a ir a buscar los recursos a la carpeta /var/www/informatica, y www.muscia.com, a /var/www/musica

{{% /pageinfo %}}

Para configurar dos sitios en Apache, vamos a crear dos archivos de configuración en `sites-available` y luego activarlos.

A continuación, encontrarás el código de ejemplo para cada archivo de configuración.

### Configuración para **www.informatica.com**

{{< highlight bash "linenos=table, hl_lines=1" >}}
<VirtualHost *:80>
{{< color >}}ServerName www.informatica.com{{< /color >}}
{{< color >}}ServerAlias informatica.com{{< /color >}}
{{< color >}}DocumentRoot /var/www/informatica{{< /color >}}

    ErrorLog ${APACHE_LOG_DIR}/informatica_error.log
    CustomLog ${APACHE_LOG_DIR}/informatica_access.log combined
</VirtualHost>
{{< / highlight >}}

### Configuración para **www.musica.com**

{{< highlight bash "linenos=table, hl_lines=1" >}}
<VirtualHost *:80>
{{< color >}}ServerName www.musica.com{{< /color >}}
{{< color >}}ServerAlias musica.com{{< /color >}}
{{< color >}}DocumentRoot /var/www/musica{{< /color >}}

    ErrorLog ${APACHE_LOG_DIR}/musica_error.log
    CustomLog ${APACHE_LOG_DIR}/musica_access.log combined
</VirtualHost>
{{< / highlight >}}

### Modificación del archivo hosts

Para realizar pruebas en local, añade los siguientes dominios al archivo `hosts` en tu equipo. En Ubuntu, el archivo se encuentra en `/etc/hosts`; en Windows, en `c:\windows\system32\drivers\etc\hosts`. Añade estas líneas:

{{< highlight bash "linenos=table, hl_lines=1" >}}
127.0.0.1 www.informatica.com informatica.com
127.0.0.1 www.musica.com musica.com
{{< / highlight >}}

Luego, puedes probar que los dominios responden ejecutando:

{{< highlight bash "linenos=table, hl_lines=1" >}}
ping www.informatica.com
ping www.musica.com
{{< / highlight >}}

### Activación de los sitios

Una vez que hayas creado estos archivos de configuración en `sites-available`, debes activarlos usando los siguientes comandos:

{{< highlight bash "linenos=table, hl_lines=1" >}}
sudo a2ensite informatica.conf
sudo a2ensite musica.conf
sudo systemctl reload apache2
{{< / highlight >}}

Esto creará los enlaces simbólicos en `sites-enabled` y recargará Apache para aplicar la configuración.

---

Este guión guía paso a paso la configuración de dos sitios en Apache usando Virtual Hosts. Asegúrate de tener las carpetas `/var/www/informatica` y `/var/www/musica` creadas y con el contenido que quieres servir antes de activar los sitios.


{{< color >}}  {{< /color >}}
### Parámetros a configurar

#### Creando el directorio

### Como crear distintos nombres para mi equipo


