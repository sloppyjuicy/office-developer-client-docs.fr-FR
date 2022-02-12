---
title: À propos des références de cellules
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
f1_keywords:
- Vis_DSS.chm82251827
ms.localizationpriority: medium
ms.assetid: e6a9aceb-90d7-fb53-eaf4-416a1ae2a98b
description: Vous pouvez créer des relations de dépendance entre des formules à l'aide de références de cellule ShapeSheet. Les références de cellule vous permettent de calculer la valeur d'une cellule en fonction de celle d'une autre. Si, par exemple, la cellule Width d'une forme contient une formule permettant de calculer la largeur de la forme en se référant à la valeur de la cellule Height, les proportions de la forme sont conservées si un utilisateur redimensionne la forme verticalement.
ms.openlocfilehash: b857eb163dcd729638d9b691809294392c99e254
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62776136"
---
# <a name="about-cell-references"></a>À propos des références de cellules

Vous pouvez créer des relations de dépendance entre des formules à l'aide de références de cellule ShapeSheet. Les références de cellule vous permettent de calculer la valeur d'une cellule en fonction de celle d'une autre. Si, par exemple, la cellule Width d'une forme contient une formule permettant de calculer la largeur de la forme en se référant à la valeur de la cellule Height, les proportions de la forme sont conservées si un utilisateur redimensionne la forme verticalement.
  
Dans la formule d’une cellule, vous pouvez faire référence à une cellule de la même forme ou d’un autre objet, par exemple un document ou une page, afin que Microsoft Visio calcule la valeur d’une cellule en fonction de celle de l’autre.
  
## <a name="what-cell-references-can-include"></a>Ce que peuvent inclure les références de cellule

Les références de cellule peuvent inclure des noms ou des ID de forme. Il est toujours possible de faire référence à une forme par son ID, que la forme soit nommée ou non. Si une forme ne possède pas de nom, elle est par défaut identifiée par le nom Sheet. *i*  , où  *i est l’ID*  de forme. L'ID est attribué lors de la création de la forme et ne change pas à moins que vous ne déplaciez la forme vers une autre page ou un autre document. Si plusieurs formes de la même page portent le même nom, vous devez inclure l'ID attribué automatiquement. 
  
## <a name="cell-reference-syntax-and-examples"></a>Syntaxe des références de cellule et exemples

La syntaxe à utiliser et la possibilité ou non de renvoyer à une cellule par un nom dépend de la relation entre les deux objets. Les règles générales ci-dessous s'appliquent.
  
- Si une forme est une homologue de celle dont vous modifiez la formule, vous pouvez y faire référence par son nom. Si la forme homologue est un groupe, vous pouvez utiliser un nom pour faire référence au groupe, mais non à ses formes membres. Vous ne pouvez pas non plus faire référence au parent d'une forme ni aux homologues de son parent par leurs noms.
    
- Vous pouvez utiliser la syntaxe Sheet.ID pour faire référence à toute forme de la page, qu'elle appartienne ou non à un groupe et qu'elle soit ou non le parent d'une autre forme.
    
- Les noms qui contiennent des caractères non standard doivent être entourés d'apostrophes. Les apostrophes à l'intérieur d'un nom qui n'est pas standard doivent être précédées d'une autre apostrophe.
    
|**Pour faire référence à une cellule**|**Utilisez cette syntaxe**|**Exemple**|
|:-----|:-----|:-----|
|De la même forme  <br/> | CellName  <br/> | Largeur  <br/> |
| D'une forme, d'un groupe ou d'un repère  <br/> | Shapename! CellName  <br/> | Étoile! Angle  <br/> |
| D'une forme, d'un groupe ou d'un repère nommé alors qu'il existe au même niveau plusieurs formes du même nom  <br/> | Shapename.ID ! CellName  <br/> | Executive.2! Height  <br/> |
| D'une colonne nommée avec des lignes indexées  <br/> | Section.Column[index]  <br/> | Char.Font[3]  <br/> |
| D'une colonne non nommée avec des lignes indexées  <br/> | Section.ColumnIndex  <br/> | Scratch.A5  <br/> |
| De toute forme, page, forme de base ou style  <br/> | Sheet.ID ! CellName  <br/> | Sheet.8! FillForegnd  <br/> |
| D'une forme de base  <br/> | Masters[MasterName]! SheetName! CellReference  <br/> | Masters[Gear]! C’est le cas ! Geometry1.X1  <br/> |
| De la page ou de la page de forme de base sur laquelle se trouve l'objet  <br/> | ThePage! CellReference  <br/> | ThePage! User.Vanishing_Point  <br/> |
| D'une autre page du document  <br/> | Pages[PageName]! SheetName! CellReference  <br/> | Pages[Page-3]! Sheet.4! BeginX  <br/> |
| D'un style  <br/> | Styles ! SheetName! CellReference  <br/> | Styles ! Responsable ! LineColor  <br/> |
| Du document  <br/> | TheDoc! CellReference  <br/> | TheDoc! PreviewQuality  <br/> |
| D'une forme, d'une page, d'une forme de base, d'un document ou d'un style dont le nom n'est pas standard | « Sheetname » ! CellName  <br/> | '1-D'! LineColor  <br/> |
   

