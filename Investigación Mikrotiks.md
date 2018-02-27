
# Mikrotik

## Que es un Mikrotik RouterOS

MilkroTik RouterOS es un sistema operativo basado en el kernel de Linux 2.6 usado en el hardware de los Microtik RouterBOARD que es la división de hardware de la marca Mikrotik. Se caracteriza por poseer su propio S.O de fácil configuración. Estos dispositivos poseen la ventaja de tener una relación costo /beneficio muy alta.

Ahora, lo que hace interesante a un RouterOS es que puede ser instalado en una computadora, convirtiéndola en un router con todas las características necesarias: firewall, routing, punto de acceso wireless, administración de ancho de banda, servidor VPN y más.

# Configuración
RouterOS soporta varios métodos de configuración como son:
- Acceso local vía teclado y monitor
- Consola serial con una terminal
- Acceso vía Telnet y SSH vía una red
- Una interfaz gráfica llamada WinBox
- Una API para el desarrollo de aplicaciones propias para la configuración
- En caso de no contar con acceso local y existe un problema con las direcciones IP RouterOS soporta una conexión basada en direcciones MAC usando las herramientas customizadas Mac-Telnet y herramientas de Winbox.

> A Partir de su versión RouterOS v4 agrega el lenguaje de Scripting Lua, que expande las posibilidades para programar y automatizar el sistema.

# Características
Se enlista lo que nos brinda RouterOS, ya sea que lo usemos en un RouterBoard o en una PC.

## Firewall
El firewall integrado implementa el filtrado de paquetes y provee funciones de seguridad que son usadas para el manejo del flujo de datos desde y hacia el router. Junto con el NAT, previene el acceso no autorizado a una red conectada directamente. Puede filtrar por direcciones IP, tuerto TCP/UDP, rango de puertos, protocolos, entre otros parámetros. Soporta además lista de direcciones estáticas y dinámicas y puede interceptar paquetes con un patrón definido. Cuenta además con soporte para IPv6.

## Routing
RouterOS soporta rutas estáticas y varios protocolos de rutas dinámicas.
- Para IPv4 soporta RIP v1 y v2, OSPF v2, BGP v4
- Para IPv6 soporta RIPng, OSPFV v3 y BGP

También soporta VRF, políticas basadas en rutas, rutas basadas en interfaz y ECMP. Se puede utilizar el Firewall para marcar los paquetes que lleguen desde una conexión determinada y que estos salgan por un proveedor distinto.

## MPLS
MPLS (Multiprotocol Label Switching), puede ser utilizado para reemplazar los paquetes IP salientes, la decisión del reenvío ya no se realiza en base al header IP o tabla de enrutamiento, sino en etiquetas adjuntadas al paquete. Este acercamiento acelera el reenvío del paquete porque la búsqueda del destino es más simple que la búsqueda del  enrutamiento. La Eficiencia en el proceso de reenvío es el mayor beneficio de MPLS.
Algunos de los features de MPLS soportados son:
- Enlazado de etiquetas estáticas para IPv4
- Protocolo de distribución de etiquetas para IPv4
- Túneles RSVP
- Descubrimiento automático y basado en la señalización VPLS MP-BGP
- MPLS IP VPN basado en MP-BGP

## VPN
RouterOS soporta diversos métodos de conexión VPN para establecer una conexión segura sobre redes abiertas o internet. Estos métodos son:
- IPSec
- Túneles de punto a punto (OpenVPN, PPTP, PPPoE, L2TP)
- Features avanzados PPP (MLPPP, BCP)
- Túneles simples (IPIP, EoIP)
- Soporte a túneles 6 a 4 (IPv6 sobre IPv4)
- VLAN
- VPN basado en MPLS

Nos permite interconectar de forma segura varias redes permitiéndonos interconectar varias localidades, usar los recursos de la organización mientras nos movilizamos y aumentar la seguridad de nuestras conexiones inalámbricas

## Conexiones inalámbricas
Las siguientes son algunas de las tecnologías wireless soportadas:
- Punto de acceso y cliente inalámbrico IEEE802.11a/b/g/n
- Protocolos propietarios Nstreme y Nstreme2
- Sondeo de clientes
- RTS/CTS
- Sistema de distribución inalámbrica
- Punto de acceso virtual
- Encriptación WEP, WPA, WPA2
- Lista de control de acceso
- WMM
- Protocolo de ruteo inalámbrico MME
- Entre otros

