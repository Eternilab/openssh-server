---
title: openssh-server ansible role
---
# Openssh-server

## Licence

Ce rôle est sous licence XXX

## Avant propos

Ce rôle est conforme au document [NT_SSH] de l'ANSSI, uniquement si vous utilisez les valeurs par défauts du rôle.

Ce rôle ne garanti pas la conformité en cas de modification de ces valeurs, bien que d'autres valeurs puissent être conformes.

## Description

Ce rôle configure le serveur OpenSSH pour qu'il soit conforme au guide 
NT_SSH de l'ANSSI :fr: :

> https://cyber.gouv.fr/publications/usage-securise-dopenssh

---

## Conformité ANSSI NT_SSH

Signification de la couverture :

* :white_check_mark: la recommandation est couverte par ce rôle
* :x: la recommandation n'est pas couverte par ce rôle
* :no_entry_sign: la recommandation ne peut pas être couverte par une solution technique


| Recommandation | Couverture | Configuration | Valeur par défaut | Commentaire |
| ---  | ---                  | ---           | ---    | ---         |
| R1   | :white_check_mark:   | Protocol      | 2 | |
| R2   | :x:                  |               | | |
| R3   | :x:                  |               | | |
| R4   | :x:                  |               | | |
| R5   | :white_check_mark:   | FIXME         | | |
| R6   | :x:                  |               | | |
| R7   | :white_check_mark:   | HostKey       | désactivé | DSA est interdit |
| R8   | :white_check_mark:   | HostKey       | désactivé | Ed25519 lui est préféré |
| R9   | :white_check_mark:   | HostKey       | désactivé | Ed25519 lui est préféré |
| R10  | :white_check_mark:   | HostKey       | désactivé | Ed25519 lui est préféré |
| R11  | :white_check_mark:   | -   | | Automatique depuis Linux 5.19 |
| R12  | :white_check_mark:   | -   | | Automatique depuis Linux 5.19 |
| R13  | :white_check_mark:   | -   | | Vérifié par le rôle ansible|
| R14  | :white_check_mark:   | StrictModes | yes | |
| R15  | :white_check_mark:   | Ciphers <br/>-<br/> MACs | chacha20-poly1305@openssh.com <br/>-<br/> hmac-sha2-512-etm@openssh.com | |
| R16  | :white_check_mark:   | -   | | Les paramètres de Debian/FreeBSD sont considérés comme durcis |
| R17  | :white_check_mark:   | KexAlgorithms <br/>-<br/> AuthenticationMethods <br/>-<br/> PubkeyAuthentication <br/>-<br/> AuthorizedKeysFile | curve25519-sha256@libssh.org <br/>-<br/> publickey <br/>-<br/> yes <br/>-<br/> %h/.ssh/authorized_keys | Ed25519 est préféré à ECDSA |
| R18  | :white_check_mark: | cell 9   || |
| R19  |          | cell 9   || |
| R20  |          | cell 9   || |
| R21  | :white_check_mark: | cell 9   || |
| R22  | :white_check_mark: | cell 9   || |
| R23  | :white_check_mark: | cell 9   || |
| R24  | :white_check_mark: | cell 9   || |
| R25  |          | cell 9   || |
| R26  | :white_check_mark: | cell 9   || |
| R27  | :white_check_mark: | cell 9   || |
| R28  | :white_check_mark: | cell 9   || |
| R29  |          | cell 9   || |
| R30  | :white_check_mark: | cell 9   || |
| R31  |          | cell 9   || |
