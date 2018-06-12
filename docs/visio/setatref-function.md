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
description: Redirections mis à jour les valeurs résultant d’actions dans l’interface utilisateur (IU) ou Automation vers une autre cellule.
ms.openlocfilehash: 69a9cb93ae3fbd807ef4f306be386f5389a6cfeb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789617"
---
# <a name="setatref-function"></a>SETATREF, fonction

Redirections mis à jour les valeurs résultant d’actions dans l’interface utilisateur (IU) ou Automation vers une autre cellule. 
  
## <a name="syntax"></a>Syntaxe

SETATREF (** *référence* ** [, ** *set_expression* ** [, ** *ignore_eval* **]]) 
  
### <a name="parameters"></a>Paramètres

|**Name**|**Obligatoire/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _référence_ <br/> |Obligatoire  <br/> |**Chaîne** <br/> |Référence à une cellule vers laquelle les mises à jour sont redirigées.  <br/> |
| _set_expression_ <br/> |Facultatif  <br/> |**Chaîne** <br/> |Une expression est affectée à la _référence_.  <br/> |
| _ignore_eval_ <br/> |Facultatif  <br/> |**Boolean** <br/> |Si TRUE, la fonction SETATREF calcule (0) zéro ; Si défini sur FALSE (valeur par défaut) la fonction SETATREF calcule la valeur de _référence_.  <br/> |
   
## <a name="remarks"></a>Note

Lorsqu’une action utilisateur dans la fenêtre de dessin, ou une méthode Automation, entraîne Microsoft Visio mettre à jour une cellule contenant une formule SETATREF, la valeur est plutôt redirigée vers la cellule référencée par la formule SETATREF ( _référence_). La formule dans la cellule contenant la fonction SETATREF reste intacte.
  
Si _set_expression_ est omis, la valeur définie dans l’interface utilisateur ou à l’aide d’Automation est attribuée à la cellule référencée ; Sinon, le contenu de la _variable set_expression_ est assigné à la cellule référencée. Ainsi, la nouvelle valeur d’être modifiée ou transformée avant d’être attribuée à la cellule référencée. 
  
La fonction SETATREF possède deux fonctions connexes : 
  
- La fonction SETATREFEXPR, vous pouvez utiliser pour représenter la nouvelle valeur dans _set_expression_. Par exemple, une _variable set_expression_ de SETATREFEXPR ()-2. peut être utilisé pour soustraire 2 pouces à partir du résultat SETATREFEXPR. 
    
- La fonction SETATREFEVAL, que vous pouvez utiliser pour indiquer qu’une partie de la _variable set_expression_ doit être évaluée et remplacée par son résultat. 
    
La fonction SETATREF est conçue pour une utilisation dans les cellules qui peuvent être modifiés par les actions de l’utilisateur dans la fenêtre de dessin. Les cellules suivantes sont prises en charge :
  
- Section ShapeTransform — cellules Width, Height, Angle, PinX et PinY
    
- Section Text Transform — cellules TxtWidth, TxtHeight, TxtAngle, TxtPinX et TxtPinY
    
- Section 1-D Endpoints — cellules BeginX, BeginY, EndX et EndY
    
- Section Controls — cellules Controls.X et Controls.Y
    
- Section Shape Data
    
Étant donné que SETATREF modifie l’emplacement où les valeurs de cellules changent, cela affecte le déclenchement des événements. Si une cellule contient SETATREF, les événements **FormulaChanged** et **CellChanged** déclenchent la cellule référencée par SETATREF, pas de la cellule contenant SETATREF. Si une cellule contenant SETATREF contient également SETATREFEXPR, l’événement **FormulaChanged** est également déclenché à la cellule contenant SETATREF car un paramètre de fonction est modifié. 
  
Autres informations importantes à connaître à propos de la fonction SETATREF :
  
- Les fonctions SETATREF peuvent attacher jusqu’à 10 références à d’autres fonctions SETATREF. 
    
- Outre la fonction SETATREF, y compris plusieurs occurrences de SETATREF dans une cellule unique, les cellules peuvent contenir d’autres expressions.
    
- Si des formes sont collées, Visio suit la chaîne de référence SETATREF dans la même feuille et place des formules de colle dans la cellule référencée. 
    
- Automation reconnaît la fonction SETATREF et suit la chaîne de cellules référencées. 
    
- À l’instar de GUARD, SETATREF ne protège pas les cellules des changements effectués à l’aide de la fonction SETF dans la feuille Shapesheet.
    
## <a name="example1"></a>Exemple1

Supposons qu’une forme dispose d’une propriété personnalisée appelée Width et que la cellule Width de la section Shape Transform contient la formule suivante :
  
=SETATREF(Prop.Width)
  
Si un utilisateur pour modifier la largeur de la forme dans l’interface utilisateur, la nouvelle valeur est attribuée à la cellule Prop.Width et pas à la cellule Width dans la section ShapeTransform ; la formule de la cellule Width reste inchangée. Vous pouvez également définir la largeur de la forme à l’aide de données de forme.
  
## <a name="example2"></a>Example2

Les solutions Visio ont souvent des formes dotées de relations hiérarchiques, nécessitant que les formes enfant soient déplacées lorsqu’une forme parente l’est également. Voici un exemple indiquant comment vous pouvez gérer cette relation à l’aide de la fonction SETATREF dans la feuille ShapeSheet. 
  
Les formules suivantes sont contenues dans la section Shape Transform de la forme enfant. Ainsi, nous définissons les cellules utilisateur appelées User.DeltaX et User.DeltaY qui assurent la dimension de décalage à partir de ParentShape. Cela permet à la forme enfant d’être déplacée en même temps que la forme parent mais aussi de préserver la relation hiérarchique si la forme enfant est déplacée.
  
PinX =SETATREF(User.DeltaX, SETATREFEVAL(SETATREFEXPR() - ParentShape!PinX)) + ParentShape!PinX
  
PinY =SETATREF(User.DeltaY, SETATREFEVAL(SETATREFEXPR() - ParentShape!PinY)) + ParentShape!PinY
  
Lorsque la forme enfant est déplacée à l’aide de l’interface utilisateur, les nouvelles valeurs PinX et PinY sont définies en tant que paramètre dans la fonction SETATREFEXPR. La fonction SETATREF calcule la formule dans SETATREFEVAL et remplace PinX et PinY par leurs résultats, puis la formule qui en résulte est affectée aux cellules utilisateur référencés inclue et User.DeltaY. Enfin, les valeurs renvoyées par SETATREF (User.DeltaX et User.DeltaY) sont ajoutés à l’emplacement du code confidentiel de ParentShape pour calculer l’emplacement du code confidentiel d’une forme enfant.
  

