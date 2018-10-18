---
title: Parent, propriété (ADO MD)
TOCTitle: Parent Property (ADO MD)
ms:assetid: 62649da7-d35f-f11f-674c-28ce95abaf20
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249370(v=office.15)
ms:contentKeyID: 48545238
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 10c183c997a3c0b49c74e08f7ef29fbe8c274516
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/17/2018
ms.locfileid: "25603335"
---
# <a name="parent-property-ado-md"></a><span data-ttu-id="3501f-102">Parent, propriété (ADO MD)</span><span class="sxs-lookup"><span data-stu-id="3501f-102">Parent Property (ADO MD)</span></span>


<span data-ttu-id="3501f-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="3501f-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="3501f-104">Indique le membre qui est le parent du membre actif dans une hiérarchie.</span><span class="sxs-lookup"><span data-stu-id="3501f-104">Indicates the member that is the parent of the current member in a hierarchy.</span></span>

<span data-ttu-id="3501f-105"><<<<<<< Tête</span><span class="sxs-lookup"><span data-stu-id="3501f-105"><<<<<<< HEAD</span></span>
## <a name="return-values"></a><span data-ttu-id="3501f-106">Valeurs renvoyées</span><span class="sxs-lookup"><span data-stu-id="3501f-106">Return Values</span></span>
=======
## <a name="return-values"></a><span data-ttu-id="3501f-107">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="3501f-107">Return values</span></span>
>>>>>>> <span data-ttu-id="3501f-108">master</span><span class="sxs-lookup"><span data-stu-id="3501f-108">master</span></span>

<span data-ttu-id="3501f-109">Retourne un objet [Member](member-object-ado-md.md) et est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="3501f-109">Returns a [Member](member-object-ado-md.md) object and is read-only.</span></span>

## <a name="remarks"></a><span data-ttu-id="3501f-110">Notes</span><span class="sxs-lookup"><span data-stu-id="3501f-110">Remarks</span></span>

<span data-ttu-id="3501f-p101">Un membre au niveau supérieur d'une hiérarchie (racine) n'a aucun parent. Cette propriété est uniquement prise en charge par les objets **Member** appartenant à un objet [Level](level-object-ado-md.md). Une erreur se produit lorsque cette propriété est référencée à partir des objets **Member** appartenant à un objet [Position](position-object-ado-md.md).</span><span class="sxs-lookup"><span data-stu-id="3501f-p101">A member that is at the top level of a hierarchy (the root) has no parent. This property is supported only on **Member** objects belonging to a [Level](level-object-ado-md.md) object. An error occurs when this property is referenced from **Member** objects belonging to a [Position](position-object-ado-md.md) object.</span></span>

