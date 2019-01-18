---
title: Méthode Relations.Append (DAO)
TOCTitle: Append Method
ms:assetid: dafcc7b8-b30d-2ba2-631d-eca0f882fc2d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835334(v=office.15)
ms:contentKeyID: 48548094
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052904
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: b8374832ad6cd6bac30fa9d129e54fb6ab4c8fd4
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28718846"
---
# <a name="relationsappend-method-dao"></a><span data-ttu-id="47b32-102">Méthode Relations.Append (DAO)</span><span class="sxs-lookup"><span data-stu-id="47b32-102">Relations.Append method (DAO)</span></span>

<span data-ttu-id="47b32-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="47b32-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="47b32-104">Ajoute un nouvel objet **Relation** à la collection **Relations**.</span><span class="sxs-lookup"><span data-stu-id="47b32-104">Adds a new **Relation** to the **Relations** collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="47b32-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="47b32-105">Syntax</span></span>

<span data-ttu-id="47b32-106">*expression* . Append (***objet***)</span><span class="sxs-lookup"><span data-stu-id="47b32-106">*expression* .Append(***Object***)</span></span>

<span data-ttu-id="47b32-107">*expression* Variable qui représente un objet **Relations** .</span><span class="sxs-lookup"><span data-stu-id="47b32-107">*expression* A variable that represents a **Relations** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="47b32-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="47b32-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="47b32-109">Nom</span><span class="sxs-lookup"><span data-stu-id="47b32-109">Name</span></span></p></th>
<th><p><span data-ttu-id="47b32-110">Requis/facultatif</span><span class="sxs-lookup"><span data-stu-id="47b32-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="47b32-111">Type de données</span><span class="sxs-lookup"><span data-stu-id="47b32-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="47b32-112">Description</span><span class="sxs-lookup"><span data-stu-id="47b32-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="47b32-113"><em>Object</em></span><span class="sxs-lookup"><span data-stu-id="47b32-113"><em>Object</em></span></span></p></td>
<td><p><span data-ttu-id="47b32-114">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="47b32-114">Required</span></span></p></td>
<td><p><span data-ttu-id="47b32-115"><strong>Object</strong></span><span class="sxs-lookup"><span data-stu-id="47b32-115"><strong>Object</strong></span></span></p></td>
<td><p><span data-ttu-id="47b32-116">Variable d'objet représentant le champ qui est ajouté à la collection.</span><span class="sxs-lookup"><span data-stu-id="47b32-116">An object variable that represents the field being appended to the collection.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="47b32-117">Remarques</span><span class="sxs-lookup"><span data-stu-id="47b32-117">Remarks</span></span>

<span data-ttu-id="47b32-118">L'objet ajouté devient un objet persistant, stocké sur le disque, tant que vous ne le supprimez pas à l'aide de la méthode **Delete**.</span><span class="sxs-lookup"><span data-stu-id="47b32-118">The appended object becomes a persistent object, stored on disk, until you delete it by using the **Delete** method.</span></span>

<span data-ttu-id="47b32-119">L'ajout d'un nouvel objet a lieu immédiatement, mais vous devez utiliser la méthode **Refresh** dans toutes les autres collections qui peuvent être affectées par les modifications apportées à la structure de la base de données.</span><span class="sxs-lookup"><span data-stu-id="47b32-119">The addition of a new object occurs immediately, but you should use the **Refresh** method on any other collections that may be affected by changes to the database structure.</span></span>

<span data-ttu-id="47b32-120">Si l'objet que vous ajoutez n'est pas complet (par exemple, si vous n'avez pas ajouté d'objets **Field** à une collection **Fields** d'un objet **Index** avant qu'il soit ajouté à une collection **Indexes**) ou si les propriétés définies dans un ou plusieurs objets subordonnés sont incorrectes, l'utilisation de la méthode **Append** entraîne une erreur.</span><span class="sxs-lookup"><span data-stu-id="47b32-120">If the object you're appending isn't complete (such as when you haven't appended any **Field** objects to a **Fields** collection of an **Index** object before it's appended to an **Indexes** collection) or if the properties set in one or more subordinate objects are incorrect, using the **Append** method causes an error.</span></span> <span data-ttu-id="47b32-121">Par exemple, si vous n’avez pas spécifié un type de champ, puis essayez d’ajouter l’objet **Field** à la collection **Fields** d’un objet **TableDef** , à l’aide de la méthode **Append** déclenche une erreur d’exécution.</span><span class="sxs-lookup"><span data-stu-id="47b32-121">For example, if you haven’t specified a field type and then try to append the **Field** object to the **Fields** collection in a **TableDef** object, using the **Append** method triggers a run-time error.</span></span>

