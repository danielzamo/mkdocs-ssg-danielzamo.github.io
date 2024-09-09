Notas/artículos relacionadas: [[Inicio]], [[Paradigmas de programación]] , [[Shell Scripting - funciones]]

Supongamos la escritura de un script con paradigma funcional de codificación. Algo como

```bash
cat app1_functions.sh
...
# Función privada. 
# Responsabilidad: Montar recurso remoto compartido vía CIFS
# Tres argumentos de entrada. Sin retorno
function _app1_mount_type_cifs(){
  local srv_cifs="$1"; local source_shared="$2"; local point_localhost="$3"

  sudo mount -t cifs "//${srv_cifs}/${source_shared}" "${point_localhost}" \
   -o username=${SMB_USER},password=${SMB_PWD},domain=${SMB_DOMAIN},uid=${SMB_UID},gid=${SMB_GID},vers=3.0
}

function app1_get_cifs_resources(){...}
```

Usar prefijos como `app1_...` para las funciones que están implementadas para un script (o funcionalidades especificas) es una excelente práctica, especialmente cuando se trabaja en proyectos colaborativos o en scripts que podrían ser ejecutados en un entorno donde existen muchas funciones definidas. Esto ayuda a evitar colisiones de nombres y deja claro que esas funciones son específicas de una implementación en particular. A continuación se detallan algunos pros y contras de usar estos prefijos tanto para funciones públicas como privadas:

## Ventajas de Usar Prefijos Personalizados

1. **Evitar Conflictos de Nombres**: El prefijo `app1_` asegura que las funciones no interfieran con otras funciones que puedan tener nombres genéricos, especialmente cuando se trabaja en scripts grandes o se utilizan bibliotecas de terceros.
    
2. **Claridad de Propiedad**: El usar propias o personalizadas iniciales como prefijo, se indica claramente que esas funciones pertenecen a tu implementación ( o una en particular) o a un módulo específico, lo cual es útil para otros desarrolladores o incluso para ti mismo en el futuro.
    
3. **Organización y Mantenimiento**: Prefijos consistentes ayudan a organizar las funciones y a encontrar rápidamente las relacionadas con tu proyecto.
    
### Prefijos para Funciones Privadas

Para las funciones privadas, usar un prefijo adicional `_` junto con el prefijo de tus iniciales (`_app1_`) también puede ser una buena práctica:

- **Ejemplo**: `_app1_set_name()`

Esto señala dos cosas:

- Que la función pertenece a tu implementación (`app1_`).
- Que es una función privada y no debería ser usada fuera de su contexto (`_`).

### ¿Puede Generar Confusión?

Si bien puede parecer que usar tanto `_` como `app1_` podría ser redundante, la práctica está alineada con convenciones comunes de programación. Sin embargo, es importante mantener la consistencia:

- **Consistencia**: Usa el prefijo `app1_` en todas tus funciones públicas.
- **Privacidad**: Usa `_app1_` para funciones privadas que no deberían ser accesibles externamente.

### Ejemplos:

- **Función Pública**: `app1_get_text()` — indica que es una función pública de tu implementación.
- **Función Privada**: `_app1_set_name()` — indica que es una función privada dentro de tu implementación.

### Recomendaciones:

1. **Documentación**: Siempre documenta el propósito de los prefijos en tus scripts o módulos para evitar confusiones.
    
2. **Separación Lógica**: Mantén las funciones bien separadas según su uso y acceso (públicas vs privadas), y utiliza los prefijos para reforzar esta separación.
    
3. **Consistencia en Prefijos**: Mantén una convención clara y consistente para los prefijos que usas en todo el proyecto para evitar malentendidos.