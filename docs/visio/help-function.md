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
description: Ouvre un fichier d’aide HTML avec le mot clé spécifique dans la zone de recherche.
ms.openlocfilehash: 639d10bf489d1ad09aef1522d3cbc743bbe66f6f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431336"
---
# <a name="help-function"></a>Fonction HELP

Ouvre un fichier d’aide HTML avec le mot clé spécifique  *dans*  la **zone de** recherche. 
  
## <a name="syntax"></a>Syntaxe

HELP( » ** *filename.chm!keyword* ** « ) 
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _filename.chm!keyword_ <br/> |Obligatoire  <br/> |**String** <br/> | Nom du fichier d’aide et mot clé à rechercher.  <br/> |
   
## <a name="remarks"></a>Remarques

Si aucun  *mot clé*  n’est spécifié, la fonction HELP ouvre la page de contenu du fichier d’aide. 
  
## <a name="example"></a>Exemple

HELP(« visio.chm!shapesheet ») 
  
Ouvre le fichier d’aide Visio et affiche une liste de la ou des rubriques dont le mot clé est « shapesheet ». 
  

