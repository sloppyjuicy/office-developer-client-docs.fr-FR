---
title: xlEventRegister
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b98637d4-02e3-4dbd-8be5-6b46d32980c6
description: 'S’applique à : Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 869122954ffe3928dfea72b8fc9fb432b9979e42
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438763"
---
# <a name="xleventregister"></a>xlEventRegister

 **S’applique à** : Excel 2013 | Office 2013 | Visual Studio 
  
Permet d'enregistrer un gestionnaire d'événements. Introduit dans Excel 2010.
  
```vb
Excel12(xlEventRegister, LPXLOPER12 pxRes, 2, LPXLOPER12 pxProcedure, LPXLOPER12 pxEvent);
```

## <a name="parameters"></a>Paramètres

 _pxProcedure_ (**xltypeStr**)
  
Nom de la fonction de gestionnaire d'événements telle qu'elle apparaît dans le code de la DLL.
  
 _pxEvent_ (**xltypeInt**)
  
Événement géré par la fonction désignée dans le paramètre _pxProcedure_ . 
  
À partir d'Excel 2010, Excel prend en charge les événements suivants:
  
|**event**|**Description**|
|:-----|:-----|
|**xleventCalculationEnded** <br/> |Déclenché lorsqu'Excel termine un calcul. Vous pouvez libérer toutes les ressources allouées pendant le calcul après cet événement.  <br/> |
|**xleventCalculationCanceled** <br/> |Déclenché lorsque l'utilisateur interrompt le calcul. Le XLL doit arrêter les activités asynchrones. L'événement CalculationEnded est déclenché immédiatement après cet événement.  <br/> |
   
## <a name="property-valuereturn-value"></a>Valeur de propriété/valeur de renvoi

Si elle réussit, renvoie la **valeur true** (**xltypeBool**). En cas d'échec, renvoie **false**.
  
## <a name="see-also"></a>Voir aussi



[Fonctions asynchrones définies par l’utilisateur](asynchronous-user-defined-functions.md)

