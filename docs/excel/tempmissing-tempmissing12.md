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
- fonction tempmissing [excel 2007], fonction TempMissing12 [Excel 2007]
localization_priority: Normal
ms.assetid: d9cb6afc-1fbb-45d6-88e5-84eba3af3c60
description: 'S�applique �: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: a6db2e1f2917ecd9361043577f4bf203b3267a5c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782199"
---
# <a name="tempmissingtempmissing12"></a>TempMissing/TempMissing12

 **S’applique à**: Excel 2013 | Office 2013 | Visual Studio 
  
Fonction de bibliothèque Framework crée un temporaire **XLOPER**/ **XLOPER12** de type **xltypeMissing**.
  
```cs
LPXLOPER TempMissing(void);
LPXLOPER12 TempMissing12(void);
```

## <a name="parameters"></a>Paramètres

Cette fonction n’utilise aucun paramètre.
  
## <a name="return-value"></a>Valeur renvoy�e

Retourne un pointeur vers une **xltypeMissing** **XLOPER**/ **XLOPER12**.
  
## <a name="example"></a>Exemple

Cet exemple utilise **TempMissing12** pour fournir trois arguments manquants à **xlcWorkspace** suivi d’un **Boolean** **FALSE** pour supprimer l’affichage des barres de défilement de feuille de calcul. Les trois premiers arguments correspondent aux autres paramètres de l’espace de travail qui ne sont pas affectés. 
  
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

