---
title: Instruction CREATE USER ou GROUP (Microsoft Access SQL)
TOCTitle: CREATE USER or GROUP statement (Microsoft Access SQL)
ms:assetid: 62148ce2-0f81-944e-a1ab-edef990fff9f
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194914(v=office.15)
ms:contentKeyID: 48545229
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: 52d376b05c195ed0ea4707e849c5ae395c2b5590
ms.sourcegitcommit: 38d0db57580cc5f4a0231c27b1643f8db5431ca3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25936825"
---
# <a name="create-user-or-group-statement-microsoft-access-sql"></a><span data-ttu-id="f81fa-102">Instruction CREATE USER ou GROUP (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="f81fa-102">CREATE USER or GROUP statement (Microsoft Access SQL)</span></span>

<span data-ttu-id="f81fa-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="f81fa-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="f81fa-104">Crée un ou plusieurs nouveaux utilisateurs ou groupes.</span><span class="sxs-lookup"><span data-stu-id="f81fa-104">Creates one or more new users or groups.</span></span>

## <a name="syntax"></a><span data-ttu-id="f81fa-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f81fa-105">Syntax</span></span>

### <a name="create-a-user"></a><span data-ttu-id="f81fa-106">Créer un utilisateur</span><span class="sxs-lookup"><span data-stu-id="f81fa-106">Create a user</span></span>

<span data-ttu-id="f81fa-107">CREATE USER *utilisateur* *le mot de passe identifiant personnel* \[, *utilisateur* *le mot de passe identifiant personnel*,...\]</span><span class="sxs-lookup"><span data-stu-id="f81fa-107">CREATE USER *user* *password pid* \[, *user* *password pid*, …\]</span></span>

### <a name="create-a-group"></a><span data-ttu-id="f81fa-108">Créer un groupe</span><span class="sxs-lookup"><span data-stu-id="f81fa-108">Create a group</span></span>

<span data-ttu-id="f81fa-109">CREATE GROUP *groupe* *identifiant personnel*\[, *groupe* *identifiant personnel*,...\]</span><span class="sxs-lookup"><span data-stu-id="f81fa-109">CREATE GROUP *group* *pid*\[, *group* *pid*, …\]</span></span>

<span data-ttu-id="f81fa-110">L'instruction CREATE USER ou GROUP est composée des arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="f81fa-110">The CREATE USER or GROUP statement has these parts:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f81fa-111">Argument</span><span class="sxs-lookup"><span data-stu-id="f81fa-111">Part</span></span></p></th>
<th><p><span data-ttu-id="f81fa-112">Description</span><span class="sxs-lookup"><span data-stu-id="f81fa-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f81fa-113"><em>utilisateur</em></span><span class="sxs-lookup"><span data-stu-id="f81fa-113"><em>user</em></span></span></p></td>
<td><p><span data-ttu-id="f81fa-114">Nom de l'utilisateur à ajouter au fichier d'informations du groupe de travail.</span><span class="sxs-lookup"><span data-stu-id="f81fa-114">The name of a user to be added to the workgroup information file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f81fa-115"><em>Groupe</em></span><span class="sxs-lookup"><span data-stu-id="f81fa-115"><em>group</em></span></span></p></td>
<td><p><span data-ttu-id="f81fa-116">Nom du groupe à ajouter au fichier d'informations du groupe de travail.</span><span class="sxs-lookup"><span data-stu-id="f81fa-116">The name of a group to be added to the workgroup information file.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f81fa-117"><em>mot de passe </em></span><span class="sxs-lookup"><span data-stu-id="f81fa-117"><em>password</em></span></span></p></td>
<td><p><span data-ttu-id="f81fa-118">Mot de passe à associer au nom de l'<em>utilisateur</em> spécifié.</span><span class="sxs-lookup"><span data-stu-id="f81fa-118">The password to be associated with the specified <em>user</em> name.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f81fa-119"><em>identifiant personnel</em></span><span class="sxs-lookup"><span data-stu-id="f81fa-119"><em>pid</em></span></span></p></td>
<td><p><span data-ttu-id="f81fa-120">Identifiant personnel.</span><span class="sxs-lookup"><span data-stu-id="f81fa-120">The personal id.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="f81fa-121">Notes</span><span class="sxs-lookup"><span data-stu-id="f81fa-121">Remarks</span></span>

<span data-ttu-id="f81fa-122">Un *utilisateur* et un *groupe* ne peut pas avoir le même nom.</span><span class="sxs-lookup"><span data-stu-id="f81fa-122">A *user* and a *group* cannot have the same name.</span></span>

<span data-ttu-id="f81fa-123">Un *mot de passe* est requis pour chaque *utilisateur* ou le *groupe* qui est créé.</span><span class="sxs-lookup"><span data-stu-id="f81fa-123">A *password* is required for each *user* or *group* that is created.</span></span>

