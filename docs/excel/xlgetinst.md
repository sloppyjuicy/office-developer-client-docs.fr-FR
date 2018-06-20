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
localization_priority: Normal
ms.assetid: 631a8f4e-ea7c-4743-9ee1-b2233fd7d98d
description: 'S�applique �: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 9484f7bbc1f5e0fc5b0def17f2ce79ef226dcd17
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782228"
---
# <a name="xlgetinst"></a>xlGetInst

 **S’applique à**: Excel 2013 | Office 2013 | Visual Studio 
  
Renvoie le descripteur d’instances de l’instance de Microsoft Excel en appelant une DLL.
  
```cs
Excel4(xlGetInst, LPXLOPER pxRes, 0); /* returns low part only */
Excel12(xlGetInst, LPXLOPER12 pxRes, 0); /* returns full handle */
```

## <a name="parameters"></a>Paramètres

Cette fonction ne comporte aucun argument.
  
## <a name="property-valuereturn-value"></a>Propriété valeur/valeur de retour

Le descripteur d’instances (**xltypeInt**) est inclus dans le champ **val.w** . 
  
## <a name="remarks"></a>Remarques

Cette fonction peut être utilisée pour faire la distinction entre plusieurs instances en cours d’exécution de Microsoft Excel qui appellent la DLL.
  
Lorsque vous appelez cette fonction à l’aide de [Excel4](excel4-excel12.md) ou [Excel4v](excel4v-excel12v.md), la variable de type entier XLOPER renvoyée est un entier signé 16 bits courte. Il s’agit des 16 bits de poids faibles de la poignée de Windows 32 bits. À compter d’Excel 2007, la variable de type entier de la **XLOPER12** est un int 32 bits signé et par conséquent contient le handle entier, évite d’avoir à parcourir toutes les fenêtres ouvertes. 
  
> [!IMPORTANT]
> Si la fonction **xlGetInst** est utilisée avec la version 64 bits de Microsoft Excel, la fonction échoue. Il s’agit, car le type de valeur **xltypeInt** n’est pas assez large pour contenir la poignée de type longue 64 bits renvoyée par Excel dans ce cas. Pour cela, Excel 2010 introduit une nouvelle fonction nommée [xlGetInstPtr](xlgetinstptr.md), qui s’exécute correctement avec les versions 32 bits et 64 bits de Microsoft Excel. 
  
## <a name="example"></a>Exemple

L’exemple suivant compare l’instance de la dernière copie d’Excel qui l’a appelé à la copie active de Microsoft Excel qui l’a appelé. Si elles sont les mêmes, elle renvoie la valeur 1 ; dans le cas contraire, elle renvoie la valeur 0 ; Si la fonction échoue, elle renvoie -1.
  
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


[Fonctions de l’API C qui peuvent être appelées uniquement à partir d’une DLL ou XLL](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

