---
title: Modèle de programmation RDS de base
TOCTitle: Basic RDS Programming Model
ms:assetid: a8dd22b0-ac9b-b5c3-4e31-d2990d36230a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249781(v=office.15)
ms:contentKeyID: 48546911
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: a666b12a3359c8212afaed66155d8cf8578f6a2c
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25886822"
---
# <a name="basic-rds-programming-model"></a>Modèle de programmation RDS de base


**S’applique à**: Access 2013, Office 2013

RDS est destiné aux applications qui existent dans l'environnement suivant : une application cliente spécifie un programme exécuté sur un serveur et les paramètres requis pour retourner les informations voulues. Le programme appelé sur le serveur accède à la source de données spécifiée, récupère les informations, traite éventuellement les données puis retourne les informations obtenues à l'application cliente sous une forme qu'elle peut facilement utiliser. RDS permet d'effectuer la séquence d'actions suivante :

  - Spécifier le programme à appeler sur le serveur et obtenir un moyen de s'y référer à partir du client. (Cette référence est parfois appelé *proxy* ; il s'agit du programme exécuté sur le serveur distant. L'application cliente « appelle » le proxy comme s'il s'agissait d'un programme local, mais elle appelle en réalité le programme sur le serveur distant.)

  - Appeler le programme sur le serveur et transmettre à ce programme des paramètres qui identifient la source de données et la commande à exécuter. (Le programme utilise en fait ADO pour accéder à la source de données. ADO établit une connexion avec le paramètre qui identifie la source de données, puis exécute la commande spécifiée par l'autre paramètre.)

  - Le programme sur le serveur obtient un objet [Recordset](recordset-object-ado.md) de la source de données. Le cas échéant, l'objet **Recordset** est traité sur le serveur.

  - Le programme sur le serveur retourne l'objet **Recordset** final à l'application cliente.

  - Sur le client, l'objet **Recordset** est présenté sous une forme facilement utilisable par des contrôles visuels.

  - Les modifications apportées à l'objet **Recordset** sont renvoyées au programme du serveur qui les utilise pour mettre à jour la source de données.

Ce modèle de programmation est pratique par certains aspects. Si vous n'avez pas besoin d'utiliser un programme complexe sur le serveur pour accéder à la source de données et si vous fournissez les paramètres de connexion et de commande requis, RDS récupère automatiquement les données spécifiées à l'aide d'un programme par défaut simple sur le serveur.

Si un traitement plus complexe est nécessaire, vous pouvez spécifier votre propre programme personnalisé à utiliser sur le serveur. Par exemple, si un programme personnalisé sur le serveur bénéficie de toute la puissance d'ADO, il peut se connecter à différentes sources de données, combiner leurs données dans des opérations complexes, puis les retourner sous une forme simple et déjà traitée à l'application cliente.

Enfin, si vous avez besoin d'un modèle de programmation à mi-chemin entre les deux exemples précédents, ADO permet à présent de personnaliser le comportement du programme serveur par défaut.

