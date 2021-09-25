---
title: Vue d’ensemble de l’objet Command
TOCTitle: Command object overview
ms:assetid: 3d6d81c4-4cf0-0c13-adb3-0c2c5934dc21
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249166(v=office.15)
ms:contentKeyID: 48544346
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 7f8be0fb8e199a33670f8388738b16b197ce9cf2
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59586136"
---
# <a name="command-object-overview"></a>Vue d’ensemble de l’objet Command

**S’applique à** : Access 2013, Office 2013

Grâce aux collections, aux méthodes et aux propriétés d'un objet **Command**, vous pouvez effectuer les opérations suivantes :

  - Définir le texte exécutable de la commande (par exemple, une instruction SQL ou une procédure stockée) en utilisant la propriété **CommandText**.

  - Définir des requêtes paramétrées ou des arguments de procédure stockée à l'aide des objets **Parameter** et de la collection **Parameters**.

  - Exécuter une commande et retourner un objet **Recordset**, le cas échéant, en utilisant la méthode **Execute**.

  - Spécifier le type de commande en utilisant la propriété **CommandType** avant l'exécution afin d'optimiser les performances.

  - Vérifier si le fournisseur enregistre une version préparée (ou compilée) de la commande avant l'exécution en utilisant la propriété **Prepared**.

  - Définir le nombre de secondes d'attente d'un fournisseur pour l'exécution d'une commande à l'aide de la propriété **CommandTimeout**.

  - Associer une connexion ouverte à un objet **Command** en définissant sa propriété **ActiveConnection**.

  - Définir la propriété **Name** pour spécifier l'objet **Command** en tant que méthode à utiliser sur l'objet **Connection** associé.

  - Passer un objet **Command** à la propriété **Source** d'un objet **Recordset** pour obtenir des données.

