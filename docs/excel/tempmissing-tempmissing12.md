---
title: TempMissing/TempMissing12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- TempMissing
- TempMissing12
keywords:
- fonction tempmissing [Excel 2007], fonction TempMissing12 [Excel 2007]
localization_priority: Normal
ms.assetid: d9cb6afc-1fbb-45d6-88e5-84eba3af3c60
description: 'S’applique à : Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 37c127b2252f18643b34dfc72fd9929885a68d01
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435956"
---
# <a name="tempmissingtempmissing12"></a>TempMissing/TempMissing12

 **S’applique à** : Excel 2013 | Office 2013 | Visual Studio 
  
Fonction de bibliothèque d'infrastructure qui crée une**XLOPER12** **XLOPER**/ temporaire de type **xltypeMissing**.
  
```cs
LPXLOPER TempMissing(void);
LPXLOPER12 TempMissing12(void);
```

## <a name="parameters"></a>Paramètres

Cette fonction n’utilise aucun paramètre.
  
## <a name="return-value"></a>Valeur renvoyée

Renvoie un pointeur vers une expression **XLOPER**/ **** **xltypeMissing** .
  
## <a name="example"></a>Exemple

Cet exemple utilise **TempMissing12** pour fournir trois arguments manquants à **xlcWorkspace** suivi d'une valeur **booléenne** **false** pour supprimer l'affichage des barres de défilement de feuille de calcul. Les trois premiers arguments correspondent à d'autres paramètres d'espace de travail qui ne sont pas affectés. 
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI TempMissingExample(void)
{
   XLOPER12 xBool;
   xBool.xltype = xltypeBool;
   xBool.val.xbool = 0;
   Excel12f(xlcWorkspace, 0, 4, TempMissing12(), TempMissing12(),
      TempMissing12(), (LPXLOPER12)&xBool);
   return 1;
}
```

## <a name="see-also"></a>Voir aussi



[Fonctions de la bibliothèque Framework](functions-in-the-framework-library.md)

