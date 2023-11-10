### Bloque 1

##### Consultas

1. Listar los nombres de los usuarios

   ```sql
   SELECT nombre FROM tblUsuarios;
   ```
   Reultado query:

     | nombre    |
     |-----------|
     | BRENDA    |
     | OSCAR     |
     | JOSE      |
     | LUIS      |
     | LUIS      |
     | DANIEL    |
     | JAQUELINE |
     | ROMAN     |
     | BLAS      |
     | JESSICA   |
     | DIANA     |
     | RICARDO   |
     | VALENTINA |
     | BRENDA    |
     | LUCIA     |
     | JUAN      |
     | ELPIDIO   |
     | JESSICA   |
     | LETICIA   |
     | LUIS      |
     | HUGO      |

2. Calcular el saldo máximo de los usuarios de sexo “Mujer”

     ```sql
      SELECT MAX(saldo) as maxSaldoMujer FROM tblUsuarios WHERE sexo="M";
     ```
     Resultado query:

     | maxSaldoMujer |
     |---------------|
     |           500 |


3. Listar nombre y teléfono de los usuarios con teléfono NOKIA, BLACKBERRY o SONY

     ```sql
      SELECT nombre, telefono FROM tblUsuarios WHERE marca="NOKIA" OR marca="BLACKBERRY" OR marca="SONY";
     ```
     Resultado query:
     | nombre    | telefono     |
     |-----------|--------------|
     | JOSE      | 655-143-3922 |
     | LUIS      | 655-100-8260 |
     | DANIEL    | 655-145-2586 |
     | JAQUELINE | 655-330-5514 |
     | DIANA     | 655-143-3952 |
     | VALENTINA | 655-137-4253 |
     | LUCIA     | 655-145-4992 |
     | JESSICA   | 655-330-5143 |
     | LETICIA   | 655-143-4019 |
     | LUIS      | 655-100-5085 |


4. Contar los usuarios sin saldo o inactivos

     ```sql
     SELECT COUNT(*) as cantUsuarios from tblUsuarios WHERE saldo=0 OR activo=0;
     ```
     Resultado query:
     | cantUsuarios |
     |--------------|
     |            7 |

5. Listar el login de los usuarios con nivel 1, 2 o 3

     ```sql
      SELECT usuario FROM tblUsuarios WHERE nivel=1 OR nivel=2 OR nivel=3;
     ```
     Resutado query:
     | usuario |
     |---------|
     | BRE2271 |
     | OSC4677 |
     | JOS7086 |
     | LUI7072 |
     | ROM6520 |
     | JES4752 |
     | DIA6570 |
     | RIC8283 |
     | BRE8106 |
     | LUC4982 |
     | ELP2984 |
     | JES9640 |
     | LET4015 |
     | LUI1076 |
     | HUG5441 |


6. Listar los números de teléfono con saldo menor o igual a 300

     ```sql
      SELECT telefono, saldo FROM tblUsuarios WHERE saldo<=300;
     ```
     Resultado query:
     | telefono     | saldo |
     |--------------|-------|
     | 655-330-5736 |   100 |
     | 655-143-4181 |     0 |
     | 655-143-3922 |   150 |
     | 655-137-1279 |    50 |
     | 655-100-8260 |    50 |
     | 655-145-2586 |   100 |
     | 655-330-5514 |     0 |
     | 655-330-3263 |    50 |
     | 655-330-3871 |   100 |
     | 655-143-3952 |   100 |
     | 655-145-6049 |   150 |
     | 655-137-4253 |    50 |
     | 655-100-1351 |   150 |
     | 655-145-4992 |     0 |
     | 655-100-6517 |     0 |
     | 655-330-5143 |   200 |
     | 655-143-4019 |   100 |
     | 655-100-5085 |   150 |

7. Calcular la suma de los saldos de los usuarios de la compañia telefónica NEXTEL

     ```sql
      SELECT SUM(saldo) as saldoTotal FROM tblUsuarios WHERE compañia="NEXTEL";
     ```
     Resultado query:
     | saldoTotal |
     |------------|
     |        150 |

8. Contar el número de usuarios por compañía telefónica

     ```sql
      SELECT compañia, COUNT(*) as cantidadUsuarios FROM tblUsuarios GROUP BY compañia;
     ```
     Resultado query:
     | compañia  | cantidadUsuarios |
     |-----------|------------------|
     | IUSACELL  |                6 |
     | TELCEL    |                3 |
     | MOVISTAR  |                2 |
     | UNEFON    |                5 |
     | AXEL      |                2 |
     | AT&T      |                2 |
     | NEXTEL    |                1 |


