---
title: Indexes.Delete Method (DAO)
TOCTitle: Delete Method
ms:assetid: 8d3c3221-3b2e-15ba-32ff-f2dfc592d82c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197351(v=office.15)
ms:contentKeyID: 48546252
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b30748c0a1388a1175512e3b8d3fd1970795b821
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25469957"
---
# <a name="indexesdelete-method-dao"></a><span data-ttu-id="00165-102">Indexes.Delete Method (DAO)</span><span class="sxs-lookup"><span data-stu-id="00165-102">Indexes.Delete Method (DAO)</span></span>


<span data-ttu-id="00165-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="00165-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="00165-104">Supprime l'objet **Index** spécifié de la collection **Indexes**.</span><span class="sxs-lookup"><span data-stu-id="00165-104">Deletes the specified **Index** from the **Indexes** collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="00165-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="00165-105">Syntax</span></span>

<span data-ttu-id="00165-106">*expression* . Supprimer (***nom***)</span><span class="sxs-lookup"><span data-stu-id="00165-106">*expression* .Delete(***Name***)</span></span>

<span data-ttu-id="00165-107">*expression* Variable qui représente un objet **Indexes** .</span><span class="sxs-lookup"><span data-stu-id="00165-107">*expression* A variable that represents an **Indexes** object.</span></span>

### <a name="parameters"></a><span data-ttu-id="00165-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="00165-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="00165-109">Name</span><span class="sxs-lookup"><span data-stu-id="00165-109">Name</span></span></p></th>
<th><p><span data-ttu-id="00165-110">Obligatoire/Facultatif</span><span class="sxs-lookup"><span data-stu-id="00165-110">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="00165-111">Type de données</span><span class="sxs-lookup"><span data-stu-id="00165-111">Data Type</span></span></p></th>
<th><p><span data-ttu-id="00165-112">Description</span><span class="sxs-lookup"><span data-stu-id="00165-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="00165-113">Name</span><span class="sxs-lookup"><span data-stu-id="00165-113">Name</span></span></p></td>
<td><p><span data-ttu-id="00165-114">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="00165-114">Required</span></span></p></td>
<td><p><span data-ttu-id="00165-115"><strong>Chaîne</strong></span><span class="sxs-lookup"><span data-stu-id="00165-115"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="00165-116">Nom de l'index à supprimer</span><span class="sxs-lookup"><span data-stu-id="00165-116">The name of the index to delete.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="00165-117">Remarques</span><span class="sxs-lookup"><span data-stu-id="00165-117">Remarks</span></span>

<span data-ttu-id="00165-118">La méthode **Delete** est pris en charge uniquement lorsque l’objet **Index** est nouveau et n’a pas été ajouté à la base de données.</span><span class="sxs-lookup"><span data-stu-id="00165-118">The **Delete** method is supported only when the **Index** object is new and hasn’t been appended to the database.</span></span>

