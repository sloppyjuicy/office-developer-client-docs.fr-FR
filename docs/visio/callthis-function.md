---
title: CALLTHIS, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251403
ms.localizationpriority: medium
ms.assetid: 461abfc1-d2cc-2354-1c2f-395c9e351a78
description: Appelle une procédure dans un projet Microsoft Visual Basic pour Applications (VBA).
ms.openlocfilehash: 7dff3b6b49eb828b5c73f4aa98da2d5c460a84d4
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59560080"
---
# <a name="callthis-function"></a>Fonction CALLTHIS

Appelle une procédure dans un projet Microsoft Visual Basic pour Applications (VBA).
  
## <a name="syntax"></a>Syntaxe

CALLTHIS( » ** *procedure* ** « ,[ » ** *project* ** « ],[ ** *arg1* **, ** *arg2* **,...]) 
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _procedure_ <br/> |Obligatoire  <br/> |**String** <br/> | Nom de la procédure à appeler.  <br/> |
| _projet_ <br/> |Facultatif  <br/> |**Chaîne** <br/> |Projet qui contient la procédure.  <br/> |
| _arg_ <br/> |Facultatif  <br/> |**Number, String, Date ou Currency** <br/> |Transmis comme paramètres à la procédure.  <br/> |
   
## <a name="remarks"></a>Remarques

Dans le projet VBA,  *la procédure*  est définie comme suit : 
  
procedure(*vsoShape* As Visio. Shape [arg1 As type, arg2 As type...]) 
  
où  *vsoShape*  est une référence à l’objet **Shape** qui contient la formule CALLTHIS en cours d’évaluation, et  _arg1_,  *arg2*  ... sont les arguments spécifiés dans cette formule. 
  
Notez  *que vsoShape*  est très proche de l’argument « this » passé à une procédure membre C++ ; d’où le nom « CALLTHIS ». En effet, une cellule qui contient une formule incluant CALLTHIS peut être lue comme « Appeler cette procédure et lui transmettre une référence à ma forme ». 
  
Si _le projet_ est spécifié, Microsoft Visio tous les documents  ouverts pour celui contenant le projet et appelle la procédure _dans_ ce projet. Si _le_ projet est omis ou null  (« ») Visio suppose que la procédure se trouve dans le projet VBA du document qui contient la formule CALLTHIS en cours d’évaluation. 
  
Les nombres  _dans arg1,_  _arg2... sont_ transmis en unités externes. Par exemple, si vous transmettez la valeur de la cellule Height à partir d’une forme haute de 3 cm, la valeur 3 est transmise. Pour transmettre différentes unités avec un nombre, utilisez la fonction FORMATEX ou définissez explicitement les unités en ajoutant une paire nombre nul-unité (0 m + Height, par exemple). 
  
La deuxième virgule dans la fonction CALLTHIS est facultative. Elle correspond au nombre de paramètres supplémentaires ajoutés à votre procédure. Si vous n’utilisez aucun paramètre supplémentaire, sauf , n’ajoutez pas la deuxième virgule ; utilisez  `(vsoShape as Visio.Shape)` CALLTHIS(« , »). Si vous ajoutez deux paramètres, par exemple, utilisez CALLTHIS("",,,). 
  
La fonction CALLTHIS est toujours évaluée à  0 et l’appel à la procédure se produit pendant les périodes d’inactivité une fois le processus de recalcul terminé.  _procedure_ peut renvoyer une valeur, mais Visio l’ignore.  _La_ procédure renvoie une valeur que Visio peut reconnaître en fixant la formule ou le résultat d’une autre cellule du document, mais pas la cellule qui a appelé la _procédure,_ sauf si vous souhaitez réécrire la formule CALLTHIS.
  
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

Utilisez la procédure suivante dans le module de classe *ThisDocument.* 
  
Utilisez l’une des syntaxes suivantes dans la cellule EventDblClick d’une forme avec les procédures qui précèdent.
  
CALLTHIS(« ThisDocument.A »,)
  
CALLTHIS(« ThisDocument.B »,,"Click »)
  
CALLTHIS("ThisDocument.C",,"Cliquez sur", " OK.")
  