9. Contar el número de usuarios por nivel

     ```sql
      SELECT nivel, COUNT(*) as cantidadUsuarios FROM tblUsuarios GROUP BY nivel;
     ```
     Resultado query:
     | nivel | cantidadUsuarios |
     |-------|------------------|
     |     2 |                5 |
     |     3 |                6 |
     |     0 |                6 |
     |     1 |                4 |

10. Listar el login de los usuarios con nivel 2

      ```sql
       SELECT usuario FROM tblUsuarios WHERE nivel=2;
      ```
      Resultado query:
     | usuario |
     |---------|
     | BRE2271 |
     | ROM6520 |
     | RIC8283 |
     | LET4015 |
     | HUG5441 |

11. Mostrar el email de los usuarios que usan gmail

      ```sql
       SELECT email FROM tblUsuarios WHERE email LIKE '%gmail%';
      ```
      Resultado query:
     | email               |
     |---------------------|
     | oscar@gmail.com     |
     | francisco@gmail.com |
     | roman@gmail.com     |
     | brenda2@gmail.com   |
     | lucia@gmail.com     |

12. Listar nombre y teléfono de los usuarios con teléfono LG, SAMSUNG o MOTOROLA

      ```sql
       SELECT nombre, telefono FROM tblUsuarios WHERE marca="LG" OR marca="SAMSUNG" OR marca="MOTOROLA";
      ```
      Resultado query:
     | nombre  | telefono     |
     |---------|--------------|
     | BRENDA  | 655-330-5736 |
     | OSCAR   | 655-143-4181 |
     | LUIS    | 655-137-1279 |
     | ROMAN   | 655-330-3263 |
     | BLAS    | 655-330-3871 |
     | JESSICA | 655-143-6861 |
     | RICARDO | 655-145-6049 |
     | BRENDA  | 655-100-1351 |
     | JUAN    | 655-100-6517 |
     | ELPIDIO | 655-145-9938 |
     | HUGO    | 655-137-3935 |

------

### Bloque 2

##### Consultas

1. Listar nombre y teléfono de los usuarios con teléfono que no sea de la marca LG o SAMSUNG

     ```sql
      SELECT nombre, telefono FROM tblUsuarios WHERE marca!="LG" AND marca!="SAMSUNG";
     ```
     Resutado query:
     | nombre    | telefono     |
     |-----------|--------------|
     | JOSE      | 655-143-3922 |
     | LUIS      | 655-100-8260 |
     | DANIEL    | 655-145-2586 |
     | JAQUELINE | 655-330-5514 |
     | DIANA     | 655-143-3952 |
     | RICARDO   | 655-145-6049 |
     | VALENTINA | 655-137-4253 |
     | BRENDA    | 655-100-1351 |
     | LUCIA     | 655-145-4992 |
     | ELPIDIO   | 655-145-9938 |
     | JESSICA   | 655-330-5143 |
     | LETICIA   | 655-143-4019 |
     | LUIS      | 655-100-5085 |
     | HUGO      | 655-137-3935 |

2. Listar el login y teléfono de los usuarios con compañia telefónica IUSACELL

     ```sql
      SELECT usuario, telefono FROM tblUsuarios WHERE compañia="IUSACELL";
     ```
     Resultado query:
     | usuario | telefono     |
     |---------|--------------|
     | BRE2271 | 655-330-5736 |
     | LUI7072 | 655-100-8260 |
     | ROM6520 | 655-330-3263 |
     | RIC8283 | 655-145-6049 |
     | LUC4982 | 655-145-4992 |
     | JES9640 | 655-330-5143 |

