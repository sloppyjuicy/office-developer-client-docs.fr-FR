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
- fonction tempstr12 [excel 2007],TempStrConst function [Excel 2007]
ms.localizationpriority: medium
ms.assetid: faf4ee4e-8d33-4cb3-ae16-5648a837ee4f
ms.openlocfilehash: ca9690f4b570ac988de2dc219d428760e6a2c1f6
ms.sourcegitcommit: 193df57ebf141020852d2ebc8cf0931edb71574a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/25/2022
ms.locfileid: "62198325"
---
# <a name="tempstrconsttempstr12"></a>TempStrConst/TempStr12

 **S’applique à**: Excel 2013 | Office 2013 | Visual Studio 
  
Fonction de bibliothèque d’infrastructure qui crée une **structure XLOPER/XLOPER12** temporaire contenant une chaîne **xltypeStr,** en prenant une chaîne source terminée par null comme entrée. La fonction alloue une nouvelle mémoire tampon et copie la chaîne transmise dans celui-ci. La chaîne d’entrée n’est pas modifiée et est donc déclarée comme **const**.
  
```cs
LPXLOPER TempStrConst(const LPSTR str);
LPXLOPER12 TempStr12(const XCHAR* lpstr);
```

## <a name="parameters"></a>Paramètres

 _str_
  
Pointeur vers la chaîne source terminée par null. Dans le cas de **XLOPER,** TempStrConst tronque les chaînes dont la taille est plus longue que 255 octets. Dans le cas de **XLOPER12** s, TempStr12Const tronque les chaînes dont la taille est plus longue que 32 767 caractères Unicode.
  
## <a name="return-value"></a>Valeur renvoyée

Renvoie une **chaîne xltypeStr** contenant une copie de la mémoire tampon de chaîne transmise. 
  
## <a name="remarks"></a>Remarques

Notez que la fonction d’infrastructure de chaîne **XLOPER,** **TempStr**, se comporte différemment et tente de overwrite le premier caractère de la chaîne fournie par la longueur de la chaîne suivante. Ce n’est pas toujours une chose sûre : Microsoft Excel peut se crasher si une chaîne en lecture seule est transmise. Cette façon de créer des chaînes temporaires est désormais dépréciée au profit de la façon dont **TempStrConst** et **TempStr12** fonctionnent. Par conséquent, le premier caractère de la chaîne d’entrée est traité comme le début de la chaîne, c’est-à-dire, non comme un caractère de longueur ou comme un espace pour un caractère de longueur. Vous ne devez pas transmettre de chaînes dont le caractère de longueur est codé au début, car les conséquences peuvent être imprévisibles. 
  
## <a name="example"></a>Exemple

Cet exemple utilise la **fonction TempStr12** pour créer une chaîne pour une boîte de message. 
  
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

