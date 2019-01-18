---
title: Instruction CREATE USER ou GROUP (Microsoft Access SQL)
TOCTitle: CREATE USER or GROUP statement (Microsoft Access SQL)
ms:assetid: 62148ce2-0f81-944e-a1ab-edef990fff9f
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194914(v=office.15)
ms:contentKeyID: 48545229
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 5b294af16498778eae94b38a7a31b93fd029585e
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28710922"
---
# <a name="create-user-or-group-statement-microsoft-access-sql"></a><span data-ttu-id="dafef-102">Instruction CREATE USER ou GROUP (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="dafef-102">CREATE USER or GROUP statement (Microsoft Access SQL)</span></span>

<span data-ttu-id="dafef-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="dafef-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="dafef-104">Crée un ou plusieurs nouveaux utilisateurs ou groupes.</span><span class="sxs-lookup"><span data-stu-id="dafef-104">Creates one or more new users or groups.</span></span>

## <a name="syntax"></a><span data-ttu-id="dafef-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="dafef-105">Syntax</span></span>

### <a name="create-a-user"></a><span data-ttu-id="dafef-106">Créer un utilisateur</span><span class="sxs-lookup"><span data-stu-id="dafef-106">Create a user</span></span>

<span data-ttu-id="dafef-107">CREATE USER *utilisateur* *le mot de passe identifiant personnel* \[, *utilisateur* *le mot de passe identifiant personnel*,...\]</span><span class="sxs-lookup"><span data-stu-id="dafef-107">CREATE USER *user* *password pid* \[, *user* *password pid*, …\]</span></span>

### <a name="create-a-group"></a><span data-ttu-id="dafef-108">Créer un groupe</span><span class="sxs-lookup"><span data-stu-id="dafef-108">Create a group</span></span>

<span data-ttu-id="dafef-109">CREATE GROUP *groupe* *identifiant personnel*\[, *groupe* *identifiant personnel*,...\]</span><span class="sxs-lookup"><span data-stu-id="dafef-109">CREATE GROUP *group* *pid*\[, *group* *pid*, …\]</span></span>

<span data-ttu-id="dafef-110">L'instruction CREATE USER ou GROUP est composée des arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="dafef-110">The CREATE USER or GROUP statement has these parts:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="dafef-111">Argument</span><span class="sxs-lookup"><span data-stu-id="dafef-111">Part</span></span></p></th>
<th><p><span data-ttu-id="dafef-112">Description</span><span class="sxs-lookup"><span data-stu-id="dafef-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="dafef-113"><em>utilisateur</em></span><span class="sxs-lookup"><span data-stu-id="dafef-113"><em>user</em></span></span></p></td>
<td><p><span data-ttu-id="dafef-114">Nom de l'utilisateur à ajouter au fichier d'informations du groupe de travail.</span><span class="sxs-lookup"><span data-stu-id="dafef-114">The name of a user to be added to the workgroup information file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dafef-115"><em>Groupe</em></span><span class="sxs-lookup"><span data-stu-id="dafef-115"><em>group</em></span></span></p></td>
<td><p><span data-ttu-id="dafef-116">Nom du groupe à ajouter au fichier d'informations du groupe de travail.</span><span class="sxs-lookup"><span data-stu-id="dafef-116">The name of a group to be added to the workgroup information file.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dafef-117"><em>mot de passe </em></span><span class="sxs-lookup"><span data-stu-id="dafef-117"><em>password</em></span></span></p></td>
<td><p><span data-ttu-id="dafef-118">Mot de passe à associer au nom de l'<em>utilisateur</em> spécifié.</span><span class="sxs-lookup"><span data-stu-id="dafef-118">The password to be associated with the specified <em>user</em> name.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dafef-119"><em>identifiant personnel</em></span><span class="sxs-lookup"><span data-stu-id="dafef-119"><em>pid</em></span></span></p></td>
<td><p><span data-ttu-id="dafef-120">Identifiant personnel.</span><span class="sxs-lookup"><span data-stu-id="dafef-120">The personal id.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="dafef-121">Notes</span><span class="sxs-lookup"><span data-stu-id="dafef-121">Remarks</span></span>

<span data-ttu-id="dafef-122">Un *utilisateur* et un *groupe* ne peut pas avoir le même nom.</span><span class="sxs-lookup"><span data-stu-id="dafef-122">A *user* and a *group* cannot have the same name.</span></span>

<span data-ttu-id="dafef-123">Un *mot de passe* est requis pour chaque *utilisateur* ou le *groupe* qui est créé.</span><span class="sxs-lookup"><span data-stu-id="dafef-123">A *password* is required for each *user* or *group* that is created.</span></span>

