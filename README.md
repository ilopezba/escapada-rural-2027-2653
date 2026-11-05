# ¡Nos vamos de casa rural! - Escapada 2027

Aplicación web moderna, intuitiva y responsive diseñada para organizar escapadas en grupo votando la disponibilidad de los fines de semana de enero y febrero de 2027.

## Características

- **Experiencia de usuario rápida:** Introduce tu nombre, selecciona tus fines de semana libres y guarda en menos de 30 segundos sin necesidad de registros complejos.
- **Calendario visual completo:** Visualización clara de los fines de semana de enero y febrero de 2027.
- **Resultados en tiempo real:** Estadísticas automáticas, indicador del fin de semana ganador y desglose por asistente.
- **Sincronización con Supabase:** Persistencia de datos en la nube para que todo el grupo comparta la misma información.
- **Compartir por WhatsApp:** Botón directo para enviar la encuesta al grupo de amigos.

## Configuración de Supabase (Backend)

Para activar la base de datos compartida:

1. Crea una tabla en tu proyecto de Supabase llamada `participants` con la siguiente estructura:
   - `id` (uuid, Primary Key, Default: `gen_random_uuid()`)
   - `name` (text, Not Null)
   - `weekends` (text array o jsonb)
2. Configura las políticas de seguridad (RLS) según tus necesidades para permitir lectura y escritura pública anónima si lo deseas.
3. Introduce tus credenciales (URL y Anon Key) en la interfaz si aparece el banner de configuración.