---
title: SETATREF, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60113
localization_priority: Normal
ms.assetid: 1ecfdb05-2533-470a-006b-e554026944d8
description: Redirige les valeurs mises à jour résultant d'actions dans l'interface utilisateur (IU) ou l'automatisation vers une autre cellule.
ms.openlocfilehash: c4f5fe94aba90ce0a69983d6637a5399b6e42707
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326018"
---
# <a name="setatref-function"></a>Fonction SETATREF

Redirige les valeurs mises à jour résultant d'actions dans l'interface utilisateur (IU) ou l'automatisation vers une autre cellule. 
  
## <a name="syntax"></a>Syntaxe

SETATREF (* * *référence* * * [, * * *expression_données* * * [, * * *ignore_eval* * *]]) 
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _reference_ <br/> |Obligatoire  <br/> |**String** <br/> |Référence à une cellule vers laquelle les mises à jour sont redirigées.  <br/> |
| _Set_Expression_ <br/> |Facultatif  <br/> |**Chaîne** <br/> |Expression assignée à _Reference_.  <br/> |
| _ignore_eval_ <br/> |Facultatif  <br/> |**Booléen** <br/> |Si la valeur est TRUE, la fonction SETATREF évalue à (0) zéro; Si la valeur est FALSe (valeur par défaut), la fonction SETATREF évalue la valeur de _Reference_.  <br/> |
   
## <a name="remarks"></a>Remarques

Lorsqu'une action utilisateur dans la fenêtre de dessin, ou une méthode Automation, entraîne la mise à jour par Microsoft Visio d'une cellule contenant une formule SETATREF, la valeur est redirigée vers la cellule référencée par la formule SETATREF ( _référence_). La formule dans la cellule contenant la fonction SETATREF reste intacte.
  
Si _set_expression_ est omis, la valeur définie dans l'interface utilisateur ou à l'aide de l'automatisation est assignée à la cellule référencée; dans le cas contraire, le contenu de _set_expression_ est affecté à la cellule référencée. Cela permet à la nouvelle valeur d’être modifiée ou transformée avant d’être attribuée à cette cellule. 
  
La fonction SETATREF possède deux fonctions connexes : 
  
- La fonction SETATREFEXPR, que vous pouvez utiliser pour représenter la nouvelle valeur dans _set_expression_. Par exemple, un _set_expression_ de SETATREFEXPR ()-2 dans. peut être utilisé pour soustraire 2 pouces du résultat SETATREFEXPR. 
    
- La fonction SETATREFEVAL, que vous pouvez utiliser pour indiquer qu'une partie de _set_expression_ doit être évaluée et remplacée par son résultat. 
    
La fonction SETATREF est conçue pour une utilisation dans les cellules qui peuvent être modifiées par les actions de l'utilisateur dans la fenêtre de dessin. Les cellules suivantes sont prises en charge :
  
- Section ShapeTransform — cellules Width, Height, Angle, PinX et PinY
    
- Section Text Transform — cellules TxtWidth, TxtHeight, TxtAngle, TxtPinX et TxtPinY
    
- Section 1-D Endpoints — cellules BeginX, BeginY, EndX et EndY
    
- Section Controls — cellules Controls.X et Controls.Y
    
- Section Shape Data
    
Étant donné que SETATREF modifie l’emplacement où les valeurs de cellules changent, cela affecte le déclenchement des événements. Si une cellule contient SETATREF, les événements **FormulaChanged** et **CellChanged** s’appliquent à la cellule référencée par SETATREF et non à celle contenant SETATREF. Si une cellule contenant SETATREF contient également SETATREFEXPR, l'événement **FormulaChanged** se déclenche également pour la cellule contenant SETATREF car un paramètre de fonction est modifié. 
  
Autres informations importantes à connaître à propos de la fonction SETATREF :
  
- Les fonctions SETATREF peuvent attacher jusqu’à 10 références à d’autres fonctions SETATREF. 
    
- Outre la fonction SETATREF, y compris plusieurs occurrences de SETATREF dans une cellule unique, les cellules peuvent contenir d’autres expressions.
    
- Si des formes sont collées, Visio suit la chaîne de référence SETATREF dans la même feuille et place des formules de colle dans la cellule référencée. 
    
- Automation reconnaît la fonction SETATREF et suit la chaîne de cellules référencées. 
    
- À l’instar de GUARD, SETATREF ne protège pas les cellules des changements effectués à l’aide de la fonction SETF dans la feuille Shapesheet.
    
## <a name="example1"></a>Exemple1

Supposons qu’une forme dispose d’une propriété personnalisée appelée Width et que la cellule Width de la section Shape Transform contient la formule suivante :
  
= SETATREF (Prop. Width)
  
Si un utilisateur modifie la largeur de la forme dans l'interface utilisateur, la nouvelle valeur est affectée à la cellule prop. Width, et non à la cellule Width de la section ShapeTransform; la formule dans la cellule Width reste inchangée. Vous pouvez également définir la largeur de la forme en utilisant des données de forme.
  
## <a name="example2"></a>Example2

Les solutions Visio ont souvent des formes dotées de relations hiérarchiques, nécessitant que les formes enfant soient déplacées lorsqu’une forme parente l’est également. Voici un exemple indiquant comment vous pouvez gérer cette relation à l’aide de la fonction SETATREF dans la feuille ShapeSheet. 
  
Les formules suivantes sont contenues dans la section Shape Transform de la forme enfant. Ainsi, nous définissons les cellules utilisateur appelées User.DeltaX et User.DeltaY qui assurent la dimension de décalage à partir de ParentShape. Cela permet à la forme enfant d’être déplacée en même temps que la forme parent mais aussi de préserver la relation hiérarchique si la forme enfant est déplacée.
  
PinX =SETATREF(User.DeltaX, SETATREFEVAL(SETATREFEXPR() - ParentShape!PinX)) + ParentShape!PinX
  
PinY =SETATREF(User.DeltaY, SETATREFEVAL(SETATREFEXPR() - ParentShape!PinY)) + ParentShape!PinY
  
Lorsque la forme enfant est déplacée à l'aide de l'interface utilisateur, les nouvelles valeurs PinX et PinY sont définies en tant que paramètre dans la fonction SETATREFEXPR. La fonction SETATREF évalue la formule incluse dans SETATREFEVAL et remplace PinX et PinY par leurs résultats, puis la formule résultante est affectée aux cellules utilisateur référencées dans la fonction SETATREF: User. DeltaX et User. deltaY. Enfin, les valeurs retournées par SETATREF (User. DeltaX ou User. deltaY) sont ajoutées à l'emplacement du code confidentiel de ParentShape pour calculer l'emplacement du code confidentiel de la forme enfant.
  

