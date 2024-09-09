Notas/artículos relacionadas: [[Inicio]], [[Paradigmas de programación]] ,  [[Shell Scripting - mas de funciones]] 
### Buenas Prácticas para Nombres de Funciones

- **Claridad**: El nombre debe describir lo que hace la función. Debe ser claro para alguien que lea el código, incluso sin tener un conocimiento profundo de inglés.
    
- **Consistencia**: Si usas un prefijo o sufijo común (como `log_` para funciones de registro), úsalo de manera consistente en todas las funciones similares.
    
- **Verbos para Acciones**: En inglés, es común usar verbos para funciones que realizan acciones, como `log`, `get`, `set`, `calculate`, etc. Esto ayuda a que el código sea más fácil de entender.

- **Usar convenciones comunes:** Además, usar un prefijo como `_` para denotar funciones "privadas" (Comentar lo de privadas en shell scripting) es una convención común en muchos lenguajes de programación, o shell scripting, como Bash, para indicar que estas funciones no deberían ser invocadas directamente fuera de su contexto o módulo. Esto puede ayudar a mantener la claridad y la estructura del código, especialmente cuando otros desarrolladores trabajen con él o en proyectos más grandes.

- **No Abusar de Abreviaturas**: Por ejemplo una función de nombre `log_exe`, donde esta implementada tal que:

```bash
log_exe() {
  local type="${1:-INFO}"  # Si $1 está vacío, usar "INFO" por defecto
  local message="$2"
  local echo_msg

  # Define los prefijos de los tipos de log
  case "$type" in
    INFO)
      echo_msg="[INFO] $(date '+%Y-%m-%d %H:%M:%S') - $message"
      ;;
    ERROR)
      echo_msg="[ERROR] $(date '+%Y-%m-%d %H:%M:%S') - $message" >&2
      ;;
    WARNING)
      echo_msg="[WARNING] $(date '+%Y-%m-%d %H:%M:%S') - $message"
      ;;
    *)
      echo_msg="[UNKNOWN] $(date '+%Y-%m-%d %H:%M:%S') - $message"
      ;;
  esac
  echo "$echo_msg" 
}
```

   Aunque `exe` es una abreviatura conocida para "execute", es mejor evitar abreviaturas excesivas que podrían no ser claras para todos. En este caso, `log_exe` es una elección razonable, pero también se podría mejor usar algo más explícito como `log_message` o `log_action` si se prefiere mayor claridad.

Otras buenas practicas para Funciones
- **Dividir el código** Dividir el código en funciones más pequeñas y específicas es una buena práctica, ya que mejora la legibilidad, facilita la depuración, y promueve la reutilización del código. 