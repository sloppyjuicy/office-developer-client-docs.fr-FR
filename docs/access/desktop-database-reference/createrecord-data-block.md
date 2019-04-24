---
title: Bloc de données CréerEnregistrement
TOCTitle: CreateRecord data block
ms:assetid: e18f47f8-2aad-9a14-ad63-ab603a4d5b07
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835671(v=office.15)
ms:contentKeyID: 48548263
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 63e189143e77f9fcc42fa8d48c3ebfb2feda6633
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295351"
---
# <a name="createrecord-data-block"></a><span data-ttu-id="6bc5b-102">Bloc de données CréerEnregistrement</span><span class="sxs-lookup"><span data-stu-id="6bc5b-102">CreateRecord data block</span></span>


<span data-ttu-id="6bc5b-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="6bc5b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="6bc5b-104">Vous pouvez utiliser le bloc de données **CréerEnregistrement** pour créer un nouvel enregistrement dans la table spécifiée.</span><span class="sxs-lookup"><span data-stu-id="6bc5b-104">You can use the **CreateRecord** data block to create a new record in the specified table.</span></span>

> [!NOTE]
> <span data-ttu-id="6bc5b-105">Le bloc de données **CréerEnregistrement** est disponible uniquement dans les macros de données.</span><span class="sxs-lookup"><span data-stu-id="6bc5b-105">The **CreateRecord** data block is available only in Data Macros.</span></span>

## <a name="setting"></a><span data-ttu-id="6bc5b-106">Setting</span><span class="sxs-lookup"><span data-stu-id="6bc5b-106">Setting</span></span>

<span data-ttu-id="6bc5b-107">Le bloc de données **CréerEnregistrement** utilise les arguments suivants.</span><span class="sxs-lookup"><span data-stu-id="6bc5b-107">The **CreateRecord** data block has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="6bc5b-108">Argument</span><span class="sxs-lookup"><span data-stu-id="6bc5b-108">Argument</span></span></p></th>
<th><p><span data-ttu-id="6bc5b-109">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="6bc5b-109">Required</span></span></p></th>
<th><p><span data-ttu-id="6bc5b-110">Description</span><span class="sxs-lookup"><span data-stu-id="6bc5b-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6bc5b-111"><strong>Créer un enregistrement dans</strong></span><span class="sxs-lookup"><span data-stu-id="6bc5b-111"><strong>Create a Record In</strong></span></span></p></td>
<td><p><span data-ttu-id="6bc5b-112">Oui</span><span class="sxs-lookup"><span data-stu-id="6bc5b-112">Yes</span></span></p></td>
<td><p><span data-ttu-id="6bc5b-113">Nom de la table dans laquelle créer le nouvel enregistrement.</span><span class="sxs-lookup"><span data-stu-id="6bc5b-113">The name of the table to create the new record in.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6bc5b-114"><strong>Alias</strong></span><span class="sxs-lookup"><span data-stu-id="6bc5b-114"><strong>Alias</strong></span></span></p></td>
<td><p><span data-ttu-id="6bc5b-115">Non</span><span class="sxs-lookup"><span data-stu-id="6bc5b-115">No</span></span></p></td>
<td><p><span data-ttu-id="6bc5b-116">Chaîne qui identifie l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="6bc5b-116">An string that identifies the record.</span></span> <span data-ttu-id="6bc5b-117">Vous pouvez utiliser l’alias de l’enregistrement pour l’identifier.</span><span class="sxs-lookup"><span data-stu-id="6bc5b-117">You can use the record's alias to identify</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="6bc5b-118">Remarques</span><span class="sxs-lookup"><span data-stu-id="6bc5b-118">Remarks</span></span>

<span data-ttu-id="6bc5b-119">L’enregistrement créé par \*\*CréerEnregistrement \*\* devient automatiquement l’enregistrement actif.</span><span class="sxs-lookup"><span data-stu-id="6bc5b-119">The record created by **CreateRecord** automatically becomes the current record.</span></span>

