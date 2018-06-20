---
title: LangID, cellule (section Annotation)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60048
localization_priority: Normal
ms.assetid: b6f5ea5e-b350-0817-d631-f059b9b95c23
description: Indique la langue dans laquelle le commentaire a été entré.
ms.openlocfilehash: 0de5ed8136a3fb1bbdca9fea0ebb5894e62cf907
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788901"
---
# <a name="langid-cell-annotation-section"></a>LangID, cellule (section Annotation)

Indique la langue dans laquelle le commentaire a été entré.
  
> [!NOTE]
> Cette cellule est utilisée pour le suivi des commentaires uniquement lors de l’ouverture d’un fichier .vsd dans Microsoft Visio 2013 ou lors de l’enregistrement d’un fichier .vsdx au format de fichier .vsd. Il n’est pas utilisé pour le suivi des commentaires dans des documents .vsdx dans Visio 2013. 
  
## <a name="remarks"></a>Remarques

Cette valeur est le paramètre régional ID (LCID) de la langue qui est active dans la barre de langue lorsque le commentaire a été entré. Pour obtenir la liste des langues prises en charge par les applications Microsoft Office, consultez la rubrique de la cellule (Section Document Properties) [DocLangID](doclangid-cell-document-properties-section.md) . 
  
Pour obtenir une référence à la cellule LangID par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | Annotation.LangID [ *i* ] où *i* = < 1 >, 2, 3...  <br/> |
   
Pour obtenir une référence à la cellule LangID par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionAnnotation** <br/> |
| Index de la ligne :  <br/> |**visRowAnnotation** +  *i* où *i* = 0, 1, 2...  <br/> |
| Index de la cellule :  <br/> |**visAnnotationLangID** <br/> |
   

