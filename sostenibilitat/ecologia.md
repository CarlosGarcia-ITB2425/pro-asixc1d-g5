# Sostenibilitat

Aquest apartat descriu la sostenibilitat i eficiència energètica

## 🌱 4. Sostenibilitat

### ♻️ 4.1 Sostenibilitat i eficiència energètica

Alineats amb els valors de l'**Institut Tecnològic de Barcelona** i els **Objectius de Desenvolupament Sostenible (ODS)**, el nostre projecte aposta per un enfocament **verd i responsable**. Volem:

* Ús de fonts d’energia renovables (proveïdors cloud amb zero emissions).
* Virtualització de serveis per reduir maquinari físic.
* Monitoratge i optimització per evitar el malbaratament de recursos.
* Elecció de regions cloud amb baixa petjada de carboni.
* Disseny del CPD físic amb ventilació passiva i racks eficients.

---

### 📊 4.2 Càlcul de la petjada ecològica

#### 1 Identificació de recursos emprats

**Serveis desplegats:**

* Màquines virtuals Ubuntu Server i Windows Server
* Serveis: DHCP, DNS, LDAP, Samba, Apache/Nginx, MySQL/MariaDB, ProFTP, VPN, correu electrònic
* Núcol: AWS EC2, RDS, S3, CloudWatch, ELB, Route53
* Protocols: TCP/IP, HTTP/HTTPS, SSH, FTP, SMTP, LDAP
* Usuaris: 20–25 estudiants
* Funcionament mitjà: 1.440 h/any
* Tràfic estimat: 1 TB/any

#### 2 Estimació del consum energètic i emissions

| **Recurs**          | **Consum**       | **Emissions (kg CO₂/any)** |
| ------------------- | ---------------- | -------------------------- |
| Màquines núcol (4x) | 2.400 kWh/any    | 960 kg CO₂ eq.             |
| Tràfic (1 TB)       | 5 kWh/any        | 2 kg CO₂ eq.               |
| CPD físic complet   | \~30.000 kWh/any | \~10.000 kg CO₂ eq.        |
| **TOTAL**           | **32.400 kWh**   | **10.962 kg CO₂ eq.**      |

> Si s’utilitzen regions 100% renovables (Irlanda, Oregon): <1.000 kg CO₂ eq./any.

---

### 💪 4.3 Mesures de reducció i optimització

#### Núcol:

* Triar regions verdes: Irlanda, Frankfurt, Oregon.
* Utilitzar instàncies eficients (AWS Graviton, GCP E2).
* Scripts d’apagat automàtic fora d’hores laborals.
* Agrupació de serveis en menys màquines.
* Autoscaling per evitar sobreprovisionament.

#### CPD físic:

* Refrigeració passiva nocturna.
* Energia contractada 100% verda.
* Canalitzacions sota terra tècnic i racks adjacents.
* Il·luminació LED intel·ligent.

#### Educació:

* Formació sobre TIC sostenibles.
* Inclusió de KPI ambientals en dashboards de seguiment.

---

### 📀 4.4 Fòrmules i plantilla de càlcul

| **Concepte**     | **Fòrmula**                    | **Resultat**   |
| ---------------- | ------------------------------ | -------------- |
| Consum núcol     | 4 màquines × 50 kWh × 12 mesos | 2.400 kWh      |
| Tràfic (1 TB)    | 1 × 5 kWh                      | 5 kWh          |
| Emissions de CO₂ | 2.405 × 0,4 kg CO₂/kWh         | 962 kg CO₂ eq. |

---

### 📋 Plantilla resum (exemple ITB)

| **Paràmetre**                 | **Valor**                              |
| ----------------------------- | -------------------------------------- |
| Proveïdor núcol               | AWS                                    |
| Regió CPD                     | Irlanda (eu-west-1)                    |
| Màquines virtuals             | 3 instàncies (Web, Vídeo, BBDD)        |
| vCPU per màquina              | 2–4 vCPU                               |
| RAM / Emmagatzematge          | 8–16 GB / 40–100 GB SSD                |
| Serveis desplegats            | EC2, RDS, S3, CloudWatch, ELB, Route53 |
| Protocols utilitzats          | HTTP/S, SSH, DNS...                    |
| Hores de funcionament/setmana | 40 h                                   |
| Setmanes l’any                | 36                                     |
| Tràfic anual estimat          | 1 TB                                   |
