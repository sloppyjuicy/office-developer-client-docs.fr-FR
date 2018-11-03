---
title: Méthode Indexes.Delete (DAO)
TOCTitle: Delete Method
ms:assetid: 8d3c3221-3b2e-15ba-32ff-f2dfc592d82c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197351(v=office.15)
ms:contentKeyID: 48546252
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 66f08fa9733de0b63ca8bb659972abbc59183e16
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25922320"
---
# <a name="indexesdelete-method-dao"></a><span data-ttu-id="ac2a5-102">Méthode Indexes.Delete (DAO)</span><span class="sxs-lookup"><span data-stu-id="ac2a5-102">Indexes.Delete method (DAO)</span></span>


<span data-ttu-id="ac2a5-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="ac2a5-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="ac2a5-104">Supprime l'objet **Index** spécifié de la collection **Indexes**.</span><span class="sxs-lookup"><span data-stu-id="ac2a5-104">Deletes the specified **Index** from the **Indexes** collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="ac2a5-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ac2a5-105">Syntax</span></span>

<span data-ttu-id="ac2a5-106">*expression* . Supprimer (***nom***)</span><span class="sxs-lookup"><span data-stu-id="ac2a5-106">*expression* .Delete(***Name***)</span></span>

<span data-ttu-id="ac2a5-107">*expression* Variable qui représente un objet **Indexes** .</span><span class="sxs-lookup"><span data-stu-id="ac2a5-107">*expression* A variable that represents an **Indexes** object.</span></span>

### <a name="parameters"></a><span data-ttu-id="ac2a5-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ac2a5-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ac2a5-109">Name</span><span class="sxs-lookup"><span data-stu-id="ac2a5-109">Name</span></span></p></th>
<th><p><span data-ttu-id="ac2a5-110">Obligatoire/Facultatif</span><span class="sxs-lookup"><span data-stu-id="ac2a5-110">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="ac2a5-111">Type de données</span><span class="sxs-lookup"><span data-stu-id="ac2a5-111">Data Type</span></span></p></th>
<th><p><span data-ttu-id="ac2a5-112">Description</span><span class="sxs-lookup"><span data-stu-id="ac2a5-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ac2a5-113">Name</span><span class="sxs-lookup"><span data-stu-id="ac2a5-113">Name</span></span></p></td>
<td><p><span data-ttu-id="ac2a5-114">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="ac2a5-114">Required</span></span></p></td>
<td><p><span data-ttu-id="ac2a5-115"><strong>Chaîne</strong></span><span class="sxs-lookup"><span data-stu-id="ac2a5-115"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="ac2a5-116">Nom de l'index à supprimer</span><span class="sxs-lookup"><span data-stu-id="ac2a5-116">The name of the index to delete.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="ac2a5-117">Remarques</span><span class="sxs-lookup"><span data-stu-id="ac2a5-117">Remarks</span></span>

<span data-ttu-id="ac2a5-118">La méthode **Delete** est pris en charge uniquement lorsque l’objet **Index** est nouveau et n’a pas été ajouté à la base de données.</span><span class="sxs-lookup"><span data-stu-id="ac2a5-118">The **Delete** method is supported only when the **Index** object is new and hasn’t been appended to the database.</span></span>

