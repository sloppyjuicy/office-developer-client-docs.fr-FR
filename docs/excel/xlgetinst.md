---
title: xlGetInst
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlGetInst
keywords:
- fonction xlGetInst [Excel 2007]
localization_priority: Normal
ms.assetid: 631a8f4e-ea7c-4743-9ee1-b2233fd7d98d
description: 'S’applique à : Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: e113ddbf55e2b4651d578549802c44e2c6413a18
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428129"
---
# <a name="xlgetinst"></a>xlGetInst

 **S’applique à** : Excel 2013 | Office 2013 | Visual Studio 
  
Renvoie le descripteur d'instance de l'instance de Microsoft Excel qui appelle actuellement une DLL.
  
```cs
Excel4(xlGetInst, LPXLOPER pxRes, 0); /* returns low part only */
Excel12(xlGetInst, LPXLOPER12 pxRes, 0); /* returns full handle */
```

## <a name="parameters"></a>Paramètres

Cette fonction n'a pas d'argument.
  
## <a name="property-valuereturn-value"></a>Valeur de propriété/valeur de renvoi

Le handle d'instance (**xltypeInt**) se trouve dans le champ **Val. w** . 
  
## <a name="remarks"></a>Remarques

Cette fonction peut être utilisée pour faire la distinction entre plusieurs instances d'Excel en cours d'exécution qui appellent la DLL.
  
Lorsque vous appelez cette fonction à l'aide de [Excel4](excel4-excel12.md) ou [Excel4v](excel4v-excel12v.md), la variable de type entier XLOPER renvoyée est un nombre entier court 16 bits signé. Il ne peut contenir que les 16 bits de poids faible du handle Windows 32 bits. À partir d'Excel 2007, la variable de type Integer de **XLOPER12** est un entier signé 32 bits et, par conséquent, le handle entier, ce qui supprime la nécessité d'itérer toutes les fenêtres ouvertes. 
  
> [!IMPORTANT]
> Si la fonction **xlGetInst** est utilisée avec la version 64 bits de Microsoft Excel, la fonction échouera. Cela est dû au fait que le type de valeur **xltypeInt** n'est pas assez large pour contenir le handle 64 bits long renvoyé par Excel dans ce cas. À cette fin, Excel 2010 a introduit une nouvelle fonction nommée [xlGetInstPtr](xlgetinstptr.md), qui s'exécute correctement avec les versions 32 bits et 64 bits d'Excel. 
  
## <a name="example"></a>Exemple

L'exemple suivant compare l'instance de la dernière copie d'Excel qui a été appelée à la copie actuelle d'Excel qui l'a appelée. Si elles sont identiques, elle renvoie 1; Si ce n'est pas le cas, il renvoie 0; Si la fonction échoue, elle renvoie-1.
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI xlGetInstExample(void)
{
    XLOPER12 xRes;
    static HANDLE hOld = 0;
    short iRet;
    if (Excel12(xlGetInst, &xRes, 0) != xlretSuccess)
        iRet = -1;
    else
    {
    HANDLE hNew;
    hNew = (HANDLE)xRes.val.w;
    if (hNew != hOld)
            iRet = 0;
    else
            iRet = 1;
    hOld = hNew;
    }
    return iRet;
}
```

## <a name="see-also"></a>Voir aussi



[xlGetHwnd](xlgethwnd.md)
  
[xlGetInstPtr](xlgetinstptr.md)


[Fonctions de l’API C à appeler à partir d’un fichier DLL ou XLL](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

