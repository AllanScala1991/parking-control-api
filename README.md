# PARKING CONTROL API REST (JAVA/SPRING BOOT)

## 📁 Acesso ao projeto

**Clonar o reposotorio : https://github.com/AllanScala1991/parking-control-api**

## 🛠️ Requisitos
- Criar um container postgres com Docker atraves do docker-compose
- Criar uma tabela chamada "parking-control-db"
- Instalar as dependencias atraves do pom.xml

## ✅ Tecnologias utilizadas:
- Java 18
- Spring Boot
- Spring Data JPA
- Spring Web
- Validation
- PostgreSQL
- Docker

## Endpoints

### Create
- [POST] "/parking-spot"
- [BODY]:

```json
{
"parkingSpotNumber": "3456",
"licensePlateCar": "ERT4356",
"brandCar": "fiat",
"modelCar": "stilo",
"colorCar": "amarelo",
"responsibleName": "Carlos Santos",
"apartment": "333",
"block": "01"
}
```
### Get All
- [GET] "/parking-spot"
- [RESPONSE]:

```json
[
  {
    "id": "e50961eb-e9f2-4e59-b847-068ec5c919e9",
    "parkingSpotNumber": "3456",
    "licensePlateCar": "ERT4356",
    "brandCar": "fiat",
    "modelCar": "stilo",
    "colorCar": "amarelo",
    "registrationDate": "2022-09-08T18:03:14Z",
    "responsibleName": "Carlos Santos",
    "apartment": "333",
    "block": "01"
  }
]
```

### Get One by ID
- [GET] "/parking-spot/e50961eb-e9f2-4e59-b847-068ec5c919e9"
- [RESPONSE]:

```json
  {
    "id": "e50961eb-e9f2-4e59-b847-068ec5c919e9",
    "parkingSpotNumber": "3456",
    "licensePlateCar": "ERT4356",
    "brandCar": "fiat",
    "modelCar": "stilo",
    "colorCar": "amarelo",
    "registrationDate": "2022-09-08T18:03:14Z",
    "responsibleName": "Carlos Santos",
    "apartment": "333",
    "block": "01"
  }
```

### Delete
- [DELETE] "/parking-spot/e50961eb-e9f2-4e59-b847-068ec5c919e9"
- [RESPONSE]:

```json
Parking sport deleted successfully.
```

### Update
- [PUT] "/parking-spot/e50961eb-e9f2-4e59-b847-068ec5c919e9"
- [BODY]:

```json
  {
    "parkingSpotNumber": "3456",
    "licensePlateCar": "ERT4356",
    "brandCar": "fiat",
    "modelCar": "idea",
    "colorCar": "vermelho",
    "responsibleName": "Carlos Santos",
    "apartment": "333",
    "block": "01"
  }
```
- [RESPONSE]:

```json
  {
    "id": "e50961eb-e9f2-4e59-b847-068ec5c919e9",
    "parkingSpotNumber": "3456",
    "licensePlateCar": "ERT4356",
    "brandCar": "fiat",
    "modelCar": "idea",
    "colorCar": "vermelho",
    "registrationDate": "2022-09-07T22:46:58.556099",
    "responsibleName": "Carlos Santos",
    "apartment": "333",
    "block": "01"
  }
```