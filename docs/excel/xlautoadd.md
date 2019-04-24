---
title: xlAutoAdd
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlAutoAdd
keywords:
- fonction xlAutoAdd [Excel 2007]
localization_priority: Normal
ms.assetid: c69299af-a28a-44d9-be10-9c9fb92e21f2
description: 'S�applique �: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 9a38d5dafd30fda87dda5eadf8fa97ab6e6768a7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303989"
---
# <a name="xlautoadd"></a>xlAutoAdd

 **S’applique à**: Excel 2013 | Office 2013 | Visual Studio 
  
Ajouté par Microsoft Excel chaque fois que l'utilisateur active le XLL au cours d'une session Excel à l'aide du gestionnaire de compléments. Cette fonction n'est pas appelée lorsqu'Excel démarre et charge un complément préinstallé.
  
Cette fonction peut être utilisée pour afficher une boîte de dialogue personnalisée qui indique à l'utilisateur que le complément a été activé, ou pour lire ou écrire dans le registre, ou pour vérifier les informations de licence, par exemple.
  
Excel ne requiert pas de XLL pour implémenter et exporter cette fonction.
  
```cs
int WINAPI xlAutoAdd(void);
```

## <a name="parameters"></a>Paramètres

Cette fonction ne prend aucun argument.
  
## <a name="property-valuereturn-value"></a>Valeur de propriété/valeur de renvoi

Votre implémentation de cette fonction doit renvoyer 1. (**int**).
  
## <a name="remarks"></a>Remarques

Utilisez cette fonction si votre XLL doit effectuer une opération lorsqu'elle est ajoutée par le gestionnaire de compléments.
  
## <a name="example"></a>Exemple

Voir `\SAMPLES\EXAMPLE\EXAMPLE.C` et `\SAMPLES\GENERIC\GENERIC.C` , par exemple, les implémentations de cette fonction. Le code suivant provient de `\SAMPLES\EXAMPLE\EXAMPLE.C`.
  
```cs
int WINAPI xlAutoAdd(void)
{
    XCHAR szBuf[255];
    wsprintfW((LPWSTR)szBuf, L"Thank you for adding Example.XLL\n"
            L"build date %hs, time %hs",__DATE__, __TIME__);
/* Display a dialog indicating that the XLL was successfully added */
    Excel12f(xlcAlert, 0, 2, TempStr12(szBuf), TempInt12(2));
    return 1;
}
```

## <a name="see-also"></a>Voir aussi



[xlAutoRemove](xlautoremove.md)


[Fonctions du Gestionnaire de compléments et de l’interface XLL](add-in-manager-and-xll-interface-functions.md)

