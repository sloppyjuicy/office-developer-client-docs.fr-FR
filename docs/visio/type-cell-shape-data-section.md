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
ms.openlocfilehash: e5471dcc1ed487a5992779f1faa4763887bebb2a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789950"
---
# <a name="type-cell-shape-data-section"></a>Type, cellule (section Shape Data)

Indique le type des données de forme.
  
|**Valeur**|**Description**|**Constante d’Automation**|
|:-----|:-----|:-----|
|0  <br/> |Chaîne. Valeur par défaut.  <br/> |**visPropTypeString** <br/> |
|1  <br/> |Liste fixe. Affiche les éléments de liste dans une liste déroulante zone dans la boîte de dialogue **Définir les données de forme** . Spécifiez les éléments de liste dans la cellule Format. Les utilisateurs peuvent sélectionner qu’un seul élément dans la liste.  <br/> |**visPropTypeListFix** <br/> |
|2  <br/> |Nombre. Inclut les valeurs de date, d'heure, de durée ainsi que les valeurs monétaires, les échelles, les cotes et les angles. Entrez un modèle de format dans la cellule Format.  <br/> |**visPropTypeNumber** <br/> |
|3  <br/> |Boolean. Affiche true et False comme éléments que les utilisateurs peuvent sélectionner dans une zone de liste déroulante dans la boîte de dialogue **Définir les données de forme** .  <br/> |**visPropTypeBool** <br/> |
|4  <br/> |Liste de variables. Affiche les éléments de liste dans une liste déroulante zone dans la boîte de dialogue **Définir les données de forme** . Spécifiez les éléments de liste dans la cellule Format. Les utilisateurs peuvent sélectionner un élément de liste, ou entrez un nouvel élément est ajouté à la liste actuelle dans la cellule Format.  <br/> |**visPropTypeListVar** <br/> |
|5  <br/> |Valeur de date ou d'heure. Affiche les jours, les mois et les années ou les secondes, les minutes et les heures ou encore une date et une heure en même temps. Entrez un modèle de format dans la cellule Format.  <br/> |**visPropTypeDate** <br/> |
|6  <br/> |Valeur de durée. Affiche le temps écoulé. Entrez un modèle de format dans la cellule Format.  <br/> |**visPropTypeDuration** <br/> |
|7  <br/> |Valeur monétaire. Utilise les paramètres régionaux actuels de votre système d'exploitation. Entrez un modèle de format dans la cellule Format.  <br/> |**visPropTypeCurrency** <br/> |
   
## <a name="remarks"></a>Note

Pour obtenir une référence à la cellule Type par un nom à partir d’une autre formule ou d’un programme en faisant appel à la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
|Nom de la cellule :  <br/> |Propriétés. *Nom* . Type de propriétés où.  *Name* est le nom de ligne  <br/> |
   
Pour obtenir une référence à la cellule Type par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
|Index de la section :  <br/> |**visSectionProp** <br/> |
|Index de la ligne :  <br/> |**visRowProp** +  *i* où *i* = 0, 1, 2...  <br/> |
|Index de la cellule :  <br/> |**visCustPropsType** <br/> |
   

