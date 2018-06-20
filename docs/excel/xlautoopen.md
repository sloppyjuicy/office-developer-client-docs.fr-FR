---
title: xlAutoOpen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlAutoOpen
keywords:
- fonction xlAutoOpen [excel 2007]
localization_priority: Normal
ms.assetid: 748cecb6-61d0-496b-a1a4-a73d22eb29e2
description: 'S�applique �: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: bf64841cbd75e25443abe5cfc7d3d7419757e245
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782203"
---
# <a name="xlautoopen"></a>xlAutoOpen

 **S’applique à**: Excel 2013 | Office 2013 | Visual Studio 
  
Fonction de rappel qui doit être implémentée et exportée par chaque XLL valide. La fonction **xlAutoOpen** est recommandée à partir duquel enregistrer les fonctions et commandes XLL, initialiser les structures de données, personnaliser l’interface utilisateur et ainsi de suite. 
  
```cs
int WINAPI xlAutoOpen(void);
```

## <a name="parameters"></a>Paramètres

Cette fonction prend aucun argument.
  
## <a name="property-valuereturn-value"></a>Propriété valeur/valeur de retour

Votre implémentation de cette fonction doit renvoyer 1 (**int**).
  
## <a name="remarks"></a>Remarques

Microsoft Excel appelle **xlAutoOpen** chaque fois que la ressource XLL est activée. La ressource XLL est activée dans les situations suivantes : 
  
- Au début d’une session Excel si elle a été actif dans la dernière session Excel qui s’est terminée normalement.
    
- Si chargée pendant une session d’Excel.
    
- Une solution XLL peut être chargé de plusieurs façons :
    
- En cliquant sur **Ouvrir** dans le menu **fichier** (où la version d’Excel prend en charge cette méthode de chargement XLL). 
    
- À l’aide du Gestionnaire de compléments.
    
- À partir d’une autre XLL qui appelle [xlfRegister](xlfregister-form-1.md) portant le nom de cette DLL comme argument uniquement. 
    
- À partir d’une feuille de macro XLM qui appelle [l’inscrire](xlfregister-form-1.md) avec le nom de cette DLL comme argument uniquement. 
    
- Si le complément est désactivé et réactivé pendant une session Excel, cette fonction est appelée sur réactivation.
    
### <a name="example"></a>Exemple

Consultez les fichiers `SAMPLES\EXAMPLE\EXAMPLE.C` et `SAMPLES\GENERIC\GENERIC.C`, par exemple les implémentations de cette fonction et.
  
## <a name="see-also"></a>Voir aussi



[xlAutoClose](xlautoclose.md)
  
[xlAutoRegister/xlAutoRegister12](xlautoregister-xlautoregister12.md)


[Gestionnaire de compléments et les fonctions de l’Interface XLL](add-in-manager-and-xll-interface-functions.md)

