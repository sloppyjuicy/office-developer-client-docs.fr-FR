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
description: Appelle une procédure dans un projet Microsoft Visual Basic pour applications (VBA).
ms.openlocfilehash: 7e0f0bafa39d6c1eb1fd39535506981c937ce8a1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32337239"
---
# <a name="callthis-function"></a>Fonction CALLTHIS

Appelle une procédure dans un projet Microsoft Visual Basic pour applications (VBA).
  
## <a name="syntax"></a>Syntaxe

CALLTHIS ("* * *procedure* * *", ["* * *project* * *"], [* * *arg1* * *, * * *arg2* * *,...]) 
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _procédure_ <br/> |Obligatoire  <br/> |**String** <br/> | Nom de la procédure à appeler.  <br/> |
| _projet_ <br/> |Facultatif  <br/> |**Chaîne** <br/> |Projet qui contient la procédure.  <br/> |
| _donnée_ <br/> |Facultatif  <br/> |**Number, String, Date ou Currency** <br/> |Transmis comme paramètres à la procédure.  <br/> |
   
## <a name="remarks"></a>Remarques

Dans le projet VBA, la *procédure* est définie comme suit: 
  
Procedure (*vsoShape* As Visio. Shape [Arg1 As Type, Arg2 As Type...]) 
  
où *vsoShape* est une référence à l'objet **Shape** qui contient la formule CALLTHIS évaluée et _Arg1_, *Arg2* ... sont les arguments spécifiés dans cette formule. 
  
Notez que *vsoShape* est très similaire à l'argument «This» transmis à une procédure membre C++; par conséquent, le nom «CALLTHIS». En effet, une cellule qui contient une formule qui inclut CALLTHIS peut être lue sous la forme «appeler cette procédure et la transmettre à ma forme». 
  
Si vous spécifiez _Project_ , Microsoft Visio recherche dans tous les documents ouverts le _projet_ contenant et la _procédure_ Call de ce projet. Si vous ne spécifiez pas l'argument _Project_ ou la valeur null (""), la _procédure_ est supposée dans le projet VBA du document qui contient la formule CALLTHIS évaluée. 
  
Les nombres dans _Arg1_, _Arg2..._ sont transmis en unités externes. Par exemple, si vous transmettez la valeur de la cellule Height à partir d’une forme haute de 3 cm, la valeur 3 est transmise. Pour transmettre différentes unités avec un nombre, utilisez la fonction FORMATEX ou définissez explicitement les unités en ajoutant une paire nombre nul-unité (0 m + Height, par exemple). 
  
La deuxième virgule dans la fonction CALLTHIS est facultative. Elle correspond au nombre de paramètres supplémentaires ajoutés à votre procédure. Si vous n'utilisez pas de paramètres supplémentaires, sauf `(vsoShape as Visio.Shape)` , n'ajoutez pas la deuxième virgule; Utilisez CALLTHIS ("",). Si vous ajoutez deux paramètres, par exemple, utilisez CALLTHIS("",,,). 
  
La fonction CALLTHIS est toujours égale à 0, et l'appel à _procedure_ se produit pendant le temps d'inactivité après la fin du processus de recalcul.  _procedure_ peut renvoyer une valeur, mais Visio l’ignore.  _Procedure_ renvoie une valeur que Visio peut reconnaître en définissant la formule ou le résultat d'une autre cellule dans le document, mais pas la cellule qui a appelé _procedure_, sauf si vous souhaitez remplacer la formule CALLTHIS.
  
La fonction CALLTHIS est différente de la fonction RUNADDON ; en effet, un projet de document ne doit pas nécessairement faire référence à un autre projet pour appeler une procédure de ce dernier. 
  
> [!NOTE]
>  Le code VBA appelé lorsque l’instance de Visio calcule une fonction CALLTHIS dans une formule ne doit pas fermer le document contenant la cellule qui utilise la fonction, sans quoi une erreur d’application se produit et Visio se ferme. 
  
Si vous devez fermer le document contenant la cellule qui utilise la fonction CALLTHIS, utilisez l’une des techniques suivantes : 
  
- fermez le document à partir de code non-VBA ;
    
- fermez le document à partir d’un projet autre que celui qui est en train de se fermer ;
    
- envoyez des messages de fenêtre pour fermer les fenêtres du document plutôt que de fermer le document.
    
Pour plus d’informations sur l’exécution de code dans Visio, reportez-vous à la rubrique [À propos des paramètres de sécurité et de l’exécution de code dans Visio](about-security-settings-and-running-code-in-visio-shapesheet.md) dans la Référence de la feuille ShapeSheet. 
  
## <a name="example-1"></a>Exemple 1

CALLTHIS("p",,FORMATEX(Height,"#,00 u",,"cm"))
  
Appelle la procédure nommée p située dans un module et transmet la valeur de la cellule Height en centimètres, par exemple 7,62 cm.
  
## <a name="example-2"></a>Exemple 2

CALLTHIS("q",,0 cm+Height,Width)
  
Appelle la procédure nommée q située dans un module et transmet la hauteur de la cellule en centimètres et la largeur en unités internes.
  
## <a name="example-3"></a>Exemple 3

Utilisez la procédure suivante dans le module de classe *ThisDocument* . 
  
Utilisez l’une des syntaxes suivantes dans la cellule EventDblClick d’une forme avec les procédures qui précèdent.
  
CALLTHIS ("ThisDocument. A",)
  
CALLTHIS ("ThisDocument. B",, "Click")
  
CALLTHIS("ThisDocument.C",,"Cliquez sur", " OK.")
  

