---
title: ADD USER, instruction (Microsoft Access SQL)
TOCTitle: ADD USER statement (Microsoft Access SQL)
ms:assetid: 1feb631f-cb8c-14ae-6214-276f1faf1a55
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845862(v=office.15)
ms:contentKeyID: 48543652
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 8ba60a646fd234748bcc39b9a5604a33675caee5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32280424"
---
# <a name="add-user-statement-microsoft-access-sql"></a><span data-ttu-id="bb237-102">ADD USER, instruction (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="bb237-102">ADD USER statement (Microsoft Access SQL)</span></span>

<span data-ttu-id="bb237-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="bb237-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="bb237-104">Ajoute un ou plusieurs *utilisateurs* existants à un *groupe* existant.</span><span class="sxs-lookup"><span data-stu-id="bb237-104">Adds one or more existing *user*s to an existing *group*.</span></span>

## <a name="syntax"></a><span data-ttu-id="bb237-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="bb237-105">Syntax</span></span>

<span data-ttu-id="bb237-106">Ajouter un \*\*\[utilisateur utilisateur, *utilisateur*,... \] Pour *Grouper*</span><span class="sxs-lookup"><span data-stu-id="bb237-106">ADD USER *user*\[, *user*, …\] TO *group*</span></span>

<span data-ttu-id="bb237-107">L'instruction ADD USER comporte trois parties :</span><span class="sxs-lookup"><span data-stu-id="bb237-107">The ADD USER statement has these parts:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="bb237-108">Élément</span><span class="sxs-lookup"><span data-stu-id="bb237-108">Part</span></span></p></th>
<th><p><span data-ttu-id="bb237-109">Description</span><span class="sxs-lookup"><span data-stu-id="bb237-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bb237-110"><em>utilisateur</em></span><span class="sxs-lookup"><span data-stu-id="bb237-110"><em>user</em></span></span></p></td>
<td><p><span data-ttu-id="bb237-111">Nom de l'utilisateur à ajouter au fichier d'informations du groupe de travail.</span><span class="sxs-lookup"><span data-stu-id="bb237-111">The name of a user to be added to the workgroup information file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bb237-112"><em>groupe</em></span><span class="sxs-lookup"><span data-stu-id="bb237-112"><em>group</em></span></span></p></td>
<td><p><span data-ttu-id="bb237-113">Nom du groupe à ajouter au fichier d'informations du groupe de travail.</span><span class="sxs-lookup"><span data-stu-id="bb237-113">The name of a group to be added to the workgroup information file.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="bb237-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="bb237-114">Remarks</span></span>

<span data-ttu-id="bb237-115">Une fois qu'un *utilisateur* a été ajouté à un *groupe*, il dispose de toutes les autorisations qui ont été accordées au *groupe*. \*\*</span><span class="sxs-lookup"><span data-stu-id="bb237-115">After a *user* had been added to a *group*, the *user* has all the permissions that have been granted to the *group*.</span></span>

