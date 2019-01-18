---
title: Description, property (ADO MD)
TOCTitle: Description property (ADO MD)
ms:assetid: 06d5e1d0-6ed7-fe14-3723-3790e225482a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248816(v=office.15)
ms:contentKeyID: 48543055
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 0f74532693f1054dd9d187757af840a3a00b451f
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28720617"
---
# <a name="description-property-ado-md"></a><span data-ttu-id="c08a5-102">Description, property (ADO MD)</span><span class="sxs-lookup"><span data-stu-id="c08a5-102">Description property (ADO MD)</span></span>


<span data-ttu-id="c08a5-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="c08a5-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="c08a5-104">Retourne une explication textuelle de l'objet actif.</span><span class="sxs-lookup"><span data-stu-id="c08a5-104">Returns a text explanation of the current object.</span></span>

## <a name="return-values"></a><span data-ttu-id="c08a5-105">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="c08a5-105">Return values</span></span>

<span data-ttu-id="c08a5-106">Retourne une valeur de type **String** et est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="c08a5-106">Returns a **String** and is read-only.</span></span>

## <a name="remarks"></a><span data-ttu-id="c08a5-107">Notes</span><span class="sxs-lookup"><span data-stu-id="c08a5-107">Remarks</span></span>

<span data-ttu-id="c08a5-p101">Pour les objets [Member](member-object-ado-md.md), la propriété **Description** s'applique uniquement aux membres de formule et de mesure. La propriété **Description** retourne une chaîne vide ("") pour tous les autres types de membres. Pour plus d'informations sur ces divers types de membres, consultez la propriété [Type](type-property-ado-md.md).</span><span class="sxs-lookup"><span data-stu-id="c08a5-p101">For [Member](member-object-ado-md.md) objects, **Description** applies only to measure and formula members. **Description** returns an empty string ("") for all other types of members. For more information about the various types of members, see the [Type](type-property-ado-md.md) property.</span></span>

<span data-ttu-id="c08a5-p102">Cette propriété est uniquement prise en charge par les objets **Member** appartenant à un objet [Level](level-object-ado-md.md). Une erreur se produit lorsque cette propriété est référencée à partir des objets **Member** appartenant à un objet [Position](position-object-ado-md.md).</span><span class="sxs-lookup"><span data-stu-id="c08a5-p102">This property is only supported on **Member** objects belonging to a [Level](level-object-ado-md.md) object. An error occurs when this property is referenced from **Member** objects belonging to a [Position](position-object-ado-md.md) object.</span></span>