3. Listar el login y teléfono de los usuarios con compañia telefónica que no sea TELCEL

     ```sql
      SELECT usuario, telefono FROM tblUsuarios WHERE compañia!="TELCEL";
     ```
     Resultado query:
     | usuario | telefono     | compañia  |
     |---------|--------------|-----------|
     | BRE2271 | 655-330-5736 | IUSACELL  |
     | JOS7086 | 655-143-3922 | MOVISTAR  |
     | LUI7072 | 655-100-8260 | IUSACELL  |
     | DAN2832 | 655-145-2586 | UNEFON    |
     | JAQ5351 | 655-330-5514 | AXEL      |
     | ROM6520 | 655-330-3263 | IUSACELL  |
     | BLA9739 | 655-330-3871 | UNEFON    |
     | DIA6570 | 655-143-3952 | UNEFON    |
     | RIC8283 | 655-145-6049 | IUSACELL  |
     | VAL6882 | 655-137-4253 | AT&T      |
     | BRE8106 | 655-100-1351 | NEXTEL    |
     | LUC4982 | 655-145-4992 | IUSACELL  |
     | JUA2337 | 655-100-6517 | AXEL      |
     | ELP2984 | 655-145-9938 | MOVISTAR  |
     | JES9640 | 655-330-5143 | IUSACELL  |
     | LET4015 | 655-143-4019 | UNEFON    |
     | LUI1076 | 655-100-5085 | UNEFON    |
     | HUG5441 | 655-137-3935 | AT&T      |

4. Calcular el saldo promedio de los usuarios que tienen teléfono marca NOKIA

     ```sql
      SELECT AVG(saldo) as Proemdio FROM tblUsuarios WHERE marca="NOKIA";
     ```
     Resultado query:
     | Promedio |
     |----------|
     |      100 |

5. Listar el login y teléfono de los usuarios con compañia telefónica IUSACELL o AXEL

     ```sql
      SELECT usuario, telefono FROM tblUsuarios WHERE compañia="IUSACELL" OR compañia="AXEL";
     ```
     Resultado query:
     | usuario | telefono     |
     |---------|--------------|
     | BRE2271 | 655-330-5736 |
     | LUI7072 | 655-100-8260 |
     | JAQ5351 | 655-330-5514 |
     | ROM6520 | 655-330-3263 |
     | RIC8283 | 655-145-6049 |
     | LUC4982 | 655-145-4992 |
     | JUA2337 | 655-100-6517 |
     | JES9640 | 655-330-5143 |

6. Mostrar el email de los usuarios que no usan yahoo

     ```sql
      SELECT email FROM tblUsuarios WHERE email NOT LIKE '%yahoo%';
     ```
     Resultado query:
     | email                 |
     |-----------------------|
     | brenda@live.com       |
     | oscar@gmail.com       |
     | francisco@gmail.com   |
     | enrique@outlook.com   |
     | luis@hotmail.com      |
     | daniel@outlook.com    |
     | jaqueline@outlook.com |
     | roman@gmail.com       |
     | blas@hotmail.com      |
     | jessica@hotmail.com   |
     | diana@live.com        |
     | ricardo@hotmail.com   |
     | valentina@live.com    |
     | brenda2@gmail.com     |
     | lucia@gmail.com       |
     | juan@outlook.com      |
     | elpidio@outlook.com   |
     | jessica2@live.com     |
     | luis2@live.com        |
     | hugo@live.com         |

7. Listar el login y teléfono de los usuarios con compañia telefónica que no sea TELCEL o IUSACELL

     ```sql
      SELECT usuario, telefono FROM tblUsuarios WHERE compañia!="TELCEL" AND compañia!="IUSACELL";
     ```
     Resultado query:
     | usuario | telefono     |
     |---------|--------------|
     | JOS7086 | 655-143-3922 |
     | DAN2832 | 655-145-2586 |
     | JAQ5351 | 655-330-5514 |
     | BLA9739 | 655-330-3871 |
     | DIA6570 | 655-143-3952 |
     | VAL6882 | 655-137-4253 |
     | BRE8106 | 655-100-1351 |
     | JUA2337 | 655-100-6517 |
     | ELP2984 | 655-145-9938 |
     | LET4015 | 655-143-4019 |
     | LUI1076 | 655-100-5085 |
     | HUG5441 | 655-137-3935 |


8. Listar el login y teléfono de los usuarios con compañia telefónica UNEFON

     ```sql
      SELECT usuario , telefono FROM tblUsuarios WHERE compañia="UNEFON";
     ```
     Resultado query:
     | usuario | telefono     |
     |---------|--------------|
     | DAN2832 | 655-145-2586 |
     | BLA9739 | 655-330-3871 |
     | DIA6570 | 655-143-3952 |
     | LET4015 | 655-143-4019 |
     | LUI1076 | 655-100-5085 |


9. Listar las diferentes marcas de celular en orden alfabético descendentemente

     ```sql
      SELECT marca FROM tblUsuarios GROUP BY marca ORDER BY marca DESC;
     ```
     Resultado query:
     | marca      |
     |------------|
     | SONY       |
     | SAMSUNG    |
     | NOKIA      |
     | MOTOROLA   |
     | LG         |
     | BLACKBERRY |