<span data-ttu-id="6bc5b-120">Après l'instruction **CréerEnregistrement** , vous pouvez insérer un bloc de commandes qui s'exécutera avant la validation du nouvel enregistrement.</span><span class="sxs-lookup"><span data-stu-id="6bc5b-120">After **CreateRecord** statement, you can insert a block of commands that will execute before the new record is committed.</span></span> <span data-ttu-id="6bc5b-121">Les actions suivantes sont disponibles dans un bloc de données **CréerEnregistrement**.</span><span class="sxs-lookup"><span data-stu-id="6bc5b-121">The following actions are available in a **CreateRecord** data block.</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6bc5b-122"><a href="cancelrecordchange-macro-action.md">CancelRecordChange, action de macro</a></span><span class="sxs-lookup"><span data-stu-id="6bc5b-122"><a href="cancelrecordchange-macro-action.md">CancelRecordChange macro action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6bc5b-123"><a href="comment-macro-statement.md">Comment, instruction de macro</a></span><span class="sxs-lookup"><span data-stu-id="6bc5b-123"><a href="comment-macro-statement.md">Comment macro statement</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6bc5b-124"><a href="group-macro-statement.md">Group, instruction de macro</a></span><span class="sxs-lookup"><span data-stu-id="6bc5b-124"><a href="group-macro-statement.md">Group macro statement</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6bc5b-125"><a href="if-then-else-macro-block.md">If... Then... Else, instruction de macro</a></span><span class="sxs-lookup"><span data-stu-id="6bc5b-125"><a href="if-then-else-macro-block.md">If...Then...Else macro statement</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6bc5b-126"><a href="setfield-macro-action.md">SetField, action de macro</a></span><span class="sxs-lookup"><span data-stu-id="6bc5b-126"><a href="setfield-macro-action.md">SetField macro action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6bc5b-127"><a href="setlocalvar-macro-action.md">SetLocalVar, action de macro</a></span><span class="sxs-lookup"><span data-stu-id="6bc5b-127"><a href="setlocalvar-macro-action.md">SetLocalVar macro action</a></span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="6bc5b-128">Après que l'action **CréerEnregistrement** a créé un enregistrement, utilisez l'action **DéfinirChamp** pour spécifier une valeur d'un champ dans le nouvel enregistrement.</span><span class="sxs-lookup"><span data-stu-id="6bc5b-128">After the **CreateRecord** action creates a record, use the **SetField** action to specify a value of a field in the new record.</span></span>

<span data-ttu-id="6bc5b-129">Vous pouvez utiliser une instruction **If... Then... Else** pour effectuer des opérations basées sur une condition.</span><span class="sxs-lookup"><span data-stu-id="6bc5b-129">You can use an **If...Then...Else** statment to perform operations based on a condition.</span></span>

<span data-ttu-id="6bc5b-p103">Pour annuler la création d'un enregistrement, utilisez l'action **AnnulerModificationEnregistrement**. Cela empêche la validation des modifications et quitte le bloc de données **CréerEnregistrement**.</span><span class="sxs-lookup"><span data-stu-id="6bc5b-p103">To cancel the creation of a record, use the **CancelRecordChange** action. This prevents the changes from being committed and exits the **CreateRecord** data block.</span></span>

<span data-ttu-id="6bc5b-132">Une fois le nouvel enregistrement validé, vous pouvez utiliser la variable locale **IdentitéDernierEnregistrementCréé** pour travailler avec l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="6bc5b-132">Once the new record is committed, you can use the **LastCreateRecordIdentity** local variable to work with the record.</span></span> <span data-ttu-id="6bc5b-133">Par exemple, utilisez la syntaxe suivante pour faire référence au champ AffectéÀ du dernier enregistrement créé.</span><span class="sxs-lookup"><span data-stu-id="6bc5b-133">For example, use the following syntax to refer to the AssignedTo field of the most recently created record.</span></span>

`[LastCreateRecordIdentity].[AssignedTo]`

<span data-ttu-id="6bc5b-134">Le bloc de données **CréerEnregistrement** peut être utilisé uniquement dans les événements de macros de données **[Après insertion](after-insert-macro-event.md)**, **[Après MAJ](after-update-macro-event.md)** et **[Après MAJ](after-update-macro-event.md)**.</span><span class="sxs-lookup"><span data-stu-id="6bc5b-134">The **CreateRecord** data block can only be used in the **[After Insert](after-insert-macro-event.md)**, **[After Update](after-update-macro-event.md)**, and **[After Update](after-update-macro-event.md)** data macro events.</span></span>

