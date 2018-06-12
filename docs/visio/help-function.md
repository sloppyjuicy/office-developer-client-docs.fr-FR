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
description: Ouvre un fichier d’aide HTML avec le mot clé spécifié dans la zone de recherche.
ms.openlocfilehash: 4671b18333bdae953c487662cd880849233df7f5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788768"
---
# <a name="help-function"></a>HELP, fonction

Ouvre un fichier d’aide HTML avec le *mot clé* de spécifié dans la zone de **recherche** . 
  
## <a name="syntax"></a>Syntaxe

AIDE (« ** *nomfichier.chm ! mot clé* ** ») 
  
### <a name="parameters"></a>Paramètres

|**Name**|**Obligatoire/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _nomfichier.chm ! mot clé_ <br/> |Obligatoire  <br/> |**Chaîne** <br/> | Nom du fichier d’aide et mot clé à rechercher.  <br/> |
   
## <a name="remarks"></a>Note

Si aucun *mot clé* n’est spécifié, la fonction HELP ouvre la page contenu du fichier d’aide. 
  
## <a name="example"></a>Exemple

Help("Visio.chm!ShapeSheet") 
  
Ouvre le fichier d’aide Visio et affiche une liste de la ou des rubriques dont le mot clé est « shapesheet ». 
  

