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

![Captura 1](img./c24.png)

I amb ldapsearch podem veure que estiguin ben implementades.

![Captura 1](img./c17.png)

## 3.2. Gestió i Administració (LAM)
Ara començarem amb la gestió i administració del servei LDAP.
Primer haurem d’instal·lar-lo.

![Captura 1](img./c18.png)

Quan s’hagi instal·lat, haurem de copiar la ip amb ip a

![Captura 1](img./c1.png)

Després hem de anar a un navegador i buscar la ip més /lam/templates/login.php i ens sortirà aquest menú. El que hem de fer aquí és anar a on diu LAM configuration.

![Captura 1](img./c1.png)

Després a edit server profiles.

![Captura 1](img./c1.png)

I haurem de ficar la contrasenya, que és lam.

![Captura 1](img./c1.png)

Un cop a dins, en la secció server settings ficarem el que surt en la captura.

![Captura 1](img./c1.png)

En la secció tool settings ficarem això.

![Captura 1](img./c1.png)

I en la segona pestanya de account types, que esta a la part superior i en la secció active account types fiquem el que surt en la captura.

![Captura 1](img./c1.png)

I aplicarem el anvis en save a la part inferior.

![Captura 1](img./c1.png)

Després haurem de anar a la pestanya d’inici i ficar la contrasenya que tinguem del LDAP.




