---
title: xlAutoAdd
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlAutoAdd
keywords:
- fonction xlautoadd [excel 2007]
ms.localizationpriority: medium
ms.assetid: c69299af-a28a-44d9-be10-9c9fb92e21f2
description: 'S’applique à : Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 574d5f446ec4114cfbf94bea984fb0df92f072f0
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59611215"
---
# <a name="xlautoadd"></a>xlAutoAdd

 **S’applique à**: Excel 2013 | Office 2013 | Visual Studio 
  
Ajouté par le Microsoft Excel chaque fois que l’utilisateur active le XLL au cours d’une session Excel à l’aide Add-In manager. Cette fonction n’est pas appelée lorsque Excel démarre et charge un module préinstallé.
  
Cette fonction permet d’afficher une boîte de dialogue personnalisée qui indique à l’utilisateur que le module complémentaire a été activé, de lire ou d’écrire dans le Registre, ou de vérifier les informations de licence, par exemple.
  
Excel ne nécessite pas de XLL pour implémenter et exporter cette fonction.
  
```cs
int WINAPI xlAutoAdd(void);
```

## <a name="parameters"></a>Paramètres

Cette fonction ne prend aucun argument.
  
## <a name="property-valuereturn-value"></a>Valeur de propriété/valeur de renvoi

Votre implémentation de cette fonction doit renvoyer 1. (**int**).
  
## <a name="remarks"></a>Remarques

Utilisez cette fonction si votre XLL doit faire quelque chose lorsqu’elle est ajoutée par Add-In manager.
  
## <a name="example"></a>Exemple

Voir  `\SAMPLES\EXAMPLE\EXAMPLE.C` et par exemple les  `\SAMPLES\GENERIC\GENERIC.C` implémentations de cette fonction. Le code suivant provient de `\SAMPLES\EXAMPLE\EXAMPLE.C`.
  
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

