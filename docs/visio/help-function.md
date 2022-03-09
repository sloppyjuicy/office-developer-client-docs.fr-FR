---
title: HELP, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251436
ms.localizationpriority: medium
ms.assetid: 5b358c38-6ed1-3fbe-c1d1-1a56ebbaa870
description: Ouvre un fichier d’aide HTML avec le mot clé spécifique dans la zone de recherche.
ms.openlocfilehash: bbe63ee7b514561b20803067d9c7c77470c7680f
ms.sourcegitcommit: f8dc13ccaadfbd6d3783c3b291d998d5255a5f38
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2022
ms.locfileid: "63405155"
---
# <a name="help-function"></a>Fonction HELP

Ouvre un fichier d’aide HTML avec le mot clé  *spécifique dans la* **zone de** recherche.
  
## <a name="syntax"></a>Syntaxe

HELP( » ***filename.chm!keyword*** « )
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| *filename.chm!keyword* <br/> |Requis  <br/> |**String** <br/> | Nom du fichier d’aide et mot clé à rechercher. |

## <a name="remarks"></a>Remarques

Si aucun  *mot clé*  n’est spécifié, la fonction HELP ouvre la page de contenu du fichier d’aide.
  
## <a name="example"></a>Exemple

HELP(« visio.chm!shapesheet »)
  
Ouvre le fichier d’aide Visio et affiche une liste de la ou des rubriques dont le mot clé est « shapesheet ».
  