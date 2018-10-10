---
title: ADD USER, instruction (Microsoft Access SQL)
TOCTitle: ADD USER Statement (Microsoft Access SQL)
ms:assetid: 1feb631f-cb8c-14ae-6214-276f1faf1a55
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845862(v=office.15)
ms:contentKeyID: 48543652
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ba08ab3104fa08780e8affa310b52a65f67d8831
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25470883"
---
# <a name="add-user-statement-microsoft-access-sql"></a><span data-ttu-id="08de4-102">ADD USER, instruction (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="08de4-102">ADD USER Statement (Microsoft Access SQL)</span></span>

<span data-ttu-id="08de4-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="08de4-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="08de4-104">Ajoute un ou plusieurs *utilisateurs* existants à un *groupe* existant.</span><span class="sxs-lookup"><span data-stu-id="08de4-104">Adds one or more existing *user*s to an existing *group*.</span></span>

## <a name="syntax"></a><span data-ttu-id="08de4-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="08de4-105">Syntax</span></span>

<span data-ttu-id="08de4-106">Ajouter un utilisateur *utilisateur*\[, *utilisateur*,... \] Au *groupe*</span><span class="sxs-lookup"><span data-stu-id="08de4-106">ADD USER *user*\[, *user*, …\] TO *group*</span></span>

<span data-ttu-id="08de4-107">L'instruction ADD USER comporte trois parties :</span><span class="sxs-lookup"><span data-stu-id="08de4-107">The ADD USER statement has these parts:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="08de4-108">Argument</span><span class="sxs-lookup"><span data-stu-id="08de4-108">Part</span></span></p></th>
<th><p><span data-ttu-id="08de4-109">Description</span><span class="sxs-lookup"><span data-stu-id="08de4-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="08de4-110"><em>utilisateur</em></span><span class="sxs-lookup"><span data-stu-id="08de4-110"><em>user</em></span></span></p></td>
<td><p><span data-ttu-id="08de4-111">Nom de l'utilisateur à ajouter au fichier d'informations du groupe de travail.</span><span class="sxs-lookup"><span data-stu-id="08de4-111">The name of a user to be added to the workgroup information file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="08de4-112"><em>Groupe</em></span><span class="sxs-lookup"><span data-stu-id="08de4-112"><em>group</em></span></span></p></td>
<td><p><span data-ttu-id="08de4-113">Nom du groupe à ajouter au fichier d'informations du groupe de travail.</span><span class="sxs-lookup"><span data-stu-id="08de4-113">The name of a group to be added to the workgroup information file.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="08de4-114">Notes</span><span class="sxs-lookup"><span data-stu-id="08de4-114">Remarks</span></span>

<span data-ttu-id="08de4-115">Une fois qu’un *utilisateur* a été ajouté à un *groupe,* l' *utilisateur* dispose des autorisations qui ont été accordées au *groupe*.</span><span class="sxs-lookup"><span data-stu-id="08de4-115">Once a *user* had been added to a *group,* the *user* has all the permissions that have been granted to the *group*.</span></span>

