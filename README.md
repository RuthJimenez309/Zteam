Web Application Exploitation
Cross-Site Scripting(XSS)_Malicious WebSockets Hijacking

-Objetivos de la Emulación
1.T1059.007 - JavaScript Exploitation (Stored XSS): Inyeccion persistente de codigo JavaScript
dentro de una aplicacion web sin controles de sanitizacion.
2.Canal de Comando y Control (C2) via WebSockets: Intercepcion prioritaria 
de vectores de autenticacion (Tokens JWT en LocalStorage y Cookies de sesion)
manteniendo un canal interactivo bidireccional activo.

-Inventario de Archivos
Servidor de Comando y Control (C2)interactivo basado en WebSockets/Web_Exploitation_XSS/Attacker_C2/server.js-
Codigo de explotacion inyectado encargado del robo de JWT/Cookies-Web_Exploitation_XSS/Attacker_C2/payload.js-
Aplicacion web desprotegida que simula un entorno vulnerable -Web_Exploitation_XSS/Vulnerable_App/app.js
Logica de auditoria y analisis de procesos de red sospechosos -Web_Exploitation_XSS/Defender_Scripts/Hunter_WebSockets.ps1- 

- Mitigacion Propuesta (CSP)
Para neutralizar la infiltración a traves de WebSockets maliciosos se debe implementar la cabecera HTTP de control de contenido: Content-Security-Policy: default-src 'self'; connect-src 'self';
