---
title: DrilledDown, propriété (ADO MD)
TOCTitle: DrilledDown Property (ADO MD)
ms:assetid: 1dfe728f-8da2-1d2b-7361-8689a0b088b4
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248972(v=office.15)
ms:contentKeyID: 48543610
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f7e53eb2a6d1735e07fa73e38adad8a59522fddf
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25871499"
---
# <a name="drilleddown-property-ado-md"></a><span data-ttu-id="a9368-102">DrilledDown, propriété (ADO MD)</span><span class="sxs-lookup"><span data-stu-id="a9368-102">DrilledDown Property (ADO MD)</span></span>


<span data-ttu-id="a9368-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="a9368-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="a9368-104">Indique si aucun enfant ne suit immédiatement le membre sur un axe.</span><span class="sxs-lookup"><span data-stu-id="a9368-104">Indicates whether no children immediately follow the member on the axis.</span></span>

## <a name="return-values"></a><span data-ttu-id="a9368-105">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="a9368-105">Return values</span></span>

<span data-ttu-id="a9368-p101">Retourne une valeur de type **Boolean** et est en lecture seule. **DrilledDown** retourne la valeur **True** s'il n'existe aucun membre enfant du membre actuel sur l'axe. **DrilledDown** retourne la valeur **False** s'il existe au moins un membre enfant du membre actuel sur l'axe.</span><span class="sxs-lookup"><span data-stu-id="a9368-p101">Returns a **Boolean** value and is read-only. **DrilledDown** returns **True** if there are no child members of the current member on the axis. **DrilledDown** returns **False** if there is one or more child members of the current member on the axis.</span></span>

## <a name="remarks"></a><span data-ttu-id="a9368-109">Notes</span><span class="sxs-lookup"><span data-stu-id="a9368-109">Remarks</span></span>

<span data-ttu-id="a9368-p102">Utilisez la propriété **DrilledDown** pour déterminer s'il existe au moins un enfant de ce membre sur l'axe situé immédiatement après lui. Ces informations sont utiles lors de l'affichage du membre.</span><span class="sxs-lookup"><span data-stu-id="a9368-p102">Use the **DrilledDown** property to determine whether there is at least one child of this member on the axis immediately following this member. This information is useful when displaying the member.</span></span>

<span data-ttu-id="a9368-p103">Cette propriété est uniquement prise en charge par les objets [Member](member-object-ado-md.md) appartenant à un objet [Position](position-object-ado-md.md). Une erreur survient lorsque cette propriété est référencée à partir des objets **Member** appartenant à un objet [Level](level-object-ado-md.md).</span><span class="sxs-lookup"><span data-stu-id="a9368-p103">This property is only supported on [Member](member-object-ado-md.md) objects belonging to a [Position](position-object-ado-md.md) object. An error occurs when this property is referenced from **Member** objects belonging to a [Level](level-object-ado-md.md) object.</span></span>

