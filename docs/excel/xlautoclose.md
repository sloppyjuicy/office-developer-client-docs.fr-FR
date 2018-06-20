---
title: xlAutoClose
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlAutoClose
keywords:
- fonction xlAutoClose [excel 2007]
localization_priority: Normal
ms.assetid: 147e46cd-d4d7-49eb-acdc-5a2ebc2fb6c2
description: 'S�applique �: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 3cbe1cd879fb5a91d14b38f8a659a7f77d943fe7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782223"
---
# <a name="xlautoclose"></a>xlAutoClose

 **S’applique à**: Excel 2013 | Office 2013 | Visual Studio 
  
Appelée par Microsoft Excel lorsque le XLL est désactivée. Le complément est désactivé lorsqu’une session Excel se termine normalement. Le complément peut être désactivé par l’utilisateur lors d’une session Excel, et cette fonction est appelée dans ce cas.
  
Excel ne nécessite pas un ressource XLL à mettre en œuvre et exporter cette fonction, même s’il est conseillé de sorte que votre XLL permettre annuler l’inscription des fonctions et les commandes, libérer les ressources, annuler des personnalisations et ainsi de suite. Si les fonctions et les commandes ne sont pas explicitement retirées par la ressource XLL, Excel effectue cette action après l’appel de la fonction **xlAutoClose** . 
  
```cs
int WINAPI xlAutoClose(void);
```

## <a name="parameters"></a>Paramètres

Cette fonction prend aucun argument.
  
## <a name="property-valuereturn-value"></a>Propriété valeur/valeur de retour

Votre implémentation de cette fonction doit renvoyer 1 (**int**).
  
## <a name="remarks"></a>Remarques

Excel appelle la fonction **xlAutoClose** chaque fois que la ressource XLL est désactivée, autrement dit, déchargé de la mémoire. La ressource XLL est désactivée dans les situations suivantes : 
  
- À la fin normale d’une session Excel si active pendant cette session.
    
- Si explicitement déchargé lors d’une session Excel.
    
- Une solution XLL peut être déchargé de plusieurs façons :
    
- À l’aide du Gestionnaire de compléments.
    
- À partir d’une autre XLL qui appelle [xlfUnregister](xlfunregister-form-1.md) avec le nom de cette DLL comme argument uniquement. 
    
- À partir d’une feuille de macro XLM qui appelle [UNREGISTER](xlfunregister-form-1.md) portant le nom de cette DLL comme argument uniquement. 
    
Cette fonction doit effectuer les opérations suivantes :
  
- Supprimer les menus ou les éléments de menu qui ont été ajoutés à la ressource XLL.
    
- Exécuter le nettoyage global nécessaire.
    
- Supprimez tous les noms qui ont été créées, notamment les noms des fonctions exportées. N’oubliez pas qu’enregistrement de fonctions risque de créer des noms à créer, si l’argument quatrième pour **inscrire** est présent. 
    
## <a name="example"></a>Exemple

Consultez les fichiers `SAMPLES\EXAMPLE\EXAMPLE.C` et `SAMPLES\GENERIC\GENERIC.C` par exemple les implémentations de cette fonction. Le code suivant présente de `SAMPLES\GENERIC\GENERIC.C`.
  
```cs
int WINAPI xlAutoClose(void)
{
   int i;
   XLOPER12 xRes;
//
// This block first deletes all names added by xlAutoOpen or
// xlAutoRegister12. Next, it checks if the drop-down menu Generic still
// exists. If it does, it is deleted using xlfDeleteMenu. It then checks
// if the Test toolbar still exists. If it is, xlfDeleteToolbar is
// used to delete it.
//
// The following code to delete the defined names
// does not work in the current version of Excel. 
// You cannot delete these names once they are Registered.
// The code is left here in case the functionality becomes 
// available in a future version.
//
   for (i = 0; i < g_rgWorksheetFuncsRows; i++)
      Excel12f(xlfSetName, 0, 1, TempStr12(g_rgWorksheetFuncs[i][2]));
   for (i = 0; i < g_rgCommandFuncsRows; i++)
      Excel12f(xlfSetName, 0, 1, TempStr12(g_rgCommandFuncs[i][2]));
//
// Everything else works as documented.
//
   Excel12f(xlfGetBar, &amp;xRes, 3, TempInt12(10), TempStr12(L"Generic"), TempInt12(0));
   if (xRes.xltype != xltypeErr)
   {
      Excel12f(xlfDeleteMenu, 0, 2, TempNum12(10), TempStr12(L"Generic"));
      // Free the XLOPER12 returned by xlfGetBar //
      Excel12f(xlFree, 0, 1, (LPXLOPER12) &amp;xRes);
   }
   Excel12f(xlfGetToolbar, &amp;xRes, 2, TempInt12(7), TempStr12(L"Test"));
   if (xRes.xltype != xltypeErr)
   {
      Excel12f(xlfDeleteToolbar, 0, 1, TempStr12(L"Test"));
      // Free the XLOPER12 returned by xlfGetToolbar //
      Excel12f(xlFree, 0, 1, (LPXLOPER12) &amp;xRes);
   }
   return 1;
}
```

## <a name="see-also"></a>Voir aussi



[xlAutoOpen](xlautoopen.md)


[Gestionnaire de compléments et les fonctions de l’Interface XLL](add-in-manager-and-xll-interface-functions.md)

