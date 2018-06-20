---
title: xlfUnregister (formulaire 1)
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlfUnregister
keywords:
- fonction xlfunregister [excel 2007]
localization_priority: Normal
ms.assetid: 850bf65f-a151-44d6-b49f-d53ae2c83760
description: 'S�applique �: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 6077027a27c054c5a5e65a751373c41a87cb3836
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782227"
---
# <a name="xlfunregister-form-1"></a>xlfUnregister (formulaire 1)

**S’applique à**: Excel 2013 | Office 2013 | Visual Studio 
  
Peut être appelée à partir d’une commande DLL ou XLL lui-même a été appelée par Microsoft Excel. Cela équivaut à appeler **Annuler l’inscription** d’une feuille de macro Excel XLM. 
  
**xlfUnregister** peut être appelée sous deux formes : 
  
- Formulaire 1 : Annule l’enregistrement d’une commande ou une fonction.
    
- Formulaire 2 : Décharge et désactive une solution XLL.
    
Appelée dans l’écran 1, cette fonction réduit le nombre d’utilisation d’une fonction DLL ou d’une commande qui a été précédemment inscrit à l’aide de **xlfRegister** ou **enregistrez**. Si le nombre d’utilisation est déjà égale à zéro, cette fonction est sans effet. Lorsque le nombre d’utilisations de toutes les fonctions dans une DLL atteint zéro, la DLL est déchargée de la mémoire.
  
**xlfRegister** (Formulaire 1) définit également le nom masqué qui est l’argument texte fonction, _pxFunctionText_, et qui correspond à la fonction ou ID de l’enregistrement. de la commande Lors de la désinscription de la fonction, ce nom doit être supprimé à l’aide de **xlfSetName** afin que le nom de la fonction n’est plus répertorié par l’Assistant fonction. Pour plus d�informations, consultez [Probl�mes connus concernant le d�veloppement de XLL Excel](known-issues-in-excel-xll-development.md).
  
```cs
Excel4(xlfUnregister, LPXLOPER pxRes, 1, LPXLOPER pxRegisterId);
```

## <a name="parameters"></a>Paramètres

_pxRegisterId_ (**xltypeNum**)
  
L’ID de l’enregistrement de la fonction doit être annulée.
  
## <a name="property-valuereturn-value"></a>Propriété valeur/valeur de retour

Si l’opération réussit, renvoie **la valeur TRUE** (**xltypeBool**), sinon il renvoie la valeur FALSE.
  
## <a name="remarks"></a>Remarques

L’inscription de le QU'ID de la fonction est retourné par **xlfRegister** lors de la fonction inscrit. Il peut également être obtenu en appelant la [fonction xlfRegisterId](xlfregisterid.md) ou la [fonction xlfEvaluate](xlfevaluate.md). Notez que xlfRegisterId tente d’inscrire la fonction si elle n’a pas déjà été enregistré. Pour cette raison, si vous essayez uniquement obtenir l’ID de sorte que vous pouvez annuler l’inscription de la fonction, il est préférable de se le procurer en transmettant le nom enregistré à **xlfEvaluate**. Si la fonction n’a pas été enregistrée, **xlfEvaluate** échoue avec une #NAME ? erreur. 
  
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

- [xlfRegister (formulaire 1)](xlfregister-form-1.md)
- [xlfRegisterId](xlfregisterid.md)
- [xlfUnregister (formulaire 2)](xlfunregister-form-2.md)
- [Fonctions XLM API C essentielles et utiles](essential-and-useful-c-api-xlm-functions.md)

