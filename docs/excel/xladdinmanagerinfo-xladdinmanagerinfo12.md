---
title: xlAddInManagerInfo/xlAddInManagerInfo12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlAddInManagerInfo
keywords:
- fonction xladdinmanagerinfo [excel 2007]
localization_priority: Normal
ms.assetid: 63a73cd2-6479-4233-ad68-93379f940717
description: 'S’applique à : Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 66d2ac05b9603d6bb587a3898bde2545c1bb844a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407794"
---
# <a name="xladdinmanagerinfoxladdinmanagerinfo12"></a>xlAddInManagerInfo/xlAddInManagerInfo12

 **S’applique à** : Excel 2013 | Office 2013 | Visual Studio 
  
Appelé par Microsoft Excel lorsque le Gestionnaire de add-in est appelé pour la première fois dans une session Excel session. Cette fonction est utilisée pour fournir au gestionnaire Add-In des informations sur votre add-in.
  
Excel 2007 et versions ultérieures appellent **xlAddInManagerInfo12** de préférence à **xlAddInManagerInfo** s’il est exporté par le XLL. La **fonction xlAddInManagerInfo12** doit fonctionner de la même manière que **xlAddInManagerInfo** pour éviter les différences propres à la version du XLL. Excel s’attend à ce que **xlAddInManagerInfo12** retourne un type de données **XLOPER12,** tandis que **xlAddInManagerInfo** doit renvoyer un **XLOPER**.
  
La **fonction xlAddInManagerInfo12** n’est pas appelée par les versions de Excel antérieures à Excel 2007, car elles ne sont pas en charge par **xlOPER12**.
  
Excel ne nécessite pas de XLL pour implémenter et exporter l’une de ces fonctions.
  
```cs
LPXLOPER WINAPI xlAddInManagerInfo(LPXLOPER pxAction);
LPXLOPER12 WINAPI xlAddInManagerInfo12(LPXLOPER12 pxAction);
```

## <a name="parameters"></a>Parameters

 _pxAction :_ Pointeur vers un **XLOPER/XLOPER12** numérique (**xltypeInt** ou **xltypeNum**).
  
Informations que Excel demande.
  
## <a name="property-valuereturn-value"></a>Valeur de propriété/valeur de renvoi

Si  _pxAction_ est ou peut être forcé, le numéro 1, votre implémentation de cette fonction doit renvoyer une chaîne contenant des informations sur le module complémentaire, généralement son nom et éventuellement un numéro de version. Sinon, elle doit renvoyer #VALUE!. 
  
Si vous ne renvoyez pas de chaîne, Excel tente de convertir la valeur renvoyée en chaîne.
  
## <a name="remarks"></a>Remarques

Si la chaîne renvoyée pointe vers une mémoire tampon allouée dynamiquement, vous devez vous assurer que ce tampon est finalement libéré. Si la chaîne a été allouée par Excel, vous le faites en paramètre **xlbitXLFree**. Si la chaîne a été allouée par la DLL, vous le faites en paramètre **xlbitDLLFree** et vous devez également implémenter dans [xlAutoFree](xlautofree-xlautofree12.md) (si vous renvoyez une **XLOPER**) ou **xlAutoFree12** (si vous renvoyez une **XLOPER12**).
  
## <a name="example"></a>Exemple

 `\SAMPLES\GENERIC\GENERIC.C`
  
```cs
LPXLOPER12 WINAPI xlAddInManagerInfo12(LPXLOPER12 xAction)
{
    static XLOPER12 xInfo, xIntAction;
/*
** This code coerces the passed-in value to an integer. This is how the
** code determines what is being requested. If it receives a 1, it returns a
** string representing the long name. If it receives anything else, it
** returns a #VALUE! error.
*/
    Excel12f(xlCoerce, &xIntAction, 2, xAction, TempInt12(xltypeInt));
    if(xIntAction.val.w == 1) 
    {
        xInfo.xltype = xltypeStr;
        xInfo.val.str = L"\026Example Standalone DLL";
    }
    else 
    {
        xInfo.xltype = xltypeErr;
        xInfo.val.err = xlerrValue;
    }
// Word of caution - returning static XLOPERs/XLOPER12s is not thread safe
// for UDFs declared as thread safe. Use alternate memory allocation mechanisms.
    return (LPXLOPER12)&xInfo;
} 

```

## <a name="see-also"></a>Voir aussi



[Fonctions du Gestionnaire de compléments et de l’interface XLL](add-in-manager-and-xll-interface-functions.md)

