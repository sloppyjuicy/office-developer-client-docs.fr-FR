---
title: Children, propriété (ADO MD)
TOCTitle: Children Property (ADO MD)
ms:assetid: 66eff203-68e5-a36d-eb2f-2e9faa80deb6
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249400(v=office.15)
ms:contentKeyID: 48545352
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: dbbae74ce8ce22255e97403fc3906dd50f36b38b
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/17/2018
ms.locfileid: "25605050"
---
# <a name="children-property-ado-md"></a><span data-ttu-id="85507-102">Children, propriété (ADO MD)</span><span class="sxs-lookup"><span data-stu-id="85507-102">Children Property (ADO MD)</span></span>


<span data-ttu-id="85507-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="85507-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="85507-104">Renvoie une collection d'objets [Member](members-collection-ado-md.md) dont l'objet [Member](member-object-ado-md.md) actif est le parent dans la hiérarchie.</span><span class="sxs-lookup"><span data-stu-id="85507-104">Returns a [Members](members-collection-ado-md.md) collection for which the current [Member](member-object-ado-md.md) is the parent in the hierarchy.</span></span>

<span data-ttu-id="85507-105"><<<<<<< Tête</span><span class="sxs-lookup"><span data-stu-id="85507-105"><<<<<<< HEAD</span></span>
## <a name="return-values"></a><span data-ttu-id="85507-106">Valeurs renvoyées</span><span class="sxs-lookup"><span data-stu-id="85507-106">Return Values</span></span>
=======
## <a name="return-values"></a><span data-ttu-id="85507-107">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="85507-107">Return values</span></span>
>>>>>>> <span data-ttu-id="85507-108">master</span><span class="sxs-lookup"><span data-stu-id="85507-108">master</span></span>

<span data-ttu-id="85507-109">Retourne la collection **Members** et est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="85507-109">Returns a **Members** collection and is read-only.</span></span>

## <a name="remarks"></a><span data-ttu-id="85507-110">Notes</span><span class="sxs-lookup"><span data-stu-id="85507-110">Remarks</span></span>

<span data-ttu-id="85507-p101">La propriété **Children** contient une collection **Members** dont le **membre** actuel est le parent hiérarchique. Les objets **Member** de niveau feuille n'ont aucun membre enfant dans la collection **Members**. Cette propriété est uniquement prise en charge par les objets **Member** appartenant à un objet [Level](level-object-ado-md.md). Une erreur se produit lorsque cette propriété est référencée à partir des objets **Member** appartenant à un objet [Position](position-object-ado-md.md).</span><span class="sxs-lookup"><span data-stu-id="85507-p101">The **Children** property contains a **Members** collection for which the current **Member** is the hierarchical parent. Leaf level **Member** objects have no child members in the **Members** collection. This property is only supported on **Member** objects belonging to a [Level](level-object-ado-md.md) object. An error occurs when this property is referenced from **Member** objects belonging to a [Position](position-object-ado-md.md) object.</span></span>

