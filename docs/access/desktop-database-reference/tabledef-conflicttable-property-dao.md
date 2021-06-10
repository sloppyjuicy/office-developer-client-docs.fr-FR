---
title: TableDef.ConflictTable, propriété (DAO)
TOCTitle: ConflictTable Property
ms:assetid: 0db8b975-eb6d-19c6-cfb7-6ce01230ebe4
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845218(v=office.15)
ms:contentKeyID: 48543228
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053356
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 0189a5163dd5e225ad34841264cf84e85785d7fb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308427"
---
# <a name="tabledefconflicttable-property-dao"></a><span data-ttu-id="2a661-102">TableDef.ConflictTable, propriété (DAO)</span><span class="sxs-lookup"><span data-stu-id="2a661-102">TableDef.ConflictTable property (DAO)</span></span>


<span data-ttu-id="2a661-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="2a661-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="2a661-p101">Renvoie le nom d'une table de conflits contenant les enregistrements de base de données qui sont entrés en conflit lors de la synchronisation de deux réplicas (espaces de travail Microsoft Access uniquement). Valeur de type **String** en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="2a661-p101">Returns the name of a conflict table containing the database records that conflicted during the synchronization of two replicas (Microsoft Access workspaces only). Read-only **String**.</span></span>

## <a name="syntax"></a><span data-ttu-id="2a661-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2a661-106">Syntax</span></span>

<span data-ttu-id="2a661-107">*.* ConflictTable</span><span class="sxs-lookup"><span data-stu-id="2a661-107">*expression* .ConflictTable</span></span>

<span data-ttu-id="2a661-108">*expression* Expression qui renvoie un **objet TableDef.**</span><span class="sxs-lookup"><span data-stu-id="2a661-108">*expression* An expression that returns a **TableDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="2a661-109">Remarques</span><span class="sxs-lookup"><span data-stu-id="2a661-109">Remarks</span></span>

<span data-ttu-id="2a661-110">La valeur renvoyée est un type de données **String** qui correspond à une chaîne nulle ("") s'il n'y a pas de table de conflits ou si la base de données n'est pas un réplica.</span><span class="sxs-lookup"><span data-stu-id="2a661-110">The return value is a **String** data type that is a zero-length string ("") if there is no conflict table or the database isn't a replica.</span></span>

<span data-ttu-id="2a661-p102">Si deux utilisateurs sur deux réplicas distincts modifient le même enregistrement de la base de données, les modifications apportées par un utilisateur ne seront pas répercutées sur l'autre réplica. Par conséquent, cet utilisateur doit résoudre les conflits.</span><span class="sxs-lookup"><span data-stu-id="2a661-p102">If two users at two separate replicas each make a change to the same record in the database, the changes made by one user will fail to be applied to the other replica. Consequently, the user with the failed change must resolve the conflicts.</span></span>

<span data-ttu-id="2a661-p103">Les conflits se produisent au niveau des enregistrements et non entre des champs. Par exemple, si un utilisateur modifie le champ Adresse et qu'un autre utilisateur met à jour le champ Téléphone du même enregistrement, l'une des modifications est refusée. Le refus se produit même s'il est peu probable que la modification acceptée et la modification refusée entraînent un conflit réel.</span><span class="sxs-lookup"><span data-stu-id="2a661-p103">Conflicts occur at the record level, not between fields. For example, if one user changes the Address field and another updates the Phone field in the same record, then one change is rejected. Because conflicts occur at the record level, the rejection occurs even though the successful change and the rejected change are unlikely to result in a true conflict of information.</span></span>

<span data-ttu-id="2a661-p104">Le mécanisme de synchronisation gère les conflits d'enregistrements en créant des tables de conflits, qui contiennent les informations qui auraient été insérées dans la table si la modification avait réussi. Vous pouvez consulter ces tables de conflits et les parcourir ligne par ligne pour résoudre les conflits.</span><span class="sxs-lookup"><span data-stu-id="2a661-p104">The synchronization mechanism handles the record conflicts by creating conflict tables, which contain the information that would have been placed in the table, if the change had been successful. You can examine these conflict tables and work through them row by row, fixing whatever is appropriate.</span></span>

<span data-ttu-id="2a661-118">Toutes les tables de conflit sont nommées conflit de table, où table est le nom d’origine de la table, tronquée à la longueur de nom de \_ table maximale.</span><span class="sxs-lookup"><span data-stu-id="2a661-118">All conflict tables are named table\_conflict, where table is the original name of the table, truncated to the maximum table name length.</span></span>

