---
title: HELP, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251436
localization_priority: Normal
ms.assetid: 5b358c38-6ed1-3fbe-c1d1-1a56ebbaa870
description: Ouvre un fichier d'aide HTML avec le mot clé spécifié dans la zone de recherche.
ms.openlocfilehash: 639d10bf489d1ad09aef1522d3cbc743bbe66f6f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329973"
---
# <a name="help-function"></a>Fonction HELP

Ouvre un fichier d'aide HTML avec le *mot clé* spécifié dans la zone de **recherche** . 
  
## <a name="syntax"></a>Syntaxe

HELP ("* * *filename. chm! Keyword* * *") 
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _nom de fichier. chm! mot clé_ <br/> |Obligatoire  <br/> |**String** <br/> | Nom du fichier d’aide et mot clé à rechercher.  <br/> |
   
## <a name="remarks"></a>Remarques

Si aucun *mot clé* n'est spécifié, la fonction Help ouvre la page de contenu du fichier d'aide. 
  
## <a name="example"></a>Exemple

HELP ("Visio. chm! ShapeSheet") 
  
Ouvre le fichier d’aide Visio et affiche une liste de la ou des rubriques dont le mot clé est « shapesheet ». 
  

