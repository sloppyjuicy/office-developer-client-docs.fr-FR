---
title: Instruction ADD USER (Microsoft Access SQL)
TOCTitle: ADD USER statement (Microsoft Access SQL)
ms:assetid: 1feb631f-cb8c-14ae-6214-276f1faf1a55
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845862(v=office.15)
ms:contentKeyID: 48543652
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: 80e3a8fe62cf077accfc18a30e188898fb279d1d
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25862288"
---
# <a name="add-user-statement-microsoft-access-sql"></a><span data-ttu-id="ed010-102">Instruction ADD USER (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="ed010-102">ADD USER statement (Microsoft Access SQL)</span></span>

<span data-ttu-id="ed010-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="ed010-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="ed010-104">Ajoute un ou plusieurs *utilisateurs* existants à un *groupe* existant.</span><span class="sxs-lookup"><span data-stu-id="ed010-104">Adds one or more existing *user*s to an existing *group*.</span></span>

## <a name="syntax"></a><span data-ttu-id="ed010-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ed010-105">Syntax</span></span>

<span data-ttu-id="ed010-106">Ajouter un utilisateur *utilisateur*\[, *utilisateur*,... \] Au *groupe*</span><span class="sxs-lookup"><span data-stu-id="ed010-106">ADD USER *user*\[, *user*, …\] TO *group*</span></span>

<span data-ttu-id="ed010-107">L'instruction ADD USER comporte trois parties :</span><span class="sxs-lookup"><span data-stu-id="ed010-107">The ADD USER statement has these parts:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ed010-108">Argument</span><span class="sxs-lookup"><span data-stu-id="ed010-108">Part</span></span></p></th>
<th><p><span data-ttu-id="ed010-109">Description</span><span class="sxs-lookup"><span data-stu-id="ed010-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ed010-110"><em>utilisateur</em></span><span class="sxs-lookup"><span data-stu-id="ed010-110"><em>user</em></span></span></p></td>
<td><p><span data-ttu-id="ed010-111">Nom de l'utilisateur à ajouter au fichier d'informations du groupe de travail.</span><span class="sxs-lookup"><span data-stu-id="ed010-111">The name of a user to be added to the workgroup information file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ed010-112"><em>Groupe</em></span><span class="sxs-lookup"><span data-stu-id="ed010-112"><em>group</em></span></span></p></td>
<td><p><span data-ttu-id="ed010-113">Nom du groupe à ajouter au fichier d'informations du groupe de travail.</span><span class="sxs-lookup"><span data-stu-id="ed010-113">The name of a group to be added to the workgroup information file.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="ed010-114">Notes</span><span class="sxs-lookup"><span data-stu-id="ed010-114">Remarks</span></span>

<span data-ttu-id="ed010-115">Une fois un *utilisateur* a été ajouté à un *groupe*, l' *utilisateur* dispose des autorisations qui ont été accordées au *groupe*.</span><span class="sxs-lookup"><span data-stu-id="ed010-115">After a *user* had been added to a *group*, the *user* has all the permissions that have been granted to the *group*.</span></span>

