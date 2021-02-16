---
title: xlAutoOpen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlAutoOpen
keywords:
- fonction xlautoopen [excel 2007]
localization_priority: Normal
ms.assetid: 748cecb6-61d0-496b-a1a4-a73d22eb29e2
description: 'S’applique à : Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: bf02f71458f2f4d8514f69a6b6f0921b5318303a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406646"
---
# <a name="xlautoopen"></a>xlAutoOpen

 **S’applique à** : Excel 2013 | Office 2013 | Visual Studio 
  
Fonction de rappel qui doit être implémentée et exportée par chaque XLL valide. La **fonction xlAutoOpen** est l’endroit recommandé où enregistrer les commandes et fonctions XLL, initialiser les structures de données, personnaliser l’interface utilisateur, etc. 
  
```cs
int WINAPI xlAutoOpen(void);
```

## <a name="parameters"></a>Paramètres

Cette fonction ne prend aucun argument.
  
## <a name="property-valuereturn-value"></a>Valeur de propriété/valeur de renvoi

Votre exécution de cette fonction doit renvoyer 1 (**ent**).
  
## <a name="remarks"></a>Remarques

Microsoft Excel appelle **xlAutoOpen chaque** fois que le XLL est activé. Le XLL est activé dans les situations suivantes : 
  
- Au début d’une session Excel si elle était active dans la dernière session Excel qui s’est terminée normalement.
    
- S’il est chargé pendant une session Excel.
    
- Un XLL peut être chargé de plusieurs manières :
    
- En choisissant **Ouvrir** dans le menu **Fichier** (où la version d’Excel prend en charge cette méthode de chargement de XL). 
    
- À l’aide du Gestionnaire de compléments.
    
- À partir d’une autre XLL qui appelle [xlfRegister](xlfregister-form-1.md) avec le nom de cette DLL comme seul argument. 
    
- À partir d’une feuille macro XLM qui appelle [REGISTER](xlfregister-form-1.md) avec le nom de cette DLL comme seul argument. 
    
- Si le add-in est désactivé et réactivé pendant une session Excel, cette fonction est appelée lors de la réactivation.
    
### <a name="example"></a>Exemple

Consultez les  `SAMPLES\EXAMPLE\EXAMPLE.C` fichiers  `SAMPLES\GENERIC\GENERIC.C` et, par exemple, les implémentations de cette fonction.
  
## <a name="see-also"></a>Voir aussi



[xlAutoClose](xlautoclose.md)
  
[xlAutoRegister/xlAutoRegister12](xlautoregister-xlautoregister12.md)


[Fonctions du Gestionnaire de compléments et de l’interface XLL](add-in-manager-and-xll-interface-functions.md)

