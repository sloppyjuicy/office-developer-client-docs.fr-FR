---
title: Modèle de programmation RDS avec des objets
TOCTitle: RDS Programming Model with Objects
ms:assetid: 207150ec-8eb5-bec5-3059-db37a0e28c19
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248987(v=office.15)
ms:contentKeyID: 48543663
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 833d3676c8fa3fac1e5cb8e16477073cde611199
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25470050"
---
# <a name="rds-programming-model-with-objects"></a>Modèle de programmation RDS avec des objets


**S’applique à**: Access 2013 | Office 2013

L'objectif de RDS est de pouvoir accéder aux sources de données et de les mettre à jour via un service intermédiaire, tel qu'IIS. Le modèle de programmation spécifie la séquence d'activités nécessaires à la réalisation de cet objectif. Le modèle objet spécifie les objets dont les méthodes et les propriétés ont une incidence sur le modèle de programmation.

RDS offre la possibilité d'exécuter les séquences d'actions suivantes :

  - Spécifier le programme à appeler sur le serveur et obtenir un moyen (proxy) d'y faire référence à partir du client ([RDS.DataSpace](dataspace-object-rds.md)).

  - Appeler le programme serveur et passer les paramètres au programme serveur qui identifie la source de données et la commande à émettre (proxy ou [RDS.DataControl](datacontrol-object-rds.md)).

  - Le programme serveur obtient un objet [Recordset](recordset-object-ado.md) de la source de données, en général à l’aide d’ADO. Le cas échéant, l’objet **Recordset** est traité sur le serveur ([RDSServer.DataFactory](datafactory-object-rdsserver.md)).

  - Le programme serveur retourne l'objet **Recordset** final à l'application cliente (proxy).

  - Sur le client, l'objet **Recordset** est présenté sous une forme facilement utilisable par les contrôles visuels (contrôle visuel et **RDS.DataControl**).

  - Les modifications apportées à l'objet **Recordset** sont renvoyées au serveur et utilisées pour mettre à jour la source de données (**RDS.DataControl** ou **RDSServer.DataFactory**).

