---
title: xlAutoRemove
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlAutoRemove
keywords:
- fonction xlautoremove [excel 2007]
localization_priority: Normal
ms.assetid: fff0de4d-605d-49e6-a5be-a000410c09d8
description: 'S�applique �: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 6e5daac21a6d89472a7d84a25e9aeaea56db1ae1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782220"
---
# <a name="xlautoremove"></a>xlAutoRemove

 **S’applique à**: Excel 2013 | Office 2013 | Visual Studio 
  
Appelée par Microsoft Excel lorsque l’utilisateur désactive le XLL pendant une session Excel à l’aide du Gestionnaire de compléments. Cette fonction n’est pas appelée lorsqu’une session Excel se ferme, normale ou anormale, avec le complément installé.
  
Cette fonction peut être utilisée pour afficher une boîte de dialogue personnalisée pour présenter à l’utilisateur que le complément a été désactivé, ou pour lire ou écrire dans le Registre, par exemple.
  
Excel ne nécessite pas un ressource XLL à mettre en œuvre et exporter cette fonction. 
  
```cs
int WINAPI xlAutoRemove(void);
```

## <a name="parameters"></a>Paramètres

Cette fonction prend aucun argument.
  
## <a name="property-valuereturn-value"></a>Propriété valeur/valeur de retour

Votre implémentation de cette fonction doit renvoyer 1 (**int**).
  
## <a name="remarks"></a>Remarques

Utilisez cette fonction si votre XLL a besoin effectuer toute tâche lorsqu’elle est supprimée par le Gestionnaire de compléments.
  
## <a name="example"></a>Exemple

Consultez les fichiers `\SAMPLES\EXAMPLE\EXAMPLE.C` et `\SAMPLES\GENERIC\GENERIC.C` par exemple les implémentations de cette fonction. Le code suivant présente de `\SAMPLES\EXAMPLE\EXAMPLE.C`.
  
```cs
int WINAPI xlAutoRemove(void)
{
/* Display a dialog box indicating that the XLL was successfully removed */
   Excel12f(xlcAlert, 0, 2,
      TempStr12(L"Thank you for removing Example.XLL!"),
      TempInt12(2));
   return 1;
}
```

## <a name="see-also"></a>Voir aussi



[xlAutoAdd](xlautoadd.md)


[Gestionnaire de compléments et les fonctions de l’Interface XLL](add-in-manager-and-xll-interface-functions.md)

