
# 🚀 Pro-ASIXc1D-G5  
**Projecte Transversal ASIXc 2024-2025**

Benvingut al manual de Documentació del Grup 5

---

## 📚 Índice
1. [🧠 Proposta de CPD](#️-ejercicio-1)  
2. [🎧 Implantació dels serveis d'Àudio i Vídeo](#️-ejercicio-2)  
3. [🗄️ Disseny i implementació d'una Base de dades](#️-ejercicio-3)  
4. [🍃 Sostenibilitat](#-ejercicio-4)

---
<!-- Ejercicio 1 -->
# 🏗️ Ejercicio 1  
## 🧠 Proposta de CPD

En aquest apartat hem dissenyat una proposta completa de Centre de Processament de Dades (CPD), tant físic com en el núvol, complint amb criteris de seguretat, eficiència, sostenibilitat i escalabilitat que es demanen en el projecte.

### 🏢 Infraestructura física

- **Ubicació**: CPD situat a l'interior de l'edifici, sense finestres ni senyalització externa, amb accés restringit i murs ignífugs.
- **Climatització**: Aire condicionat redundant, control de temperatura (18-27 °C) i humitat (40-60 %), amb filtrat HEPA i monitoratge en temps real.
- **Cablejat i distribució**: Ús de sòl i sostre tècnic per a la canalització de cables i la refrigeració. Separació de cablejat elèctric i de dades.
- **Racks**: Dos racks de 42U amb passadissos fred/calor. Cada rack inclou patch panell, switch, SAI i servidors específics (web, àudio, vídeo, BBDD).

### 💻 Infraestructura IT

- **Servidors**: 3 Dell PowerEdge R650xs (Intel Xeon, 64GB RAM, 2×1TB SSD en RAID1).
- **Switches**: 2 Cisco Catalyst 9300 amb uplinks de 10Gb i redundància.
- **Patch panels**: Un per rack per a xarxes interna i externa.

### ⚡ Infraestructura elèctrica

- **Alimentació redundant**: Doble línia elèctrica + generador d'emergència amb arrencada automàtica.
- **SAIs**: 2 UPS APC Smart-UPS X 3000VA (30 min d'autonomia per rack).

### 🔐 Seguretat

- **Física**: Accés per NFC i PIN, videovigilància 24/7, sensors ambientals, sistema FM-200 i rutes d'evacuació senyalitzades.
- **Lògica**: Accés per claus SSH, firewalls (pfSense, UFW, AWS SG), còpies de seguretat locals i en el núvol, monitoratge amb Zabbix i Netdata, ús de RAID 1 i 5.

### 🦺 Prevenció de riscos laborals

- Extintors CO₂, senyalització, EPI, zones sense obstacles i accés segur.

### 🌿 Sostenibilitat

- **Optimització energètica**: Apagada automàtica en hores vall, maquinari eficient.
- **Energia verda**: Contracte amb proveïdor d'energia renovable i ús de regions AWS sostenibles (ex. Irlanda).
- **Disseny eficient**: Rack centralitzat, cablejat optimitzat i ventilació natural passiva.

### ☁️ Implementació en el núvol (AWS)

- **Serveis utilitzats**:
 - EC2 (instàncies per a web, àudio, vídeo)
 - S3 (emmagatzematge i còpies de seguretat)
 - RDS (bases de dades)
 - CloudWatch (monitoratge)
 - Elastic Lloeu Balancer
 - Route 53 (DNS)

### 📊 Comparativa de proveïdors cloud

| Proveïdor     | Energia verda | Emisions per regió    | Eines de sostenibilitat                    |
|---------------|---------------|-----------------------|--------------------------------------------|
| AWS           | Alta (≥80%)   | Sí                    | Carbon Footprint Tool                      |
| Azure         | Alta (≥60%)   | Sí                    | Sustainability Calculator                  |
| Google Cloud  | Excel·lent (100%) | Sí                | Carbon-Free Energy Score                   |

**Conclusió**: Veiem que AWS ofereix la millor integració i serveis per empreses com InnovateTech.

---
<!-- Ejercicio 2 -->
# 📽️ Ejercicio 2  
## 🎙️ Implantació dels serveis d'Àudio i Vídeo

**- Implantació d'un servidor d'Àudio:** Hem instal·lat un servidor d'àudio que ens permet gestionar transmissions en temps real per als nostres clients i usuaris. La infraestructura ha de ser capaç de suportar el volum de trànsit generat per aquesta mena de servei, sense comprometre la qualitat del contingut. A més, hem realitzat diverses comprovacions per a assegurar-nos que la nostra xarxa pugui gestionar de manera eficient aquest trànsit.


**- Implantació d'un servidor de Streaming Vídeo:** Un altre dels serveis és el streaming de vídeo. Hem sol·licitat la implementació d'un servidor que permeti una distribució fluida i de qualitat del nostre contingut audiovisual. Al mateix temps, hem fet diverses proves per a evitar saturacions en la xarxa i garantir una experiència d'usuari òptima, maximitzant l'ús responsable dels recursos disponibles.


**- Comprovacions d'Amplada de banda:** Les comprovacions d'amplada de banda seran una prioritat per a assegurar-nos que el sistema dissenyat pugui gestionar adequadament els fluxos simultanis d'àudio i vídeo sense pèrdues de qualitat ni col·lapses en la xarxa. Volem una solució que optimitzi l'ús de la infraestructura existent i minimitzi l'impacte ambiental dels serveis que oferim.


---
<!-- Ejercicio 3 -->
# 🗄️ Ejercicio 3  
## 🧾 Disseny i implementació d'una Base de dades

En aquesta fase del projecte es va dissenyar i va crear una base de dades enfocada en la gestió de clients, complint amb els requisits definits.

### 🧩 Model Entitat-Relació (ER)

- **Entitats**: Empleats, Nivells de Grup, Departaments
- Es van definir claus primàries, atributs i relacions.

### 🔄 Transformació a Model Relacional

- Taules, claus primàries i foranes, tipus de dades adequades.
- Base per a implementació en MySQL.

  
## 🛠️ Implementació en MySQL

Instal·lem **MySQL Server** en una màquina amb Ubuntu 24.04 i iniciem el procés de creació de la base de dades. Seguidament, es van crear en les diferents taules i es van inserir les dades en elles.


També, es van crear diferents **usuaris i rols** amb unes certes restriccions. Alguns podien *inserir noves dades* en les taules, algun només podia *consultar-les*, entre altres casos...

---
<!-- Ejercicio 4 -->
# 🌿 Ejercicio 4
## 🍃 Sostenibilitat


Seguint els ODS i valors del Institut Tecnològic de Barcelona, s'han implementat les següents mesures:

### ✅ Accions sostenibles implementades

- Proveïdors cloud amb energia renovable.
- Virtualització per a reduir màquines.
- Monitoratge del consum.
- Regions cloud amb baixa petjada de carboni.
- 
### 📉 Estimació d'impacte ambiental

- **Consum anual estimat**: ~2.400 kWh
- **Emissions CO₂**: ~960 kg CO₂/any (reduïble)

### ➕ Altres Mesures adicionals

- Apagada automàtica fora d'horari.
- Instàncies eficients energèticament.
- Autoscaling i bones pràctiques TIC sostenibles.
