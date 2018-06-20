---
title: xlEventRegister
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b98637d4-02e3-4dbd-8be5-6b46d32980c6
description: 'S�applique �: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: d837d87c479f70f0184a7cf1612dea5ab8c99e6d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782221"
---
# <a name="xleventregister"></a>xlEventRegister

 **S’applique à**: Excel 2013 | Office 2013 | Visual Studio 
  
Utilisé pour enregistrer un gestionnaire d’événements. Une nouveauté dans Excel 2010.
  
```vb
Excel12(xlEventRegister, LPXLOPER12 pxRes, 2, LPXLOPER12 pxProcedure, LPXLOPER12 pxEvent);
```

## <a name="parameters"></a>Paramètres

 _pxProcedure_ (**xltypeStr**)
  
Le nom de la fonction de gestionnaire d’événements tel qu’il apparaît dans le code de la DLL.
  
 _pxEvent_ (**xltypeInt**)
  
L’événement est géré par la fonction désignée dans le paramètre _pxProcedure_ . 
  
À compter d’Excel 2010, Excel prend en charge les événements suivants :
  
|**Événement**|**Description**|
|:-----|:-----|
|**xleventCalculationEnded** <br/> |Déclenché lorsque Excel termine un calcul. Vous pouvez libérer les ressources allouées au cours du calcul après cet événement.  <br/> |
|**xleventCalculationCanceled** <br/> |Déclenché lorsque l’utilisateur interrompt le calcul. La ressource XLL doit s’arrêter toutes les activités asynchrones. L’événement CalculationEnded est déclenché immédiatement après cet événement.  <br/> |
   
## <a name="property-valuereturn-value"></a>Propriété valeur/valeur de retour

Si l’opération réussit, renvoie **la valeur TRUE** (**xltypeBool**). En cas d’échec, renvoie **FALSE**.
  
## <a name="see-also"></a>Voir aussi



[Fonctions asynchrones définies par l’utilisateur](asynchronous-user-defined-functions.md)

