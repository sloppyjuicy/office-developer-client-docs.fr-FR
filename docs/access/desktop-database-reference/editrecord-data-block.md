---
title: ModifierEnregistrement, bloc de données
TOCTitle: EditRecord Data Block
ms:assetid: fe9f55eb-d7ed-1914-65a9-fa2fcb332b98
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837277(v=office.15)
ms:contentKeyID: 48548940
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 9c4d5a5a1565aeda41e5a52127e9f82b5304e686
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25876882"
---
# <a name="editrecord-data-block"></a><span data-ttu-id="0ca2f-102">ModifierEnregistrement, bloc de données</span><span class="sxs-lookup"><span data-stu-id="0ca2f-102">EditRecord Data Block</span></span>

<span data-ttu-id="0ca2f-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="0ca2f-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="0ca2f-104">Vous pouvez utiliser le bloc de données **ModifierEnregistrement** pour modifier les valeurs contenues dans un enregistrement existant.</span><span class="sxs-lookup"><span data-stu-id="0ca2f-104">You can use the **EditRecord** data block to change the values contained in an existing record.</span></span>

> [!NOTE]
> <span data-ttu-id="0ca2f-105">[!REMARQUE] Le bloc de données **ModifierEnregistrement** est disponible uniquement dans les macros de données.</span><span class="sxs-lookup"><span data-stu-id="0ca2f-105">The **EditRecord** data block is available only in Data Macros.</span></span>


## <a name="setting"></a><span data-ttu-id="0ca2f-106">Paramètre</span><span class="sxs-lookup"><span data-stu-id="0ca2f-106">Setting</span></span>

<span data-ttu-id="0ca2f-107">Le bloc de données **ModifierEnregistrement** utilise les arguments suivants.</span><span class="sxs-lookup"><span data-stu-id="0ca2f-107">The **EditRecord** data block has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="0ca2f-108">Argument</span><span class="sxs-lookup"><span data-stu-id="0ca2f-108">Argument</span></span></p></th>
<th><p><span data-ttu-id="0ca2f-109">Description</span><span class="sxs-lookup"><span data-stu-id="0ca2f-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0ca2f-110"><strong>Alias</strong></span><span class="sxs-lookup"><span data-stu-id="0ca2f-110"><strong>Alias</strong></span></span></p></td>
<td><p><span data-ttu-id="0ca2f-p101">Chaîne qui identifie l’enregistrement à modifier. Si l’argument <em>Alias</em> n’est pas spécifié, l’enregistrement actif est modifié.</span><span class="sxs-lookup"><span data-stu-id="0ca2f-p101">A string that identifies the record to edit. If the <em>Alias</em> argument is not specified, then the current record is edited.</span></span></p></td>
</tr>
</tbody>
</table>

## <a name="remarks"></a><span data-ttu-id="0ca2f-113">Notes</span><span class="sxs-lookup"><span data-stu-id="0ca2f-113">Remarks</span></span>

<span data-ttu-id="0ca2f-p102">Après l'instruction **ModifierEnregistrement**, vous pouvez insérer un bloc de commandes qui sera exécuté avant la validation des modifications apportées à l'enregistrement. Les actions suivantes sont disponibles dans un bloc de données **ModifierEnregistrement**.</span><span class="sxs-lookup"><span data-stu-id="0ca2f-p102">After **EditRecord** statement, you can insert a block of commands that will execute before the changes to the record are comitted. The following actions are available in a **EditRecord** data block.</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0ca2f-116"><a href="cancelrecordchange-macro-action.md">Action de Macro AnnulerModificationEnregistrement</a></span><span class="sxs-lookup"><span data-stu-id="0ca2f-116"><a href="cancelrecordchange-macro-action.md">CancelRecordChange Macro Action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0ca2f-117"><a href="comment-macro-statement.md">Instruction de Macro commentaire</a></span><span class="sxs-lookup"><span data-stu-id="0ca2f-117"><a href="comment-macro-statement.md">Comment Macro Statement</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0ca2f-118"><a href="group-macro-statement.md">Group, instruction de Macro</a></span><span class="sxs-lookup"><span data-stu-id="0ca2f-118"><a href="group-macro-statement.md">Group Macro Statement</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0ca2f-119"><a href="if-then-else-macro-block.md">If... Procédez comme suit... Else, instruction de Macro</a></span><span class="sxs-lookup"><span data-stu-id="0ca2f-119"><a href="if-then-else-macro-block.md">If...Then...Else Macro Statement</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0ca2f-120"><a href="setfield-macro-action.md">Action de Macro SetField</a></span><span class="sxs-lookup"><span data-stu-id="0ca2f-120"><a href="setfield-macro-action.md">SetField Macro Action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0ca2f-121"><a href="setlocalvar-macro-action.md">Action de Macro DéfinirVarLocale</a></span><span class="sxs-lookup"><span data-stu-id="0ca2f-121"><a href="setlocalvar-macro-action.md">SetLocalVar Macro Action</a></span></span></p></td>
</tr>
</tbody>
</table>

<span data-ttu-id="0ca2f-122">Utilisez l'action **DéfinirChamp** pour spécifier les nouvelles valeurs d'un champ dans l'enregistrement modifié.</span><span class="sxs-lookup"><span data-stu-id="0ca2f-122">Use the **SetField** action to specify the new values of a field in the edited record.</span></span>

<span data-ttu-id="0ca2f-123">Vous pouvez utiliser une instruction **If... Then... Else** pour effectuer des opérations basées sur une condition.</span><span class="sxs-lookup"><span data-stu-id="0ca2f-123">You can use an **If...Then...Else** statment to perform operations based on a condition.</span></span>

<span data-ttu-id="0ca2f-p103">Pour annuler la modification d'un enregistrement, utilisez l'action **AnnulerModificationEnregistrement**. Cela empêche la validation des modifications et quitte le bloc de données **ModifierEnregistrement**.</span><span class="sxs-lookup"><span data-stu-id="0ca2f-p103">To cancel the editing of a record, use the **CancelRecordChange** action. This prevents the changes from being committed and exits the **EditRecord** data block.</span></span>

<span data-ttu-id="0ca2f-126">Vous pouvez utiliser la variable locale **IdentitéDernierEnregistrementCréé** pour travailler avec le dernier enregistrement créé dans un bloc de données **CréerEnregistrement**.</span><span class="sxs-lookup"><span data-stu-id="0ca2f-126">You can use the **LastCreateRecordIdentity** local variable to work with last record created in a **CreateRecord** data block.</span></span> <span data-ttu-id="0ca2f-127">Par exemple, utilisez la syntaxe suivante pour faire référence au champ AssignedTo du dernier enregistrement :</span><span class="sxs-lookup"><span data-stu-id="0ca2f-127">For example, use the following syntax to refer to the AssignedTo field of the most recently created record:</span></span>

`[LastCreateRecordIdentity].[AssignedTo]`

<span data-ttu-id="0ca2f-128">Le bloc de données CréerEnregistrement peut être utilisé uniquement dans les événements de macros de données **[Après insertion](after-insert-macro-event.md)**, **[Après MAJ](after-update-macro-event.md)** et **[Après MAJ](after-update-macro-event.md)**.</span><span class="sxs-lookup"><span data-stu-id="0ca2f-128">The CreateRecord data block can only be used in the **[After Insert](after-insert-macro-event.md)**, **[After Update](after-update-macro-event.md)**, and **[After Update](after-update-macro-event.md)** data macro events.</span></span>

