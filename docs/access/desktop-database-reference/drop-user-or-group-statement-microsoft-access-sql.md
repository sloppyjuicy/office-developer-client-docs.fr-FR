---
title: Instruction DROP USER ou GROUP (Microsoft Access SQL)
TOCTitle: DROP USER or GROUP statement (Microsoft Access SQL)
ms:assetid: 46bc5916-556b-17df-2f4c-8fd7bbd21ef7
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193192(v=office.15)
ms:contentKeyID: 48544575
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: a7988a2124af13dc84cefe678342da969e349a06
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25864027"
---
# <a name="drop-user-or-group-statement-microsoft-access-sql"></a><span data-ttu-id="71261-102">Instruction DROP USER ou GROUP (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="71261-102">DROP USER or GROUP statement (Microsoft Access SQL)</span></span>

<span data-ttu-id="71261-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="71261-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="71261-104">Supprime un ou plusieurs *utilisateurs* ou *groupes*, ou un ou plusieurs *utilisateurs* existants à partir d’un *groupe*existant.</span><span class="sxs-lookup"><span data-stu-id="71261-104">Deletes one or more existing *users* or *groups*, or removes one or more existing *users* from an existing *group*.</span></span>

## <a name="syntax"></a><span data-ttu-id="71261-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="71261-105">Syntax</span></span>

<span data-ttu-id="71261-106">**Supprimer un ou plusieurs _utilisateurs_ ou supprimer un ou plusieurs _utilisateurs_ d’un _groupe_**:</span><span class="sxs-lookup"><span data-stu-id="71261-106">**Delete one or more _users_ or remove one or more _users_ from a _group_**:</span></span>

<span data-ttu-id="71261-107">DROP USER *utilisateur*\[, *utilisateur*,... \] \[De *groupe*\]</span><span class="sxs-lookup"><span data-stu-id="71261-107">DROP USER *user*\[, *user*, …\] \[FROM *group*\]</span></span>

<span data-ttu-id="71261-108">**Supprimer un ou plusieurs _groupes_**:</span><span class="sxs-lookup"><span data-stu-id="71261-108">**Delete one or more _groups_**:</span></span>

<span data-ttu-id="71261-109">DROP GROUP *groupe*\[, *groupe*,...\]</span><span class="sxs-lookup"><span data-stu-id="71261-109">DROP GROUP *group*\[, *group*, …\]</span></span>

<span data-ttu-id="71261-110">L'instruction DROP USER ou GROUP est composée des arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="71261-110">The DROP USER or GROUP statement has these parts:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="71261-111">Argument</span><span class="sxs-lookup"><span data-stu-id="71261-111">Part</span></span></p></th>
<th><p><span data-ttu-id="71261-112">Description</span><span class="sxs-lookup"><span data-stu-id="71261-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="71261-113"><em>utilisateur</em></span><span class="sxs-lookup"><span data-stu-id="71261-113"><em>user</em></span></span></p></td>
<td><p><span data-ttu-id="71261-114">Nom de l'utilisateur à supprimer du fichier d'informations du groupe de travail.</span><span class="sxs-lookup"><span data-stu-id="71261-114">The name of a user to be removed from the workgroup information file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="71261-115"><em>Groupe</em></span><span class="sxs-lookup"><span data-stu-id="71261-115"><em>group</em></span></span></p></td>
<td><p><span data-ttu-id="71261-116">Nom du groupe à supprimer du fichier d'informations du groupe de travail.</span><span class="sxs-lookup"><span data-stu-id="71261-116">The name of a group to be removed from the workgroup information file.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="71261-117">Notes</span><span class="sxs-lookup"><span data-stu-id="71261-117">Remarks</span></span>

<span data-ttu-id="71261-118">Si le mot clé FROM est utilisé dans l’instruction DROP USER, chacun des *utilisateurs* figurant dans l’instruction sera supprimé du *groupe* spécifié après le mot clé FROM.</span><span class="sxs-lookup"><span data-stu-id="71261-118">If the FROM keyword is used in the DROP USER statement, each of the *users* listed in the statement will be removed from the *group* specified following the FROM keyword.</span></span> <span data-ttu-id="71261-119">Toutefois, les *utilisateurs* eux-mêmes ne seront pas supprimés.</span><span class="sxs-lookup"><span data-stu-id="71261-119">However, the *users* themselves will not be deleted.</span></span>

<span data-ttu-id="71261-120">L’instruction DROP GROUP supprimera spécifié *groupe*(s).</span><span class="sxs-lookup"><span data-stu-id="71261-120">The DROP GROUP statement will delete the specified *group*(s).</span></span> <span data-ttu-id="71261-121">Les *utilisateurs* qui sont membres du *groupe*(s) ne seront pas affectés, mais ils ne seront plus membres supprimés de *groupe (s)*.</span><span class="sxs-lookup"><span data-stu-id="71261-121">The *users* who are members of the *group*(s) will not be affected, but they will no longer be members of the deleted *group*(s).</span></span>

