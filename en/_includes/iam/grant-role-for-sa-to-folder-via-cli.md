1. Find out the service account ID by its name:

    ```
    $ yc iam service-account get my-robot
    id: aje6o61dvog2h6g9a33s
    folder_id: b1gvmob03goohplct641
    created_at: "2018-10-15T18:01:25Z"
    name: my-robot
    ```

    If you don't know the name of the service account, get a list of service accounts with their IDs:

    ```
    $ yc iam service-account list
    +----------------------+------------------+-----------------+
    |          ID          |       NAME       |   DESCRIPTION   |
    +----------------------+------------------+-----------------+
    | aje6o61dvog2h6g9a33s | my-robot         | my description  |
    +----------------------+------------------+-----------------+
    ```

1. Assign a role to the `my-robot` service account using its ID:

    ```
    $ yc resource-manager folder add-access-binding my-folder \
        --role viewer \
        --subject serviceAccount:aje6o61dvog2h6g9a33s
    ```

