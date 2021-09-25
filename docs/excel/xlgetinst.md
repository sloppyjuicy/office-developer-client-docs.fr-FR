---
title: xlGetInst
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlGetInst
keywords:
- fonction xlgetinst [excel 2007]
ms.localizationpriority: medium
ms.assetid: 631a8f4e-ea7c-4743-9ee1-b2233fd7d98d
description: 'S’applique à : Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 1346eb97fb70912c5acfb49bebffa016e05a17ab
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59572339"
---
# <a name="xlgetinst"></a>xlGetInst

 **S’applique à**: Excel 2013 | Office 2013 | Visual Studio 
  
Renvoie le handle d’instance de l’instance de Microsoft Excel qui appelle actuellement une DLL.
  
```cs
Excel4(xlGetInst, LPXLOPER pxRes, 0); /* returns low part only */
Excel12(xlGetInst, LPXLOPER12 pxRes, 0); /* returns full handle */
```

## <a name="parameters"></a>Paramètres

Cette fonction n’a pas d’arguments.
  
## <a name="property-valuereturn-value"></a>Valeur de propriété/valeur de renvoi

Le handle d’instance (**xltypeInt**) sera dans le **champ val.w.** 
  
## <a name="remarks"></a>Remarques

Cette fonction peut être utilisée pour faire la distinction entre plusieurs instances de Excel qui appellent la DLL.
  
Lorsque vous appelez cette fonction à l’aide [d’Excel4](excel4-excel12.md) ou [d’Excel4v,](excel4v-excel12v.md)la variable d’integer XLOPER renvoyée est un int court signé 16 bits. Cette capacité ne peut contenir que les 16 bits faibles de la poignée de Windows 32 bits. À compter de Excel 2007, la variable entière de la **xlOPER12** est un entier signé 32 bits et contient donc la poignée entière, ce qui supprime la nécessité d’itérer toutes les fenêtres ouvertes. 
  
> [!IMPORTANT]
> Si la **fonction xlGetInst** est utilisée avec la version 64 bits de Microsoft Excel, la fonction échoue. Cela est dû au fait que le type de valeur **xltypeInt** n’est pas assez large pour contenir la poignée longue 64 bits renvoyée par Excel dans ce cas. À cet effet, Excel 2010 a introduit une nouvelle fonction nommée [xlGetInstPtr](xlgetinstptr.md), qui s’exécute correctement avec les versions 32 bits et 64 bits de Excel. 
  
## <a name="example"></a>Exemple

L’exemple suivant compare l’instance de la dernière copie de Excel qui l’a appelée à la copie actuelle de la Excel qui l’a appelée. Si elles sont identiques, elle renvoie 1 ; si ce n’est pas le cas, elle renvoie 0 ; Si la fonction échoue, elle renvoie -1.
  
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

