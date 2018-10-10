---
title: Parent, propriété (ADO MD)
TOCTitle: Parent Property (ADO MD)
ms:assetid: 62649da7-d35f-f11f-674c-28ce95abaf20
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249370(v=office.15)
ms:contentKeyID: 48545238
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: eb1606a745cb8572f54b253bdbbbbbb461cfc74a
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25470322"
---
# <a name="parent-property-ado-md"></a><span data-ttu-id="ab50e-102">Parent, propriété (ADO MD)</span><span class="sxs-lookup"><span data-stu-id="ab50e-102">Parent Property (ADO MD)</span></span>


<span data-ttu-id="ab50e-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="ab50e-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="ab50e-104">Indique le membre qui est le parent du membre actif dans une hiérarchie.</span><span class="sxs-lookup"><span data-stu-id="ab50e-104">Indicates the member that is the parent of the current member in a hierarchy.</span></span>

## <a name="return-values"></a><span data-ttu-id="ab50e-105">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="ab50e-105">Return Values</span></span>

<span data-ttu-id="ab50e-106">Retourne un objet [Member](member-object-ado-md.md) et est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="ab50e-106">Returns a [Member](member-object-ado-md.md) object and is read-only.</span></span>

## <a name="remarks"></a><span data-ttu-id="ab50e-107">Notes</span><span class="sxs-lookup"><span data-stu-id="ab50e-107">Remarks</span></span>

<span data-ttu-id="ab50e-p101">Un membre au niveau supérieur d'une hiérarchie (racine) n'a aucun parent. Cette propriété est uniquement prise en charge par les objets **Member** appartenant à un objet [Level](level-object-ado-md.md). Une erreur se produit lorsque cette propriété est référencée à partir des objets **Member** appartenant à un objet [Position](position-object-ado-md.md).</span><span class="sxs-lookup"><span data-stu-id="ab50e-p101">A member that is at the top level of a hierarchy (the root) has no parent. This property is supported only on **Member** objects belonging to a [Level](level-object-ado-md.md) object. An error occurs when this property is referenced from **Member** objects belonging to a [Position](position-object-ado-md.md) object.</span></span>

