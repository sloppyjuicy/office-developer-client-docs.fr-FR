---
title: Description, property (ADO MD)
TOCTitle: Description Property (ADO MD)
ms:assetid: 06d5e1d0-6ed7-fe14-3723-3790e225482a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248816(v=office.15)
ms:contentKeyID: 48543055
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 96f3762df84f2534b31501bdf44059152e7077bb
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25873151"
---
# <a name="description-property-ado-md"></a><span data-ttu-id="d5988-102">Description, property (ADO MD)</span><span class="sxs-lookup"><span data-stu-id="d5988-102">Description Property (ADO MD)</span></span>


<span data-ttu-id="d5988-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="d5988-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="d5988-104">Retourne une explication textuelle de l'objet actif.</span><span class="sxs-lookup"><span data-stu-id="d5988-104">Returns a text explanation of the current object.</span></span>

## <a name="return-values"></a><span data-ttu-id="d5988-105">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="d5988-105">Return values</span></span>

<span data-ttu-id="d5988-106">Retourne une valeur de type **String** et est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="d5988-106">Returns a **String** and is read-only.</span></span>

## <a name="remarks"></a><span data-ttu-id="d5988-107">Notes</span><span class="sxs-lookup"><span data-stu-id="d5988-107">Remarks</span></span>

<span data-ttu-id="d5988-p101">Pour les objets [Member](member-object-ado-md.md), la propriété **Description** s'applique uniquement aux membres de formule et de mesure. La propriété **Description** retourne une chaîne vide ("") pour tous les autres types de membres. Pour plus d'informations sur ces divers types de membres, consultez la propriété [Type](type-property-ado-md.md).</span><span class="sxs-lookup"><span data-stu-id="d5988-p101">For [Member](member-object-ado-md.md) objects, **Description** applies only to measure and formula members. **Description** returns an empty string ("") for all other types of members. For more information about the various types of members, see the [Type](type-property-ado-md.md) property.</span></span>

<span data-ttu-id="d5988-p102">Cette propriété est uniquement prise en charge par les objets **Member** appartenant à un objet [Level](level-object-ado-md.md). Une erreur se produit lorsque cette propriété est référencée à partir des objets **Member** appartenant à un objet [Position](position-object-ado-md.md).</span><span class="sxs-lookup"><span data-stu-id="d5988-p102">This property is only supported on **Member** objects belonging to a [Level](level-object-ado-md.md) object. An error occurs when this property is referenced from **Member** objects belonging to a [Position](position-object-ado-md.md) object.</span></span>

