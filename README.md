Web Application Exploitation
Cross-Site Scripting(XSS)_Malicious WebSockets Hijacking

-Objetivos de la Emulación
1.T1059.007 - JavaScript Exploitation (Stored XSS): Inyeccion persistente de codigo JavaScript
dentro de una aplicacion web sin controles de sanitizacion.
2.Canal de Comando y Control (C2) via WebSockets: Intercepcion prioritaria 
de vectores de autenticacion (Tokens JWT en LocalStorage y Cookies de sesion)
manteniendo un canal interactivo bidireccional activo.

-Inventario de Archivos
1.Web_Exploitation_XSS/Attacker_C2/server.js: Servidor de Comando y Control (C2)
interactivo basado en WebSockets.
2.Web_Exploitation_XSS/Attacker_C2/payload.js: Codigo de explotacion 
inyectado encargado del robo de JWT/Cookies.
3.Web_Exploitation_XSS/Vulnerable_App/app.js: Aplicacion web desprotegida
que simula un entorno vulnerable.
4.Web_Exploitation_XSS/Defender_Scripts/Hunter_WebSockets.ps1: Logica de auditoria y
analisis de procesos de red sospechosos.

- Mitigacion Propuesta (CSP)
Para neutralizar la infiltración a traves de WebSockets maliciosos se debe implementar la cabecera HTTP de control de contenido: Content-Security-Policy: default-src 'self'; connect-src 'self';
