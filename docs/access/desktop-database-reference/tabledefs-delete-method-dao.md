---
title: TableDefs.Delete Method (DAO)
TOCTitle: Delete Method
ms:assetid: 130bb50d-17c3-b2ab-9360-0d91d0cee131
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845419(v=office.15)
ms:contentKeyID: 48543358
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: e39a1390c9ea26baa83d8203967d603237a3ab1c
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25470782"
---
# <a name="tabledefsdelete-method-dao"></a><span data-ttu-id="a3c0e-102">TableDefs.Delete Method (DAO)</span><span class="sxs-lookup"><span data-stu-id="a3c0e-102">TableDefs.Delete Method (DAO)</span></span>


<span data-ttu-id="a3c0e-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="a3c0e-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="a3c0e-104">Supprime l'objet **TableDef** spécifié de la collection **TableDefs**.</span><span class="sxs-lookup"><span data-stu-id="a3c0e-104">Deletes the specified **TableDef** object from the **TableDefs** collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="a3c0e-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a3c0e-105">Syntax</span></span>

<span data-ttu-id="a3c0e-106">*expression* . Supprimer (***nom***)</span><span class="sxs-lookup"><span data-stu-id="a3c0e-106">*expression* .Delete(***Name***)</span></span>

<span data-ttu-id="a3c0e-107">*expression* Variable qui représente un objet **TableDef** .</span><span class="sxs-lookup"><span data-stu-id="a3c0e-107">*expression* A variable that represents a **TableDefs** object.</span></span>

### <a name="parameters"></a><span data-ttu-id="a3c0e-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a3c0e-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a3c0e-109">Name</span><span class="sxs-lookup"><span data-stu-id="a3c0e-109">Name</span></span></p></th>
<th><p><span data-ttu-id="a3c0e-110">Obligatoire/Facultatif</span><span class="sxs-lookup"><span data-stu-id="a3c0e-110">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="a3c0e-111">Type de données</span><span class="sxs-lookup"><span data-stu-id="a3c0e-111">Data Type</span></span></p></th>
<th><p><span data-ttu-id="a3c0e-112">Description</span><span class="sxs-lookup"><span data-stu-id="a3c0e-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a3c0e-113">Name</span><span class="sxs-lookup"><span data-stu-id="a3c0e-113">Name</span></span></p></td>
<td><p><span data-ttu-id="a3c0e-114">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="a3c0e-114">Required</span></span></p></td>
<td><p><span data-ttu-id="a3c0e-115"><strong>Chaîne</strong></span><span class="sxs-lookup"><span data-stu-id="a3c0e-115"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="a3c0e-116">Nom de l'objet TableDef à supprimer.</span><span class="sxs-lookup"><span data-stu-id="a3c0e-116">The name of the TableDef to delete.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="a3c0e-117">Remarques</span><span class="sxs-lookup"><span data-stu-id="a3c0e-117">Remarks</span></span>

<span data-ttu-id="a3c0e-118">La méthode Delete est pris en charge uniquement lorsque l’objet **TableDef** est nouveau et n’a pas été ajouté à la base de données, ou lorsque la propriété **Updatable** de l' **objet TableDef** est définie sur **True**.</span><span class="sxs-lookup"><span data-stu-id="a3c0e-118">The Delete method is supported only when the **TableDef** object is new and hasn’t been appended to the database, or when the **Updatable** property of the **TableDef** is set to **True**.</span></span>

