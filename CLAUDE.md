# Programacion-Servicios-Y-Procesos (PSP, 2º DAM)

## Cómo trabajar conmigo
Reglas comunes a todos mis repos (copia de mi `C:\dev\CLAUDE.md`, para que también las lean las sesiones en la nube). Soy estudiante de DAM en el IES Isidra de Guzmán.
- En prácticas evaluables, resuélvelas completas (sin modo de pistas). Al terminar, crea junto a la entrega (en `docs/` si existe) un `guia-defensa-<practica>.md` para defenderla en clase, al estilo de la guía de DataStock. Las guías de defensa no se suben nunca a GitHub: cada repo tiene `guia-defensa-*.md` en su `.gitignore` (añádelo si falta).
- Estructura de la guía de defensa: cómo usarla; cómo arrancar, ejecutar y ensayar sin estropear la entrega; qué pide el enunciado y dónde se cumple cada requisito; visión general (capas, flujo, decisiones de diseño a justificar); y por cada requisito: qué pide, dónde está, explicación línea a línea, cómo demostrarlo, errores típicos, preguntas de la profesora con su respuesta y 🔧 modificaciones en directo (el cambio que podrían pedir, con el código exacto y dónde va). Al final: casos prácticos «¿qué pasaría si…?», «corrige este error» (síntoma → causa → arreglo) y chuleta con plan de ensayo.
- Si la tarea es grande, antes de tocar nada dime cómo lo harías (plan por pasos) y espera a que lo apruebe o lo corrija.
- Cuando escribas código, explícalo línea por línea y di por qué elegiste esa forma y no otra.
- Si ves un error de concepto o algo que no entiendo bien, dímelo aunque no te lo pregunte.
- Responde en español.
- No hagas commit ni push sin que te lo pida. Commits sin `Co-Authored-By` ni líneas de atribución.
- **Pull requests en todos los repos (asignaturas y personales):** nunca se commitea directo en `main`. Una rama por cambio (nombre con guiones, sin barra: con barra GitHub dio error 500), sus commits pequeños, `gh pr create --fill --base main`, tests en local y CI en verde (`gh pr checks <n> --watch`), y `gh pr merge <n> --merge --delete-branch` (nunca squash, para que cada commit quede en el historial). Si el repo no tiene tests o CI para lo que cambia, dilo y propón añadirlos. Si la carpeta la comparten otras sesiones, trabaja en un worktree propio y no cambies de rama allí. Sigue valiendo que el commit, push y merge solo se hacen cuando yo lo pida.
- No subas binarios generados (`target/`, `*.class`, `__pycache__/`, `*.pyc`, `bin/`, `obj/`, `Library/` de Unity).
- Nunca leas, muestres ni subas ficheros `.env`, tokens ni credenciales.
- PDFs, .docx, .odt y .pptx son apuntes o enunciados: léelos solo si hacen falta para la tarea.

Programación concurrente en Java: procesos, hilos y (más adelante) sockets y servicios.

## Estructura
- `ut0-repaso/` — repaso de Java y streams (PDF/PPTX).
- `ut1-procesos/apuntes/` — `psp-ut1.pdf` y `ejemplos-en-clase/` (Lanzador*.java y el proyecto IntelliJ `ut1-ejemplos-comunicacion-procesos`, paquete `PSP`: ProcessBuilder, redirecciones, pipes, inheritIO).
- `ut1-procesos/ejercicios/` — enunciados y proyecto IntelliJ `ut1-procesos` (configuraciones en `run/`).
- `ut1-procesos/practica/`
- `ut1-procesos/soluciones/` — soluciones de los ejercicios y tareas de la UT1 (Linux y Windows); `apuntes/apuntes-ut1-procesos.md`.
- `ut2-hilos/apuntes/` — unidad en curso.
- `ut2-hilos/ejercicios/` — enunciado, proyecto IntelliJ `bloque1-4` de la profesora (paquetes `bloqueN.<ejercicio>`, no tocar) y `soluciones-ejercicios-ut2.md`.
- `ut2-hilos/soluciones/bloque1-4/` — copia del proyecto con los TODO resueltos y comentados línea a línea.

## Compilar y ejecutar
- Proyectos IntelliJ (`.iml`, sin Maven): abrir la carpeta del proyecto en IntelliJ, o `javac -d out src/PSP/*.java && java -cp out PSP.Clase`.
- Los ejemplos de procesos lanzan otros programas Java: compila también la clase hija (p. ej. `HijoCuadrado`) antes de ejecutar el padre.

## Notas
- Los `.zip` de Ejercicios son material del profesor (enunciado y solución): no los modifiques.
