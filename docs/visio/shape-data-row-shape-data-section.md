---
title: Shape Data, ligne (section Shape Data)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251344
localization_priority: Normal
ms.assetid: f3a83496-fccc-9d6a-02b9-60ebaf4911ea
description: Contient les informations d'un seul élément de données de forme associé à une forme. Une forme contient une ligne de données de forme pour chaque élément de données de forme. Les lignes de données de forme sont nommées Prop.name et contiennent les cellules suivantes. Pour plus de détails, consultez les rubriques spécifiques aux cellules.
ms.openlocfilehash: 058f8f180a2eca4736d06dfcc533d81f45150c86
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415396"
---
# <a name="shape-data-row-shape-data-section"></a>Shape Data Row (Shape Data Section)

Contient les informations d'un seul élément de données de forme associé à une forme. Une forme contient une ligne de données de forme pour chaque élément de données de forme. Les lignes de données de forme sont nommées Prop.name et contiennent les cellules suivantes. Pour plus de détails, consultez les rubriques spécifiques aux cellules.
  
|**Cellule**|**Description**|
|:-----|:-----|
|[Label](label-cell-shape-data-section.md) <br/> |Indique l'intitulé qui s'affiche dans la boîte de dialogue ou fenêtre **Données de forme**.  <br/> |
|[Prompt](prompt-cell-shape-data-section.md) <br/> |Indique la description ou l'instruction qui est présentée aux utilisateurs dans la boîte de dialogue ou fenêtre **Données de forme** lorsqu'ils sélectionnent l'élément.  <br/> |
|[Type](type-cell-shape-data-section.md) <br/> |Indique le type de données de la valeur de l'élément de données de forme : chaîne (0), liste fixe (1), nombre (2), valeur booléenne (3), liste de variables (4), date ou heure (5), durée (6) ou devise (7).  <br/> |
|[Format](format-cell-shape-data-section.md) <br/> |Indique la mise en forme d'un élément de données de forme.  <br/> |
|[Valeur](value-cell-shape-data-section.md) <br/> |Contient la valeur de l'élément de données de forme telle qu'elle a été entrée dans la boîte de dialogue ou fenêtre **Données de forme**.  <br/> |
|[SortKey](sortkey-cell-shape-data-section.md) <br/> |Indique le critère de tri des éléments de la boîte de dialogue ou fenêtre **Données de forme**.  <br/> |
|[Visibilité](invisible-cell-shape-data-section.md) <br/> |Indique si l'élément de données de forme est visible dans la boîte de dialogue ou fenêtre **Données de forme** : TRUE = invisible ; FALSE = visible.<br/> |
|[Vous](ask-cell-shape-data-section.md) <br/> |Détermine si un utilisateur est invité à entrer les éléments de données d'une forme lorsqu'une occurrence est créée ou lorsque la forme est dupliquée ou copiée.  <br/> |
|[ID](langid-cell-shape-data-section.md) <br/> |Indique la langue d'affichage de l'élément de données de forme Value.  <br/> |
|[Calendar](calendar-cell-miscellaneous-section.md) <br/> |Indique le type de calendrier utilisé lorsque le Type d'un élément de données de forme est Date.  <br/> |
   
## <a name="remarks"></a>Remarques

 Vous pouvez ajouter autant de prop.  *Nommez* les lignes selon vos besoins, assignez des noms parlants aux lignes et définissez des valeurs de cellule. Pour ajouter un élément de données de forme à une section Shape Data existante, cliquez avec le bouton droit de la souris, puis cliquez sur **Insérer une ligne** dans le menu contextuel. 
  
Vous pouvez désigner ces cellules à l'aide de leur nom de ligne, qui apparaît en rouge dans la fenêtre Feuille ShapeSheet. Pour assigner des noms parlants à prop. *Nommez* des lignes, cliquez sur la ligne, puis tapez un nom tel que *Price* , par exemple, pour créer le nom de ligne prop. Price. Vous pouvez alors faire référence à la cellule Label en utilisant Prop.Prix.Label. 
  
Le nom de ligne que vous entrez doit être unique dans la section.
  