10. Listar las diferentes compañias en orden alfabético aleatorio

      ```sql
       SELECT compañia FROM tblUsuarios GROUP BY compañia  ORDER BY RAND();
      ```
     Resultado query:
     | compañia  |
     |-----------|
     | AT&T      |
     | NEXTEL    |
     | IUSACELL  |
     | UNEFON    |
     | AXEL      |
     | MOVISTAR  |
     | TELCEL    |


11. Listar el login de los usuarios con nivel 0 o 2

      ```sql
       SELECT usuario FROM tblUsuarios WHERE nivel=2 OR nivel=0;
      ```
      Resultado query:
     | usuario |
     |---------|
     | BRE2271 |
     | LUI6115 |
     | DAN2832 |
     | JAQ5351 |
     | ROM6520 |
     | BLA9739 |
     | RIC8283 |
     | VAL6882 |
     | JUA2337 |
     | LET4015 |
     | HUG5441 |


12. Calcular el saldo promedio de los usuarios que tienen teléfono marca LG

      ```sql
       SELECT AVG(saldo) as PromedioUsuariosLG FROM tblUsuarios WHERE marca="LG";
      ```
      Resultado query:
     | PromedioUsuariosLG |
     |--------------------|
     |                 50 |

------

### Bloque 3

##### Consultas

1. Listar el login de los usuarios con nivel 1 o 3

     ```sql
      SELECT usuario FROM tblUsuarios WHERE nivel=3 OR nivel=1;
     ```
     Resultado query:
     | usuario |
     |---------|
     | OSC4677 |
     | JOS7086 |
     | LUI7072 |
     | JES4752 |
     | DIA6570 |
     | BRE8106 |
     | LUC4982 |
     | ELP2984 |
     | JES9640 |
     | LUI1076 |

2. Listar nombre y teléfono de los usuarios con teléfono que no sea de la marca BLACKBERRY

     ```sql
      SELECT nombre, telefono FROM tblUsuarios WHERE marca!="BLACKBERRY";
     ```
     Resultado query:
     | nombre  | telefono     |
     |---------|--------------|
     | BRENDA  | 655-330-5736 |
     | OSCAR   | 655-143-4181 |
     | JOSE    | 655-143-3922 |
     | LUIS    | 655-137-1279 |
     | LUIS    | 655-100-8260 |
     | DANIEL  | 655-145-2586 |
     | ROMAN   | 655-330-3263 |
     | BLAS    | 655-330-3871 |
     | JESSICA | 655-143-6861 |
     | DIANA   | 655-143-3952 |
     | RICARDO | 655-145-6049 |
     | BRENDA  | 655-100-1351 |
     | JUAN    | 655-100-6517 |
     | ELPIDIO | 655-145-9938 |
     | JESSICA | 655-330-5143 |
     | LUIS    | 655-100-5085 |
     | HUGO    | 655-137-3935 |

3. Listar el login de los usuarios con nivel 3

     ```sql
      SELECT usuario FROM tblUsuarios WHERE nivel=3;
     ```
     Resultado query:
     | usuario |
     |---------|
     | OSC4677 |
     | JOS7086 |
     | BRE8106 |
     | LUC4982 |
     | JES9640 |
     | LUI1076 |

4. Listar el login de los usuarios con nivel 0

     ```sql
      SELECT usuario FROM tblUsuarios WHERE nivel=0;
     ```
     Resultado query:
     | usuario |
     |---------|
     | LUI6115 |
     | DAN2832 |
     | JAQ5351 |
     | BLA9739 |
     | VAL6882 |
     | JUA2337 |

5. Listar el login de los usuarios con nivel 1

     ```sql
      SELECT usuario FROM tblUsuarios WHERE nivel=1;
     ```
     Resultado query:
     | usuario |
     |---------|
     | LUI7072 |
     | JES4752 |
     | DIA6570 |
     | ELP2984 |

6. Contar el número de usuarios por sexo

     ```sql
      SELECT sexo, COUNT(*) as cantidad FROM tblUsuarios GROUP BY sexo;
     ```
     Resultado query:
     | sexo | cantidad |
     |------|----------|
     | M    |        9 |
     | H    |       12 |
