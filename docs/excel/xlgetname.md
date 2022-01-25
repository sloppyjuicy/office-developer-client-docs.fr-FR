---
title: xlGetName
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlGetName
keywords:
- fonction xlgetname [excel 2007]
ms.localizationpriority: medium
ms.assetid: 72dbebc0-7436-4771-8fbf-2b445341da65
ms.openlocfilehash: f95a0e2f610a119eae730f0ebd81c26aaa0191a2
ms.sourcegitcommit: 193df57ebf141020852d2ebc8cf0931edb71574a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/25/2022
ms.locfileid: "62198582"
---
# <a name="xlgetname"></a>xlGetName

**S’applique à**: Excel 2013 | Office 2013 | Visual Studio 
  
Renvoie le chemin d’accès complet et le nom de fichier de la DLL sous la forme d’une chaîne.
  
```cs
Excel12(xlGetName, LPXLOPER12 pxRes, 0);
```

## <a name="parameters"></a>Paramètres

Cette fonction n’a pas d’arguments.
  
## <a name="property-valuereturn-value"></a>Valeur de propriété/valeur de renvoi

Renvoie le chemin d’accès et le nom de fichier (**xltypeStr**). 
  
## <a name="example"></a>Exemple

`\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI xlGetNameExample(void)
{
    XLOPER12 xRes;
    Excel12(xlGetName, (LPXLOPER12)&xRes, 0);
    Excel12(xlcAlert, 0, 1, (LPXLOPER12)&xRes);
    Excel12(xlFree, 0, 1, (LPXLOPER12)&xRes);
    return 1;
}
```

## <a name="see-also"></a>Voir aussi

- [Fonctions de l’API C à appeler à partir d’un fichier DLL ou XLL](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

