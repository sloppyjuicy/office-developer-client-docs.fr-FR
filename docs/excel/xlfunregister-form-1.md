---
title: xlfUnregister (formulaire 1)
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlfUnregister
keywords:
- fonction xlfUnregister [Excel 2007]
localization_priority: Normal
ms.assetid: 850bf65f-a151-44d6-b49f-d53ae2c83760
description: 'S�applique �: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 3f5ebc08f89651331186990d8574e3150d4f484a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303891"
---
# <a name="xlfunregister-form-1"></a>xlfUnregister (formulaire 1)

**S’applique à**: Excel 2013 | Office 2013 | Visual Studio 
  
Peut être appelée à partir d'une commande DLL ou XLL qui a elle-même été appelée par Microsoft Excel. Cela équivaut à appeler **Unregister** à partir d'une feuille macro XLM Excel. 
  
**xlfUnregister** peut être appelé sous deux formes: 
  
- Formulaire 1: annule l'inscription d'une commande ou d'une fonction individuelle.
    
- Formulaire 2: décharge et désactive un XLL.
    
Appelée dans le formulaire 1, cette fonction réduit le nombre d'utilisations d'une fonction ou commande DLL précédemment inscrite à l'aide de **xlfRegister** ou **Register**. Si le nombre d'utilisations est déjà égal à zéro, cette fonction n'a aucun effet. Lorsque le nombre d'utilisations de toutes les fonctions dans une DLL atteint zéro, la DLL est déchargée de la mémoire.
  
**xlfRegister** (Formulaire 1) définit également un nom masqué qui est l'argument de texte de la fonction, _pxFunctionText_, et qui prend la valeur de l'ID d'enregistrement de la fonction ou de la commande. Lors de l'annulation de l'inscription de la fonction, ce nom doit être supprimé à l'aide de **xlfSetName** afin que le nom de la fonction ne soit plus mentionné par l'Assistant fonction. Pour plus d�informations, consultez [Probl�mes connus concernant le d�veloppement de XLL Excel](known-issues-in-excel-xll-development.md).
  
```cs
Excel4(xlfUnregister, LPXLOPER pxRes, 1, LPXLOPER pxRegisterId);
```

## <a name="parameters"></a>Paramètres

_pxRegisterId_ (**xltypeNum**)
  
ID d'inscription de la fonction dont l'inscription doit être annulée.
  
## <a name="property-valuereturn-value"></a>Valeur de propriété/valeur de renvoi

Si elle réussit, renvoie la **valeur true** (**xltypeBool**), sinon elle renvoie la valeur false.
  
## <a name="remarks"></a>Remarques

L'ID d'inscription de la fonction est retourné par **xlfRegister** lorsque la fonction est inscrite pour la première fois. Elle peut également être obtenue en appelant la [fonction xlfRegisterId](xlfregisterid.md) ou la [fonction xlfEvaluate](xlfevaluate.md). Notez que xlfRegisterId essaie d'enregistrer la fonction si elle n'a pas encore été inscrite. Pour cette raison, si vous tentez d'obtenir l'ID de sorte que vous puissiez annuler l'inscription de la fonction, il est préférable de l'obtenir en transmettant le nom enregistré à **xlfEvaluate**. Si la fonction n'a pas été enregistrée, **xlfEvaluate** échoue avec une #NAME? «. 
  
## <a name="example"></a>Exemple

Voir le code de la fonction **fExit** dans `\SAMPLES\GENERIC\GENERIC.C`.
  
```cs
int WINAPI fExit(void)
{
   XLOPER12  xDLL,    // The name of this DLL //
   xFunc,             // The name of the function //
   xRegId;            // The registration ID //
   int i;
//
// This code gets the DLL name. It then uses this along with information
// from g_rgFuncs[] to obtain a REGISTER.ID() for each function. The
// register ID is then used to unregister each function. Then the code
// frees the DLL name and calls xlAutoClose.
//
   // Make xFunc a string //
   xFunc.xltype = xltypeStr;
   Excel12f(xlGetName, &xDLL, 0);
   for (i = 0; i < g_rgWorksheetFuncsRows; i++)
   {
      xFunc.val.str = (LPWSTR) (g_rgWorksheetFuncs[i][0]);
      Excel12f(xlfRegisterId,&xRegId,2,(LPXLOPER12)&xDLL,(LPXLOPER12)&xFunc);
      Excel12f(xlfUnregister, 0, 1, (LPXLOPER12) &xRegId);
   }
   for (i = 0; i < g_rgCommandFuncsRows; i++)
   {
      xFunc.val.str = (LPWSTR) (g_rgCommandFuncs[i][0]);
      Excel12f(xlfRegisterId,&xRegId,2,(LPXLOPER12)&xDLL,(LPXLOPER12)&xFunc);
      Excel12f(xlfUnregister, 0, 1, (LPXLOPER12) &xRegId);
   }
   Excel12f(xlFree, 0, 1,  (LPXLOPER12) &xDLL);
   return xlAutoClose();
}
```

## <a name="see-also"></a>Voir aussi

- [xlfRegister (formulaire 1)](xlfregister-form-1.md)
- [xlfRegisterId](xlfregisterid.md)
- [xlfUnregister (formulaire 2)](xlfunregister-form-2.md)
- [Fonctions XLM essentielles et utiles de l’API C](essential-and-useful-c-api-xlm-functions.md)

