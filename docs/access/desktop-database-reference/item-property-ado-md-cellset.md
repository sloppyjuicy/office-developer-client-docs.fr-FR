---
title: Item, propriété (Ensemble de cellules ADO MD)
TOCTitle: Item Property (ADO MD Cellset)
ms:assetid: 47510643-47af-0bfd-dc1f-ab984057bcd3
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249220(v=office.15)
ms:contentKeyID: 48544595
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d4f2f67daf4bf072037fac07ecdc3cd163904818
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25883798"
---
# <a name="item-property-ado-md-cellset"></a><span data-ttu-id="669a3-102">Item, propriété (Ensemble de cellules ADO MD)</span><span class="sxs-lookup"><span data-stu-id="669a3-102">Item Property (ADO MD Cellset)</span></span>

<span data-ttu-id="669a3-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="669a3-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="669a3-104">Permet d'extraire une cellule d'un ensemble de cellules à l'aide de ses coordonnées.</span><span class="sxs-lookup"><span data-stu-id="669a3-104">Retrieves a cell from a cellset using its coordinates.</span></span>

## <a name="syntax"></a><span data-ttu-id="669a3-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="669a3-105">Syntax</span></span>

<span data-ttu-id="669a3-106">Définir la*cellule* = *ensemble de cellules*. Élément (*Positions*)</span><span class="sxs-lookup"><span data-stu-id="669a3-106">Set*Cell* = *Cellset*.Item (*Positions*)</span></span>

## <a name="parameters"></a><span data-ttu-id="669a3-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="669a3-107">Parameters</span></span>

- <span data-ttu-id="669a3-108">*Positions*</span><span class="sxs-lookup"><span data-stu-id="669a3-108">*Positions*</span></span>

- <span data-ttu-id="669a3-109">Un **tableau** **variable** de valeurs qui spécifient une cellule de manière unique.</span><span class="sxs-lookup"><span data-stu-id="669a3-109">A **Variant** **Array** of values that uniquely specify a cell.</span></span> <span data-ttu-id="669a3-110">*Positions* peut être une des options suivantes :</span><span class="sxs-lookup"><span data-stu-id="669a3-110">*Positions* can be one of the following:</span></span>
    
  - <span data-ttu-id="669a3-111">Un tableau de numéros de positions</span><span class="sxs-lookup"><span data-stu-id="669a3-111">An array of position numbers</span></span>
    
  - <span data-ttu-id="669a3-112">Un tableau de noms de membres</span><span class="sxs-lookup"><span data-stu-id="669a3-112">An array of member names</span></span>
    
  - <span data-ttu-id="669a3-113">La position ordinale</span><span class="sxs-lookup"><span data-stu-id="669a3-113">The ordinal position</span></span>

## <a name="remarks"></a><span data-ttu-id="669a3-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="669a3-114">Remarks</span></span>

<span data-ttu-id="669a3-115">La propriété **Item** permet de renvoyer un objet [Cell](cell-object-ado-md.md) d'un objet [Cellset](cellset-object-ado-md.md).</span><span class="sxs-lookup"><span data-stu-id="669a3-115">Use the **Item** property to return a [Cell](cell-object-ado-md.md) object within a [Cellset](cellset-object-ado-md.md) object.</span></span> <span data-ttu-id="669a3-116">Si la propriété **Item** ne peut pas trouver la cellule correspondant à l’argument *Positions* , une erreur se produit.</span><span class="sxs-lookup"><span data-stu-id="669a3-116">If the **Item** property cannot find the cell corresponding to the *Positions* argument, an error occurs.</span></span>

<span data-ttu-id="669a3-p103">La propriété **Item** est la propriété par défaut de l'objet **Cellset**. Les syntaxes suivantes sont interchangeables :</span><span class="sxs-lookup"><span data-stu-id="669a3-p103">The **Item** property is the default property for the **Cellset** object. The following syntax forms are interchangeable:</span></span>

```vb
    Cellset.Item ( Positions )
    Cellset ( Positions )
```

<span data-ttu-id="669a3-119">L’argument *Positions* spécifie la cellule à renvoyer.</span><span class="sxs-lookup"><span data-stu-id="669a3-119">The *Positions* argument specifies which cell to return.</span></span> <span data-ttu-id="669a3-120">Vous pouvez spécifier la cellule par position ordinale ou par la position le long de chaque axe.</span><span class="sxs-lookup"><span data-stu-id="669a3-120">You can specify the cell by ordinal position or by the position along each axis.</span></span> <span data-ttu-id="669a3-121">Dans ce second cas, vous pouvez spécifier la valeur numérique de la position ou les noms des membres de chaque position.</span><span class="sxs-lookup"><span data-stu-id="669a3-121">When specifying the cell by position along each axis, you can specify the numeric value of the position or the names of the members for each position.</span></span>

<span data-ttu-id="669a3-p105">La position ordinale est un numéro qui identifie une cellule de manière unique dans un **ensemble de cellules**. En théorie, les cellules sont numérotées dans un **ensemble de cellules** comme si ce dernier\*\*\*\* était un tableau *p*-dimensionnel, où *p* correspond au nombre des axes. Les cellules sont classées par ordre ligne-majeur.</span><span class="sxs-lookup"><span data-stu-id="669a3-p105">The ordinal position is a number that uniquely identifies one cell within the **Cellset**. Conceptually, cells are numbered in a **Cellset** as if the **Cellset** were a *p*-dimensional array, where *p* is the number of axes. Cells are addressed in row-major order.</span></span>

<span data-ttu-id="669a3-p106">Si les noms de membres sont transmis sous la forme de chaînes à la propriété **Item**, les membres doivent être répertoriés par ordre croissant d'identificateurs d'axe numériques. Sur un axe, les membres doivent être classés par ordre croissant d'imbrication des dimensions. En d'autres termes, le membre de la dimension externe arrive en premier, suivi par les membres des dimensions internes. Chaque dimension doit être représentée par une chaîne séparée et la liste des chaînes de membres doit être séparée par des virgules.</span><span class="sxs-lookup"><span data-stu-id="669a3-p106">If member names are passed as strings to **Item**, the members must be listed in increasing order of the numeric axis identifiers. Within an axis, the members must be listed in increasing order of dimension nesting — that is, the outermost dimension's member comes first, followed by members of inner dimensions. Each dimension should be represented by a separate string, and the list of member strings should be separated by commas.</span></span>


> [!NOTE]
> <span data-ttu-id="669a3-p107">[!REMARQUE] L'extraction des cellules par nom de membre n'est peut-être pas prise en charge par votre fournisseur de données. Reportez-vous à la documentation de ce dernier pour plus d'informations.</span><span class="sxs-lookup"><span data-stu-id="669a3-p107">Retrieving cells by member name may not be supported by your data provider. See the documentation for your provider for more information.</span></span>


