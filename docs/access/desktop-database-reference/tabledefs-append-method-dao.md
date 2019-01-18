---
title: Méthode TableDefs.Append (DAO)
TOCTitle: Append Method
ms:assetid: f951a3c4-dade-c1ef-3bfc-6b2a60e12adc
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837001(v=office.15)
ms:contentKeyID: 48548811
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 31eca3f4ca5993a401bd85a4b04299a8697c16e2
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28702788"
---
# <a name="tabledefsappend-method-dao"></a><span data-ttu-id="7dcb3-102">Méthode TableDefs.Append (DAO)</span><span class="sxs-lookup"><span data-stu-id="7dcb3-102">TableDefs.Append method (DAO)</span></span>

<span data-ttu-id="7dcb3-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="7dcb3-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="7dcb3-104">Ajoute un nouvel objet **TableDef** à la collection **TableDefs**.</span><span class="sxs-lookup"><span data-stu-id="7dcb3-104">Adds a new **TableDef** to the **TableDefs** collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="7dcb3-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7dcb3-105">Syntax</span></span>

<span data-ttu-id="7dcb3-106">*expression* . Append (***objet***)</span><span class="sxs-lookup"><span data-stu-id="7dcb3-106">*expression* .Append(***Object***)</span></span>

<span data-ttu-id="7dcb3-107">*expression* Variable qui représente un objet **TableDef** .</span><span class="sxs-lookup"><span data-stu-id="7dcb3-107">*expression* A variable that represents a **TableDefs** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="7dcb3-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7dcb3-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="7dcb3-109">Nom</span><span class="sxs-lookup"><span data-stu-id="7dcb3-109">Name</span></span></p></th>
<th><p><span data-ttu-id="7dcb3-110">Requis/facultatif</span><span class="sxs-lookup"><span data-stu-id="7dcb3-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="7dcb3-111">Type de données</span><span class="sxs-lookup"><span data-stu-id="7dcb3-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="7dcb3-112">Description</span><span class="sxs-lookup"><span data-stu-id="7dcb3-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7dcb3-113"><em>Object</em></span><span class="sxs-lookup"><span data-stu-id="7dcb3-113"><em>Object</em></span></span></p></td>
<td><p><span data-ttu-id="7dcb3-114">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="7dcb3-114">Required</span></span></p></td>
<td><p><span data-ttu-id="7dcb3-115"><strong>Object</strong></span><span class="sxs-lookup"><span data-stu-id="7dcb3-115"><strong>Object</strong></span></span></p></td>
<td><p><span data-ttu-id="7dcb3-116">Variable d'objet représentant le champ qui est ajouté à la collection.</span><span class="sxs-lookup"><span data-stu-id="7dcb3-116">An object variable that represents the field being appended to the collection.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="7dcb3-117">Remarques</span><span class="sxs-lookup"><span data-stu-id="7dcb3-117">Remarks</span></span>

<span data-ttu-id="7dcb3-118">L'objet ajouté devient un objet persistant, stocké sur le disque, tant que vous ne le supprimez pas à l'aide de la méthode **Delete**.</span><span class="sxs-lookup"><span data-stu-id="7dcb3-118">The appended object becomes a persistent object, stored on disk, until you delete it by using the **Delete** method.</span></span>

<span data-ttu-id="7dcb3-119">L'ajout d'un nouvel objet a lieu immédiatement, mais vous devez utiliser la méthode **Refresh** dans toutes les autres collections qui peuvent être affectées par les modifications apportées à la structure de la base de données.</span><span class="sxs-lookup"><span data-stu-id="7dcb3-119">The addition of a new object occurs immediately, but you should use the **Refresh** method on any other collections that may be affected by changes to the database structure.</span></span>

<span data-ttu-id="7dcb3-120">Si l'objet que vous ajoutez n'est pas complet (par exemple, si vous n'avez pas ajouté d'objets **Field** à une collection **Fields** d'un objet **Index** avant qu'il soit ajouté à une collection **Indexes**) ou si les propriétés définies dans un ou plusieurs objets subordonnés sont incorrectes, l'utilisation de la méthode **Append** entraîne une erreur.</span><span class="sxs-lookup"><span data-stu-id="7dcb3-120">If the object you're appending isn't complete (such as when you haven't appended any **Field** objects to a **Fields** collection of an **Index** object before it's appended to an **Indexes** collection) or if the properties set in one or more subordinate objects are incorrect, using the **Append** method causes an error.</span></span> <span data-ttu-id="7dcb3-121">Par exemple, si vous n’avez pas spécifié un type de champ, puis essayez d’ajouter l’objet **Field** à la collection **Fields** d’un objet **TableDef** , à l’aide de la méthode **Append** déclenche une erreur d’exécution.</span><span class="sxs-lookup"><span data-stu-id="7dcb3-121">For example, if you haven’t specified a field type and then try to append the **Field** object to the **Fields** collection in a **TableDef** object, using the **Append** method triggers a run-time error.</span></span>

