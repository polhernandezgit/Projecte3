# T04: Serveis de directori. LDAP
Primer de tot haurem de canviar el nom del server per *srever.innovatech13.test*.

![Captura 1](img./c1.png)

I també el nom de directori.

![Captura 1](img./c2.png)

Farem la comanda hostname per verificar que s'ha canviat el nom de la màquina.

![Captura 1](img./c3.png)

Després configurarem la xarxa de la màquina d’aquesta manera.

![Captura 1](img./c4.png)

Farem ip a per veure si la ip s’ha configurat correctament.

![Captura 1](img./c5.png)

Un cop fet els passos de la configuració inicial, connectarem al interfície de host only.

![Captura 1](img./c6.png)

Ara anirem amb l’instal·lació del servei OpenLDAP.

![Captura 1](img./c7.png)

Aquí només hem de ficar la contrasenya que vulguem que tingui el LDAP, per exemple usuari.

![Captura 1](img./c8.png)

Farem la comanda sudo apt upgrade && update per aplicar els canvis.

![Captura 1](img./c9.png)

I amb systemctl status slapd i sudo slapcat podem verificar si el servei està activat.

![Captura 1](img./c10.png)

![Captura 1](img./c11.png)

A continuació crearem dues Unitats Organitzatives ( OU ), una d'usuaris i l’altre de users mitjançant un fitxer .ldif.

![Captura 1](img./c12.png)

![Captura 1](img./c13.png)

Quan haguem escrit el necessari, implementarem les dos OU per la comanda ldapadd.

![Captura 1](img./c14.png)

![Captura 1](img./c15.png)

I amb ldapsearch podem veure que estiguin ben implementades.

![Captura 1](img./c16.png)

## 3.2. Gestió i Administració (LAM)
Ara començarem amb la gestió i administració del servei LDAP.
Primer haurem d’instal·lar-lo.

![Captura 1](img./c17.png)

Quan s’hagi instal·lat, haurem de copiar la ip amb ip a

![Captura 1](img./c18.png)

Després hem de anar a un navegador i buscar la ip més /lam/templates/login.php i ens sortirà aquest menú. El que hem de fer aquí és anar a on diu LAM configuration.

![Captura 1](img./c19.png)

Després a edit server profiles.

![Captura 1](img./c20.png)

I haurem de ficar la contrasenya, que és lam.

![Captura 1](img./c21.png)

Un cop a dins, en la secció server settings ficarem el que surt en la captura.

![Captura 1](img./c22.png)

En la secció tool settings ficarem això.

![Captura 1](img./c23.png)

I en la segona pestanya de account types, que esta a la part superior i en la secció active account types fiquem el que surt en la captura.

![Captura 1](img./c24.png)

I aplicarem el anvis en save a la part inferior.
Després haurem de anar a la pestanya d’inici i ficar la contrasenya que tinguem del LDAP.

![Captura 1](img./c25.png)

Un cop hem iniciat sessió, anem a la secció de grupos per crear els grups.

![Captura 1](img./c26.png)

Crearem els dos grups de tech i manager.

![Captura 1](img./c27.png)

![Captura 1](img./c28.png)

Ara crearem usuaris. Donem a nuevo usuario.

![Captura 1](img./c29.png)

El primer es dirà tech01 i anem a la secció de Unix.

![Captura 1](img./c30.png)

I ficarem el surt en la captura.

![Captura 1](img./c31.png)

I el mateix però amb manager01.

![Captura 1](img./c32.png)

![Captura 1](img./c33.png)

## 4. Integració de Client (Client Ubuntu Desktop)
En la màquina client ficarem la segona interficie en host only.

![Captura 1](img./c34.png)

Un cop a dins, anem a la terminal i canviem el nom de domini.

![Captura 1](img./c35.png)

![Captura 1](img./c36.png)

Utilitzem la comanda dig per veure si els noms funcionen bé.

![Captura 1](img./c37.png)

Ara instal·larem el ldap.

![Captura 1](img./c38.png)

I en les configuracions de paquets fiquem el que surt en les captures.

![Captura 1](img./c39.png)

![Captura 1](img./c40.png)

La versió que elegim dona igual.

![Captura 1](img./c41.png)

![Captura 1](img./c42.png)

![Captura 1](img./c43.png)

![Captura 1](img./c44.png)

Aqui fiquem la contrasenya del lam.

![Captura 1](img./c45.png)

Amb aquesta comanda veurem si el client es connecta amb el servidor.

![Captura 1](img./c46.png)

Ara entrarem a l’arxiu següent.

![Captura 1](img./c47.png)

I ho configurarem com en la captura.

![Captura 1](img./c48.png)

Ara entrem en aquest fitxer per per eliminar la línea marcada.

![Captura 1](img./c49.png)

![Captura 1](img./c50.png)

Després entrem en aquest fitxer i afegim la línea marcada.

![Captura 1](img./c51.png)

![Captura 1](img./c52.png)

Resetejem el nsdc per guardar bé els canvis.

![Captura 1](img./c53.png)

Ara mirem si els usuaris es veuen en el LDAP.

![Captura 1](img./c54.png)

Després entrarem en aquest altre fitxer i afegim la línea marcada.

![Captura 1](img./c55.png)

![Captura 1](img./c56.png)

Ara reiniciarem la màquina per iniciar sessió per on diu ¿No está en la lista?.

![Captura 1](img./c57.png)

Aqui posem de nom d’usuari manager01 i posem la contrasenya del LAM.

![Captura 1](img./c58.png)

Si hem pogut iniciar sessió, tornem a entrar a la terminal i comprovem que l’usuari estigu bé.

![Captura 1](img./c59.png)
