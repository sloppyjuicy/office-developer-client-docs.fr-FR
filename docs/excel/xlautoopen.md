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
ms.localizationpriority: medium
ms.assetid: 748cecb6-61d0-496b-a1a4-a73d22eb29e2
ms.openlocfilehash: 685b4ea63f6aeb73754c1da8e474f2774c5a0df6
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63378365"
---
# <a name="xlautoopen"></a>xlAutoOpen

 **S’applique à**: Excel 2013 | Office 2013 | Visual Studio
  
Fonction de rappel qui doit être implémentée et exportée par chaque XLL valide. La **fonction xlAutoOpen** est l’endroit recommandé où enregistrer les commandes et fonctions XLL, initialiser les structures de données, personnaliser l’interface utilisateur, etc.
  
```cs
int WINAPI xlAutoOpen(void);
```

## <a name="parameters"></a>Paramètres

Cette fonction ne prend aucun argument.
  
## <a name="property-valuereturn-value"></a>Valeur de propriété/valeur de renvoi

Votre exécution de cette fonction doit renvoyer 1 (**ent**).
  
## <a name="remarks"></a>Remarques

Microsoft Excel **appelle xlAutoOpen** chaque fois que le XLL est activé. Le XLL est activé dans les situations suivantes :
  
- Au début d’une session Excel si elle était active dans la dernière session Excel qui s’est terminée normalement.

- S’il est chargé au cours d Excel session.

- Un XLL peut être chargé de plusieurs manières :

- En choisissant **Ouvrir** **dans le menu** Fichier (où la version de Excel prend en charge cette méthode de chargement des XL).

- À l’aide du Gestionnaire de compléments.

- À partir d’une autre XLL [qui appelle xlfRegister](xlfregister-form-1.md) avec le nom de cette DLL comme seul argument.

- À partir d’une feuille macro XLM qui appelle [REGISTER](xlfregister-form-1.md) avec le nom de cette DLL comme seul argument.

- Si le add-in est désactivé et réactivé pendant une session Excel, cette fonction est appelée lors de la réactivation.

### <a name="example"></a>Exemple

Consultez les fichiers `SAMPLES\EXAMPLE\EXAMPLE.C` et `SAMPLES\GENERIC\GENERIC.C`, par exemple, les implémentations de cette fonction.
  
## <a name="see-also"></a>Voir aussi

[xlAutoClose](xlautoclose.md)  
[xlAutoRegister/xlAutoRegister12](xlautoregister-xlautoregister12.md)
 [Fonctions du Gestionnaire de modules et de l’interface XLL](add-in-manager-and-xll-interface-functions.md)
