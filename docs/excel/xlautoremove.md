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
ms.localizationpriority: medium
ms.assetid: fff0de4d-605d-49e6-a5be-a000410c09d8
ms.openlocfilehash: 657009e82ff2f011fe36e3d2965768f33efe5a3d
ms.sourcegitcommit: 193df57ebf141020852d2ebc8cf0931edb71574a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/25/2022
ms.locfileid: "62198449"
---
# <a name="xlautoremove"></a>xlAutoRemove

 **S’applique à**: Excel 2013 | Office 2013 | Visual Studio 
  
Appelé par Microsoft Excel chaque fois que l’utilisateur désactive le XLL pendant une session Excel à l’aide du gestionnaire Add-In client. Cette fonction n’est pas appelée lors de la fermeture normale ou anormale d’une session Excel lorsque le complément est installé.
  
Cette fonction peut être utilisée pour afficher une boîte de dialogue personnalisée qui dit à l’utilisateur que le module a été désactivé, ou pour lire ou écrire dans le Registre, par exemple.
  
Excel ne nécessite pas de XLL pour implémenter et exporter cette fonction. 
  
```cs
int WINAPI xlAutoRemove(void);
```

## <a name="parameters"></a>Paramètres

Cette fonction ne prend aucun argument.
  
## <a name="property-valuereturn-value"></a>Valeur de propriété/valeur de renvoi

Votre exécution de cette fonction doit renvoyer 1 (**ent**).
  
## <a name="remarks"></a>Remarques

Utilisez cette fonction si votre XLL doit effectuer une tâche lorsqu’elle est supprimée par Add-In manager.
  
## <a name="example"></a>Exemple

Reportez-vous aux fichiers `\SAMPLES\EXAMPLE\EXAMPLE.C` et `\SAMPLES\GENERIC\GENERIC.C` pour des exemples d’implémentation de cette fonction. Le code suivant provient de `\SAMPLES\EXAMPLE\EXAMPLE.C`.
  
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


[Fonctions du Gestionnaire de compléments et de l’interface XLL](add-in-manager-and-xll-interface-functions.md)

