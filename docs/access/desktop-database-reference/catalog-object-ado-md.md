---
title: Catalog, objet (ADO MD)
TOCTitle: Catalog Object (ADO MD)
ms:assetid: 708c4082-3589-7f3b-5ea3-f3705f3d3ff1
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249445(v=office.15)
ms:contentKeyID: 48545559
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 68af66ad00567e06649df6003eeac482eacd6686
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25470881"
---
# <a name="catalog-object-ado-md"></a><span data-ttu-id="31702-102">Catalog, objet (ADO MD)</span><span class="sxs-lookup"><span data-stu-id="31702-102">Catalog Object (ADO MD)</span></span>


<span data-ttu-id="31702-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="31702-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="31702-104">Contient les informations de schéma multidimensionnel (en d'autres termes, les cubes et dimensions sous-jacentes, les hiérarchies, les niveaux et les membres) spécifiques à un fournisseur de données multidimensionnelles (MDP).</span><span class="sxs-lookup"><span data-stu-id="31702-104">Contains multidimensional schema information (that is, cubes and underlying dimensions, hierarchies, levels, and members) specific to a multidimensional data provider (MDP).</span></span>

## <a name="remarks"></a><span data-ttu-id="31702-105">Remarques</span><span class="sxs-lookup"><span data-stu-id="31702-105">Remarks</span></span>

<span data-ttu-id="31702-106">Avec les collections et propriétés d'un objet **Catalog**, vous pouvez :</span><span class="sxs-lookup"><span data-stu-id="31702-106">With the collections and properties of a **Catalog** object, you can do the following:</span></span>

  - <span data-ttu-id="31702-107">Ouvrir le catalogue en définissant la propriété [ActiveConnection](activeconnection-property-ado-md.md) sur un objet ADO [Connection](connection-object-ado.md) standard ou une chaîne de connexion valide.</span><span class="sxs-lookup"><span data-stu-id="31702-107">Open the catalog by setting the [ActiveConnection](activeconnection-property-ado-md.md) property to a standard ADO [Connection](connection-object-ado.md) object or to a valid connection string.</span></span>

  - <span data-ttu-id="31702-108">Identifier le **catalogue** à l'aide de la propriété [Name](name-property-ado-md.md).</span><span class="sxs-lookup"><span data-stu-id="31702-108">Identify the **Catalog** with the [Name](name-property-ado-md.md) property.</span></span>

  - <span data-ttu-id="31702-109">Parcourir les cubes d'un catalogue à l'aide de la collection [CubeDefs](cubedefs-collection-ado-md.md).</span><span class="sxs-lookup"><span data-stu-id="31702-109">Iterate through the cubes in a catalog using the [CubeDefs](cubedefs-collection-ado-md.md) collection.</span></span>

