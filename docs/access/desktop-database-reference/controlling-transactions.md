---
title: Contrôle des transactions
TOCTitle: Controlling Transactions
ms:assetid: 21a9f055-6907-3818-e232-21e579cc67b7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248994(v=office.15)
ms:contentKeyID: 48543685
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 4acd03e387f50d9035c73dd2fef934f6fd6985a5
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25889643"
---
# <a name="controlling-transactions"></a><span data-ttu-id="f7d37-102">Contrôle des transactions</span><span class="sxs-lookup"><span data-stu-id="f7d37-102">Controlling Transactions</span></span>


<span data-ttu-id="f7d37-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="f7d37-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="f7d37-104">Une *transaction* délimitant le début et la fin d’une série d’opérations d’accès aux données cours d’une connexion.</span><span class="sxs-lookup"><span data-stu-id="f7d37-104">A *transaction* delimits the beginning and end of a series of data access operations that transpire across a connection.</span></span> <span data-ttu-id="f7d37-105">Selon les fonctionnalités transactionnelles de votre source de données, l'objet **Connection** permet également de créer et de gérer des transactions.</span><span class="sxs-lookup"><span data-stu-id="f7d37-105">Subject to the transactional capabilities of your data source, the **Connection** object also allows you to create and manage transactions.</span></span> <span data-ttu-id="f7d37-106">Par exemple, si vous utilisez le fournisseur Microsoft OLE DB pour SQL Server pour accéder à une base de données Microsoft SQL Server 2000, vous pouvez créer plusieurs transactions imbriquées pour les commandes que vous exécutez.</span><span class="sxs-lookup"><span data-stu-id="f7d37-106">For example, using the Microsoft OLE DB Provider for SQL Server to access a database on Microsoft SQL Server 2000, you can create multiple nested transactions for the commands you execute.</span></span>

<span data-ttu-id="f7d37-107">ADO garantit que les modifications d'une source de données résultant des opérations effectuées au cours d'une transaction réussissent ou échouent globalement.</span><span class="sxs-lookup"><span data-stu-id="f7d37-107">ADO ensures that changes to a data source resulting from operations in a transaction occur successfully together or not at all.</span></span>

<span data-ttu-id="f7d37-p102">Si vous annulez la transaction ou si l'une de ses opérations échoue, aucune des opérations de la transaction n'aboutit. La source de données reste telle qu'elle était au début de la la transaction.</span><span class="sxs-lookup"><span data-stu-id="f7d37-p102">If you cancel the transaction, or if one of its operations fails, the ultimate result will be as if none of the operations in the transaction occurred. The data source will remain as it was before the transaction began.</span></span>

<span data-ttu-id="f7d37-110">Le modèle d'objet ADO n'inclut pas explicitement de transactions ; en revanche, il les représente par un ensemble de méthodes de l'objet **Connection** (**BeginTrans**, **CommitTrans** et **RollbackTrans**).</span><span class="sxs-lookup"><span data-stu-id="f7d37-110">The ADO object model does not explicitly include transactions, but represents them with a set of **Connection** object methods (**BeginTrans**, **CommitTrans**, and **RollbackTrans**).</span></span>

<span data-ttu-id="f7d37-111">Pour plus d'informations sur les transactions, consultez le [Chapitre 5 : Mise à jour et persistance des données](chapter-5-updating-and-persisting-data.md).</span><span class="sxs-lookup"><span data-stu-id="f7d37-111">For more information about transactions, see [Chapter 5: Updating and Persisting Data](chapter-5-updating-and-persisting-data.md).</span></span>

