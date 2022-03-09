---
title: Shape Data, ligne (section Shape Data)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251344
ms.localizationpriority: medium
ms.assetid: f3a83496-fccc-9d6a-02b9-60ebaf4911ea
description: Contient les informations d'un seul élément de données de forme associé à une forme. Une forme contient une ligne Shape Data pour chaque élément de données de forme.Les lignes Shape Data sont nommées Prop.nom et contiennent les cellules suivantes. Pour plus de détails, consultez les rubriques spécifiques aux cellules.
ms.openlocfilehash: e55c7d96a609da86ee79242c0287c052b4d5074f
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63379555"
---
# <a name="shape-data-row-shape-data-section"></a>Shape Data Row (Shape Data Section)

Contient les informations d'un seul élément de données de forme associé à une forme. Une forme contient une ligne Shape Data pour chaque élément de données de forme.Les lignes Shape Data sont nommées Prop.nom et contiennent les cellules suivantes. Pour plus de détails, consultez les rubriques spécifiques aux cellules.
  
|**Cell**|**Description**|
|:-----|:-----|
|[Label](label-cell-shape-data-section.md) <br/> |Indique l'intitulé qui s'affiche dans la boîte de dialogue ou fenêtre **Données de forme**. |
|[Prompt](prompt-cell-shape-data-section.md) <br/> |Indique la description ou l'instruction qui est présentée aux utilisateurs dans la boîte de dialogue ou fenêtre **Données de forme** lorsqu'ils sélectionnent l'élément. |
|[Type (Type)](type-cell-shape-data-section.md) <br/> |Indique le type de données de la valeur de l'élément de données de forme : chaîne (0), liste fixe (1), nombre (2), valeur booléenne (3), liste de variables (4), date ou heure (5), durée (6) ou devise (7). |
|[Format](format-cell-shape-data-section.md) <br/> |Indique la mise en forme d'un élément de données de forme. |
|[Valeur](value-cell-shape-data-section.md) <br/> |Contient la valeur de l'élément de données de forme telle qu'elle a été entrée dans la boîte de dialogue ou fenêtre **Données de forme**. |
|[SortKey](sortkey-cell-shape-data-section.md) <br/> |Indique le critère de tri des éléments de la boîte de dialogue ou fenêtre **Données de forme**. |
|[Invisible](invisible-cell-shape-data-section.md) <br/> |Indique si l'élément de données de forme est visible dans la boîte de dialogue ou fenêtre **Données de forme** : TRUE = invisible ; FALSE = visible. |
|[Ask](ask-cell-shape-data-section.md) <br/> |Détermine si un utilisateur est invité à entrer les éléments de données d'une forme lorsqu'une occurrence est créée ou lorsque la forme est dupliquée ou copiée. |
|[LangID](langid-cell-shape-data-section.md) <br/> |Indique la langue d'affichage de l'élément de données de forme Value. |
|[Calendar](calendar-cell-miscellaneous-section.md) <br/> |Indique le type de calendrier utilisé lorsque le Type d'un élément de données de forme est Date. |

## <a name="remarks"></a>Remarques

 Vous pouvez ajouter autant de prop.  *nommez*  les lignes selon vos besoins, attribuez des noms significatifs aux lignes et définissez des valeurs de cellule. Pour ajouter un élément de données de forme à une section Shape Data existante, cliquez avec le bouton droit de la souris, puis cliquez sur **Insérer une ligne** dans le menu contextuel.
  
Vous pouvez désigner ces cellules à l'aide de leur nom de ligne, qui apparaît en rouge dans la fenêtre Feuille ShapeSheet. Pour attribuer des noms significatifs aux lignes Prop. *name*  , cliquez sur la ligne, puis tapez un nom tel que *Price*, par exemple, pour créer le nom de ligne Prop.Price. Vous pouvez alors faire référence à la cellule Label en utilisant Prop.Prix.Label.
  
Le nom de ligne que vous entrez doit être unique dans la section.
  