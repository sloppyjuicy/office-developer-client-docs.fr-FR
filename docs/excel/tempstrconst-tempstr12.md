---
title: TempStrConst/TempStr12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- TempStr12
- TempStrConst
keywords:
- fonction tempstr12 [excel 2007], fonction TempStrConst [Excel 2007]
localization_priority: Normal
ms.assetid: faf4ee4e-8d33-4cb3-ae16-5648a837ee4f
description: 'S�applique �: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 321c41aa87a3bfa0edc1d77ecc8fbe4b6a6a4730
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782204"
---
# <a name="tempstrconsttempstr12"></a>TempStrConst/TempStr12

 **S’applique à**: Excel 2013 | Office 2013 | Visual Studio 
  
Fonction de bibliothèque Framework qui crée un temporaire **XLOPER/XLOPER12** qui contient une chaîne de **xltypeStr** , prenant une chaîne source se termine par null comme entrée. La fonction alloue une nouvelle mémoire tampon et copie de la chaîne transmise dans celui-ci. La chaîne d’entrée n’est pas modifiée et est donc déclarée comme **const**.
  
```cs
LPXLOPER TempStrConst(const LPSTR str);
LPXLOPER12 TempStr12(const XCHAR* lpstr);
```

## <a name="parameters"></a>Paramètres

 _Str_
  
Pointeur vers la chaîne source terminée. Dans le cas de **XLOPER**s, TempStrConst tronque les chaînes qui sont supérieures à 255 octets. Dans le cas de **XLOPER12**s, TempStr12Const tronque les chaînes de longueur supérieure à 32 767 caractères Unicode.
  
## <a name="return-value"></a>Valeur renvoy�e

Renvoie une chaîne **xltypeStr** contenant une copie de la mémoire tampon de chaîne transmise. 
  
## <a name="remarks"></a>Remarques

Notez que la chaîne **XLOPER** fonction Framework, **TempStr**, se comporte différemment et tente de remplacer le premier caractère de la chaîne fournie avec la longueur de la chaîne suivante. Ce n’est pas toujours une chose à faire fiable : Microsoft Excel peut s’interrompre si reçoit une chaîne en lecture seule. Cette méthode de création de chaînes temporaires est désormais déconseillée en faveur de celle dans laquelle le travail à la fois **TempStrConst** et **TempStr12** . Par conséquent, le premier caractère de la chaîne d’entrée est traité comme point de départ de la chaîne, autrement dit, pas un caractère de longueur ou un espace pour un caractère de longueur. Vous ne devez pas passer les chaînes qui ont un caractère de longueur codé au début, que les conséquences pourraient être imprévisibles. 
  
## <a name="example"></a>Exemple

Cet exemple utilise la fonction **TempStr12** pour créer une chaîne d’une zone de message. 
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI TempStrExample(void)
{
   Excel12f(xlcAlert, 0, 1, TempStr12Const(L"Made it!"));
   return 1;
}
```

## <a name="see-also"></a>Voir aussi



[Fonctions de la bibliothèque Framework](functions-in-the-framework-library.md)

