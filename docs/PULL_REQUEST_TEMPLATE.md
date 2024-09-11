    Los integrantes del proyecto deben hacer una actualización de su sucursal(repositorio) local
    git remote add upstream url_del_repositorio_foo
    git fetch upstream
    git switch main
    git merge upstream/main
 
    NOTA: Cuando el encargado del repositorio este modo "code review" en el ambiente de main-test(rama local)
    seguir los pasos de forma estricta con 2 opcione tú ejecutas la de tú preferencia

    opcion #1
    git fetch origin pull/id_del_pull_request/head:nombre-de-rama
    git switch main-test
    git merge nombreDelUsuario/nombre-de-rama --no-commit
    git switch main  

    opcion #2
    git fetch origin pull/id_del_pull_request/head:nombreDelUsuario/nombre-de-la-feature-NÚMERO-DE-PR
    git switch main-test
    git merge nombreDelUsuario/nombre-de-la-feature-NÚMERO-DE-PR --no-commit
    git switch main  
    
    Conectar tú repositorio local, con el repositorio base
    git remote add upstream url_del_repositorio_base.git
    
    Si la escuadra quiere recibir los últimos cambios del repositorio base, realizar lo siguiente:
    git fetch upstream
    git merge upstream/main
