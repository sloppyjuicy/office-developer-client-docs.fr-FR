---
title: Item, propriété (Ensemble de cellules ADO MD)
TOCTitle: Item property (ADO MD Cellset)
ms:assetid: 47510643-47af-0bfd-dc1f-ab984057bcd3
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249220(v=office.15)
ms:contentKeyID: 48544595
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 99f381ad2f38dc7d2c467ed1e40e4084032006d1
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28707016"
---
# <a name="item-property-ado-md-cellset"></a>Item, propriété (Ensemble de cellules ADO MD)

**S’applique à**: Access 2013, Office 2013

Permet d'extraire une cellule d'un ensemble de cellules à l'aide de ses coordonnées.

## <a name="syntax"></a>Syntaxe

Définir la*cellule* = *ensemble de cellules*. Élément (*Positions*)

## <a name="parameters"></a>Parameters

|Paramètre|Description|
|:--------|:----------|
|*Positions* |Un **tableau de type Variant** de valeurs qui spécifient une cellule de manière unique. *Positions* peut être une des options suivantes :<br/><br/>-Un tableau de numéros de positions<br/>-Un tableau de noms de membres<br/>-La position ordinale |

## <a name="remarks"></a>Remarques

La propriété **Item** permet de renvoyer un objet [Cell](cell-object-ado-md.md) d'un objet [Cellset](cellset-object-ado-md.md). Si la propriété **Item** ne peut pas trouver la cellule correspondant à l’argument *Positions* , une erreur se produit.

La propriété **Item** est la propriété par défaut de l'objet **Cellset**. Les syntaxes suivantes sont interchangeables :

```vb
    Cellset.Item ( Positions )
    Cellset ( Positions )
```

L’argument *Positions* spécifie la cellule à renvoyer. Vous pouvez spécifier la cellule par position ordinale ou par la position le long de chaque axe. Dans ce second cas, vous pouvez spécifier la valeur numérique de la position ou les noms des membres de chaque position.

La position ordinale est un numéro qui identifie une cellule de manière unique dans un **ensemble de cellules**. En théorie, les cellules sont numérotées dans un **ensemble de cellules** comme si ce dernier**** était un tableau *p*-dimensionnel, où *p* correspond au nombre des axes. Les cellules sont classées par ordre ligne-majeur.

Si les noms de membres sont transmis sous la forme de chaînes à la propriété **Item**, les membres doivent être répertoriés par ordre croissant d'identificateurs d'axe numériques. Sur un axe, les membres doivent être classés par ordre croissant d'imbrication des dimensions. En d'autres termes, le membre de la dimension externe arrive en premier, suivi par les membres des dimensions internes. Chaque dimension doit être représentée par une chaîne séparée et la liste des chaînes de membres doit être séparée par des virgules.


> [!NOTE]
> [!REMARQUE] L'extraction des cellules par nom de membre n'est peut-être pas prise en charge par votre fournisseur de données. Reportez-vous à la documentation de ce dernier pour plus d'informations.


