# Tasca S5.01 Spring boot API rest + Aplicació web

## Objectius
-Protocol HTTP / REST.
-JPA.
-CRUD amb Spring.
-MySQL.
-Thymeleaf.

## Descripció
Tenim una entitat anomenada FlorEntity, que disposa de les següents propietats:

-          Integer pk_FlorID

-          String nomFlor

-          String paisFlor

 

També tenim una DTO anomenada FlorDTO, que tindrà les mateixes propietats que l’entitat Sucursal, afegint-ne una:

-          String tipusFlor.

Aquesta propietat, en funció del país d'origen de la flor, haurà d’indicar si és “UE” o “Fora UE”. Per a fer això, pots tenir una llista privada a la mateixa DTO (per exemple: List<String> països), amb els països que formen part de la UE.

Aprofitant l’especificació JPA, hauràs de persistir l’entitat FlorEntity a una base de dades MySQL, seguint el patró MVC.

El consell és que FlorDTO la facis servir al Controller, i FlorEntity al Repository. La capa de serveis serà l’encarregada de fer la traducció entre les dues.

Per a això, depenent del package principal, crearàs una estructura de packages, on ubicaràs les classes que necessitis:

-          cat.itacademy.barcelonactiva.cognoms.nom.s05.t01.n02.controllers

-          cat.itacademy.barcelonactiva.cognoms.nom.s05.t01.n02.model.domain

-          cat.itacademy.barcelonactiva.cognoms.nom.s05.t01.n02.model.dto

-          cat.itacademy.barcelonactiva.cognoms.nom.s05.t01.n02.model.services

-          cat.itacademy.barcelonactiva.cognoms.nom.s05.t01.n02.model.repository

## Notes

Nivell 2  

**Exercici API Rest CRUD amb MySQL

La classe ubicada al paquet controllers (FlorController, per exemple), haurà de ser capaç de donar resposta a les següents peticions per actualitzar i consultar informació:

- Crea
```
http://localhost:9001/flor/add
```
- Update
```
http://localhost:9001/flor/update
```
- Delete
```
http://localhost:9001/flor/delete/{id}
```
- GetOne
```
http://localhost:9001/flor/getOne/{id}
```
- GetAll
```
http://localhost:9001/flor/getAll
```
