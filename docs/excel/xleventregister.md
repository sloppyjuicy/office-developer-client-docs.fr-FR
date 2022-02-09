---
title: xlEventRegister
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: b98637d4-02e3-4dbd-8be5-6b46d32980c6
ms.openlocfilehash: 48e891ee61d8af1facf4b8609310a408987ea21b
ms.sourcegitcommit: 5969c693475e22a3f5a4fdde3473ecc33013b76f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/09/2022
ms.locfileid: "62462595"
---
# <a name="xleventregister"></a>xlEventRegister

 **S’applique à**: Excel 2013 | Office 2013 | Visual Studio 
  
Utilisé pour inscrire un handler d’événements. Introduit dans Excel 2010.
  
```vb
Excel12(xlEventRegister, LPXLOPER12 pxRes, 2, LPXLOPER12 pxProcedure, LPXLOPER12 pxEvent);
```

## <a name="parameters"></a>Paramètres

 _pxProcedure_ (**xltypeStr**)
  
Nom de la fonction de handler d’événement telle qu’elle apparaît dans le code DLL.
  
 _pxEvent_ (**xltypeInt**)
  
Événement géré par la fonction désignée dans le _paramètre pxProcedure_ . 
  
À compter Excel 2010, Excel prend en charge les événements suivants :
  
|**Event**|**Description**|
|:-----|:-----|
|**xleventCalculationEnded** <br/> |Cette erreur est Excel à la fin d’un calcul. Vous pouvez libérer toutes les ressources allouées pendant le calcul après cet événement.  <br/> |
|**xleventCalculationCanceled** <br/> |Élevé lorsque l’utilisateur interrompt le calcul. Le XLL doit arrêter toutes les activités asynchrones. L’événement CalculationEnded est lancé immédiatement après cet événement.  <br/> |
   
## <a name="property-valuereturn-value"></a>Valeur de propriété/valeur de renvoi

Si elle réussit, pxRes (**xltypeInt**) a une valeur > 0. En cas d’échec, pxRes ==0.
  
## <a name="see-also"></a>Voir aussi



[Fonctions asynchrones définies par l’utilisateur](asynchronous-user-defined-functions.md)

