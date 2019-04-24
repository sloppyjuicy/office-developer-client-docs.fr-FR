---
title: CellSet, objet (ADO MD)
TOCTitle: Cellset object (ADO MD)
ms:assetid: 28d4b3b9-f907-9ec0-00e1-9666c887cdf0
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249047(v=office.15)
ms:contentKeyID: 48543869
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: c8cb75ad7277386cfe81b2edcffa234498318444
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296513"
---
# <a name="cellset-object-ado-md"></a><span data-ttu-id="a611c-102">CellSet, objet (ADO MD)</span><span class="sxs-lookup"><span data-stu-id="a611c-102">Cellset object (ADO MD)</span></span>

<span data-ttu-id="a611c-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="a611c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="a611c-104">Représente les résultats d'une requête multidimensionnelle.</span><span class="sxs-lookup"><span data-stu-id="a611c-104">Represents the results of a multidimensional query.</span></span> <span data-ttu-id="a611c-105">Il s'agit d'une collection de cellules sélectionnées dans des cubes ou d'autres ensembles de cellules.</span><span class="sxs-lookup"><span data-stu-id="a611c-105">It is a collection of cells selected from cubes or other cellsets.</span></span>

## <a name="remarks"></a><span data-ttu-id="a611c-106">Remarques</span><span class="sxs-lookup"><span data-stu-id="a611c-106">Remarks</span></span>

<span data-ttu-id="a611c-p102">Les données d'un **ensemble de cellules** sont extraites à l'aide d'un accès direct de type matrice. Vous pouvez détailler un certain membre pour obtenir les données le concernant. Par exemple, le code suivant renvoie la légende du premier membre de la première position sur le premier axe d'un ensemble de cellules appelé cst :</span><span class="sxs-lookup"><span data-stu-id="a611c-p102">Data within a **Cellset** is retrieved using direct, array-like access. You can "drill down" to a specific member to obtain data about that member. For example, the following code returns the caption of the first member in the first position on the first axis of a cellset named cst:</span></span>

`cst.Axes(0).Positions(0).Members(0).Caption`

<span data-ttu-id="a611c-p103">La notion de cellule active est inexistante dans un ensemble de cellules. En revanche, la propriété [Item](item-property-ado-md-cellset.md) extrait un objet [Cell](cell-object-ado-md.md) spécifique de l'ensemble de cellules. Les arguments de la propriété **Item** déterminent la cellule à extraire. Vous pouvez spécifier la valeur ordinale unique d'une cellule. Vous pouvez également extraire des cellules via leur numéro de position sur chaque axe de l'ensemble de cellules. Pour plus d'informations sur l'extraction des cellules, reportez-vous à la rubrique consacrée à la propriété [Item](item-property-ado-md-cellset.md).</span><span class="sxs-lookup"><span data-stu-id="a611c-p103">There is no notion of a current cell within a cellset. Instead, the [Item](item-property-ado-md-cellset.md) property retrieves a specific [Cell](cell-object-ado-md.md) object from the cellset. The arguments of the **Item** property determine which cell is retrieved. You can specify the unique ordinal value of a cell. You can also retrieve cells by using their position numbers along each axis of the cellset. For more information about retrieving cells, see the [Item](item-property-ado-md-cellset.md) property.</span></span>

<span data-ttu-id="a611c-116">Avec les collections, méthodes et propriétés d'un objet **Cellset**, vous pouvez :</span><span class="sxs-lookup"><span data-stu-id="a611c-116">With the collections, methods, and properties of a **Cellset** object, you can do the following:</span></span>

  - <span data-ttu-id="a611c-117">Associer une connexion ouverte à un objet **Cellset** en définissant sa propriété [ActiveConnection](activeconnection-property-ado-md.md).</span><span class="sxs-lookup"><span data-stu-id="a611c-117">Associate an open connection with a **Cellset** object by setting its [ActiveConnection](activeconnection-property-ado-md.md) property.</span></span>

  - <span data-ttu-id="a611c-118">Exécuter une requête multidimensionnelle et en extraire les résultats à l'aide de la méthode [Open](open-method-ado-md.md).</span><span class="sxs-lookup"><span data-stu-id="a611c-118">Execute and retrieve the results of a multidimensional query with the [Open](open-method-ado-md.md) method.</span></span>

  - <span data-ttu-id="a611c-119">Extraire une **cellule** de l' **ensemble de cellules** à l'aide de la propriété [Item](item-property-ado-md-cellset.md).</span><span class="sxs-lookup"><span data-stu-id="a611c-119">Retrieve a **Cell** from the **Cellset** with the [Item](item-property-ado-md-cellset.md) property.</span></span>

  - <span data-ttu-id="a611c-120">Renvoyer les objets [Axis](axis-object-ado-md.md) définissant l' **ensemble de cellules** à l'aide de la collection [Axes](axes-collection-ado-md.md).</span><span class="sxs-lookup"><span data-stu-id="a611c-120">Return the [Axis](axis-object-ado-md.md) objects that define the **Cellset** with the [Axes](axes-collection-ado-md.md) collection.</span></span>

  - <span data-ttu-id="a611c-121">Extraire les informations relatives aux dimensions utilisées pour filtrer les données de l' **ensemble de cellules** à l'aide de la propriété [FilterAxis](filteraxis-property-ado-md.md).</span><span class="sxs-lookup"><span data-stu-id="a611c-121">Retrieve information about the dimensions used to filter the data in the **Cellset** with the [FilterAxis](filteraxis-property-ado-md.md) property.</span></span>

  - <span data-ttu-id="a611c-122">Renvoyer ou spécifier la requête utilisée pour définir l' **ensemble de cellules** à l'aide de la propriété [Source](source-property-ado-md.md).</span><span class="sxs-lookup"><span data-stu-id="a611c-122">Return or specify the query used to define the **Cellset** with the [Source](source-property-ado-md.md) property.</span></span>

  - <span data-ttu-id="a611c-123">Renvoyer l'état actuel de l' **ensemble de cellules** (ouvert, fermé, en cours d'exécution ou de connexion) à l'aide de la propriété [State](state-property-ado-md.md).</span><span class="sxs-lookup"><span data-stu-id="a611c-123">Return the current state of the **Cellset** (open, closed, executing, or connecting) with the [State](state-property-ado-md.md) property.</span></span>

  - <span data-ttu-id="a611c-124">Fermer un **ensemble de cellules** ouvert à l'aide de la méthode [Close](close-method-ado-md.md).</span><span class="sxs-lookup"><span data-stu-id="a611c-124">Close an open **Cellset** with the [Close](close-method-ado-md.md) method.</span></span>

  - <span data-ttu-id="a611c-125">Extraire les informations spécifiques au fournisseur relatives à l' **ensemble de cellules** à l'aide de la collection ADO standard [Properties](properties-collection-ado.md).</span><span class="sxs-lookup"><span data-stu-id="a611c-125">Retrieve provider-specific information about the **Cellset** with the standard ADO [Properties](properties-collection-ado.md) collection.</span></span>

