---
title: DeleteRecord, action de macro
TOCTitle: DeleteRecord macro action
ms:assetid: c656a72c-c037-76a5-dc07-f6eccb6590dd
ms:mtpsurl: https://msdn.microsoft.com/library/Ff823132(v=office.15)
ms:contentKeyID: 48547624
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 8fb20068052972696b09ea0d2165b344e97ea922
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294014"
---
# <a name="deleterecord-macro-action"></a><span data-ttu-id="8841f-102">DeleteRecord, action de macro</span><span class="sxs-lookup"><span data-stu-id="8841f-102">DeleteRecord macro action</span></span>

<span data-ttu-id="8841f-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="8841f-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="8841f-104">Vous pouvez utiliser l’action **SupprimerEnregistrement** pour supprimer un enregistrement.</span><span class="sxs-lookup"><span data-stu-id="8841f-104">You can use the **DeleteRecord** action to delete a record.</span></span>

## <a name="setting"></a><span data-ttu-id="8841f-105">Paramètre</span><span class="sxs-lookup"><span data-stu-id="8841f-105">Setting</span></span>

<span data-ttu-id="8841f-106">Le bloc de données **CréerEnregistrement** utilise les arguments suivants.</span><span class="sxs-lookup"><span data-stu-id="8841f-106">The **CreateRecord** data block has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="8841f-107">Argument</span><span class="sxs-lookup"><span data-stu-id="8841f-107">Argument</span></span></p></th>
<th><p><span data-ttu-id="8841f-108">Description</span><span class="sxs-lookup"><span data-stu-id="8841f-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8841f-109"><strong>Alias d’enregistrement</strong></span><span class="sxs-lookup"><span data-stu-id="8841f-109"><strong>Record Alias</strong></span></span></p></td>
<td><p><span data-ttu-id="8841f-p101">Chaîne qui identifie l’enregistrement à supprimer. Si l’argument <em>Alias</em> n’est pas spécifié, l’enregistrement actif est supprimé.</span><span class="sxs-lookup"><span data-stu-id="8841f-p101">A string that identifies the record to delete. If the <em>Alias</em> argument is not specified, then the current record is deleted.</span></span></p></td>
</tr>
</tbody>
</table>

## <a name="remarks"></a><span data-ttu-id="8841f-112">Remarques</span><span class="sxs-lookup"><span data-stu-id="8841f-112">Remarks</span></span>

<span data-ttu-id="8841f-113">Vous pouvez utiliser la variable locale **IdentitéDernierEnregistrementCréé** pour travailler avec le dernier enregistrement créé dans un bloc de données **CréerEnregistrement**.</span><span class="sxs-lookup"><span data-stu-id="8841f-113">You can use the **LastCreateRecordIdentity** local variable to work with last record created in a **CreateRecord** data block.</span></span> <span data-ttu-id="8841f-114">Par exemple, utilisez la syntaxe suivante pour faire référence au dernier enregistrement créé :</span><span class="sxs-lookup"><span data-stu-id="8841f-114">For example, use the following syntax to refer to the most recently created record:</span></span>

`[LastCreateRecordIdentity]`

