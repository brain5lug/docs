# Загрузить Docker-образ в реестр

Инструкция описывает, как загрузить локальный [Docker-образ](../../concepts/docker-image.md) в реестр.

> [!NOTE]
>
> Чтобы загрузить образ, необходимо [аутентифицироваться](../authentication.md) в реестре.


---
 
**[!TAB CLI]**

1. Посмотрите список доступных для загрузки Docker-образов:
    
    ```
    $ docker image list
    REPOSITORY                                                        TAG                 IMAGE ID            CREATED             SIZE
    container-registry.cloud.yandex.net/crpd50616s9a2t7gr8mi/ubuntu   hello               50ff4b0e5783        23 hours ago        86.7MB
    ubuntu                                                            latest              1d9c17228a9e        2 weeks ago         86.7MB
    ```
    
1. Загрузите необходимый Docker-образ в реестр:
    
    ```
    $ docker push container-registry.cloud.yandex.net/crpd50616s9a2t7gr8mi/ubuntu:hello
    ```

1. Проверьте, что образ загрузился в реестр, [получив список Docker-образов в реестре](docker-image-list.md#docker-image-list).
 
---
