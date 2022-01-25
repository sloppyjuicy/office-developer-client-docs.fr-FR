---
title: xlfUnregister (formulaire 1)
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlfUnregister
keywords:
- fonction xlfunregister [excel 2007]
ms.localizationpriority: medium
ms.assetid: 850bf65f-a151-44d6-b49f-d53ae2c83760
ms.openlocfilehash: 1125cb9966c6ad43ee543f82a3beaa54b9b4e4b7
ms.sourcegitcommit: 193df57ebf141020852d2ebc8cf0931edb71574a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/25/2022
ms.locfileid: "62198456"
---
# <a name="xlfunregister-form-1"></a>xlfUnregister (formulaire 1)

**S’applique à**: Excel 2013 | Office 2013 | Visual Studio 
  
Peut être appelée à partir d’une commande DLL ou XLL qui a elle-même été appelée par Microsoft Excel. Cela équivaut à appeler **UNREGISTER** à partir d’Excel feuille macro XLM. 
  
**xlfUnregister** peut être appelé sous deux formes : 
  
- Formulaire 1 : désinsère une commande ou une fonction individuelle.
    
- Formulaire 2 : décharge et désactive une XLL.
    
Appelée dans le formulaire 1, cette fonction réduit le nombre d’utilisations d’une fonction ou d’une commande DLL précédemment inscrite à l’aide de **xlfRegister** ou **REGISTER**. Si le nombre d’utilisations est déjà zéro, cette fonction n’a aucun effet. Lorsque le nombre d’utilisations de toutes les fonctions dans une DLL atteint zéro, la DLL est déchargée de la mémoire.
  
**xlfRegister** (formulaire 1) définit également un nom masqué qui est l’argument de texte de la fonction,  _pxFunctionText_, et qui est évalué en fonction de l’ID d’inscription de la fonction ou de la commande. Lors de la désinssion de la fonction, ce nom doit être supprimé à l’aide de **xlfSetName** afin que le nom de la fonction ne soit plus répertorié par l’Assistant Fonction. Pour plus d’informations, reportez-vous à la rubrique [Problèmes connus concernant le développement de XLL Excel](known-issues-in-excel-xll-development.md).
  
```cs
Excel4(xlfUnregister, LPXLOPER pxRes, 1, LPXLOPER pxRegisterId);
```

## <a name="parameters"></a>Paramètres

_pxRegisterId_ (**xltypeNum**)
  
ID d’inscription de la fonction à désinsister.
  
## <a name="property-valuereturn-value"></a>Valeur de propriété/valeur de renvoi

Si elle réussit, renvoie **TRUE** (**xltypeBool**), sinon elle renvoie FALSE.
  
## <a name="remarks"></a>Remarques

L’ID d’inscription de la fonction est renvoyé par **xlfRegister** lors de la première inscription de la fonction. Il peut également être obtenu en appelant la fonction [xlfRegisterId](xlfregisterid.md) ou [la fonction xlfEvaluate](xlfevaluate.md). Notez que xlfRegisterId tente d’inscrire la fonction si elle n’a pas déjà été inscrite. Pour cette raison, si vous essayez uniquement d’obtenir l’ID afin de pouvoir désinsérer la fonction, il est préférable de l’obtenir en passant le nom enregistré à **xlfEvaluate**. Si la fonction n’a pas été enregistrée, **xlfEvaluate** échoue avec une #NAME ? erreur. 
  
## <a name="example"></a>Exemple

Consultez le code de la **fonction fExit** dans  `\SAMPLES\GENERIC\GENERIC.C` .
  
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

