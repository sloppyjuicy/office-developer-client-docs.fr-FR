---
title: xlEventRegister
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: b98637d4-02e3-4dbd-8be5-6b46d32980c6
description: 'S’applique à : Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: c5236a2859b69a45481b4eedd587b923dbe0776e
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59631488"
---
# <a name="xleventregister"></a>xlEventRegister

 **S’applique à**: Excel 2013 | Office 2013 | Visual Studio 
  
Utilisé pour inscrire un handler d’événements. Introduit dans Excel 2010.
  
```vb
Excel12(xlEventRegister, LPXLOPER12 pxRes, 2, LPXLOPER12 pxProcedure, LPXLOPER12 pxEvent);
```

## <a name="parameters"></a>Paramètres

 _pxProcedure_ (**xltypeStr**)
  
Nom de la fonction de handler d’événements telle qu’elle apparaît dans le code DLL.
  
 _pxEvent_ (**xltypeInt**)
  
Événement géré par la fonction désignée dans le _paramètre pxProcedure._ 
  
À compter Excel 2010, Excel prend en charge les événements suivants :
  
|**Event**|**Description**|
|:-----|:-----|
|**xleventCalculationEnded** <br/> |Cette erreur est Excel à la fin d’un calcul. Vous pouvez libérer toutes les ressources allouées pendant le calcul après cet événement.  <br/> |
|**xleventCalculationCanceled** <br/> |Élevé lorsque l’utilisateur interrompt le calcul. Le XLL doit arrêter toutes les activités asynchrones. L’événement CalculationEnded est lancé immédiatement après cet événement.  <br/> |
   
## <a name="property-valuereturn-value"></a>Valeur de propriété/valeur de renvoi

Si elle réussit, pxRes (**xltypeInt**) a une valeur > 0. En cas d’échec, pxRes ==0.
  
## <a name="see-also"></a>Voir aussi



[Fonctions asynchrones définies par l’utilisateur](asynchronous-user-defined-functions.md)

