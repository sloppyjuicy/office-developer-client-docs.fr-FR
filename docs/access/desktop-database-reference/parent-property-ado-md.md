---
title: Parent, propriété (ADO MD)
TOCTitle: Parent Property (ADO MD)
ms:assetid: 62649da7-d35f-f11f-674c-28ce95abaf20
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249370(v=office.15)
ms:contentKeyID: 48545238
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 7beba341a2374e1868c67c8f7b4fab73c71c0ba8
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25880298"
---
# <a name="parent-property-ado-md"></a><span data-ttu-id="8f4f2-102">Parent, propriété (ADO MD)</span><span class="sxs-lookup"><span data-stu-id="8f4f2-102">Parent Property (ADO MD)</span></span>


<span data-ttu-id="8f4f2-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="8f4f2-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="8f4f2-104">Indique le membre qui est le parent du membre actif dans une hiérarchie.</span><span class="sxs-lookup"><span data-stu-id="8f4f2-104">Indicates the member that is the parent of the current member in a hierarchy.</span></span>

## <a name="return-values"></a><span data-ttu-id="8f4f2-105">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="8f4f2-105">Return values</span></span>

<span data-ttu-id="8f4f2-106">Retourne un objet [Member](member-object-ado-md.md) et est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="8f4f2-106">Returns a [Member](member-object-ado-md.md) object and is read-only.</span></span>

## <a name="remarks"></a><span data-ttu-id="8f4f2-107">Notes</span><span class="sxs-lookup"><span data-stu-id="8f4f2-107">Remarks</span></span>

<span data-ttu-id="8f4f2-p101">Un membre au niveau supérieur d'une hiérarchie (racine) n'a aucun parent. Cette propriété est uniquement prise en charge par les objets **Member** appartenant à un objet [Level](level-object-ado-md.md). Une erreur se produit lorsque cette propriété est référencée à partir des objets **Member** appartenant à un objet [Position](position-object-ado-md.md).</span><span class="sxs-lookup"><span data-stu-id="8f4f2-p101">A member that is at the top level of a hierarchy (the root) has no parent. This property is supported only on **Member** objects belonging to a [Level](level-object-ado-md.md) object. An error occurs when this property is referenced from **Member** objects belonging to a [Position](position-object-ado-md.md) object.</span></span>

