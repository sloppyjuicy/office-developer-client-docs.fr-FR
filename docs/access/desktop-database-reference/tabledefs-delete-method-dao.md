---
title: TableDefs. Delete, méthode (DAO)
TOCTitle: Delete Method
ms:assetid: 130bb50d-17c3-b2ab-9360-0d91d0cee131
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845419(v=office.15)
ms:contentKeyID: 48543358
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 63f543fd86e309372e0432c3e45513cd9d3942ab
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32313992"
---
# <a name="tabledefsdelete-method-dao"></a><span data-ttu-id="2edbe-102">TableDefs. Delete, méthode (DAO)</span><span class="sxs-lookup"><span data-stu-id="2edbe-102">TableDefs.Delete method (DAO)</span></span>

<span data-ttu-id="2edbe-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="2edbe-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="2edbe-104">Supprime l'objet **TableDef** spécifié de la collection **TableDefs**.</span><span class="sxs-lookup"><span data-stu-id="2edbe-104">Deletes the specified **TableDef** object from the **TableDefs** collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="2edbe-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2edbe-105">Syntax</span></span>

<span data-ttu-id="2edbe-106">*expression* . Delete (***Name***)</span><span class="sxs-lookup"><span data-stu-id="2edbe-106">*expression* .Delete(***Name***)</span></span>

<span data-ttu-id="2edbe-107">*expression* Variable qui représente un objet **TableDefs** .</span><span class="sxs-lookup"><span data-stu-id="2edbe-107">*expression* A variable that represents a **TableDefs** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="2edbe-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2edbe-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="2edbe-109">Nom</span><span class="sxs-lookup"><span data-stu-id="2edbe-109">Name</span></span></p></th>
<th><p><span data-ttu-id="2edbe-110">Obligatoire/facultatif</span><span class="sxs-lookup"><span data-stu-id="2edbe-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="2edbe-111">Type de données</span><span class="sxs-lookup"><span data-stu-id="2edbe-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="2edbe-112">Description</span><span class="sxs-lookup"><span data-stu-id="2edbe-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2edbe-113"><em>Name</em></span><span class="sxs-lookup"><span data-stu-id="2edbe-113"><em>Name</em></span></span></p></td>
<td><p><span data-ttu-id="2edbe-114">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="2edbe-114">Required</span></span></p></td>
<td><p><span data-ttu-id="2edbe-115"><strong>String</strong></span><span class="sxs-lookup"><span data-stu-id="2edbe-115"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="2edbe-116">Nom de l'objet TableDef à supprimer.</span><span class="sxs-lookup"><span data-stu-id="2edbe-116">The name of the TableDef to delete.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="2edbe-117">Remarques</span><span class="sxs-lookup"><span data-stu-id="2edbe-117">Remarks</span></span>

<span data-ttu-id="2edbe-118">La méthode Delete n'est prise en charge que lorsque l'objet **TableDef** est nouveau et n'a pas été ajouté à la base de données, ou lorsque la propriété **Updatable** de l'objet **TableDef** prend la valeur **True**.</span><span class="sxs-lookup"><span data-stu-id="2edbe-118">The Delete method is supported only when the **TableDef** object is new and hasn’t been appended to the database, or when the **Updatable** property of the **TableDef** is set to **True**.</span></span>

