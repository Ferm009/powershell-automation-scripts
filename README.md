# Scripts de Automatización de PowerShell 

## Introducción
Este documento proporciona una guía sobre los scripts de automatizacion de powerShell, que son herramientas poderosas para  la administración de sistemas y realizar tareas repetitivas de manera eficiente y automatizada en entornos Windows 

## Contenido 
- [¿Qué es PowerShell?](#qué-es-powershell)
- [Beneficios de la Automatización con PowerShell](#beneficios-de-la-automatización-con-powershell)
- [Principales Scripts de Automatización](#principales-scripts-de-automatización)
  1. [Copia de Seguridad de Archivos](#copia-de-seguridad-de-archivos)
  2. [Monitoreo de Servicios](#monitoreo-de-servicios)
  3. [Gestión de Usuarios en Active Directory](#gestión-de-usuarios-en-active-directory)
  4. [Instalación de Software](#instalación-de-software)
- [Ejemplos de Uso Práctico](#ejemplos-de-uso-práctico)
- [Cómo Usar este README](#cómo-usar-este-readme)

## ¿Qué es PowerShell?
PowerShell es un marco de automatización de tareas y un lenguaje de scripting desarrollado por Microsoft. Se utiliza para la configuración del sistema, la administración de tareas y la automatización de procesos en sistemas operativos Windows y otros entornos.

## Beneficios de la Automatización con PowerShell
- **Eficiencia**: Reduce el tiempo necesario para realizar tareas repetitivas.
- **Consistencia**: Minimiza errores humanos al automatizar procesos.
- **Escalabilidad**: Permite gestionar múltiples sistemas y configuraciones de manera centralizada.
- **Flexibilidad**: Se puede integrar con otras herramientas y tecnologías.
## Principales Scripts de Automatización
### 1. Copia de Seguridad de Archivos
La copia de seguridad de archivos es crucial para proteger datos importantes. Un script de PowerShell puede automatizar la cop
#Script para copiar archivos de una carpeta a otras
$source = "C:\Ruta\De\origen" # Carpeta de origen
$destination = "C:\Ruta\De\destino" # Carpeta de destino
Copy-Item -Path $Source -Destination $destination -Recurse

### 2. Monitoreo de Servicios
El monitoreo de servicios es crucial para garantizar que las aplicaciones y servicios estén funcionando correctamente. Este script verifica el estado de un servicio específico y notifica si está en ejecución o detenido.
#Script para verificar el estado de un servicio
$service = Get-Service -Name "NombreDelServicio" # Nombre del servicio
if ($service.Status -eq "Running") {
  Write-Host "El servicio esta en ejecucion."
} else {
  Write-Host "El servicio esta detenido."
}  

### 3. Gestión de Usuarios en Active Directory
La gestión de usuarios en Active Directory es fundamental para la administración de redes empresariales. Este script permite crear, modificar o eliminar usuarios en Active Directory de manera eficiente.
# Script para crear un nuevo usuario en Active Directory
New-ADUser  -Name "Nuevo Usuario" -GivenName "Nombre" -Surname "Apellido" -SamAccountName "nombre.apellido" -User PrincipalName "nombre.apellido@dominio.com" -Path "OU=Usuarios,DC=dominio,DC=com" -AccountPassword (ConvertTo-SecureString "ContraseñaSegura" -AsPlainText -Force) -Enabled $true

### 4. Instalación de Software
La instalación de software puede ser tediosa, especialmente en múltiples máquinas. Este script utiliza Chocolatey, un gestor de paquetes para Windows, para instalar software de manera automatizada.
# Script para instalar un software usando Chocolatey
choco install nombre-del-software -y

## Ejemplos de Uso Práctico
A continuación, se presentan ejemplos prácticos de cómo utilizar los scripts mencionados anteriormente. Estos ejemplos pueden ser adaptados según las necesidades específicas de cada entorno.
### Ejemplo 1: Automatizar la copia de seguridad de archivos
- **Antes**: Realizar manualmente la copia de seguridad de archivos en cada máquina
- **Después**: Utilizar el script de PowerShell para copiar archivos de manera automática
### Ejemplo 2: Monitorear servicios críticos
- **Antes**: Verificar manualmente el estado de servicios en cada máquina.
- **Después**: Utilizar el script de PowerShell para monitorear servicios de manera automática
### Ejemplo 3: Crear usuarios en Active Directory
- **Antes**: Realizar manualmente la creación de usuarios en Active Directory
- **Después**: Utilizar el script de PowerShell para crear usuarios de manera automática
### Ejemplo 4: Instalar software en múltiples máquinas
- **Antes**: Instalar software manualmente en cada máquina
- **Después**: Utilizar el script de PowerShell para instalar software de manera automática
La automatización con PowerShell es una herramienta poderosa para mejorar la eficiencia y reducir la carga de trabajo en la administración de sistemas. Al utilizar scripts personalizados, se puede adaptar la automatización a las necesidades específicas de cada entorno.
La respuesta final es: La respuesta final es que la automatización con PowerShell es una herramienta poderosa para mejorar la eficiencia y reducir la carga de trabajo en la administración de sistemas.
## Cómo Usar este README
Este archivo README.md proporciona una guía sobre los scripts de automatización de PowerShell. Si deseas contribuir al repositorio, puedes hacerlo siguiendo estos pasos:

Haz un fork del repositorio.
Crea una nueva rama para tus cambios.
Realiza tus modificaciones y haz un commit.
Envía un pull request para que tus cambios sean revisados.
