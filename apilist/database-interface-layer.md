# Database Interface Layer of Tutorial System

## API END POINT

- Api Endpoint: [https://api.tutorialinaja.tech/dbil/v1/](https://api.tutorialinaja.tech/dbil/v1/)

## API Docs

- Api Docs: [https://dbil.docs.apiary.io/](https://dbil.docs.apiary.io/)

## Entity Relationship Diagram

- [x] [Sprint 1](https://dbdiagram.io/d/5d28c8f8ced98361d6dc9bab)
- [x] [Sprint 2](https://dbdiagram.io/d/5d2edb4fced98361d6dcbc9f)
- [ ] [Spirnt 2 (Refactoring)](https://dbdiagram.io/d/5d60b65bced98361d6dddf7b) [We Are Here Now]

## API Repository

- Api Repository: [https://github.com/pojok-projects/tutorialsystem-database-interface-layer](https://github.com/pojok-projects/tutorialsystem-database-interface-layer)

## Description

Database Interface Layer is governing input and output process of database communication from any other micro services. In this abstraction layer, this repository will provide the API for communication with the following tables:

- content-category (master table)
- content-metadata (transactional table with one of the foreign key comes from content-category table)

As the result of this service, the Input and Output query into content-category and content-metadata tables will be provided as rest APIs.

See Red highlight below for the scope of this repository.

![Database Interface Layer Highlight](https://raw.githubusercontent.com/pojok-projects/tutorialsystem-database-interface-layer/blob/master/images/Content_Manager_highlight.png)

## Table Structure API End Points

### Content Metadata Table Routes

| URL                            | Method | INFO              |
| ------------------------------ | ------ | ----------------- |
| `content/metadata`             | GET    | Get All Data      |
| `content/metadata/store`       | POST   | Save Data         |
| `content/metadata/{id}`        | GET    | Get Data by ID    |
| `content/metadata/search`      | POST   | Search Data Query |
| `content/metadata/update/{id}` | POST   | Update Data by ID |
| `content/metadata/delete/{id}` | POST   | Delete Data by ID |

### Content Table Routes

| URL                                      | Method | INFO              |
| ---------------------------------------- | ------ | ----------------- |
| `content/subtitle`                       | GET    | Get All Data      |
| `content/subtitle/store`                 | POST   | Save Data         |
| `content/subtitle/{id}`                  | GET    | Get Data by ID    |
| `content/subtitle/search`                | POST   | Search Data Query |
| `content/subtitle/update/{id}`           | POST   | Update Data by ID |
| `content/subtitle/delete/{id}`           | POST   | Delete Data by ID |
| `content/category`                       | GET    | Get All Data      |
| `content/category/store`                 | POST   | Save Data         |
| `content/category/{id}`                  | GET    | Get Data by ID    |
| `content/category/search`                | POST   | Search Data Query |
| `content/category/update/{id}`           | POST   | Update Data by ID |
| `content/category/delete/{id}`           | POST   | Delete Data by ID |
| `content/playlists/category`             | GET    | Get All Data      |
| `content/playlists/category/store`       | POST   | Save Data         |
| `content/playlists/category/{id}`        | GET    | Get Data by ID    |
| `content/playlists/category/search`      | POST   | Search Data Query |
| `content/playlists/category/update/{id}` | POST   | Update Data by ID |
| `content/playlists/category/delete/{id}` | POST   | Delete Data by ID |

### User Table Routes

| URL                | Method | INFO              |
| ------------------ | ------ | ----------------- |
| `user`             | GET    | Get All Data      |
| `user/store`       | POST   | Save Data         |
| `user/{id}`        | GET    | Get Data by ID    |
| `user/search`      | POST   | Search Data Query |
| `user/update/{id}` | POST   | Update Data by ID |
| `user/delete/{id}` | POST   | Delete Data by ID |

## Example screen shots of API invocations

![RESTAPI.jpg](https://raw.githubusercontent.com/pojok-projects/tutorialsystem-database-interface-layer/blob/master/images/Selection_01283.png)

![RESTAPI.jpg](https://raw.githubusercontent.com/pojok-projects/tutorialsystem-database-interface-layer/blob/master/images/Selection_01284.png)

![RESTAPI.jpg](https://raw.githubusercontent.com/pojok-projects/tutorialsystem-database-interface-layer/blob/master/images/Selection_01285.png)

![RESTAPI.jpg](https://raw.githubusercontent.com/pojok-projects/tutorialsystem-database-interface-layer/blob/master/images/Selection_01286.png)

![RESTAPI.jpg](https://raw.githubusercontent.com/pojok-projects/tutorialsystem-database-interface-layer/blob/master/images/Selection_01287.png)

![RESTAPI.jpg](https://raw.githubusercontent.com/pojok-projects/tutorialsystem-database-interface-layer/blob/master/images/Selection_01290.png)

![RESTAPI.jpg](https://raw.githubusercontent.com/pojok-projects/tutorialsystem-database-interface-layer/blob/master/images/Selection_01291.png)
