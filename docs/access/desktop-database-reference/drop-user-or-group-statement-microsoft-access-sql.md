---
title: DROP USER ou GROUP, instruction (Microsoft Access SQL)
TOCTitle: DROP USER or GROUP Statement (Microsoft Access SQL)
ms:assetid: 46bc5916-556b-17df-2f4c-8fd7bbd21ef7
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193192(v=office.15)
ms:contentKeyID: 48544575
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3a5cf75de06c13e2452e5f33b8355b7fb480d8a3
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25469604"
---
# <a name="drop-user-or-group-statement-microsoft-access-sql"></a><span data-ttu-id="ca9ef-102">DROP USER ou GROUP, instruction (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="ca9ef-102">DROP USER or GROUP Statement (Microsoft Access SQL)</span></span>


<span data-ttu-id="ca9ef-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="ca9ef-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="ca9ef-104">Supprime un ou plusieurs *utilisateurs* ou *groupes* existants ou un ou plusieurs *utilisateurs* d'un *groupe* existant.</span><span class="sxs-lookup"><span data-stu-id="ca9ef-104">Deletes one or more existing *user*s or *group*s, or removes one or more existing *user*s from an existing *group*.</span></span>

## <a name="syntax"></a><span data-ttu-id="ca9ef-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ca9ef-105">Syntax</span></span>

<span data-ttu-id="ca9ef-106">Supprimer un ou plusieurs *utilisateurs* ou supprimer un ou plusieurs *utilisateurs* d'un *groupe*:</span><span class="sxs-lookup"><span data-stu-id="ca9ef-106">Delete one or more *user*s or remove one or more *user*s from a *group*:</span></span>

<span data-ttu-id="ca9ef-107">DROP USER *utilisateur*\[, *utilisateur*,... \] \[De *groupe*\]</span><span class="sxs-lookup"><span data-stu-id="ca9ef-107">DROP USER *user*\[, *user*, …\] \[FROM *group*\]</span></span>

<span data-ttu-id="ca9ef-108">Supprimer un ou plusieurs *groupes* :</span><span class="sxs-lookup"><span data-stu-id="ca9ef-108">Delete one or more *group*s:</span></span>

<span data-ttu-id="ca9ef-109">DROP GROUP *groupe*\[, *groupe*,...\]</span><span class="sxs-lookup"><span data-stu-id="ca9ef-109">DROP GROUP *group*\[, *group*, …\]</span></span>

<span data-ttu-id="ca9ef-110">L'instruction DROP USER ou GROUP est composée des arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="ca9ef-110">The DROP USER or GROUP statement has these parts:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ca9ef-111">Argument</span><span class="sxs-lookup"><span data-stu-id="ca9ef-111">Part</span></span></p></th>
<th><p><span data-ttu-id="ca9ef-112">Description</span><span class="sxs-lookup"><span data-stu-id="ca9ef-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ca9ef-113"><em>utilisateur</em></span><span class="sxs-lookup"><span data-stu-id="ca9ef-113"><em>user</em></span></span></p></td>
<td><p><span data-ttu-id="ca9ef-114">Nom de l'utilisateur à supprimer du fichier d'informations du groupe de travail.</span><span class="sxs-lookup"><span data-stu-id="ca9ef-114">The name of a user to be removed from the workgroup information file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ca9ef-115"><em>Groupe</em></span><span class="sxs-lookup"><span data-stu-id="ca9ef-115"><em>group</em></span></span></p></td>
<td><p><span data-ttu-id="ca9ef-116">Nom du groupe à supprimer du fichier d'informations du groupe de travail.</span><span class="sxs-lookup"><span data-stu-id="ca9ef-116">The name of a group to be removed from the workgroup information file.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="ca9ef-117">Notes</span><span class="sxs-lookup"><span data-stu-id="ca9ef-117">Remarks</span></span>

<span data-ttu-id="ca9ef-p101">Si le mot clé FROM est utilisé dans l'instruction DROP USER, alors chacun des *utilisateurs* indiqué dans l'instruction est supprimé du *groupe* spécifié à la suite du mot clé FROM. En revanche, les *utilisateurs* eux-mêmes ne sont pas supprimés.</span><span class="sxs-lookup"><span data-stu-id="ca9ef-p101">If the FROM keyword is used in the DROP USER statement, then each of the *user*s listed in the statement will be removed from the *group* specified following the FROM keyword. However, the *user*s themselves will not be deleted.</span></span>

<span data-ttu-id="ca9ef-p102">L'instruction DROP GROUP supprime les *groupes* spécifiés. Les *utilisateurs* qui sont membres des *groupes* ne sont pas supprimés, mais ils ne sont plus membres des *groupes* supprimés.</span><span class="sxs-lookup"><span data-stu-id="ca9ef-p102">The DROP GROUP statement will delete the specified *group*(s). The *user*s who are members of the *group*(s) will not be affected, but they will no longer be members of the deleted *group*(s).</span></span>

