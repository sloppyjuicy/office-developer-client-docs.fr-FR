---
title: RUNMACRO, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033809
localization_priority: Normal
ms.assetid: 86b0f071-5e0b-56de-ff5b-63c114ad823a
description: Appelle une macro dans un Microsoft Visual Basic pour Applications (VBA) project.
ms.openlocfilehash: e3dd989956ce9c5f795ae3ef0d8535ab2776d6d7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789586"
---
# <a name="runmacro-function"></a>RUNMACRO, fonction

Appelle une macro dans un Microsoft Visual Basic pour Applications (VBA) project. 
  
## <a name="syntax"></a>Syntaxe

RUNMACRO (** *nommacro* ** [, ** *projname_opt* **]) 
  
### <a name="parameters"></a>Paramètres

|**Name**|**Obligatoire/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _nommacro_ <br/> |Obligatoire  <br/> |**Chaîne** <br/> |Nom de la macro à appeler  <br/> |
| _projname_opt_ <br/> |Facultatif  <br/> |**Chaîne** <br/> | Projet qui contient la macro  <br/> |
   
## <a name="remarks"></a>Note

Si un projet n’est spécifié, Microsoft Visio recherche tous les documents ouverts pour l’un contenant _projname_opt_ et appelle _macroname_ dans ce projet. Si le _nomproj_facult_ est omis ou nul (« »), _nommacro_ est supposé pour être dans le projet VBA du document contenant la formule RUNMACRO calculée. 
  
La fonction RUNMACRO diffère de la fonction CALLTHIS car elle ne transmet une référence à la forme qui possède la formule à _nommacro_. Comme CALLTHIS, la fonction RUNMACRO ne nécessite pas une référence à _projname_opt_ pour l’appeler. 
  
 Le code VBA appelé par l’évaluation d’une fonction RUNMACRO dans une formule par une instance Visio ne doit pas fermer le document contenant la cellule qui utilise la fonction ; dans le cas contraire, une erreur d’application se produit et Visio se ferme. 
  
Si vous devez fermer le document contenant la cellule qui utilise la fonction RUNMACRO, procédez de l’une des manières suivantes :
  
- Fermez le document à partir d’un code non-VBA.
    
- Fermez le document à partir d’un projet différent de celui en cours de fermeture.
    
- Envoyez des messages de fenêtre dans le document pour fermer les fenêtres plutôt que de fermer le document.
    
Pour plus d’informations sur l’exécution de code dans Visio, voir [à propos des paramètres de sécurité et l’exécution de code dans Visio](about-security-settings-and-running-code-in-visio-shapesheet.md) dans ce guide de référence de feuille ShapeSheet. 
  
## <a name="example"></a>Exemple

L’exemple suivant appelle une macro appelée MyTest dans le module de classe ThisDocument du projet VBA contenant la formule RUNMACRO. 
  
RUNMACRO (« ThisDocument.MyTest ») 
  

