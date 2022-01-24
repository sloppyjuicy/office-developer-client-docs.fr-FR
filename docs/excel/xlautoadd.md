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
ms.openlocfilehash: 3a5dfb456ecf511bb79fbfda7688d7f3e63fd246
ms.sourcegitcommit: 2411ec8262cd0ed92f8a072fb53b51e3e496d49e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/24/2022
ms.locfileid: "62179472"
---
# <a name="xlautoadd"></a>xlAutoAdd

 **S’applique à**: Excel 2013 | Office 2013 | Visual Studio 
  
Ajouté par le Microsoft Excel chaque fois que l’utilisateur active le XLL au cours d’une session Excel à l’aide du gestionnaire Add-In client. Cette fonction n’est pas appelée lorsque Excel démarre et charge un add-in préinstallé.
  
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

Voir `\SAMPLES\EXAMPLE\EXAMPLE.C` et par exemple les  `\SAMPLES\GENERIC\GENERIC.C` implémentations de cette fonction. Le code suivant provient de `\SAMPLES\EXAMPLE\EXAMPLE.C`.
  
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

