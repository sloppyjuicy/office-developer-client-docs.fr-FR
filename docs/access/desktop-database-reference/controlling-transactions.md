---
title: Contrôle des transactions
TOCTitle: Controlling Transactions
ms:assetid: 21a9f055-6907-3818-e232-21e579cc67b7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248994(v=office.15)
ms:contentKeyID: 48543685
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 78380cda81e7260eee609e01bed0f88ce04f96c7
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59581608"
---
# <a name="controlling-transactions"></a>Contrôle des transactions


**S’applique à** : Access 2013, Office 2013

Une *transaction* délimite le début et la fin d'une série d'opérations d'accès aux données au cours d'une connexion. Selon les fonctionnalités transactionnelles de votre source de données, l'objet **Connection** permet également de créer et de gérer des transactions. Par exemple, si vous utilisez le fournisseur Microsoft OLE DB pour SQL Server pour accéder à une base de données Microsoft SQL Server 2000, vous pouvez créer plusieurs transactions imbriquées pour les commandes que vous exécutez.

ADO garantit que les modifications d'une source de données résultant des opérations effectuées au cours d'une transaction réussissent ou échouent globalement.

Si vous annulez la transaction ou si l'une de ses opérations échoue, aucune des opérations de la transaction n'aboutit. La source de données reste telle qu'elle était au début de la la transaction.

Le modèle d'objet ADO n'inclut pas explicitement de transactions ; en revanche, il les représente par un ensemble de méthodes de l'objet **Connection** (**BeginTrans**, **CommitTrans** et **RollbackTrans**).

Pour plus d’informations sur les transactions, consultez le [Chapitre  5 : Mise à jour et persistance des données](chapter-5-updating-and-persisting-data.md).

