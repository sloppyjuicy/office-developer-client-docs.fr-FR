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
- fonction TempStr12 [Excel 2007], fonction TempStrConst [Excel 2007]
localization_priority: Normal
ms.assetid: faf4ee4e-8d33-4cb3-ae16-5648a837ee4f
description: 'S’applique à : Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: d93f9de021c7ba325d9c11af2cede0245ffbbf6b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407150"
---
# <a name="tempstrconsttempstr12"></a>TempStrConst/TempStr12

 **S’applique à** : Excel 2013 | Office 2013 | Visual Studio 
  
Fonction de bibliothèque d'infrastructure qui crée un **XLOPER/XLOPER12** temporaire qui contient une chaîne **xltypeStr** , en prenant une chaîne source se terminant par null comme entrée. La fonction alloue une nouvelle mémoire tampon et y copie la chaîne passée. La chaîne d'entrée n'est pas modifiée et est déclarée **const**.
  
```cs
LPXLOPER TempStrConst(const LPSTR str);
LPXLOPER12 TempStr12(const XCHAR* lpstr);
```

## <a name="parameters"></a>Paramètres

 _str_
  
Pointeur vers la chaîne source se terminant par null. Dans le cas de **XLOPER**s, TempStrConst tronque les chaînes dont la taille est supérieure à 255 octets. Dans le cas de **XLOPER12**s, TempStr12Const tronque les chaînes qui sont plus longues que 32 767 caractères Unicode.
  
## <a name="return-value"></a>Valeur renvoyée

Renvoie une chaîne **xltypeStr** contenant une copie de la mémoire tampon de chaîne passée. 
  
## <a name="remarks"></a>Remarques

Notez que la fonction de l'infrastructure de chaîne **XLOPER** , **TempStr**, se comporte différemment et tente de remplacer le premier caractère de la chaîne fournie avec la longueur de la chaîne suivante. Cette opération n'est pas toujours sûre: Microsoft Excel peut se bloquer si une chaîne en lecture seule a été transmise. Cette méthode de création de chaînes temporaires est désormais déconseillée en faveur de la façon dont **TempStrConst** et **TempStr12** fonctionnent. Par conséquent, le premier caractère de la chaîne d'entrée est traité comme le début de la chaîne, c'est-à-dire, non comme un caractère de longueur ou comme un espace pour un caractère de longueur. Vous ne devez pas transmettre des chaînes dont le caractère de longueur est encodé au début, car les conséquences peuvent être imprévisibles. 
  
## <a name="example"></a>Exemple

Cet exemple utilise la fonction **TempStr12** pour créer une chaîne pour une zone de message. 
  
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

