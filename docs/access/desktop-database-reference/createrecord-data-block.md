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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28719815"
---
# <a name="createrecord-data-block"></a><span data-ttu-id="cf4b1-102">Bloc de données CréerEnregistrement</span><span class="sxs-lookup"><span data-stu-id="cf4b1-102">CreateRecord data block</span></span>


<span data-ttu-id="cf4b1-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="cf4b1-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="cf4b1-104">Vous pouvez utiliser le bloc de données **CréerEnregistrement** pour créer un nouvel enregistrement dans la table spécifiée.</span><span class="sxs-lookup"><span data-stu-id="cf4b1-104">You can use the **CreateRecord** data block to create a new record in the specified table.</span></span>

> [!NOTE]
> <span data-ttu-id="cf4b1-105">[!REMARQUE] Le bloc de données **CréerEnregistrement** est disponible uniquement dans les macros de données.</span><span class="sxs-lookup"><span data-stu-id="cf4b1-105">The **CreateRecord** data block is available only in Data Macros.</span></span>

## <a name="setting"></a><span data-ttu-id="cf4b1-106">Paramètre</span><span class="sxs-lookup"><span data-stu-id="cf4b1-106">Setting</span></span>

<span data-ttu-id="cf4b1-107">Le bloc de données **SupprimerEnregistrement** utilise les arguments suivants.</span><span class="sxs-lookup"><span data-stu-id="cf4b1-107">The **CreateRecord** data block has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="cf4b1-108">Argument</span><span class="sxs-lookup"><span data-stu-id="cf4b1-108">Argument</span></span></p></th>
<th><p><span data-ttu-id="cf4b1-109">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="cf4b1-109">Required</span></span></p></th>
<th><p><span data-ttu-id="cf4b1-110">Description</span><span class="sxs-lookup"><span data-stu-id="cf4b1-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cf4b1-111"><strong>Créer un enregistrement dans</strong></span><span class="sxs-lookup"><span data-stu-id="cf4b1-111"><strong>Create a Record In</strong></span></span></p></td>
<td><p><span data-ttu-id="cf4b1-112">Oui</span><span class="sxs-lookup"><span data-stu-id="cf4b1-112">Yes</span></span></p></td>
<td><p><span data-ttu-id="cf4b1-113">Nom de la table dans laquelle créer le nouvel enregistrement.</span><span class="sxs-lookup"><span data-stu-id="cf4b1-113">The name of the table to create the new record in.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cf4b1-114"><strong>Alias</strong></span><span class="sxs-lookup"><span data-stu-id="cf4b1-114"><strong>Alias</strong></span></span></p></td>
<td><p><span data-ttu-id="cf4b1-115">Non</span><span class="sxs-lookup"><span data-stu-id="cf4b1-115">No</span></span></p></td>
<td><p><span data-ttu-id="cf4b1-116">Chaîne qui identifie l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="cf4b1-116">An string that identifies the record.</span></span> <span data-ttu-id="cf4b1-117">Vous pouvez utiliser l’alias de l’enregistrement pour l’identifier.</span><span class="sxs-lookup"><span data-stu-id="cf4b1-117">You can use the record's alias to identify</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="cf4b1-118">Notes</span><span class="sxs-lookup"><span data-stu-id="cf4b1-118">Remarks</span></span>

<span data-ttu-id="cf4b1-119">L'enregistrement créé par **CréerEnregistrement** devient automatiquement l'enregistrement actif.</span><span class="sxs-lookup"><span data-stu-id="cf4b1-119">The record created by **CreateRecord** automatically becomes the current record.</span></span>

