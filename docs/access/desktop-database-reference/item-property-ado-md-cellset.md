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
# <a name="item-property-ado-md-cellset"></a>Item, propriété (Ensemble de cellules ADO MD)

**S’applique à**: Access 2013, Office 2013

Permet d'extraire une cellule d'un ensemble de cellules à l'aide de ses coordonnées.

## <a name="syntax"></a>Syntaxe

Définir la*cellule* = *ensemble de cellules*. Élément (*Positions*)

## <a name="parameters"></a>Paramètres

- *Positions*

- Un **tableau** **variable** de valeurs qui spécifient une cellule de manière unique. *Positions* peut être une des options suivantes :
    
  - Un tableau de numéros de positions
    
  - Un tableau de noms de membres
    
  - La position ordinale

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


