---
title: Indexes.Delete Method (DAO)
TOCTitle: Delete Method
ms:assetid: 8d3c3221-3b2e-15ba-32ff-f2dfc592d82c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197351(v=office.15)
ms:contentKeyID: 48546252
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 5b863780208e6ea59e7c518bcb09cb20f38d30a6
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25887130"
---
# <a name="indexesdelete-method-dao"></a><span data-ttu-id="ef89b-102">Indexes.Delete Method (DAO)</span><span class="sxs-lookup"><span data-stu-id="ef89b-102">Indexes.Delete Method (DAO)</span></span>


<span data-ttu-id="ef89b-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="ef89b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="ef89b-104">Supprime l'objet **Index** spécifié de la collection **Indexes**.</span><span class="sxs-lookup"><span data-stu-id="ef89b-104">Deletes the specified **Index** from the **Indexes** collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="ef89b-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ef89b-105">Syntax</span></span>

<span data-ttu-id="ef89b-106">*expression* . Supprimer (***nom***)</span><span class="sxs-lookup"><span data-stu-id="ef89b-106">*expression* .Delete(***Name***)</span></span>

<span data-ttu-id="ef89b-107">*expression* Variable qui représente un objet **Indexes** .</span><span class="sxs-lookup"><span data-stu-id="ef89b-107">*expression* A variable that represents an **Indexes** object.</span></span>

### <a name="parameters"></a><span data-ttu-id="ef89b-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ef89b-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ef89b-109">Name</span><span class="sxs-lookup"><span data-stu-id="ef89b-109">Name</span></span></p></th>
<th><p><span data-ttu-id="ef89b-110">Obligatoire/Facultatif</span><span class="sxs-lookup"><span data-stu-id="ef89b-110">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="ef89b-111">Type de données</span><span class="sxs-lookup"><span data-stu-id="ef89b-111">Data Type</span></span></p></th>
<th><p><span data-ttu-id="ef89b-112">Description</span><span class="sxs-lookup"><span data-stu-id="ef89b-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ef89b-113">Name</span><span class="sxs-lookup"><span data-stu-id="ef89b-113">Name</span></span></p></td>
<td><p><span data-ttu-id="ef89b-114">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="ef89b-114">Required</span></span></p></td>
<td><p><span data-ttu-id="ef89b-115"><strong>Chaîne</strong></span><span class="sxs-lookup"><span data-stu-id="ef89b-115"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="ef89b-116">Nom de l'index à supprimer</span><span class="sxs-lookup"><span data-stu-id="ef89b-116">The name of the index to delete.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="ef89b-117">Remarques</span><span class="sxs-lookup"><span data-stu-id="ef89b-117">Remarks</span></span>

<span data-ttu-id="ef89b-118">La méthode **Delete** est pris en charge uniquement lorsque l’objet **Index** est nouveau et n’a pas été ajouté à la base de données.</span><span class="sxs-lookup"><span data-stu-id="ef89b-118">The **Delete** method is supported only when the **Index** object is new and hasn’t been appended to the database.</span></span>