7. Listar el login y teléfono de los usuarios con compañia telefónica AT&T

     ```sql
      SELECT usuario, telefono FROM tblUsuarios WHERE compañia="AT&T";
     ```
     Resultado query:
     | usuario | telefono     |
     |---------|--------------|
     | VAL6882 | 655-137-4253 |
     | HUG5441 | 655-137-3935 |


8. Listar las diferentes compañias en orden alfabético descendentemente

     ```sql
      SELECT compañia FROM tblUsuarios GROUP BY compañia ORDER BY compañia DESC;
     ```
     Resultado query:
     | compañia  |
     |-----------|
     | UNEFON    |
     | TELCEL    |
     | NEXTEL    |
     | MOVISTAR  |
     | IUSACELL  |
     | AXEL      |
     | AT&T      |

9. Listar el logn de los usuarios inactivos

     ```sql
      SELECT usuario FROM tblUsuarios WHERE activo=0;
     ```
     Resultado query:
     | usuario |
     |---------|
     | LUI7072 |
     | DIA6570 |
     | VAL6882 |
     | JUA2337 |


10. Listar los números de teléfono sin saldo

      ```sql
       SELECT telefono FROM tblUsuarios  WHERE saldo=0;
      ```
      Resultado query:
     | telefono     |
     |--------------|
     | 655-143-4181 |
     | 655-330-5514 |
     | 655-145-4992 |
     | 655-100-6517 |

11. Calcular el saldo mínimo de los usuarios de sexo “Hombre”

      ```sql
       SELECT MIN(saldo) FROM tblUsuarios WHERE sexo="H";
      ```
      Resultado query:
     |  minSaldo  |
     |------------|
     |          0 |


12. Listar los números de teléfono con saldo mayor a 300

      ```sql
       SELECT telefono FROM tblUsuarios WHERE saldo>300;
      ```
      Resultado query:
     | telefono     |
     |--------------|
     | 655-143-6861 |
     | 655-145-9938 |
     | 655-137-3935 |

------

### Bloque 4

##### Consultas

1. Contar el número de usuarios por marca de teléfono

     ```sql
      SELECT marca, COUNT(*) as cantidadUsuario FROM tblUsuarios GROUP BY marca;
     ```
     Resultado query:
     | marca      | cantidadUsuarios |
     |------------|------------------|
     | SAMSUNG    |                4 |
     | LG         |                3 |
     | NOKIA      |                2 |
     | SONY       |                4 |
     | BLACKBERRY |                4 |
     | MOTOROLA   |                4 |

2. Listar nombre y teléfono de los usuarios con teléfono que no sea de la marca LG

     ```sql
      SELECT nombre, telefono FROM tblUsuarios WHERE marca != 'LG';
     ```
     Resultado query:
     | nombre    | telefono     |
     |-----------|--------------|
     | BRENDA    | 655-330-5736 |
     | JOSE      | 655-143-3922 |
     | LUIS      | 655-137-1279 |
     | LUIS      | 655-100-8260 |
     | DANIEL    | 655-145-2586 |
     | JAQUELINE | 655-330-5514 |
     | JESSICA   | 655-143-6861 |
     | DIANA     | 655-143-3952 |
     | RICARDO   | 655-145-6049 |
     | VALENTINA | 655-137-4253 |
     | BRENDA    | 655-100-1351 |
     | LUCIA     | 655-145-4992 |
     | JUAN      | 655-100-6517 |
     | ELPIDIO   | 655-145-9938 |
     | JESSICA   | 655-330-5143 |
     | LETICIA   | 655-143-4019 |
     | LUIS      | 655-100-5085 |
     | HUGO      | 655-137-3935 |

3. Listar las diferentes compañias en orden alfabético ascendentemente

     ```sql
      SELECT compañia FROM tblUsuarios GROUP BY compañia  ORDER BY compañia;
     ```
     Resultado query:
     | compañia  |
     |-----------|
     | AT&T      |
     | AXEL      |
     | IUSACELL  |
     | MOVISTAR  |
     | NEXTEL    |
     | TELCEL    |
     | UNEFON    |


4. Calcular la suma de los saldos de los usuarios de la compañia telefónica UNEFON

     ```sql
      SELECT SUM(saldo) as TotalSaldosUNEFON FROM tblUsuarios WHERE compañia="UNEFON";
     ```
     Resultado query:
     | TotalSaldosUNEFON |
     |-------------------|
     |               550 |

