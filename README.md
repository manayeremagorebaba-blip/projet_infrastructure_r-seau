# Infrastructure réseau — Établissement scolaire

Conception et simulation d'une infrastructure réseau pour un établissement scolaire, réalisée avec Cisco Packet Tracer. Le réseau relie trois sous-réseaux locaux à travers trois routeurs interconnectés, avec attribution automatique des adresses IP par un serveur DHCP.

Projet transversal réalisé en équipe dans le cadre de ma première année de Bachelor Informatique et Systèmes Digitaux à l'EPSI.

## Architecture du réseau

- **3 routeurs** (R1, R2, R3) interconnectés en triangle (chaque routeur est relié aux deux autres)
- **3 sous-réseaux locaux**, un par routeur, accueillant les postes de travail
- **1 serveur DHCP** distribuant automatiquement les adresses IP
- **6 postes** (PC1 à PC6) répartis sur les trois sous-réseaux
- Routage configuré entre les routeurs pour que tous les sous-réseaux communiquent entre eux

## Plan d'adressage IP

**Sous-réseaux locaux**

| Sous-réseau | Réseau | Routeur | Équipements |
|-------------|--------|---------|-------------|
| LAN 1 | 192.168.200.0 /24 | R1 | Serveur DHCP, PC1, PC2 |
| LAN 2 | 192.168.50.0 /24 | R2 | PC3, PC4 |
| LAN 3 | 192.168.100.0 /24 | R3 | PC5, PC6 |

**Liaisons entre les routeurs**

| Liaison | Réseau |
|---------|--------|
| R1 — R2 | 10.20.0.0 /16 |
| R1 — R3 | 10.10.0.0 /16 |
| R2 — R3 | 10.30.0.0 /16 |

**Serveur DHCP** : `192.168.200.2` — Passerelle `192.168.200.1` — DNS `8.8.8.8`

## Contenu du projet

- `vlan.pkt` — le fichier Cisco Packet Tracer (à ouvrir avec Packet Tracer)
- `Plan_Adressage_Reseau.docx` — le plan d'adressage IP détaillé
- `Projet transversal_Infrastructure_Reseau.pdf` — l'énoncé du projet

## Comment ouvrir le projet

1. Installer Cisco Packet Tracer (disponible via Cisco NetAcad)
2. Ouvrir le fichier `vlan.pkt`
3. Tester la connectivité entre les postes avec la commande `ping`

## Concepts mis en œuvre

- Adressage IP et découpage en sous-réseaux
- Configuration de routeurs et routage entre sous-réseaux
- Attribution automatique des adresses IP (DHCP)
- Configuration de VLANs
- Tests de connectivité entre équipements

## Aperçu 

<img width="1920" height="1020" alt="image" src="https://github.com/user-attachments/assets/0f0d8e3e-6bf9-4965-95d2-b446d5686a4a" />


## Auteur

Réalisé par Mana, étudiant en Bachelor Informatique et Systèmes Digitaux à l'EPSI.
