---
title: Instruction DROP USER ou GROUP (Microsoft Access SQL)
TOCTitle: DROP USER or GROUP statement (Microsoft Access SQL)
ms:assetid: 46bc5916-556b-17df-2f4c-8fd7bbd21ef7
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193192(v=office.15)
ms:contentKeyID: 48544575
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 995f935ceea5af3b740215c5a4137e02e7ebb1b2
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28700835"
---
# <a name="drop-user-or-group-statement-microsoft-access-sql"></a><span data-ttu-id="590ff-102">Instruction DROP USER ou GROUP (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="590ff-102">DROP USER or GROUP statement (Microsoft Access SQL)</span></span>

<span data-ttu-id="590ff-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="590ff-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="590ff-104">Supprime un ou plusieurs *utilisateurs* ou *groupes*, ou un ou plusieurs *utilisateurs* existants à partir d’un *groupe*existant.</span><span class="sxs-lookup"><span data-stu-id="590ff-104">Deletes one or more existing *users* or *groups*, or removes one or more existing *users* from an existing *group*.</span></span>

## <a name="syntax"></a><span data-ttu-id="590ff-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="590ff-105">Syntax</span></span>

### <a name="delete-one-or-more-users-or-remove-one-or-more-users-from-a-group"></a><span data-ttu-id="590ff-106">Supprimer un ou plusieurs utilisateurs ou supprimer un ou plusieurs utilisateurs d’un groupe</span><span class="sxs-lookup"><span data-stu-id="590ff-106">Delete one or more users or remove one or more users from a group</span></span>

<span data-ttu-id="590ff-107">DROP USER *utilisateur*\[, *utilisateur*,... \] \[De *groupe*\]</span><span class="sxs-lookup"><span data-stu-id="590ff-107">DROP USER *user*\[, *user*, …\] \[FROM *group*\]</span></span>

### <a name="delete-one-or-more-groups"></a><span data-ttu-id="590ff-108">Supprimer un ou plusieurs groupes</span><span class="sxs-lookup"><span data-stu-id="590ff-108">Delete one or more groups</span></span>

<span data-ttu-id="590ff-109">DROP GROUP *groupe*\[, *groupe*,...\]</span><span class="sxs-lookup"><span data-stu-id="590ff-109">DROP GROUP *group*\[, *group*, …\]</span></span>

<span data-ttu-id="590ff-110">L'instruction DROP USER ou GROUP est composée des arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="590ff-110">The DROP USER or GROUP statement has these parts:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="590ff-111">Argument</span><span class="sxs-lookup"><span data-stu-id="590ff-111">Part</span></span></p></th>
<th><p><span data-ttu-id="590ff-112">Description</span><span class="sxs-lookup"><span data-stu-id="590ff-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="590ff-113"><em>utilisateur</em></span><span class="sxs-lookup"><span data-stu-id="590ff-113"><em>user</em></span></span></p></td>
<td><p><span data-ttu-id="590ff-114">Nom de l'utilisateur à supprimer du fichier d'informations du groupe de travail.</span><span class="sxs-lookup"><span data-stu-id="590ff-114">The name of a user to be removed from the workgroup information file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="590ff-115"><em>Groupe</em></span><span class="sxs-lookup"><span data-stu-id="590ff-115"><em>group</em></span></span></p></td>
<td><p><span data-ttu-id="590ff-116">Nom du groupe à supprimer du fichier d'informations du groupe de travail.</span><span class="sxs-lookup"><span data-stu-id="590ff-116">The name of a group to be removed from the workgroup information file.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="590ff-117">Notes</span><span class="sxs-lookup"><span data-stu-id="590ff-117">Remarks</span></span>

<span data-ttu-id="590ff-118">Si le mot clé FROM est utilisé dans l’instruction DROP USER, chacun des *utilisateurs* figurant dans l’instruction sera supprimé du *groupe* spécifié après le mot clé FROM.</span><span class="sxs-lookup"><span data-stu-id="590ff-118">If the FROM keyword is used in the DROP USER statement, each of the *users* listed in the statement will be removed from the *group* specified following the FROM keyword.</span></span> <span data-ttu-id="590ff-119">Toutefois, les *utilisateurs* eux-mêmes ne seront pas supprimés.</span><span class="sxs-lookup"><span data-stu-id="590ff-119">However, the *users* themselves will not be deleted.</span></span>

<span data-ttu-id="590ff-120">L’instruction DROP GROUP supprimera spécifié *groupe*(s).</span><span class="sxs-lookup"><span data-stu-id="590ff-120">The DROP GROUP statement will delete the specified *group*(s).</span></span> <span data-ttu-id="590ff-121">Les *utilisateurs* qui sont membres du *groupe*(s) ne seront pas affectés, mais ils ne seront plus membres supprimés de *groupe (s)*.</span><span class="sxs-lookup"><span data-stu-id="590ff-121">The *users* who are members of the *group*(s) will not be affected, but they will no longer be members of the deleted *group*(s).</span></span>

