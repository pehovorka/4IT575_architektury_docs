@startuml

cloud "Google Cloud Platform" as gcp <<cloud provider>> {
node "CloudSQL" as cloudsql <<DBaaS environment>> {
node "PostgreSQL" as pgsql <<DBMS>> {
database "DB systému hodnocení studentských prog. úloh"
}
}
node "Cloud Run" as run <<execution environment>> {
node "Web server container" as webServer <<docker container>> {
artifact "Mediátor" <<application>>
}
node "Runtime enviroments" as enviroments {
node "Node.js runtime env container" as nodeEnv <<docker container>>{
artifact "Aplikace node.js runtime" <<application>>
}
node "Python runtime env container" as pythonEnv <<docker container>>{
artifact "Aplikace Python runtime" <<application>>
}
node "Java runtime env container" as javaEnv <<docker container>>{
artifact "Aplikace Java runtime" <<application>>
}
}

    }
    node "Firebase Hosting" as firebase <<execution environment>> {
        artifact "Frontend React aplikace" <<application>>
    }

    node "Cloud Storage" as storage <<storage>> {
        storage "Úložiště"
    }

}

node "Zařízení uživatele aplikace" as userDevice
node "Server studijího IS" as studyISServer
node "Server TurnItIn" as turnitinServer

enviroments -- storage : WebSocket
enviroments -right- webServer : WebSocket

webServer -- cloudsql : WebSocket

firebase -- userDevice : WebSocket
webServer -- studyISServer : WebSocket
webServer -- turnitinServer : WebSocket
webServer -- firebase : WebSocket

cloudsql -[hidden]- firebase
cloudsql -[hidden]- run

webServer -- storage : WebSocket

@enduml
