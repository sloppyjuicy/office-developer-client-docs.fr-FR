---
title: Members, collection (ADO MD)
TOCTitle: Members collection (ADO MD)
ms:assetid: 1389c554-e4f1-107d-22c6-7fe851d53d23
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248910(v=office.15)
ms:contentKeyID: 48543371
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: adc8ed771bcba6a4b6532b33b27980f8aab695c5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32289240"
---
# <a name="members-collection-ado-md"></a><span data-ttu-id="bf38b-102">Members, collection (ADO MD)</span><span class="sxs-lookup"><span data-stu-id="bf38b-102">Members collection (ADO MD)</span></span>


<span data-ttu-id="bf38b-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="bf38b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="bf38b-104">Contient les objets [Member](member-object-ado-md.md) d’un niveau ou d’une position le long d’un axe.</span><span class="sxs-lookup"><span data-stu-id="bf38b-104">Contains the [Member](member-object-ado-md.md) objects from a level or a position along an axis.</span></span>

## <a name="remarks"></a><span data-ttu-id="bf38b-105">Remarques</span><span class="sxs-lookup"><span data-stu-id="bf38b-105">Remarks</span></span>

<span data-ttu-id="bf38b-106">Une collection **Members** permet de contenir les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="bf38b-106">A **Members** collection is used to contain the following types of members:</span></span>

  - <span data-ttu-id="bf38b-p101">Les membres constituant un niveau dans un cube. Ils figurent dans la collection **Members** d'un objet [Level](level-object-ado-md.md). Par exemple, dans le cadre de l'exemple de la rubrique [Présentation des schémas et données multidimensionnels](overview-of-multidimensional-schemas-and-data.md), les quatre membres du niveau Pays sont Canada, USA, UK et Germany.</span><span class="sxs-lookup"><span data-stu-id="bf38b-p101">The members that make up a level in a cube. These are contained in the **Members** collection of a [Level](level-object-ado-md.md) object. For example, using the sample from [Overview of Multidimensional Schemas and Data](overview-of-multidimensional-schemas-and-data.md), the four members of the Countries level are Canada, USA, UK, and Germany.</span></span>

  - <span data-ttu-id="bf38b-p102">Les membres qui sont les enfants d'un membre spécifique au sein d'une hiérarchie. Ces membres sont renvoyés par la propriété [Children](children-property-ado-md.md) de l'objet **Member** parent. Par exemple, toujours dans le cadre du même exemple, les deux enfants du membre Canada sont Canada-East et Canada-West.</span><span class="sxs-lookup"><span data-stu-id="bf38b-p102">The members that are the children of a specific member within a hierarchy. These members are returned by the [Children](children-property-ado-md.md) property of the parent **Member** object. For example, again using the same sample, the two children of the Canada member are Canada-East and Canada-West.</span></span>

  - <span data-ttu-id="bf38b-p103">Les membres définissant une position spécifique le long d'un axe d'un [ensemble de cellules](cellset-object-ado-md.md). En se basant sur l'ensemble de cellules de l'exemple de la rubrique [Utilisation de données multidimensionnelles](working-with-multidimensional-data.md), les deux membres de la première position de l' axe des x sont Valentine et Seattle. Ces membres font partie de la collection **Members** d'un objet [Position](position-object-ado-md.md).</span><span class="sxs-lookup"><span data-stu-id="bf38b-p103">The members that define a specific position along an axis of a [cellset](cellset-object-ado-md.md). Using the cellset from [Working with Multidimensional Data](working-with-multidimensional-data.md) as an example, the two members of the first position on the x-axis are Valentine and Seattle. These members are contained by the **Members** collection of a [Position](position-object-ado-md.md) object.</span></span>

<span data-ttu-id="bf38b-p104">**Members** est une collection ADO standard. Avec les propriétés et méthodes d'une collection, vous pouvez :</span><span class="sxs-lookup"><span data-stu-id="bf38b-p104">**Members** is a standard ADO collection. With the properties and methods of a collection, you can do the following:</span></span>

  - <span data-ttu-id="bf38b-118">Obtenir le nombre d'objets d'une collection à l'aide de la propriété [Count](count-property-ado.md).</span><span class="sxs-lookup"><span data-stu-id="bf38b-118">Obtain the number of objects in the collection with the [Count](count-property-ado.md) property.</span></span>

  - <span data-ttu-id="bf38b-119">Renvoyer un objet de la collection à l'aide de la propriété [Item](item-property-ado.md) par défaut.</span><span class="sxs-lookup"><span data-stu-id="bf38b-119">Return an object from the collection with the default [Item](item-property-ado.md) property.</span></span>

  - <span data-ttu-id="bf38b-120">Mettre à jour les objets de la collection à partir du fournisseur à l'aide de la méthode [Refresh](refresh-method-ado.md).</span><span class="sxs-lookup"><span data-stu-id="bf38b-120">Update the objects in the collection from the provider with the [Refresh](refresh-method-ado.md) method.</span></span>

