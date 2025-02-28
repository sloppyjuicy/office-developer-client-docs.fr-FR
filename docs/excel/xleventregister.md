---
title: xlEventRegister
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: b98637d4-02e3-4dbd-8be5-6b46d32980c6
ms.openlocfilehash: 9a6edcfb850d6263bde572f302ae8b31002a4a83
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62773738"
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
|**xleventCalculationEnded** <br/> |Cette erreur est Excel à la fin d’un calcul. Vous pouvez libérer toutes les ressources allouées pendant le calcul après cet événement. |
|**xleventCalculationCanceled** <br/> |Élevé lorsque l’utilisateur interrompt le calcul. Le XLL doit arrêter toutes les activités asynchrones. L’événement CalculationEnded est lancé immédiatement après cet événement. |
   
## <a name="property-valuereturn-value"></a>Valeur de propriété/valeur de renvoi

Si elle réussit, pxRes (**xltypeInt**) a une valeur > 0. En cas d’échec, pxRes ==0.
  
## <a name="see-also"></a>Voir aussi



[Fonctions asynchrones définies par l’utilisateur](asynchronous-user-defined-functions.md)

