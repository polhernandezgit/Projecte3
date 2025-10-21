

# T01: Gestor de contrasenyes
Pol Hernández

---

## Index:

### Fase 1: Anàlisi i justificació
- Introducció i Justificació
- Comparativa Tècnica
- Avantatges i Inconvenients
- Recomanació

### Fase 2: Guia d'Ús Tècnica
- Instal·lació i Configuració Inicial
- Generació de Contrasenyes Segures
- Exemples d'Ús i Emplenament Automàtic
- Gestió de Còpies de Seguretat (Backup)

---

## Informe

### Introducció i Justificació:
Explicació de per què les contrasenyes febles o reutilitzades són un risc crític per a l'empresa (atac de diccionari, credential stuffing, etc.).

El principal motiu de perquè les contrasenyes febles són tan perilloses per a una empresa és perquè solen ser contrasenyes curtes com per exemple “1234”, “password”, etc. Les tècniques com atac de diccionari consisteixen en que l’atacant utilitza una llista de paraules o password més comuns fins que coincideixen.

En canvi les contrasenyes reutilitzables el perill que tenen és que al utilitzar una contrasenya per a varies aplicacions com el correu o plataformes digitals, si una d’aquestes aplicacions sofreix una filtració de contrasenya, els atacants poden provar de utilitzar aquesta contrasenya per a varies aplicacions i entrar.

---

### La funció crucial d'un gestor de contrasenyes per mitigar aquests riscos.

Un gestor de contrasenyes sol ser crucial per reduir riscos de seguretat per diferents raons:

- Emmagatzema les contrasenyes de forma segura en una base de dades xifrada.
- Genera contrasenyes fortes i úniques, evitant-ne la reutilització.
- Protegeix contra atacs com el credential stuffing o el força bruta.
- Facilita la gestió corporativa, permetent compartir credencials de manera segura i controlar l’accés dels empleats.
- Complementa altres mesures com l’autenticació multifactor.

---

### Comparativa Tècnica

**Bitwarden (Alternativa Online / Núvol):** Analitzeu la sincronització, el model de seguretat (xifratge end-to-end), la facilitat d'accés des de múltiples dispositius i el cost/model freemium.

**KeePassX / KeePassXC (Alternativa Offline / Escriptori):** Analitzeu l'emmagatzematge local de l'arxiu (KDBX), la independència del núvol, el model open source i la portabilitat de l'arxiu.



---

### Avantatges i Inconvenients

**Bitwarden:**

**Avantatges:**
- Seguretat.
- Usabilitat.
- Continuïtat.
- Col·laboració.

**Inconvenients:**
- Dependència del núvol.
- Superfície d’atac ampliada.
- Cost.

**KeePassX:**

**Avantatges:**
- Seguretat.
- Control i privacitat.
- Open source.

**Inconvenients:**
- Usabilitat.
- Continuïtat.
- Col·laboració limitada.

---

### Recomanació final

Per al personal tècnic de l’empresa, recomanem KeePassXC com a eina de gestió de contrasenyes. Aquesta elecció es basa en la seva capacitat de garantir control total i seguretat robusta, ja que les credencials s’emmagatzemen localment amb xifrat AES-256 i opcions de fitxer clau. A més, l’arxiu .kdbx és portable i es pot sincronitzar segons les necessitats de l’empresa, mentre que els tècnics poden gestionar còpies de seguretat i recuperació de manera segura.
