---
title: ClippingPath Cell (Foreign Image Info Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 0ec70417-5b23-45af-95a0-1b26f6791699
description: Contient une référence à la géométrie du chemin d’accès d’une image.
ms.openlocfilehash: a5f8b32077c8654df4bedb03105a9e874ce06cef
ms.sourcegitcommit: f8dc13ccaadfbd6d3783c3b291d998d5255a5f38
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2022
ms.locfileid: "63404819"
---
# <a name="clippingpath-cell-foreign-image-info-section"></a>ClippingPath Cell (Foreign Image Info Section)

Contient une référence à la géométrie du chemin d’accès d’une image.
  
## <a name="remarks"></a>Remarques

Si la **cellule ClippingPath** pointe vers un chemin d’accès valide, l’image est découpée de sorte que l’image soit restituer à l’intérieur du chemin d’accès. Si la **cellule ClippingPath** est vide ou contient une entrée non valide, l’image est rendue avec un clip rectangulaire, à l’aide des valeurs d’échelle et de décalage.
  
> [!NOTE]
> Seuls les chemins définis par [une section Geometry](geometry-section.md) dans la feuille ShapeSheet de l’image sont des entrées valides pour la **cellule ClippingPath** . Les références de feuille croisée ne peuvent pas être utilisées pour définir un chemin de découpage d’image.
  
Pour obtenir une référence à la cellule **ClippingPath** par un nom à partir d’une autre formule, de l’attribut **N** d’un élément **Cell** ou d’un programme en faisant appel à la propriété **CellsU** , utilisez :
  
||Valeur |
|:-----|:-----|
| **Nom de cellule :**  <br/> | ClippingPath  <br/> |

Pour obtenir une référence à la cellule **ClippingPath** à l’aide d’un index à partir d’un programme, utilisez la **propriété CellsSRC** avec les arguments suivants :
  
||Valeur |
|:-----|:-----|
| **Index de la section :**  <br/> |**visSectionObject** <br/> |
| **Index de la ligne :**  <br/> |**visRowForeign** <br/> |
| **Index de la cellule :**  <br/> |**visFrgnImgClippingPath** <br/> |

## <a name="example"></a>Exemple

Vous pouvez modifier la forme de limite d’une image en ovale en :
  
- Insérez l’image sur la zone de dessin.

- Cliquez avec le bouton droit sur l’image, puis **sélectionnez Afficher la feuille ShapeSheet**.

- Cliquez avec le bouton droit n’importe où dans la feuille ShapeSheet et **sélectionnez Insérer une section**.

- Dans la **boîte de dialogue Insérer une section** , **sélectionnez Geometry** , puis cliquez sur **OK**.

- Dans la nouvelle section Geometry (par exemple, « Geometry2 »), supprimez toutes les lignes sauf une.

- Cliquez avec le bouton droit sur la ligne restante, puis cliquez **sur Modifier le type de ligne**.

- Dans la **boîte de dialogue Modifier le type de** ligne, sélectionnez **Ellipse** , puis cliquez sur **OK**.

- Dans la section **Image étrangère** , définissez la formule de la cellule **ClippingPath** `="Geometry2.Path"` sur, puis acceptez la formule.
