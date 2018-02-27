<h1 id="mikrotik">Mikrotik</h1>
<h2 id="que-es-un-mikrotik-routeros">Que es un Mikrotik RouterOS</h2>
<p>MilkroTik RouterOS es un sistema operativo basado en el kernel de Linux 2.6 usado en el hardware de los Microtik RouterBOARD que es la división de hardware de la marca Mikrotik. Se caracteriza por poseer su propio S.O de fácil configuración. Estos dispositivos poseen la ventaja de tener una relación costo /beneficio muy alta.</p>
<p>Ahora, lo que hace interesante a un RouterOS es que puede ser instalado en una computadora, convirtiéndola en un router con todas las características necesarias: firewall, routing, punto de acceso wireless, administración de ancho de banda, servidor VPN y más.</p>
<h1 id="configuración">Configuración</h1>
<p>RouterOS soporta varios métodos de configuración como son:</p>
<ul>
<li>Acceso local vía teclado y monitor</li>
<li>Consola serial con una terminal</li>
<li>Acceso vía Telnet y SSH vía una red</li>
<li>Una interfaz gráfica llamada WinBox</li>
<li>Una API para el desarrollo de aplicaciones propias para la configuración</li>
<li>En caso de no contar con acceso local y existe un problema con las direcciones IP RouterOS soporta una conexión basada en direcciones MAC usando las herramientas customizadas Mac-Telnet y herramientas de Winbox.</li>
</ul>
<blockquote>
<p>A Partir de su versión RouterOS v4 agrega el lenguaje de Scripting Lua, que expande las posibilidades para programar y automatizar el sistema.</p>
</blockquote>
<h1 id="características">Características</h1>
<p>Se enlista lo que nos brinda RouterOS, ya sea que lo usemos en un RouterBoard o en una PC.</p>
<h2 id="firewall">Firewall</h2>
<p>El firewall integrado implementa el filtrado de paquetes y provee funciones de seguridad que son usadas para el manejo del flujo de datos desde y hacia el router. Junto con el NAT, previene el acceso no autorizado a una red conectada directamente. Puede filtrar por direcciones IP, tuerto TCP/UDP, rango de puertos, protocolos, entre otros parámetros. Soporta además lista de direcciones estáticas y dinámicas y puede interceptar paquetes con un patrón definido. Cuenta además con soporte para IPv6.</p>
<h2 id="routing">Routing</h2>
<p>RouterOS soporta rutas estáticas y varios protocolos de rutas dinámicas.</p>
<ul>
<li>Para IPv4 soporta RIP v1 y v2, OSPF v2, BGP v4</li>
<li>Para IPv6 soporta RIPng, OSPFV v3 y BGP</li>
</ul>
<p>También soporta VRF, políticas basadas en rutas, rutas basadas en interfaz y ECMP. Se puede utilizar el Firewall para marcar los paquetes que lleguen desde una conexión determinada y que estos salgan por un proveedor distinto.</p>
<h2 id="mpls">MPLS</h2>
<p>MPLS (Multiprotocol Label Switching), puede ser utilizado para reemplazar los paquetes IP salientes, la decisión del reenvío ya no se realiza en base al header IP o tabla de enrutamiento, sino en etiquetas adjuntadas al paquete. Este acercamiento acelera el reenvío del paquete porque la búsqueda del destino es más simple que la búsqueda del  enrutamiento. La Eficiencia en el proceso de reenvío es el mayor beneficio de MPLS.<br>
Algunos de los features de MPLS soportados son:</p>
<ul>
<li>Enlazado de etiquetas estáticas para IPv4</li>
<li>Protocolo de distribución de etiquetas para IPv4</li>
<li>Túneles RSVP</li>
<li>Descubrimiento automático y basado en la señalización VPLS MP-BGP</li>
<li>MPLS IP VPN basado en MP-BGP</li>
</ul>
<h2 id="vpn">VPN</h2>
<p>RouterOS soporta diversos métodos de conexión VPN para establecer una conexión segura sobre redes abiertas o internet. Estos métodos son:</p>
<ul>
<li>IPSec</li>
<li>Túneles de punto a punto (OpenVPN, PPTP, PPPoE, L2TP)</li>
<li>Features avanzados PPP (MLPPP, BCP)</li>
<li>Túneles simples (IPIP, EoIP)</li>
<li>Soporte a túneles 6 a 4 (IPv6 sobre IPv4)</li>
<li>VLAN</li>
<li>VPN basado en MPLS</li>
</ul>
<p>Nos permite interconectar de forma segura varias redes permitiéndonos interconectar varias localidades, usar los recursos de la organización mientras nos movilizamos y aumentar la seguridad de nuestras conexiones inalámbricas</p>
<h2 id="conexiones-inalámbricas">Conexiones inalámbricas</h2>
<p>Las siguientes son algunas de las tecnologías wireless soportadas:</p>
<ul>
<li>Punto de acceso y cliente inalámbrico IEEE802.11a/b/g/n</li>
<li>Protocolos propietarios Nstreme y Nstreme2</li>
<li>Sondeo de clientes</li>
<li>RTS/CTS</li>
<li>Sistema de distribución inalámbrica</li>
<li>Punto de acceso virtual</li>
<li>Encriptación WEP, WPA, WPA2</li>
<li>Lista de control de acceso</li>
<li>WMM</li>
<li>Protocolo de ruteo inalámbrico MME</li>
<li>Entre otros</li>
</ul>
<p>Los protocolos Nstreme le permiten a RouterOS extender el alcance y la velocidad de la conexión inalámbrica cuando se utiliza los routers de Mikrotik en cada extremo. Soporta además NStreme dual que permite utilizar dos antenas en cada extremo, una para recibir y otra para enviar.</p>
<h2 id="hostpot">Hostpot</h2>
<p>La puerta de enlace de Mikrotik Hotspot permite crear una red de acceso público para usuarios alámbricos e inalámbricos. Al usuario le será presentada una pantalla de login cuando accede al navegador web. Una vez provee credenciales validos se le dará acceso a internet. No es necesaria ninguna instalación de un software, el hotspot dirigirá cualquier conexión al formulario de login. Podemos administrar además las conexiones de los usuarios, uso de ancho de banda, tiempo de conexión y más.<br>
Hotspot soporta autenticación standard de servidores RADIUS o el administrador de usuarios integrados que nos permite una administración centralizada de todos los usuarios en nuestra red.</p>
<h2 id="web-proxy">Web Proxy</h2>
<p>RouterOS cuenta con un servidor proxy para el almacenamiento en cache de recursos en la web, aumentando la velocidad de acceso entregando al cliente archivos en cache a la velocidad interna de la red. RouterOS provee las siguientes características de un servidor proxy:</p>
<ul>
<li>Proxy HTTP regular</li>
<li>Proxy transparente</li>
<li>Lista de acceso por fuente, destino, URL o método solicitado</li>
<li>Almacenamiento del cache en Discos externos</li>
<li>Soporte a proxy SOCKS</li>
<li>Lista de acceso cache para especificar el recursos deben ser accedidos directamente y cuales vía otro servidor</li>
<li>Entre otros.</li>
</ul>
<h2 id="herramientas">Herramientas</h2>
<p>RouterOS nos provee una serie de herramientas para administrar nuestra red y para optimizar las tareas.</p>
<p><strong>Herramientas</strong></p>
<ul>
<li>Prueba de ancho de banda</li>
<li>SSH</li>
<li>Herramientas para el envio de Email y SMS</li>
<li>Tabla de conexiones activas</li>
<li>Servidor TFTP</li>
<li>Servidor NTP</li>
<li>SNMP</li>
<li>RADIUS</li>
</ul>
<p>RouterOS le agrega diversas funcionalidades a los mismo routers de Mikrotik como a cualquier PC que esté sin uso, y con el sistema operativo se le pueda implementar alguna función.</p>
<h1 id="tipos-de-aplicaciones--de-los-mikrotiks">Tipos de aplicaciones  de los Mikrotiks</h1>
<h2 id="aplicaciones-por-default-de-mikrotikrouteros">Aplicaciones por default de MikrotikRouterOS</h2>
<p>Mikrotik te brinda la posibilidad de gestionar varias aplicaciones, ya sea instalando el software en PC o entre ellas:</p>
<ul>
<li><strong>Enlaces inalámbricos.</strong></li>
<li><strong>Web Caché</strong>. De archivos pequeños o de páginas. Puedes hacerlos en un Pc pero no en un RB, ya que en un RB750 por ejemplo no tiene suficiente memoria de almacenamiento.</li>
<li><strong>Identificación y priorización de tráfico.</strong> Control de tráfico, marcado de paquete. Con esta aplicación de serie en el software de Mikrotik puedes aplicar muchas reglas para optimizar tu ISP.</li>
</ul>
<h2 id="aplicaciones-profesionales-de-mikrotikrouteros">Aplicaciones profesionales de MikrotikRouterOS</h2>
<ul>
<li><strong>Balanceo de conexiones WAN.</strong> Esta herramienta te será de gran ayuda a la hora de ofrecer un servicio de calidad a tus clientes. Esto se hace cuando tienes contratados dos proveedores de Internet haciendo un Load Balanceque hace que tus clientes nunca se pierdan la conexión.</li>
<li><strong>PPPOE Server.</strong> Podrás configurarlo fácilmente gracias a la herramienta que incorpora el software de Mikotik.</li>
<li><strong>Enlaces punto a punto.</strong> Permitiéndote abarcar mayores zonas de cobertura y cubrir las necesidades de clientes más lejanos aumentando la calidad y el servicio, lo que te permitirá ir ampliando progresivamente tu empresa de ISP.</li>
</ul>
<h2 id="aplicaciones-de-seguridad-de-mikrotik-routeros">Aplicaciones de seguridad de Mikrotik RouterOS</h2>
<ul>
<li><strong>Seguridad Wireless.</strong> La seguridad siempre ha de ser una prioridad en Internet, para ti como proveedor de servicio hacia tus suscriptores y para que ellos tengan la garantía de que están trabajando con una empresa seria. Mikrotik RouterOS te ofrece las máximas posibilidades en este campo.</li>
<li><strong>Firewall NAT.</strong> Evidentemente Mikrotik te ofrece aplicaciones de última tecnología para impedir que alguien pueda entrar en tu red.</li>
</ul>
<h1 id="análisis-de-routers-mikrotiks">Análisis de routers Mikrotiks</h1>

<table>
<thead>
<tr>
<th align="center">Nombre</th>
<th align="center">Descripción</th>
<th align="center">Arquitectura</th>
<th align="right">RAM</th>
<th align="center">Almacenamiento</th>
<th align="right">Precio</th>
</tr>
</thead>
<tbody>
<tr>
<td align="center">RB750r2 (hEX lite)</td>
<td align="center">Es un pequeño enrutador ethernet de cinco puertos en una carcasa de plástico.</td>
<td align="center">MIPSBE</td>
<td align="right">64 MB</td>
<td align="center">16 MB</td>
<td align="right">$ 39.95</td>
</tr>
</tbody>
</table><blockquote>
<p>Escrito Por <a href="https://github.com/YadielFicachi">Hugo Yadiel</a></p>
</blockquote>

