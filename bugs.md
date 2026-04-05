# QA Testing Project - Bugs encontrados

--

#Bug 1: API no guarda datos después de POST

**Descripción:**  
Al realizar una solicitud POST para crear un usuario, la API devuelve un ID indicando que el usuario fue creado. Sin embargo, al consultar la lista de usuarios, el nuevo usuario no aparece.

**Pasos para reproducir:**
1. Abrir Postman
2. Enviar solicitud POST a: https://jsonplaceholder.typicode.com/users
3. Enviar datos de usuario (ejemplo: { "name": "Jony" })
4. Verificar respuesta con ID generado
5. Enviar solicitud GET a: https://jsonplaceholder.typicode.com/users

**Resultado esperado:**  
El usuario debería guardarse y aparecer en la lista

**Resultado actual:**  
El usuario no se guarda y no aparece en la lista

**Severidad:** Media

---

#Bug 2: Campo "Name" permite números

**Descripción:**  
En el formulario de compra, el campo "Name" permite ingresar únicamente valores numéricos sin aplicar validación de formato.

**Pasos para reproducir:**
1. Ingresar a la página principal
2. Seleccionar un producto
3. Hacer clic en "Place Order"
4. Ingresar "12345" en el campo "Name"
5. Completar el formulario

**Resultado esperado:**  
El sistema debería validar que el campo "Name" contenga solo letras

**Resultado actual:**  
El sistema permite ingresar números sin restricción

**Severidad:** Media
