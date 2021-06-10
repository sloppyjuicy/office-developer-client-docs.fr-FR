---
title: Indexes.Delete, méthode (DAO)
TOCTitle: Delete Method
ms:assetid: 8d3c3221-3b2e-15ba-32ff-f2dfc592d82c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197351(v=office.15)
ms:contentKeyID: 48546252
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 6ab52f353b7a3e636f64ff2ad6ad5354d62bed48
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32291551"
---
# <a name="indexesdelete-method-dao"></a><span data-ttu-id="2b5ec-102">Indexes.Delete, méthode (DAO)</span><span class="sxs-lookup"><span data-stu-id="2b5ec-102">Indexes.Delete method (DAO)</span></span>

<span data-ttu-id="2b5ec-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="2b5ec-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="2b5ec-104">Supprime l'objet **Index** spécifié de la collection **Indexes**.</span><span class="sxs-lookup"><span data-stu-id="2b5ec-104">Deletes the specified **Index** from the **Indexes** collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="2b5ec-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2b5ec-105">Syntax</span></span>

<span data-ttu-id="2b5ec-106">*.* Delete(***Name***)</span><span class="sxs-lookup"><span data-stu-id="2b5ec-106">*expression* .Delete(***Name***)</span></span>

<span data-ttu-id="2b5ec-107">*expression* Variable qui représente un objet **Indexes.**</span><span class="sxs-lookup"><span data-stu-id="2b5ec-107">*expression* A variable that represents an **Indexes** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="2b5ec-108">Parameters</span><span class="sxs-lookup"><span data-stu-id="2b5ec-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="2b5ec-109">Nom</span><span class="sxs-lookup"><span data-stu-id="2b5ec-109">Name</span></span></p></th>
<th><p><span data-ttu-id="2b5ec-110">Obligatoire/facultatif</span><span class="sxs-lookup"><span data-stu-id="2b5ec-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="2b5ec-111">Type de données</span><span class="sxs-lookup"><span data-stu-id="2b5ec-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="2b5ec-112">Description</span><span class="sxs-lookup"><span data-stu-id="2b5ec-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2b5ec-113"><em>Name</em></span><span class="sxs-lookup"><span data-stu-id="2b5ec-113"><em>Name</em></span></span></p></td>
<td><p><span data-ttu-id="2b5ec-114">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="2b5ec-114">Required</span></span></p></td>
<td><p><span data-ttu-id="2b5ec-115"><strong>String</strong></span><span class="sxs-lookup"><span data-stu-id="2b5ec-115"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="2b5ec-116">Nom de l'index à supprimer</span><span class="sxs-lookup"><span data-stu-id="2b5ec-116">The name of the index to delete.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="2b5ec-117">Remarques</span><span class="sxs-lookup"><span data-stu-id="2b5ec-117">Remarks</span></span>

<span data-ttu-id="2b5ec-118">La méthode **Delete** n'est prise en charge que lorsque l'objet **Index** est nouveau et qu'il n'a pas été ajouté à la base de données.</span><span class="sxs-lookup"><span data-stu-id="2b5ec-118">The **Delete** method is supported only when the **Index** object is new and hasn’t been appended to the database.</span></span>

