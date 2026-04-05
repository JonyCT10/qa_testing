# QA Testing Project - Bugs encontrados

## Bug 1: API no guarda datos después de POST

Descripción:
La API devuelve un ID indicando creación exitosa, pero el usuario no aparece al consultar la lista.

Pasos:
1. POST /users
2. GET /users

Resultado esperado:
El usuario debería guardarse

Resultado actual:
No se guarda

Severidad: Media

---

## Bug 2: Campo nombre permite números

Descripción:
El campo "Name" permite ingresar solo números sin validación.

Pasos:
1. Ir a compra
2. Ingresar "12345" en nombre

Resultado esperado:
Validar solo letras

Resultado actual:
Acepta números

Severidad: Media
