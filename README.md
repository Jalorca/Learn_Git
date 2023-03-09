# Learn_Git
Este repositorio es para registrar los conocimientos y buenas prácticas en el uso de las herrramientas de Git y GitHub, donde se emplearan distintos recursos.
## Video: Uso común de Git - Data Latam - https://www.youtube.com/watch?v=SVzyWV1Iep8
> Presenta el uso de la herramienta Git y GitHub a través del editor RStudio. El espacio de trabajo en RStudio es más amigable y simple para la ejecución de los comandos de Git a través del mismo editor, lo cual hace más visual la ejecución de los pasos en el flujo de trabajo con GitHub. Es necesario comprender el flujo de trabajo en GitHub, es un requisito totalmente indispensable.

Los comandos o acciones presentados para Git y GitHub son para mantener una colabaración, el flujo de trabajo y evitar errores.

Los comandos son los siguientes:

- Desde GitHub:
    - Indentificar el repositorio (**Upstream**) donde se va a trabajar.
    - Realizar una bifurcación (**Origin**), se hara con la herramienta ***Fork*** en la página del repositorio en GitHub seleccionado.
- Desde el terminal del editor, Git:
    - ***git config user.name*** [ Nombre en GitHub ], configurar nombre de usuario GitHub.
    - ***git config user.email*** [ Correo GitHub ], configurar email GitHub de usuario.
    - ***git clone*** [ HTTPS del repositorio bifurcado ], Clonar la bifurcación en un directorio local (**Master**) donde se trabajara.
    - ***git branch*** [ Nombre de la rama, por acuerdo es T#, # es el número del tiquete ], Crear rama del directorio local, donde se realizaran los cambios correspondientes al tiquite asignado.
    - ***git checkout*** [ Rama ], Cambiar de rama.
    - ***git add*** [ Nombre de archivo que ha tenido cambios/ . ], agrega los cambios al área de preparación. Considerar que antes es necesario guardar los cambios en el archivo.
    - ***git status***, muestra el estados de los cambios realizados con respeto al repositorio **Origin**.
    - ***git commit***, agrega al repositorio local los cambios realizados.
    - ***git push*** , empuja los commits o cambios al repositorio **Origin**.
- Desde GitHub
    - Realizar un **Pull Request**, cuando ingresar al repositorio bifurcado en GitHub se mostrará una notificación de Pull Request.
    - Indicar el tiquete al cual se vincula el Pull Request y los cambios realizados, finalmente se asigna un revisor y se envia el Pull Request.
    - El revisor verifica los cambios y puede aceptar, rechazar o observar el pull request.
- Desde el terminal del editor, Git:
    - Si el Pull Request ha sido aceptado el propietario del repositorio Upstream le hara merge con el los cambios de Origin a Upstream.
    - Mantener actualizado Master
    - ***git fetch*** [ upstream ], verifica y trae los últimos cambios de Upstream hacia master.
    - ***git rebase*** [ upstream/master ], aplica los últimos cambios de Upstream en Master.
    - ***git push*** , empuja los commits o cambios al repositorio **Origin**.
> Desde RStudio estos comandos pueden ser ejecutados desde la interfza de usuario que te presneta el editor, haciendo más visual el flujo de trabajo

## Video: Ayuda para solicitudes de fusión en GitHub - Data Latam - https://www.youtube.com/watch?v=PSNNbeVUxFc
> La librería 'usethis' empaqueta y simplifica los pasos para mantener el flujo en el trabajo con GitHub, pero es necesario entender bien los comandos básicos de Git y el entorno de GitHub. Además, muestra de el proceso que realizan las funciones de la librería 'usethis' lo cual ayuda a mantener un seguimiento a lo que se esta ejecutando.

La librería 'usethis' intenta simplicar los pasos para mantener el flujo de trabajo con GitHub presentando los siguientes comandos ejecutados desde el editor RStudio:
- ***create_from_github( Upstream )***, crea Fork y Master.
- **git_sitrep()**, muestra reporte y configuración del repositorio.
- ***pr_init("Nombre de pullrequest")***, indica el inicio del pull request.
- ***pr_push()***, Empujar cambios a origin
- ***pr_sync()***, sincroniza upstream con el master y el origin con el master y compara cambios, se pueden resolver comflictros ene sta partes.
- ***pr_view***, muestra vista del pull request en GitHub. se puede ejecutar luego de un pr_push()
- ***pr_finish()***, actuliza master con base en el upstream e ilimina ramas sobrantes.
> Al apllicar estos comandos te muestra en el terminal lo que se esta ejecutando.