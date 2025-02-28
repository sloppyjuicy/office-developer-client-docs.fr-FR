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
- fonction tempmissing [excel 2007],TempMissing12 function [Excel 2007]
ms.localizationpriority: medium
ms.assetid: d9cb6afc-1fbb-45d6-88e5-84eba3af3c60
ms.openlocfilehash: 98bced5a47b80792be1ca85083f22e336eecae0f
ms.sourcegitcommit: 193df57ebf141020852d2ebc8cf0931edb71574a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/25/2022
ms.locfileid: "62198841"
---
# <a name="tempmissingtempmissing12"></a>TempMissing/TempMissing12

 **S’applique à**: Excel 2013 | Office 2013 | Visual Studio 
  
Fonction de bibliothèque d’infrastructure qui crée une **xlOPER** /  **XLOPER12** temporaire de type **xltypeMissing**.
  
```cs
LPXLOPER TempMissing(void);
LPXLOPER12 TempMissing12(void);
```

## <a name="parameters"></a>Paramètres

Cette fonction n’utilise aucun paramètre.
  
## <a name="return-value"></a>Valeur renvoyée

Renvoie un pointeur vers un **xltypeMissing** **XLOPER** /  **XLOPER12**.
  
## <a name="example"></a>Exemple

Cet exemple utilise **TempMissing12** pour fournir trois arguments manquants à **xlcWorkspace** suivis d’un **booléen** **FALSE** pour supprimer l’affichage des barres de défilement de feuille de calcul. Les trois premiers arguments correspondent à d’autres paramètres d’espace de travail qui ne sont pas affectés. 
  
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

