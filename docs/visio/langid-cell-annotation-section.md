---
title: LangID, cellule (section Annotation)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60048
ms.localizationpriority: medium
ms.assetid: b6f5ea5e-b350-0817-d631-f059b9b95c23
description: Indique la langue dans laquelle le commentaire a été entré.
ms.openlocfilehash: 8874d48ca5b4eb7957b5d6ad6a45835537ba22b5
ms.sourcegitcommit: 7b410a51d1e8c97e9cce8d4aa75074162b7d9485
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/12/2022
ms.locfileid: "63447647"
---
# <a name="langid-cell-annotation-section"></a>LangID, cellule (section Annotation)

Indique la langue dans laquelle le commentaire a été entré.
  
> [!NOTE]
> Cette cellule est utilisée pour suivre les commentaires uniquement lors de l’ouverture d’un fichier .vsd dans Microsoft Visio 2013 ou lors de l’enregistrement d’un fichier .vsdx au format de fichier .vsd. Il n’est pas utilisé pour le suivi des commentaires dans les documents .vsdx Visio 2013. 
  
## <a name="remarks"></a>Remarques

Cette valeur est l’ID de paramètres régionaux (LCID) de la langue active dans la barre de langue lorsque le commentaire a été entré. Pour une liste des langues prises en charge par les applications Microsoft Office, reportez-vous à la rubrique [DocLangID](doclangid-cell-document-properties-section.md) (section Document Properties). 
  
Pour obtenir une référence à la cellule LangID par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
||Valeur |
|:-----|:-----|
| **Nom de cellule :**  <br/> | Annotation.LangID[  *i*  ] où  *i*  = <1>, 2, 3... |
   
Pour obtenir une référence à la cellule LangID à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
||Valeur |
|:-----|:-----|
| **Index de la section :**  <br/> |**visSectionAnnotation** <br/> |
| **Index de la ligne :**  <br/> |**visRowAnnotation** +   *i* où *i* = 0, 1, 2... |
| **Index de la cellule :**  <br/> |**visAnnotationLangID** <br/> |
   

