---
title: xlAutoOpen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlAutoOpen
keywords:
- fonction xlAutoOpen [Excel 2007]
localization_priority: Normal
ms.assetid: 748cecb6-61d0-496b-a1a4-a73d22eb29e2
description: 'S�applique �: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: bf02f71458f2f4d8514f69a6b6f0921b5318303a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310289"
---
# <a name="xlautoopen"></a>xlAutoOpen

 **S’applique à**: Excel 2013 | Office 2013 | Visual Studio 
  
Fonction de rappel qui doit être implémentée et exportée par chaque XLL valide. La fonction **xlAutoOpen** est l'emplacement recommandé à partir duquel enregistrer les fonctions et les commandes XLL, initialiser les structures de données, personnaliser l'interface utilisateur, etc. 
  
```cs
int WINAPI xlAutoOpen(void);
```

## <a name="parameters"></a>Paramètres

Cette fonction ne prend aucun argument.
  
## <a name="property-valuereturn-value"></a>Valeur de propriété/valeur de renvoi

Votre exécution de cette fonction doit renvoyer 1 (**ent**).
  
## <a name="remarks"></a>Remarques

Microsoft Excel appelle **xlAutoOpen** chaque fois que la XLL est activée. Le XLL est activé dans les situations suivantes: 
  
- Au début d'une session Excel si elle était active dans la dernière session Excel qui s'est terminée normalement.
    
- S'il est chargé pendant une session Excel.
    
- Un XLL peut être chargé de plusieurs façons:
    
- En choisissant **ouvrir** dans le menu **fichier** (où la version d'Excel prend en charge cette méthode de chargement des XLL). 
    
- À l’aide du Gestionnaire de compléments.
    
- À partir d'un autre XLL qui appelle [xlfRegister](xlfregister-form-1.md) avec le nom de cette dll comme étant le seul argument. 
    
- À partir d'une feuille macro XLM qui appelle [Register](xlfregister-form-1.md) avec le nom de cette dll comme étant le seul argument. 
    
- Si le complément est désactivé et réactivé au cours d'une session Excel, cette fonction est appelée lors de la réactivation.
    
### <a name="example"></a>Exemple

Voir les fichiers `SAMPLES\EXAMPLE\EXAMPLE.C` et `SAMPLES\GENERIC\GENERIC.C`et, par exemple, les implémentations de cette fonction.
  
## <a name="see-also"></a>Voir aussi



[xlAutoClose](xlautoclose.md)
  
[xlAutoRegister/xlAutoRegister12](xlautoregister-xlautoregister12.md)


[Fonctions du Gestionnaire de compléments et de l’interface XLL](add-in-manager-and-xll-interface-functions.md)