Los protocolos Nstreme le permiten a RouterOS extender el alcance y la velocidad de la conexión inalámbrica cuando se utiliza los routers de Mikrotik en cada extremo. Soporta además NStreme dual que permite utilizar dos antenas en cada extremo, una para recibir y otra para enviar.

## Hostpot

La puerta de enlace de Mikrotik Hotspot permite crear una red de acceso público para usuarios alámbricos e inalámbricos. Al usuario le será presentada una pantalla de login cuando accede al navegador web. Una vez provee credenciales validos se le dará acceso a internet. No es necesaria ninguna instalación de un software, el hotspot dirigirá cualquier conexión al formulario de login. Podemos administrar además las conexiones de los usuarios, uso de ancho de banda, tiempo de conexión y más.
Hotspot soporta autenticación standard de servidores RADIUS o el administrador de usuarios integrados que nos permite una administración centralizada de todos los usuarios en nuestra red.

## Web Proxy
RouterOS cuenta con un servidor proxy para el almacenamiento en cache de recursos en la web, aumentando la velocidad de acceso entregando al cliente archivos en cache a la velocidad interna de la red. RouterOS provee las siguientes características de un servidor proxy:
- Proxy HTTP regular
- Proxy transparente
- Lista de acceso por fuente, destino, URL o método solicitado
- Almacenamiento del cache en Discos externos
- Soporte a proxy SOCKS
- Lista de acceso cache para especificar el recursos deben ser accedidos directamente y cuales vía otro servidor
- Entre otros.

## Herramientas
RouterOS nos provee una serie de herramientas para administrar nuestra red y para optimizar las tareas. 

**Herramientas**
- Prueba de ancho de banda
- SSH
- Herramientas para el envio de Email y SMS
- Tabla de conexiones activas
- Servidor TFTP
- Servidor NTP
- SNMP
- RADIUS


RouterOS le agrega diversas funcionalidades a los mismo routers de Mikrotik como a cualquier PC que esté sin uso, y con el sistema operativo se le pueda implementar alguna función. 

# Tipos de aplicaciones  de los Mikrotiks

## Aplicaciones por default de MikrotikRouterOS
Mikrotik te brinda la posibilidad de gestionar varias aplicaciones, ya sea instalando el software en PC o entre ellas:
- **Enlaces inalámbricos.**
- **Web Caché**. De archivos pequeños o de páginas. Puedes hacerlos en un Pc pero no en un RB, ya que en un RB750 por ejemplo no tiene suficiente memoria de almacenamiento.
- **Identificación y priorización de tráfico.** Control de tráfico, marcado de paquete. Con esta aplicación de serie en el software de Mikrotik puedes aplicar muchas reglas para optimizar tu ISP.

## Aplicaciones profesionales de MikrotikRouterOS
- **Balanceo de conexiones WAN.** Esta herramienta te será de gran ayuda a la hora de ofrecer un servicio de calidad a tus clientes. Esto se hace cuando tienes contratados dos proveedores de Internet haciendo un Load Balanceque hace que tus clientes nunca se pierdan la conexión.
- **PPPOE Server.** Podrás configurarlo fácilmente gracias a la herramienta que incorpora el software de Mikotik.
- **Enlaces punto a punto.** Permitiéndote abarcar mayores zonas de cobertura y cubrir las necesidades de clientes más lejanos aumentando la calidad y el servicio, lo que te permitirá ir ampliando progresivamente tu empresa de ISP.

## Aplicaciones de seguridad de Mikrotik RouterOS
- **Seguridad Wireless.** La seguridad siempre ha de ser una prioridad en Internet, para ti como proveedor de servicio hacia tus suscriptores y para que ellos tengan la garantía de que están trabajando con una empresa seria. Mikrotik RouterOS te ofrece las máximas posibilidades en este campo.
- **Firewall NAT.** Evidentemente Mikrotik te ofrece aplicaciones de última tecnología para impedir que alguien pueda entrar en tu red.


## Analisis de Mikrotiks
| Column 1 | Column 2 |
|:--------:| -------------:|
| centered | right-aligned |

> Escrito Por [Hugo Yadiel](https://github.com/YadielFicachi)
