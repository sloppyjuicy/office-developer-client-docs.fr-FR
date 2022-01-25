---
title: TempInt/TempInt12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- TempInt
- TempInt12
keywords:
- tempint12 function [excel 2007],TempInt function [Excel 2007]
ms.localizationpriority: medium
ms.assetid: 86d690b8-caca-450d-93f7-69ca4cd1a6e0
ms.openlocfilehash: a827ee31c293437ce699a86fb6b734aef8976bdf
ms.sourcegitcommit: 193df57ebf141020852d2ebc8cf0931edb71574a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/25/2022
ms.locfileid: "62198736"
---
# <a name="tempinttempint12"></a>TempInt/TempInt12

 **S’applique à**: Excel 2013 | Office 2013 | Visual Studio 
  
Fonction de bibliothèque d’infrastructure qui crée une **xlOPER** /  **XLOPER12** temporaire contenant unger. 
  
```cs
LPXLOPER TempInt(short int i);
LPXLOPER12 TempInt12(int i);
```

## <a name="parameters"></a>Paramètres

 _i_
  
Valeur de l’objet integer prévu. Notez que l’integer **XLOPER** est un integer 16 bits signé (int court), tandis que l’integer **XLOPER12** est un integer 32 bits signé ([long] int). 
  
## <a name="return-value"></a>Valeur renvoyée

Renvoie un **integer xltypeInt** contenant la valeur transmise. 
  
## <a name="example"></a>Exemple

Cet exemple utilise la **fonction TempInt12** pour passer un argument à **xlfGetWorkspace**.
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI TempIntExample(void)
{
    XLOPER12 xRes;
    Excel12f(xlfGetWorkspace, (LPXLOPER12)&xRes, 1, TempInt12(44));
    Excel12f(xlFree, 0, 1, (LPXLOPER12)&xRes);
    return 1;
}
```

## <a name="see-also"></a>Voir aussi



[Fonctions de la bibliothèque Framework](functions-in-the-framework-library.md)

