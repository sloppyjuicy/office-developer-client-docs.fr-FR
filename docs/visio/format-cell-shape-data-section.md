---
title: Format, cellule (section Shape Data)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251340
ms.localizationpriority: medium
ms.assetid: c36fc895-5577-59f6-0ff5-5892ca81a58f
description: Définit la mise en forme d'un élément de données de forme qui est une chaîne, une liste fixe, un nombre, une liste variable, une date, une heure ou une monnaie.
ms.openlocfilehash: e57e23525219ea1db515f303830464e7da363876
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59574208"
---
# <a name="format-cell-shape-data-section"></a>Format, cellule (section Shape Data)

Définit la mise en forme d'un élément de données de forme qui est une chaîne, une liste fixe, un nombre, une liste variable, une date, une heure ou une monnaie.
  
## <a name="remarks"></a>Remarques

|**Type de données d'article de forme**|**Valeur**|**Contenu de la cellule Format**|
|:-----|:-----|:-----|
| Chaîne  <br/> | 0  <br/> | Modèle de format approprié pour le type de données.  <br/> |
| Liste fixe  <br/> | 1  <br/> | Éléments de la liste, séparés par des signes deux-points.  <br/> |
| Nombre  <br/> | 2  <br/> | Modèle de format approprié pour le type de données.  <br/> |
| Liste variable  <br/> | 4   <br/> | Éléments de la liste, séparés par des signes deux-points.  <br/> |
| Date ou heure  <br/> | 5  <br/> | Modèle de format approprié pour le type de données.  <br/> |
| Durée  <br/> | 6   <br/> | Modèle de format approprié pour le type de données.  <br/> |
| Devise  <br/> | 7   <br/> | Modèle de format approprié pour le type de données.  <br/> |
   
Un exemple de modèle de format approprié pour le type de données est « 0,000 u », qui fait apparaître le nombre 250 cm sous la forme 250,000 cm. Pour plus d'informations sur les modèles de format, reportez-vous à [À propos des modèles de format](about-format-pictures.md).
  
Un exemple d'éléments spécifiés pour une liste est « Ingénierie;Ressources humaines;Ventes;Marketing ».
  
Les valeurs de date (type = 5) sont affichées au format de date court. Les valeurs monétaires (type = 7) utilisent le paramètre utilisateur actif pour **Symbole monétaire** dans l'onglet **Options régionales** de l'élément **Options régionales et linguistiques** du **Panneau de configuration**.
  
Un nombre (type = 2) peut représenter une cote, un vecteur, un angle, une date, une heure ou une devise. Pour vous assurer qu'un nombre entré est toujours évalué comme une date, une heure ou une devise, utilisez la fonction DATEHEURE ou CY dans la cellule Format au lieu d'un modèle de format.
  
Pour obtenir une référence à la cellule Format par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
| Nom de cellule :  <br/> | Prop.  *nom*  . Format où Prop.  *nom est*  le nom de ligne  <br/> |
   
Pour obtenir une référence à la cellule Format à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionProp** <br/> |
| Index de la ligne :  <br/> |**visRowProp**  +   *i* où *i* = 0, 1, 2...  <br/> |
| Index de la cellule :  <br/> |**visCustPropsFormat** <br/> |
   

