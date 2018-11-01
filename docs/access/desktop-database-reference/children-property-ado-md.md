---
title: Children, propriété (ADO MD)
TOCTitle: Children Property (ADO MD)
ms:assetid: 66eff203-68e5-a36d-eb2f-2e9faa80deb6
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249400(v=office.15)
ms:contentKeyID: 48545352
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 57049e0e68e4620664687cd261881af953de189f
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25875209"
---
# <a name="children-property-ado-md"></a><span data-ttu-id="d7d2a-102">Children, propriété (ADO MD)</span><span class="sxs-lookup"><span data-stu-id="d7d2a-102">Children Property (ADO MD)</span></span>


<span data-ttu-id="d7d2a-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="d7d2a-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="d7d2a-104">Renvoie une collection d'objets [Member](members-collection-ado-md.md) dont l'objet [Member](member-object-ado-md.md) actif est le parent dans la hiérarchie.</span><span class="sxs-lookup"><span data-stu-id="d7d2a-104">Returns a [Members](members-collection-ado-md.md) collection for which the current [Member](member-object-ado-md.md) is the parent in the hierarchy.</span></span>

## <a name="return-values"></a><span data-ttu-id="d7d2a-105">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="d7d2a-105">Return values</span></span>

<span data-ttu-id="d7d2a-106">Retourne la collection **Members** et est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="d7d2a-106">Returns a **Members** collection and is read-only.</span></span>

## <a name="remarks"></a><span data-ttu-id="d7d2a-107">Notes</span><span class="sxs-lookup"><span data-stu-id="d7d2a-107">Remarks</span></span>

<span data-ttu-id="d7d2a-p101">La propriété **Children** contient une collection **Members** dont le **membre** actuel est le parent hiérarchique. Les objets **Member** de niveau feuille n'ont aucun membre enfant dans la collection **Members**. Cette propriété est uniquement prise en charge par les objets **Member** appartenant à un objet [Level](level-object-ado-md.md). Une erreur se produit lorsque cette propriété est référencée à partir des objets **Member** appartenant à un objet [Position](position-object-ado-md.md).</span><span class="sxs-lookup"><span data-stu-id="d7d2a-p101">The **Children** property contains a **Members** collection for which the current **Member** is the hierarchical parent. Leaf level **Member** objects have no child members in the **Members** collection. This property is only supported on **Member** objects belonging to a [Level](level-object-ado-md.md) object. An error occurs when this property is referenced from **Member** objects belonging to a [Position](position-object-ado-md.md) object.</span></span>

