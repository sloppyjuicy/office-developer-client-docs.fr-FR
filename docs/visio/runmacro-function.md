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
ms.openlocfilehash: 24882eaf3fda5cba62e080f0ecec70e09cdb46e1
ms.sourcegitcommit: f8dc13ccaadfbd6d3783c3b291d998d5255a5f38
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2022
ms.locfileid: "63403422"
---
# <a name="runmacro-function"></a>Fonction RUNMACRO

Appelle une macro dans un projet Microsoft Visual Basic pour Applications (VBA).
  
## <a name="syntax"></a>Syntaxe

RUNMACRO (***macroname** _ [, _ *_projname_opt_** ])
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| *macroname* <br/> |Requis  <br/> |**String** <br/> |Nom de la macro à appeler |
| *projname_opt* <br/> |Facultatif  <br/> |**Chaîne** <br/> | Projet qui contient la macro |

## <a name="remarks"></a>Remarques

Si un projet est spécifié, Microsoft Visio recherche dans tous les documents ouverts celui contenant *projname_opt* et appelle *macroname* dans ce projet. Si *projname_opt* est omis ou a la valeur null (""), *macroname* est supposé être dans le projet VBA du document qui contient la formule RUNMACRO calculée.
  
La fonction RUNMACRO diffère de la fonction CALLTHIS car elle ne transmet pas à *macroname* une référence à la forme qui possède la formule calculée. Comme CALLTHIS, la fonction RUNMACRO ne nécessite pas de référence à *projname_opt pour* l’appeler.
  
 Le code VBA appelé par l’évaluation d’une fonction RUNMACRO dans une formule par une instance Visio ne doit pas fermer le document contenant la cellule qui utilise la fonction ; dans le cas contraire, une erreur d’application se produit et Visio se ferme.
  
Si vous devez fermer le document contenant la cellule qui utilise la fonction RUNMACRO, procédez de l’une des manières suivantes :
  
- Fermez le document à partir d’un code non-VBA.

- fermez le document à partir d’un projet autre que celui qui est en train de se fermer ;

- Envoyez des messages de fenêtre dans le document pour fermer les fenêtres plutôt que de fermer le document.

Pour plus d’informations sur l’exécution de code dans Visio, reportez-vous à la rubrique [À propos des paramètres de sécurité et de l’exécution de code dans Visio](about-security-settings-and-running-code-in-visio-shapesheet.md) dans la Référence de la feuille ShapeSheet.
  
## <a name="example"></a>Exemple

L’exemple suivant appelle une macro appelée MyTest dans le module de classe ThisDocument du projet VBA contenant la formule RUNMACRO.
  
RUNMACRO (« ThisDocument.MyTest »)
  