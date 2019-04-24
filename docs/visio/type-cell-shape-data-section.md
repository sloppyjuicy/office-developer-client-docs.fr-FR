---
title: Type, cellule (section Shape Data)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1055
localization_priority: Normal
ms.assetid: 1e24a906-83ce-32d2-5d7b-ba6dd6eea2d3
description: Indique le type des données de forme.
ms.openlocfilehash: c2d38b521a8597a4582a4145ad808b0c0e26ff0a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32350896"
---
# <a name="type-cell-shape-data-section"></a>Type, cellule (section Shape Data)

Indique le type des données de forme.
  
|**Value**|**Description**|**Constante d'automation**|
|:-----|:-----|:-----|
|0  <br/> |Chaîne. Valeur par défaut.  <br/> |**visPropTypeString** <br/> |
|0,1  <br/> |Liste fixe. Affiche les éléments de la liste dans une zone de liste déroulante fixe de la boîte de dialogue **Définir les données de forme**. Indiquez les éléments de la liste dans la cellule Format. Les utilisateurs ne peuvent sélectionner qu’un seul élément dans la liste.<br/> |**visPropTypeListFix** <br/> |
|n°2  <br/> |Nombre. Inclut les valeurs de date, d'heure, de durée ainsi que les valeurs monétaires, les échelles, les cotes et les angles. Entrez un modèle de format dans la cellule Format.  <br/> |**visPropTypeNumber** <br/> |
|3  <br/> |Booléen. Affiche TRUE et FALSE comme éléments pouvant être sélectionnés par l’utilisateur dans la zone de liste déroulante fixe de la boîte de dialogue **Définir les données de forme**.<br/> |**visPropTypeBool** <br/> |
|4  <br/> |Liste de variables. Affiche les éléments de la liste dans une zone de liste déroulante fixe de la boîte de dialogue **Définir les données de forme**. Indiquez les éléments de la liste dans la cellule Format. Les utilisateurs peuvent sélectionner un élément de la liste ou entrer un nouvel élément, qui est alors ajouté à la liste actuelle dans la cellule Format.<br/> |**visPropTypeListVar** <br/> |
|disque  <br/> |Valeur de date ou d'heure. Affiche les jours, les mois et les années ou les secondes, les minutes et les heures ou encore une date et une heure en même temps. Entrez un modèle de format dans la cellule Format.  <br/> |**visPropTypeDate** <br/> |
|6.x  <br/> |Valeur de durée. Affiche le temps écoulé. Entrez un modèle de format dans la cellule Format.  <br/> |**visPropTypeDuration** <br/> |
|7j/7  <br/> |Valeur monétaire. Utilise les paramètres régionaux actuels de votre système d'exploitation. Entrez un modèle de format dans la cellule Format.  <br/> |**visPropTypeCurrency** <br/> |
   
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule Type par un nom dans une autre formule ou dans un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
|Nom de cellule :  <br/> |Hélice. *Nom* . Type où prop.  *Name* est le nom de la ligne  <br/> |
   
Pour obtenir une référence à la cellule Type par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
|Index de la section :  <br/> |**visSectionProp** <br/> |
|Index de la ligne :  <br/> |**visRowProp** +  *i* où *i* = 0, 1, 2...  <br/> |
|Index de la cellule :  <br/> |**visCustPropsType** <br/> |
   

