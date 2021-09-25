---
title: 'Chapitre 2 : Obtention de données'
TOCTitle: 'Chapter 2: Getting data'
ms:assetid: 72d097e1-9284-cc27-fd48-e6bbb6a2a543
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249465(v=office.15)
ms:contentKeyID: 48545619
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 6fca58a5235e37a56e66d0b16f8634c3b096f1a7
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59586130"
---
# <a name="chapter-2-getting-data"></a>Chapitre 2 : Obtention de données

**S’applique à** : Access 2013, Office 2013

Le chapitre précédent a présenté les quatre opérations primaires impliquées dans la création d'une application ADO : l'extraction des données, l'examen des données, la modification des données et la mise à jour des données. Ce chapitre va se pencher plus en détail sur les concepts relatifs à la première opération : l'extraction des données.

Plusieurs objets ADO peuvent jouer un rôle dans cette opération. Tout d'abord, vous vous connectez à la source de données à l'aide d'un objet **Connection** ADO (qui est parfois créé de manière implicite). Ensuite, vous transmettez vos instructions à la source de données à l'aide d'un objet **Command** ADO (qui peut aussi être créé de manière implicite). Le résultat du transfert d'une commande à la source de données et la réception de sa réponse est généralement représenté dans un objet **Recordset** ADO.

Pour extraire les données, votre application doit être en communication avec une source de données, comme un SGBD, un stockage de fichiers ou un fichier texte délimité par des virgules. Cette communication représente une *connexion* , l'environnement indispensable à tout échange de données.

Le modèle d'objet ADO représente le concept d'une connexion avec l'objet **Connection**: la clé de voûte d'une grande partie de la fonctionnalité ADO. La finalité d'un objet **Connection** est la suivante :

- Déterminer les informations qu'ADO doit communiquer aux sources de données et créer des sessions.

- Déterminer les capacités transactionnelles de la session.

- Vous permettre de créer et d'exécuter des commandes sur la source de données.

- Fournir des informations sur la conception de la source de données sous-jacente sous la forme d'ensembles de lignes schématiques. Pour en savoir plus sur ces derniers, reportez-vous à la rubrique [OpenSchema, méthode](openschema-method-ado.md).

Ce chapitre présente les rubriques suivantes :

- [Connexion](making-a-connection.md)
- [Utilisation de la référence d’objet de connexion (ADO)](using-the-connection-object-access.md)
- [Utilisation de la référence d’objet de commande (ADO)](using-the-command-object-access.md)
- [Ajout de données à un recordset (ADO)](adding-data-to-a-recordset.md)
