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
localization_priority: Normal
ms.assetid: c69299af-a28a-44d9-be10-9c9fb92e21f2
description: 'S�applique �: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: ae0b4ae2d5f5fc58c3e18ffa9d79ec4128cb4639
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782202"
---
# <a name="xlautoadd"></a>xlAutoAdd

 **S’applique à**: Excel 2013 | Office 2013 | Visual Studio 
  
Ajouté par Microsoft Excel lorsque l’utilisateur Active la XLL pendant une session Excel à l’aide du Gestionnaire de compléments. Cette fonction n’est pas appelée lorsqu’Excel démarre et charge un complément préinstallé.
  
Cette fonction peut être utilisée pour afficher une boîte de dialogue personnalisée qui indique à l’utilisateur que le complément a été activé, ou pour lire ou écrire dans le Registre ou pour vérifier les informations de licence, par exemple.
  
Excel ne nécessite pas un ressource XLL à mettre en œuvre et exporter cette fonction.
  
```cs
int WINAPI xlAutoAdd(void);
```

## <a name="parameters"></a>Paramètres

Cette fonction prend aucun argument.
  
## <a name="property-valuereturn-value"></a>Propriété valeur/valeur de retour

Votre implémentation de cette fonction doit renvoyer 1. (**int**).
  
## <a name="remarks"></a>Remarques

Utilisez cette fonction si rien que votre XLL doit faire lorsqu’elle est ajoutée par le Gestionnaire de compléments.
  
## <a name="example"></a>Exemple

Voir `\SAMPLES\EXAMPLE\EXAMPLE.C` et `\SAMPLES\GENERIC\GENERIC.C` par exemple les implémentations de cette fonction. Le code suivant présente de `\SAMPLES\EXAMPLE\EXAMPLE.C`.
  
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


[Gestionnaire de compléments et les fonctions de l’Interface XLL](add-in-manager-and-xll-interface-functions.md)

