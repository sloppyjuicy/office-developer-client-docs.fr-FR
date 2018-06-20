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
description: Contient les informations d’un élément de données de forme unique associé à une forme. Une forme contient une ligne de données de forme pour chaque élément de données de forme. Lignes de données de forme sont nommées Prop.nom et contiennent les cellules suivantes. Pour plus d’informations, consultez les rubriques de la cellule spécifique.
ms.openlocfilehash: 7bf7eafd1869aa3c3ee03efbde30560cdaaeb302
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789621"
---
# <a name="shape-data-row-shape-data-section"></a>Shape Data, ligne (section Shape Data)

Contient les informations d’un élément de données de forme unique associé à une forme. Une forme contient une ligne de données de forme pour chaque élément de données de forme. Lignes de données de forme sont nommées Prop.nom et contiennent les cellules suivantes. Pour plus d’informations, consultez les rubriques de la cellule spécifique.
  
|**Cell**|**Description**|
|:-----|:-----|
|[Étiquette](label-cell-shape-data-section.md) <br/> |Indique l’intitulé qui s’affiche dans la fenêtre ou la boîte de dialogue **Données de forme** .  <br/> |
|[Prompt](prompt-cell-shape-data-section.md) <br/> |Spécifie le texte descriptif ou d’instructions qui s’affiche dans la boîte de dialogue **Données de forme** ou lorsque l’élément est sélectionné.  <br/> |
|[Type](type-cell-shape-data-section.md) <br/> |Indique le type de données de la valeur de l'élément de données de forme : chaîne (0), liste fixe (1), nombre (2), valeur booléenne (3), liste de variables (4), date ou heure (5), durée (6) ou devise (7).  <br/> |
|[Format](format-cell-shape-data-section.md) <br/> |Indique la mise en forme d'un élément de données de forme.  <br/> |
|[Valeur](value-cell-shape-data-section.md) <br/> |Contient la valeur de l’élément entré dans la fenêtre ou la boîte de dialogue **Données de forme** .  <br/> |
|[SortKey](sortkey-cell-shape-data-section.md) <br/> |Spécifie un critère de tri des éléments dans la boîte de dialogue **Données de forme** zone ou la fenêtre.  <br/> |
|[Invisible](invisible-cell-shape-data-section.md) <br/> |Spécifie si l’élément de données de forme est visible dans la fenêtre ou la boîte de dialogue **Données de forme** . TRUE ne = pas visible ; FALSE = visible.  <br/> |
|[Demandez à](ask-cell-shape-data-section.md) <br/> |Détermine si un utilisateur est invité à entrer les éléments de données d'une forme lorsqu'une occurrence est créée ou lorsque la forme est dupliquée ou copiée.  <br/> |
|[ID de langue](langid-cell-shape-data-section.md) <br/> |Indique la langue d'affichage de l'élément de données de forme Value.  <br/> |
|[Calendrier](calendar-cell-miscellaneous-section.md) <br/> |Indique le type de calendrier utilisé lorsque le Type d'un élément de données de forme est Date.  <br/> |
   
## <a name="remarks"></a>Remarques

 Vous pouvez ajouter autant de propriétés.  *nom de* lignes que vous le souhaitez, assigner des noms explicites aux lignes et définir des valeurs de cellule. Pour ajouter un élément de données de forme à une section Shape Data existante, cliquez sur une ligne, cliquez sur **Insérer une ligne** dans le menu contextuel. 
  
Vous pouvez référencer ces cellules par leur nom de ligne, qui s’affiche dans une fenêtre feuille ShapeSheet en texte rouge. Pour assigner des noms explicites aux propriétés. *nom de* lignes, cliquez sur la ligne, puis tapez un nom tel que *prix* , par exemple, pour créer le nom de ligne Prop.prix. Vous pouvez ensuite référencer la cellule Label en utilisant Prop.prix.Label. 
  
Le nom de ligne que vous entrez doit être unique dans la section.
  

