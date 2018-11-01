---
title: Vue d'ensemble de l'objet Command
TOCTitle: Command Object Overview
ms:assetid: 3d6d81c4-4cf0-0c13-adb3-0c2c5934dc21
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249166(v=office.15)
ms:contentKeyID: 48544346
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 39724156b8644b6d99ffec82bdf79624b6cfaee1
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25875034"
---
# <a name="command-object-overview"></a>Vue d'ensemble de l'objet Command


**S’applique à**: Access 2013, Office 2013

Grâce aux collections, aux méthodes et aux propriétés d'un objet **Command**, vous pouvez effectuer les opérations suivantes :

  - Définir le texte exécutable de la commande (par exemple, une instruction SQL ou une procédure stockée) en utilisant la propriété **CommandText**.

  - Définir des requêtes paramétrées ou des arguments de procédure stockée à l'aide des objets **Parameter** et de la collection **Parameters**.

  - Exécuter une commande et retourner un objet **Recordset**, le cas échéant, en utilisant la méthode **Execute**.

  - Spécifier le type de commande en utilisant la propriété **CommandType** avant l'exécution afin d'optimiser les performances.

  - Vérifier si le fournisseur enregistre une version préparée (ou compilée) de la commande avant l'exécution en utilisant la propriété **Prepared**.

  - Définir le nombre de secondes d'attente d'un fournisseur pour l'exécution d'une commande à l'aide de la propriété **CommandTimeout**.

  - Associer une connexion ouverte à un objet **Command** en définissant sa propriété **ActiveConnection**.

  - définir la propriété **Name** pour identifier l'objet **Command** en tant que méthode pour l'objet **Connection** associé ;

  - Passer un objet **Command** à la propriété **Source** d'un objet **Recordset** pour obtenir des données.

