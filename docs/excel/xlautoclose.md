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
description: 'S’applique à : Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: e27ac922c4ba53a30e8e485d3210acc62b7d4bd3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310233"
---
# <a name="xlautoclose"></a>xlAutoClose

 **S’applique à**: Excel 2013 | Office 2013 | Visual Studio 
  
Activée par Microsoft Excel chaque fois que la XLL est désactivée. Le complément est désactivé lorsqu’une session Excel se termine normalement. Le complément peut être désactivé par l’utilisateur pendant une session Excel et, dans ce cas, cette fonction est activée.
  
Excel ne requiert pas de XLL pour exécuter et exporter cette fonction, bien que cela soit conseillé afin que votre XLL puisse désinscrire des fonctions et des commandes, libérer des ressources, annuler des personnalisations et ainsi de suite. Si les fonctions et les commandes ne sont pas explicitement désinscrites par la XLL, Excel l’effectue après avoir activé la fonction **xlAutoClose**. 
  
```cs
int WINAPI xlAutoClose(void);
```

## <a name="parameters"></a>Paramètres

Cette fonction ne prend aucun argument.
  
## <a name="property-valuereturn-value"></a>Valeur de propriété/valeur de renvoi

Votre exécution de cette fonction doit renvoyer 1 (**ent**).
  
## <a name="remarks"></a>Remarques

Excel active la fonction **xlAutoClose** chaque fois que la XLL est désactivée, autrement dit, déchargée à partir de la mémoire. La XLL est désactivée dans les situations suivantes : 
  
- À la fin d’une session normale Excel si celle-ci est active au cours de cette session.
    
- Si elle est explicitement déchargée pendant une session Excel.
    
- Une XLL peut être déchargée de différentes manières :
    
- À l’aide du Gestionnaire de compléments.
    
- À partir d’une autre XLL qui active [xlfUnregister](xlfunregister-form-1.md) avec le nom de cette DLL comme argument unique. 
    
- À partir d’une autre feuille macro XLL qui active [DÉSINCRIRE](xlfunregister-form-1.md) avec le nom de cette DLL comme argument unique. 
    
Cette fonction effectue les opérations suivantes :
  
- Supprimer les menus ou les éléments du menu qui ont été ajoutés via la XLL.
    
- Effectuer tout nettoyage général nécessaire.
    
- Supprimer les noms qui ont été créés en particulier les noms de fonctions exportées. N’oubliez pas qu’inscrire les fonctions peut entraîner la création de certains noms, si le quatrième argument de **INSCRIRE** est présent. 
    
## <a name="example"></a>Exemple

Reportez-vous aux fichiers `SAMPLES\EXAMPLE\EXAMPLE.C` et `SAMPLES\GENERIC\GENERIC.C` pour des exemples d’implémentation de cette fonction. Le code suivant provient de `SAMPLES\GENERIC\GENERIC.C`.
  
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


[Fonctions du Gestionnaire de compléments et de l’interface XLL](add-in-manager-and-xll-interface-functions.md)