<span data-ttu-id="cf4b1-120">Après l’instruction **CréerEnregistrement** , vous pouvez insérer un bloc de commandes qui sera exécuté avant que le nouvel enregistrement est validé.</span><span class="sxs-lookup"><span data-stu-id="cf4b1-120">After **CreateRecord** statement, you can insert a block of commands that will execute before the new record is committed.</span></span> <span data-ttu-id="cf4b1-121">Les actions suivantes sont disponibles dans un bloc de données **CréerEnregistrement**.</span><span class="sxs-lookup"><span data-stu-id="cf4b1-121">The following actions are available in a **CreateRecord** data block.</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cf4b1-122"><a href="cancelrecordchange-macro-action.md">CancelRecordChange, action de macro</a></span><span class="sxs-lookup"><span data-stu-id="cf4b1-122"><a href="cancelrecordchange-macro-action.md">CancelRecordChange macro action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cf4b1-123"><a href="comment-macro-statement.md">Comment, instruction de macro</a></span><span class="sxs-lookup"><span data-stu-id="cf4b1-123"><a href="comment-macro-statement.md">Comment macro statement</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cf4b1-124"><a href="group-macro-statement.md">Group, instruction de macro</a></span><span class="sxs-lookup"><span data-stu-id="cf4b1-124"><a href="group-macro-statement.md">Group macro statement</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cf4b1-125"><a href="if-then-else-macro-block.md">If... Procédez comme suit... Else, instruction de macro</a></span><span class="sxs-lookup"><span data-stu-id="cf4b1-125"><a href="if-then-else-macro-block.md">If...Then...Else macro statement</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cf4b1-126"><a href="setfield-macro-action.md">SetField, action de macro</a></span><span class="sxs-lookup"><span data-stu-id="cf4b1-126"><a href="setfield-macro-action.md">SetField macro action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cf4b1-127"><a href="setlocalvar-macro-action.md">SetLocalVar, action de macro</a></span><span class="sxs-lookup"><span data-stu-id="cf4b1-127"><a href="setlocalvar-macro-action.md">SetLocalVar macro action</a></span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="cf4b1-128">Après que l'action **CréerEnregistrement** a créé un enregistrement, utilisez l'action **DéfinirChamp** pour spécifier une valeur d'un champ dans le nouvel enregistrement.</span><span class="sxs-lookup"><span data-stu-id="cf4b1-128">After the **CreateRecord** action creates a record, use the **SetField** action to specify a value of a field in the new record.</span></span>

<span data-ttu-id="cf4b1-129">Vous pouvez utiliser une instruction **If... Then... Else** pour effectuer des opérations basées sur une condition.</span><span class="sxs-lookup"><span data-stu-id="cf4b1-129">You can use an **If...Then...Else** statment to perform operations based on a condition.</span></span>

<span data-ttu-id="cf4b1-p103">Pour annuler la création d'un enregistrement, utilisez l'action **AnnulerModificationEnregistrement**. Cela empêche la validation des modifications et quitte le bloc de données **CréerEnregistrement**.</span><span class="sxs-lookup"><span data-stu-id="cf4b1-p103">To cancel the creation of a record, use the **CancelRecordChange** action. This prevents the changes from being committed and exits the **CreateRecord** data block.</span></span>

<span data-ttu-id="cf4b1-132">Une fois le nouvel enregistrement validé, vous pouvez utiliser la variable locale **IdentitéDernierEnregistrementCréé** pour travailler avec l'enregistrement.</span><span class="sxs-lookup"><span data-stu-id="cf4b1-132">Once the new record is committed, you can use the **LastCreateRecordIdentity** local variable to work with the record.</span></span> <span data-ttu-id="cf4b1-133">Par exemple, utilisez la syntaxe suivante pour faire référence au champ AssignedTo du dernier enregistrement.</span><span class="sxs-lookup"><span data-stu-id="cf4b1-133">For example, use the following syntax to refer to the AssignedTo field of the most recently created record.</span></span>

`[LastCreateRecordIdentity].[AssignedTo]`

<span data-ttu-id="cf4b1-134">Le bloc de données **CréerEnregistrement** peut être utilisé uniquement dans les événements de macros de données **[Après insertion](after-insert-macro-event.md)**, **[Après MAJ](after-update-macro-event.md)** et **[Après MAJ](after-update-macro-event.md)**.</span><span class="sxs-lookup"><span data-stu-id="cf4b1-134">The **CreateRecord** data block can only be used in the **[After Insert](after-insert-macro-event.md)**, **[After Update](after-update-macro-event.md)**, and **[After Update](after-update-macro-event.md)** data macro events.</span></span>

