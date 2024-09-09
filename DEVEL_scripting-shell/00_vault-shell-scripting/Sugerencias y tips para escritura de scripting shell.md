## Uso de rutas absolutas

- Usar rutas absolutas para cargar el archivo de entorno (`ENV_FILE="$HOME/.dz/env/my.sh"`) o dependientes (necesarios) para el propio script. Esto es una buena práctica porque asegura que siempre se cargue el archivo correcto sin depender del `$PATH` desde donde se invoque.

## Verificación de archivos de entorno (del propio script)

-  