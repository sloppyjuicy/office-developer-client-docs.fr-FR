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
description: 'S�applique �: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: e42cca809c4426ddf9a98b3b275d08490d31c8db
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782196"
---
# <a name="xladdinmanagerinfoxladdinmanagerinfo12"></a>xlAddInManagerInfo/xlAddInManagerInfo12

 **S’applique à**: Excel 2013 | Office 2013 | Visual Studio 
  
Appelée par Microsoft Excel lorsque le Gestionnaire de compléments est appelé pour la première fois dans une session d’Excel. Cette fonction est utilisée pour fournir le Gestionnaire de compléments avec des informations concernant votre complément.
  
Excel 2007 et versions ultérieures appellent **xlAddInManagerInfo12** plutôt que **xlAddInManagerInfo** si exportée par la ressource XLL. La fonction **xlAddInManagerInfo12** devrait fonctionner de la même manière que **xlAddInManagerInfo** pour éviter les différences spécifiques à la version de comportement de la ressource XLL. Excel attend **xlAddInManagerInfo12** pour renvoyer un type de données **XLOPER12** , tandis que **xlAddInManagerInfo** doit renvoyer une **XLOPER**.
  
La fonction **xlAddInManagerInfo12** n’est pas appelée par les versions d’Excel antérieures à Excel 2007, comme ces ne prennent pas en charge la **XLOPER12**.
  
Excel ne nécessite pas un ressource XLL à mettre en œuvre et exporter une de ces fonctions.
  
```cs
LPXLOPER WINAPI xlAddInManagerInfo(LPXLOPER pxAction);
LPXLOPER12 WINAPI xlAddInManagerInfo12(LPXLOPER12 pxAction);
```

## <a name="parameters"></a>Paramètres

 _pxAction :_ Pointeur vers un **XLOPER/XLOPER12** numérique (**xltypeInt** ou **xltypeNum**).
  
Les informations qui vous demande pour Excel.
  
## <a name="property-valuereturn-value"></a>Propriété valeur/valeur de retour

Si _pxAction_ est, ou peut être forcé sur le numéro 1, votre implémentation de cette fonction doit renvoyer une chaîne contenant des informations sur le complément, généralement son nom et éventuellement un numéro de version. Dans le cas contraire, elle doit retourner #VALUE !. 
  
Si vous ne renvoyez pas une chaîne, Excel tente de convertir la valeur renvoyée en une chaîne.
  
## <a name="remarks"></a>Remarques

Si la chaîne renvoyée pointe vers le tampon alloué dynamiquement, il se peut que vous devez vous assurer que ce tampon est libéré par la suite. Si la chaîne a été attribuée par Excel, cela en définissant **xlbitXLFree**. Si la chaîne a été affectée par la DLL, pour ce faire, le paramètre **xlbitDLLFree**, et vous devez également implémenter dans [xlAutoFree](xlautofree-xlautofree12.md) (si vous souhaitez retourner un **XLOPER**) ou **xlAutoFree12** (si vous souhaitez retourner un **XLOPER12**).
  
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



[Gestionnaire de compléments et les fonctions de l’Interface XLL](add-in-manager-and-xll-interface-functions.md)

