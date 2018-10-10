---
title: Workspaces.Append Method (DAO)
TOCTitle: Append Method
ms:assetid: 195c26a6-a1d1-40a8-7e7e-13cd632008b6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845644(v=office.15)
ms:contentKeyID: 48543498
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b2724a08b08f05af31fd4693eec2f28b0d2607bb
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25472211"
---
# <a name="workspacesappend-method-dao"></a><span data-ttu-id="a3acc-102">Workspaces.Append Method (DAO)</span><span class="sxs-lookup"><span data-stu-id="a3acc-102">Workspaces.Append Method (DAO)</span></span>


<span data-ttu-id="a3acc-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="a3acc-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="a3acc-104">Ajoute un nouvel objet **Workspace** à la collection **Workspaces**.</span><span class="sxs-lookup"><span data-stu-id="a3acc-104">Adds a new **Workspace** to the **Workspaces** collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="a3acc-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a3acc-105">Syntax</span></span>

<span data-ttu-id="a3acc-106">*expression* . Append (***objet***)</span><span class="sxs-lookup"><span data-stu-id="a3acc-106">*expression* .Append(***Object***)</span></span>

<span data-ttu-id="a3acc-107">*expression* Variable qui représente un objet **espaces de travail** .</span><span class="sxs-lookup"><span data-stu-id="a3acc-107">*expression* A variable that represents a **Workspaces** object.</span></span>

### <a name="parameters"></a><span data-ttu-id="a3acc-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a3acc-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a3acc-109">Name</span><span class="sxs-lookup"><span data-stu-id="a3acc-109">Name</span></span></p></th>
<th><p><span data-ttu-id="a3acc-110">Obligatoire/Facultatif</span><span class="sxs-lookup"><span data-stu-id="a3acc-110">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="a3acc-111">Type de données</span><span class="sxs-lookup"><span data-stu-id="a3acc-111">Data Type</span></span></p></th>
<th><p><span data-ttu-id="a3acc-112">Description</span><span class="sxs-lookup"><span data-stu-id="a3acc-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a3acc-113">Objet</span><span class="sxs-lookup"><span data-stu-id="a3acc-113">Object</span></span></p></td>
<td><p><span data-ttu-id="a3acc-114">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="a3acc-114">Required</span></span></p></td>
<td><p><span data-ttu-id="a3acc-115"><strong>Object</strong></span><span class="sxs-lookup"><span data-stu-id="a3acc-115"><strong>Object</strong></span></span></p></td>
<td><p><span data-ttu-id="a3acc-116">Variable d'objet représentant le champ qui est ajouté à la collection.</span><span class="sxs-lookup"><span data-stu-id="a3acc-116">An object variable that represents the field being appended to the collection.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="a3acc-117">Remarques</span><span class="sxs-lookup"><span data-stu-id="a3acc-117">Remarks</span></span>

<span data-ttu-id="a3acc-118">L'objet ajouté devient un objet persistant, stocké sur le disque, tant que vous ne le supprimez pas à l'aide de la méthode **Delete**.</span><span class="sxs-lookup"><span data-stu-id="a3acc-118">The appended object becomes a persistent object, stored on disk, until you delete it by using the **Delete** method.</span></span>

<span data-ttu-id="a3acc-119">L'ajout d'un nouvel objet a lieu immédiatement, mais vous devez utiliser la méthode **Refresh** dans toutes les autres collections qui peuvent être affectées par les modifications apportées à la structure de la base de données.</span><span class="sxs-lookup"><span data-stu-id="a3acc-119">The addition of a new object occurs immediately, but you should use the **Refresh** method on any other collections that may be affected by changes to the database structure.</span></span>

<span data-ttu-id="a3acc-120">Si l'objet que vous ajoutez n'est pas complet (par exemple, si vous n'avez pas ajouté d'objets **Field** à une collection **Fields** d'un objet **Index** avant qu'il soit ajouté à une collection **Indexes**) ou si les propriétés définies dans un ou plusieurs objets subordonnés sont incorrectes, l'utilisation de la méthode **Append** entraîne une erreur.</span><span class="sxs-lookup"><span data-stu-id="a3acc-120">If the object you're appending isn't complete (such as when you haven't appended any **Field** objects to a **Fields** collection of an **Index** object before it's appended to an **Indexes** collection) or if the properties set in one or more subordinate objects are incorrect, using the **Append** method causes an error.</span></span> <span data-ttu-id="a3acc-121">Par exemple, si vous n’avez pas spécifié un type de champ, puis essayez d’ajouter l’objet **Field** à la collection **Fields** d’un objet **TableDef** , à l’aide de la méthode **Append** déclenche une erreur d’exécution.</span><span class="sxs-lookup"><span data-stu-id="a3acc-121">For example, if you haven’t specified a field type and then try to append the **Field** object to the **Fields** collection in a **TableDef** object, using the **Append** method triggers a run-time error.</span></span>

