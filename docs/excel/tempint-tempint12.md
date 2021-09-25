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
description: 'S’applique à : Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 390de41b38b10d3ab794c615824bd8b32cbdbb32
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59572360"
---
# <a name="tempinttempint12"></a>TempInt/TempInt12

 **S’applique à**: Excel 2013 | Office 2013 | Visual Studio 
  
Fonction de bibliothèque d’infrastructure qui crée une **xlOPER** /  **XLOPER12** temporaire qui contient unger. 
  
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

