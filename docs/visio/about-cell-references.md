---
title: À propos des références de cellules
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
f1_keywords:
- Vis_DSS.chm82251827
localization_priority: Normal
ms.assetid: e6a9aceb-90d7-fb53-eaf4-416a1ae2a98b
description: Vous pouvez créer des relations de dépendance entre des formules à l'aide de références de cellule ShapeSheet. Les références de cellule vous permettent de calculer la valeur d'une cellule en fonction de celle d'une autre. Si, par exemple, la cellule Width d'une forme contient une formule permettant de calculer la largeur de la forme en se référant à la valeur de la cellule Height, les proportions de la forme sont conservées si un utilisateur redimensionne la forme verticalement.
ms.openlocfilehash: 54c7fd69e2ddaa9350996e2d8c921958a04e34ab
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787987"
---
# <a name="about-cell-references"></a>À propos des références de cellules

Vous pouvez créer des relations de dépendance entre des formules à l'aide de références de cellule ShapeSheet. Les références de cellule vous permettent de calculer la valeur d'une cellule en fonction de celle d'une autre. Si, par exemple, la cellule Width d'une forme contient une formule permettant de calculer la largeur de la forme en se référant à la valeur de la cellule Height, les proportions de la forme sont conservées si un utilisateur redimensionne la forme verticalement.
  
Dans la formule d’une cellule, vous pouvez faire référence à une cellule de la même forme ou d’un autre objet, par exemple un document ou une page, afin que Microsoft Visio calcule la valeur d’une cellule en fonction de celle de l’autre.
  
## <a name="what-cell-references-can-include"></a>Peuvent inclure les références de cellule

Références de cellule peuvent inclure des noms ou des identificateurs (ID) de la forme. Vous pouvez toujours faire référence à une forme dans la page par son ID, si la forme est nommée ou non. Si une forme n’a pas été appelée, son nom par défaut est feuille. *i* , où *i* est l’ID de forme. L’ID est affecté lorsque la forme est créée et qu’il ne change pas, sauf si vous déplacez la forme à une autre page du document. Si plusieurs formes sur une page a le même nom, vous devez inclure l’ID affecté. 
  
## <a name="cell-reference-syntax-and-examples"></a>Syntaxe des références de cellule et exemples

La syntaxe à utiliser et la possibilité ou non de renvoyer à une cellule par un nom dépend de la relation entre les deux objets. Les règles générales ci-dessous s'appliquent.
  
- Si une forme est une homologue de celle dont vous modifiez la formule, vous pouvez y faire référence par son nom. Si la forme homologue est un groupe, vous pouvez utiliser un nom pour faire référence au groupe, mais non à ses formes membres. Vous ne pouvez pas non plus faire référence au parent d'une forme ni aux homologues de son parent par leurs noms.
    
- Vous pouvez utiliser la syntaxe Sheet.ID pour faire référence à toute forme de la page, qu'elle appartienne ou non à un groupe et qu'elle soit ou non le parent d'une autre forme.
    
- Les noms qui contiennent des caractères non standard doivent être entourés d'apostrophes. Les apostrophes à l'intérieur d'un nom qui n'est pas standard doivent être précédées d'une autre apostrophe.
    
|**Pour faire référence à une cellule de**|**Utilisez cette syntaxe**|**Exemple**|
|:-----|:-----|:-----|
|La même forme  <br/> | CellName  <br/> | Width  <br/> |
| Une forme, le groupe ou le guide  <br/> | Argument shapename ! CellName  <br/> | Étoile ! Angle  <br/> |
| Une forme, un groupe ou un guide dans lequel plusieurs formes au même niveau a le même nom  <br/> | Shapename.ID ! CellName  <br/> | Executive.2 ! Hauteur  <br/> |
| Une colonne nommée avec des lignes indexées  <br/> | Section.Column[index]  <br/> | Char.Font[3]  <br/> |
| Une colonne non nommée avec des lignes indexées  <br/> | Section.ColumnIndex  <br/> | Scratch.A5  <br/> |
| N’importe quel forme, page, master ou style  <br/> | Sheet.ID ! CellName  <br/> | Sheet.8 ! FillForegnd  <br/> |
| Une forme de base  <br/> | Formes de base [MasterName] ! SheetName ! CellReference  <br/> | Formes de base [ENGRENAGE] ! Arbre ! Geometry1.X1  <br/> |
| La page ou la page maître sur lequel se trouve l’objet  <br/> | Passe ! CellReference  <br/> | Passe ! User.Vanishing_Point  <br/> |
| Une autre page dans le document  <br/> | Pages [PageName] ! SheetName ! CellReference  <br/> | Pages [Page 3] ! Feuille.4 ! BeginX  <br/> |
| Un style  <br/> | Styles ! SheetName ! CellReference  <br/> | Styles ! Gestionnaire de ! LineColor  <br/> |
| Le document  <br/> | TheDoc ! CellReference  <br/> | TheDoc ! PreviewQuality  <br/> |
| Une forme, page, master, document ou style avec un nom non standard.  <br/> | « Sheetname ! » CellName  <br/> | ' 1-D'! LineColor  <br/> |
   