5. Mostrar el email de los usuarios que usan hotmail

     ```sql
      SELECT email FROM tblUsuarios WHERE email LIKE '%hotmail%';
     ```
     Resultado query:
     | email               |
     |---------------------|
     | luis@hotmail.com    |
     | blas@hotmail.com    |
     | jessica@hotmail.com |
     | ricardo@hotmail.com |

6. Listar los nombres de los usuarios sin saldo o inactivos

     ```sql
      SELECT nombre FROM tblUsuarios WHERE saldo=0 OR activo=0;
     ```
     Resultado query:
     | nombre    |
     |-----------|
     | OSCAR     |
     | LUIS      |
     | JAQUELINE |
     | DIANA     |
     | VALENTINA |
     | LUCIA     |
     | JUAN      |

7. Listar el login y teléfono de los usuarios con compañia telefónicaIUSACELL o TELCEL

     ```sql
      SELECT usuario, telefono FROM tblUsuarios WHERE compañia="IUSACELL" OR compañia="TELCEL";
     ```
     Resultado query:
     | usuario | telefono     |
     |---------|--------------|
     | BRE2271 | 655-330-5736 |
     | OSC4677 | 655-143-4181 |
     | LUI6115 | 655-137-1279 |
     | LUI7072 | 655-100-8260 |
     | ROM6520 | 655-330-3263 |
     | JES4752 | 655-143-6861 |
     | RIC8283 | 655-145-6049 |
     | LUC4982 | 655-145-4992 |
     | JES9640 | 655-330-5143 |

8. Listar las diferentes marcas de celular en orden alfabético ascendentemente

     ```sql
      SELECT marca FROM tblUsuarios GROUP BY marca ORDER BY marca;
     ```
     Resultado query:
     | marca      |
     |------------|
     | BLACKBERRY |
     | LG         |
     | MOTOROLA   |
     | NOKIA      |
     | SAMSUNG    |
     | SONY       |

9. Listar las diferentes marcas de celular en orden alfabético aleatorio

     ```sql
      SELECT marca FROM tblUsuarios GROUP BY marca ORDER BY RAND();
     ```
     Resultado query:
     | marca      |
     |------------|
     | LG         |
     | SAMSUNG    |
     | BLACKBERRY |
     | SONY       |
     | MOTOROLA   |
     | NOKIA      |

10. Listar el login y teléfono de los usuarios con compañia telefónica IUSACELL o UNEFON

      ```sql
       SELECT usuario, telefono FROM tblUsuarios WHERE compañia="IUSACELL" OR compañia="TELCEL";
      ```
      Resultado query:
     | usuario | telefono     |
     |---------|--------------|
     | BRE2271 | 655-330-5736 |
     | OSC4677 | 655-143-4181 |
     | LUI6115 | 655-137-1279 |
     | LUI7072 | 655-100-8260 |
     | ROM6520 | 655-330-3263 |
     | JES4752 | 655-143-6861 |
     | RIC8283 | 655-145-6049 |
     | LUC4982 | 655-145-4992 |
     | JES9640 | 655-330-5143 |


11. Listar nombre y teléfono de los usuarios con teléfono que no sea de la marca MOTOROLA o NOKIA

      ```sql
       SELECT nombre, telefono FROM tblUsuarios WHERE marca!="MOTOROLA" AND marca!="NOKIA";
      ```
      Resultado query:
     | nombre    | telefono     |
     |-----------|--------------|
     | BRENDA    | 655-330-5736 |
     | OSCAR     | 655-143-4181 |
     | LUIS      | 655-137-1279 |
     | DANIEL    | 655-145-2586 |
     | JAQUELINE | 655-330-5514 |
     | ROMAN     | 655-330-3263 |
     | BLAS      | 655-330-3871 |
     | JESSICA   | 655-143-6861 |
     | DIANA     | 655-143-3952 |
     | VALENTINA | 655-137-4253 |
     | LUCIA     | 655-145-4992 |
     | JUAN      | 655-100-6517 |
     | JESSICA   | 655-330-5143 |
     | LETICIA   | 655-143-4019 |
     | LUIS      | 655-100-5085 |

12. Calcular la suma de los saldos de los usuarios de la compañia telefónica TELCEL

      ```sql
       SELECT SUM(saldo) as TotalSaldosTELCEL FROM tblUsuarios WHERE compañia="TELCEL";
      ```
      Resultado query:
     | TotalSaldosTELCEL |
     |-------------------|
     |               550 |
