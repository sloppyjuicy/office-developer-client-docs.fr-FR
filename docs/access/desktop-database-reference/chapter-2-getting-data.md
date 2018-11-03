---
title: 'Chapitre 2 : Extraction de données'
TOCTitle: 'Chapter 2: Getting data'
ms:assetid: 72d097e1-9284-cc27-fd48-e6bbb6a2a543
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249465(v=office.15)
ms:contentKeyID: 48545619
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 729d7a74c8e1ead84810e82d608e4e9b37268a6b
ms.sourcegitcommit: 38d0db57580cc5f4a0231c27b1643f8db5431ca3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25937000"
---
# <a name="chapter-2-getting-data"></a>Chapitre 2 : Extraction de données

**S’applique à**: Access 2013, Office 2013

Le chapitre précédent a présenté les quatre opérations primaires impliquées dans la création d'une application ADO : l'extraction des données, l'examen des données, la modification des données et la mise à jour des données. Ce chapitre va se pencher plus en détail sur les concepts relatifs à la première opération : l'extraction des données.

Plusieurs objets ADO peuvent jouer un rôle dans cette opération. Tout d'abord, vous vous connectez à la source de données à l'aide d'un objet **Connection** ADO (qui est parfois créé de manière implicite). Ensuite, vous transmettez vos instructions à la source de données à l'aide d'un objet **Command** ADO (qui peut aussi être créé de manière implicite). Le résultat du transfert d'une commande à la source de données et la réception de sa réponse est généralement représenté dans un objet **Recordset** ADO.

Pour extraire les données, votre application doit être en communication avec une source de données, comme un SGBD, un stockage de fichiers ou un fichier texte délimité par des virgules. Cette communication représente une *connexion* — l’environnement nécessaire pour l’échange de données.

Le modèle d'objet ADO représente le concept d'une connexion avec l'objet **Connection**: la clé de voûte d'une grande partie de la fonctionnalité ADO. La finalité d'un objet **Connection** est la suivante :

- Déterminer les informations qu'ADO doit communiquer aux sources de données et créer des sessions.

- Déterminer les capacités transactionnelles de la session.

- Vous permettre de créer et d'exécuter des commandes sur la source de données.

- Fournir des informations sur la conception de la source de données sous-jacente sous la forme d'ensembles de lignes schématiques. Pour en savoir plus sur ces derniers, reportez-vous à la rubrique [OpenSchema, méthode](openschema-method-ado.md).

Ce chapitre présente les rubriques suivantes :

- [Établissement d’une connexion](making-a-connection.md)
- [À l’aide de la référence d’objet connection (ADO)](using-the-connection-object-access.md)
- [À l’aide de la référence d’objet commande (ADO)](using-the-command-object-access.md)
- [Ajout de données à un jeu d’enregistrements (ADO)](adding-data-to-a-recordset.md)