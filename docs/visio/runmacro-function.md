---
title: RUNMACRO, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033809
ms.localizationpriority: medium
ms.assetid: 86b0f071-5e0b-56de-ff5b-63c114ad823a
description: Appelle une macro dans un projet Microsoft Visual Basic pour Applications (VBA).
ms.openlocfilehash: b3d84f672913841d609320a3af7e3b9734291117
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59598184"
---
# <a name="runmacro-function"></a>Fonction RUNMACRO

Appelle une macro dans un projet Microsoft Visual Basic pour Applications (VBA). 
  
## <a name="syntax"></a>Syntaxe

RUNMACRO (** *nommacro* ** [, ** *projname_opt* ** ]) 
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _macroname_ <br/> |Obligatoire  <br/> |**String** <br/> |Nom de la macro à appeler  <br/> |
| _projname_opt_ <br/> |Facultatif  <br/> |**Chaîne** <br/> | Projet qui contient la macro  <br/> |
   
## <a name="remarks"></a>Remarques

Si un projet est spécifié, Microsoft Visio tous les documents  ouverts pour celui contenant projname_opt et appelle le _nom de macro_ dans ce projet. Si projname_opt est omis ou null («  _»)_ le nom de  _macro_ est supposé se trouver dans le projet VBA du document qui contient la formule RUNMACRO évaluée. 
  
La fonction RUNMACRO diffère de la fonction CALLTHIS en ce qu’elle ne passe pas de référence à la forme propriétaire de la formule évaluée au nom _de macro._ Comme CALLTHIS, la fonction RUNMACRO ne nécessite pas de référence à projname_opt  _pour_ l’appeler. 
  
 Le code VBA appelé par l’évaluation d’une fonction RUNMACRO dans une formule par une instance Visio ne doit pas fermer le document contenant la cellule qui utilise la fonction ; dans le cas contraire, une erreur d’application se produit et Visio se ferme. 
  
Si vous devez fermer le document contenant la cellule qui utilise la fonction RUNMACRO, procédez de l’une des manières suivantes :
  
- Fermez le document à partir d’un code non-VBA.
    
- fermez le document à partir d’un projet autre que celui qui est en train de se fermer ;
    
- Envoyez des messages de fenêtre dans le document pour fermer les fenêtres plutôt que de fermer le document.
    
Pour plus d’informations sur l’exécution de code dans Visio, reportez-vous à la rubrique [À propos des paramètres de sécurité et de l’exécution de code dans Visio](about-security-settings-and-running-code-in-visio-shapesheet.md) dans la Référence de la feuille ShapeSheet. 
  
## <a name="example"></a>Exemple

L’exemple suivant appelle une macro appelée MyTest dans le module de classe ThisDocument du projet VBA contenant la formule RUNMACRO. 
  
RUNMACRO (« ThisDocument.MyTest ») 
  

