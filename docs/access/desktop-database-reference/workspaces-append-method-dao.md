---
title: Workspaces.Append, méthode (DAO)
TOCTitle: Append Method
ms:assetid: 195c26a6-a1d1-40a8-7e7e-13cd632008b6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845644(v=office.15)
ms:contentKeyID: 48543498
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 11d721d58301d2adb33b2e381d88d7245531ff06
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32302491"
---
# <a name="workspacesappend-method-dao"></a><span data-ttu-id="05953-102">Workspaces.Append, méthode (DAO)</span><span class="sxs-lookup"><span data-stu-id="05953-102">Workspaces.Append method (DAO)</span></span>

<span data-ttu-id="05953-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="05953-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="05953-104">Ajoute un nouvel objet **Workspace** à la collection **Workspaces**.</span><span class="sxs-lookup"><span data-stu-id="05953-104">Adds a new **Workspace** to the **Workspaces** collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="05953-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="05953-105">Syntax</span></span>

<span data-ttu-id="05953-106">*expression* .Append(***Object***)</span><span class="sxs-lookup"><span data-stu-id="05953-106">*expression* .Append(***Object***)</span></span>

<span data-ttu-id="05953-107">*expression* Variable qui représente un **objet Workspaces.**</span><span class="sxs-lookup"><span data-stu-id="05953-107">*expression* A variable that represents a **Workspaces** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="05953-108">Parameters</span><span class="sxs-lookup"><span data-stu-id="05953-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="05953-109">Nom</span><span class="sxs-lookup"><span data-stu-id="05953-109">Name</span></span></p></th>
<th><p><span data-ttu-id="05953-110">Obligatoire/facultatif</span><span class="sxs-lookup"><span data-stu-id="05953-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="05953-111">Type de données</span><span class="sxs-lookup"><span data-stu-id="05953-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="05953-112">Description</span><span class="sxs-lookup"><span data-stu-id="05953-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="05953-113"><em>Object</em></span><span class="sxs-lookup"><span data-stu-id="05953-113"><em>Object</em></span></span></p></td>
<td><p><span data-ttu-id="05953-114">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="05953-114">Required</span></span></p></td>
<td><p><span data-ttu-id="05953-115"><strong>Object</strong></span><span class="sxs-lookup"><span data-stu-id="05953-115"><strong>Object</strong></span></span></p></td>
<td><p><span data-ttu-id="05953-116">Variable d'objet représentant le champ qui est ajouté à la collection.</span><span class="sxs-lookup"><span data-stu-id="05953-116">An object variable that represents the field being appended to the collection.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="05953-117">Remarques</span><span class="sxs-lookup"><span data-stu-id="05953-117">Remarks</span></span>

<span data-ttu-id="05953-118">L'objet ajouté devient un objet persistant, stocké sur le disque, tant que vous ne le supprimez pas à l'aide de la méthode **Delete**.</span><span class="sxs-lookup"><span data-stu-id="05953-118">The appended object becomes a persistent object, stored on disk, until you delete it by using the **Delete** method.</span></span>

<span data-ttu-id="05953-119">L'ajout d'un nouvel objet a lieu immédiatement, mais vous devez utiliser la méthode **Refresh** dans toutes les autres collections qui peuvent être affectées par les modifications apportées à la structure de la base de données.</span><span class="sxs-lookup"><span data-stu-id="05953-119">The addition of a new object occurs immediately, but you should use the **Refresh** method on any other collections that may be affected by changes to the database structure.</span></span>

<span data-ttu-id="05953-120">Si l'objet que vous ajoutez n'est pas complet (par exemple, si vous n'avez pas ajouté d'objets **Field** à une collection **Fields** d'un objet **Index** avant qu'il soit ajouté à une collection **Indexes**) ou si les propriétés définies dans un ou plusieurs objets subordonnés sont incorrectes, l'utilisation de la méthode **Append** entraîne une erreur.</span><span class="sxs-lookup"><span data-stu-id="05953-120">If the object you're appending isn't complete (such as when you haven't appended any **Field** objects to a **Fields** collection of an **Index** object before it's appended to an **Indexes** collection) or if the properties set in one or more subordinate objects are incorrect, using the **Append** method causes an error.</span></span> <span data-ttu-id="05953-121">Par exemple, si vous n'avez pas spécifié un type de champ et que vous tentez d'ajouter l'objet **Field** à la collection **Fields** dans un objet **TableDef** à l'aide de la méthode **Append**, une erreur d'exécution est générée.</span><span class="sxs-lookup"><span data-stu-id="05953-121">For example, if you haven’t specified a field type and then try to append the **Field** object to the **Fields** collection in a **TableDef** object, using the **Append** method triggers a run-time error.</span></span>

