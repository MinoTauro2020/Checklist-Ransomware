### Checklist de Respuesta Temprana a Ransomware con Instrucciones para Microsoft Defender

1. **Confirmar el incidente**:
   - [ ] Verifica la alerta:
     - Ve al portal de Microsoft Defender (security.microsoft.com).
     - Haz clic en **Incidents & Alerts** en el menú izquierdo.
     - Selecciona el incidente relacionado con el ransomware para ver detalles.
   - [ ] Identifica dispositivos/usuarios afectados:
     - En la página del incidente, revisa las pestañas **Devices** y **Users** para listar los afectados.

2. **Aislar sistemas comprometidos**:
   - [ ] Aislar dispositivos:
     - En el incidente, haz clic en la pestaña **Devices**.
     - Selecciona el dispositivo afectado, haz clic en **Actions** (tres puntos o botón de acción) y elige **Isolate Device**.
   - [ ] Prioriza endpoints no críticos:
     - Revisa la lista de dispositivos para evitar aislar servidores críticos (como controladores de dominio).
   - [ ] Desconectar backups online:
     - Esto es manual; verifica en tu sistema de backups y desactiva conexiones de red si es necesario.

3. **Restringir accesos sospechosos**:
   - [ ] Suspender cuentas:
     - En el incidente, ve a la pestaña **Users**.
     - Selecciona la cuenta sospechosa, haz clic en **Actions** y elige **Suspend User** o **Sign Out User**.
   - [ ] Restablecer contraseñas:
     - Ve a **Microsoft 365 Admin Center** (admin.microsoft.com).
     - En **Users > Active Users**, selecciona la cuenta, haz clic en **Reset Password**.
   - [ ] Habilitar MFA:
     - En el Admin Center, ve a **Users > Active Users**, selecciona el usuario, haz clic en **Manage Multifactor Authentication** y actívalo.

4. **Bloquear actividad maliciosa**:
   - [ ] Añadir indicadores de bloqueo:
     - En Defender, haz clic en **Settings** (menú izquierdo) > **Endpoints** > **Indicators**.
     - Selecciona **IP**, **URL** o **File**, añade los detalles sospechosos (ej. IP del atacante) y configura la acción como **Block**.
   - [ ] Revisar firewalls/proxies:
     - Esto es externo a Defender; accede a tu firewall o proxy y bloquea las IPs/URLs identificadas.

5. **Preservar evidencias**:
   - [ ] Registrar detalles:
     - En el incidente, haz clic en **Timeline** para ver eventos relacionados y anótalos manualmente (hora, dispositivos, alertas).
   - [ ] Evitar eliminar archivos:
     - No hagas clic en opciones como **Delete** o **Quarantine** en archivos sospechosos hasta recopilar evidencias.
   - [ ] Guardar capturas:
     - Si ves una nota de rescate, usa una herramienta de captura (ej. Snipping Tool) y guárdala en un dispositivo seguro.

6. **Establecer comunicación segura**:
   - [ ] Usar canal externo:
     - No uses Defender para esto; coordina por teléfono o una app segura (ej. Signal, WhatsApp).
   - [ ] Notificar al equipo:
     - En Defender, puedes exportar detalles del incidente (clic en **Export** en la página del incidente) para compartir con el equipo de ciberseguridad.

7. **Evaluar el alcance inicial**:
   - [ ] Revisar vector de entrada:
     - En el incidente, ve a **Timeline** o **Evidence and Response** para ver alertas sobre phishing, RDP o exploits.
   - [ ] Buscar archivos cifrados:
     - En la pestaña **Devices**, selecciona un dispositivo, haz clic en **File Inventory** y busca extensiones inusuales (ej. .locky, .crypt).
   - [ ] Identificar datos críticos:
     - Revisa manualmente las carpetas afectadas en el dispositivo aislado (usa **Live Response** si está habilitado).

8. **Evitar acciones prematuras**:
   - [ ] No pagar el rescate:
     - No hay clics en Defender para esto; simplemente evita contactar a los atacantes.
   - [ ] No descifrar archivos:
     - Evita usar herramientas de descifrado no verificadas; no hay opción directa en Defender para esto.

**Notas**:
- Registra cada acción (fecha, hora, responsable) en un documento externo.
- Si ves más dispositivos afectados o una nota de rescate, actualiza el checklist.
- Cuando tengas más datos, podemos detallar pasos como análisis forense o restauración.
