# Predicados II
1. Selecciona la última zona:
```xml
//zone[last()]
```

2. Selecciona todos los elementos service, de la última zona (usa una función para sacar el
último)
```xml
//zone[last()]/service
```

3. Selecciona el atributo target de la penúltima zona:
```xml
//zone[last()-1]/@target
```

4. Selecciona las zonas que tengan atributo target presente
```xml
//zone[@target]
```

5. Selecciona las zonas cuyo atributo target valga ACCEPT
```xml
//zone[@target = "ACCEPT"]
```

6. Selecciona las zonas 2 y 4 (la Internal y la Block).
```xml
//zone[position()=2 or position() = 4]
```

7. Selecciona de la zona con posición 3 en adelante
``` xml
//zone [position()>=3]
```

8. Selecciona el elemento zone, cuyo elemento short valga DMZ.
``` xml
//zone[short="DMZ"]
```

9. Selecciona las zonas que tengan un elemento service (sin importar su valor):
``` xml
//zone[service]
```

10. Selecciona las zonas que tengan un elemento service, cuyo atributo name valga “ssh”
``` xml
//zone[service/@name="ssh"]
```

11. Selecciona las zonas que tengan un elemento service, cuyo atributo name valga “mdns”
o “ssh”:
``` xml
//zone[service/@name="ssh" or @name="mdns"]
```

12. Selecciona de la zona 6 el servicio con el nombre samba-client
``` xml
//zone[position()=6 and service/@name="samba-client"]
```