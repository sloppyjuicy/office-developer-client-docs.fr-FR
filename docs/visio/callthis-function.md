---
title: CALLTHIS, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251403
localization_priority: Normal
ms.assetid: 461abfc1-d2cc-2354-1c2f-395c9e351a78
description: Appelle une procédure dans un Microsoft Visual Basic pour Applications (VBA) project.
ms.openlocfilehash: 04065384453e55b745daa89273fb4c23b32fb90c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788186"
---
# <a name="callthis-function"></a>CALLTHIS, fonction

Appelle une procédure dans un Microsoft Visual Basic pour Applications (VBA) project.
  
## <a name="syntax"></a>Syntaxe

CALLTHIS (« ** *procédure* ** », [« ** *project* ** »], [** *arg1* **, ** *arg2* **,...]) 
  
### <a name="parameters"></a>Paramètres

|**Name**|**Obligatoire/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _procédure_ <br/> |Obligatoire  <br/> |**Chaîne** <br/> | Nom de la procédure à appeler.  <br/> |
| _projet_ <br/> |Facultatif  <br/> |**Chaîne** <br/> |Projet qui contient la procédure.  <br/> |
| _arg_ <br/> |Facultatif  <br/> |**Nombre, chaîne, Date ou Currency** <br/> |Transmis comme paramètres à la procédure.  <br/> |
   
## <a name="remarks"></a>Remarques

Dans le projet VBA, *procedure* est défini comme suit : 
  
procédure (*vsoShape* en tant que Visio.Shape [arg1 que vous tapez, arg2 en tant que type...]) 
  
où *vsoShape* est une référence à l’objet **Shape** qui contient la formule CALLTHIS calculée et _arg1_, *arg2* ... sont les arguments indiqués dans cette formule. 
  
Notez que *vsoShape* est très semblable à l’argument « this » transmis à une procédure C++ ; Par conséquent, le nom « CALLTHIS ». En effet, une cellule contenant une formule qui inclut CALLTHIS peut se lire, « Appeler cette procédure et lui transmettre une référence à ma forme ». 
  
Si le _projet_ est spécifié, Microsoft Visio recherche tous les documents ouverts pour l’un contenant _project_ et appelle la _procédure_ dans ce projet. Si le _projet_ est omis ou nul (« »), Visio suppose que la _procédure_ se trouve dans le projet VBA du document contenant la formule CALLTHIS qui est évaluée. 
  
Les nombres de _arg1_, _arg2..._ sont transmis en unités externes. Par exemple, si vous transmettez la valeur de la cellule Height à partir d’une forme haute de 3 cm, 3 est transmise. Pour transmettre différentes unités avec un nombre, utilisez la fonction FORMATEX ou définissez explicitement unités en ajoutant une paire nombre-unité nulle, par exemple, 0 ft + hauteur. 
  
La deuxième virgule dans la fonction CALLTHIS est facultative. Il correspond au nombre de paramètres supplémentaires ajoutés à votre procédure. Si vous n’utilisez pas les paramètres supplémentaires, sauf `(vsoShape as Visio.Shape)` , n’ajoutez pas la deuxième virgule ; utilisez CALLTHIS("",). Si vous ajoutez deux paramètres supplémentaires, par exemple, utilisez CALLTHIS("",,,). 
  
La fonction CALLTHIS est toujours 0 et l’appel de _procédure_ se produit pendant la durée d’inactivité après le processus de recalcul.  _Procédure_ peut renvoyer une valeur, mais Visio l’ignore.  _Procédure_ renvoie une valeur que Visio peut reconnaître en définissant la formule ou le résultat d’une autre cellule dans le document, mais pas la cellule qui a appelé la _procédure_, sauf si vous souhaitez remplacer la formule CALLTHIS.
  
La fonction CALLTHIS est différente de la fonction RUNADDON ; en effet, un projet de document ne doit pas nécessairement faire référence à un autre projet pour appeler une procédure de ce dernier. 
  
> [!NOTE]
>  Le code VBA appelé lorsque l’instance de Visio calcule une fonction CALLTHIS dans une formule ne doit pas fermer le document contenant la cellule qui utilise la fonction, sans quoi une erreur d’application se produit et Visio se ferme. 
  
Si vous devez fermer le document contenant la cellule qui utilise la fonction CALLTHIS, utilisez l’une des techniques suivantes : 
  
- fermez le document à partir de code non-VBA ;
    
- Fermez le document à partir d’un projet différent de celui en cours de fermeture.
    
- Envoyez des messages de fenêtre dans le document pour fermer les fenêtres plutôt que de fermer le document.
    
Pour plus d’informations sur l’exécution de code dans Visio, voir [sur les paramètres de sécurité et l’exécution de Code dans Visio](about-security-settings-and-running-code-in-visio-shapesheet.md) dans ce guide de référence de feuille ShapeSheet. 
  
## <a name="example-1"></a>Exemple 1

CALLTHIS("p",,FORMATEX(Height,"#,00 u",,"cm"))
  
Appelle la procédure nommée p située dans un module et transmet la valeur de la cellule Height en centimètres, par exemple 7,62 cm.
  
## <a name="example-2"></a>Exemple 2

CALLTHIS("q",,0 cm+Height,Width)
  
Appelle la procédure nommée q située dans un module et transmet la hauteur de la cellule en centimètres et la largeur en unités internes.
  
## <a name="example-3"></a>Exemple 3

Utilisez la procédure suivante dans le module de classe *ThisDocument* . 
  
Utilisez l’une des syntaxes suivantes dans la cellule EventDblClick d’une forme avec les procédures qui précèdent.
  
CALLTHIS("ThisDocument.A",)
  
CALLTHIS("ThisDocument.B",,"Click")
  
CALLTHIS("ThisDocument.C",,"Cliquez sur", " OK.")
  

