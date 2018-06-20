---
title: fExit
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- fExit
keywords:
- fonction fexit [excel 2007]
localization_priority: Normal
ms.assetid: d85685fa-df70-45bb-b629-a9d43b5cb926
description: 'S�applique �: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 3abb5cd68a45fbcd16665dbc4d492d764bbd315e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782116"
---
# <a name="fexit"></a>fExit

 **S’applique à**: Excel 2013 | Office 2013 | Visual Studio 
  
Exemple définies par l’utilisateur de commande qui décharge GENERIC.xll. Lorsque GENERIC.xll est chargé, il crée un menu défini par l’utilisateur, générique, par le biais de laquelle cette commande est accessible. 
  
```cs
int WINAPI fExit(void);
```

## <a name="parameters"></a>Paramètres

La fonction ne prend aucun paramètre.
  
## <a name="property-valuereturn-value"></a>Propriété valeur/valeur de retour

La fonction renvoie toujours 1.
  
## <a name="remarks"></a>Remarques

Il s’agit d’une routine initiées par l’utilisateur pour quitter GENERIC.xll doivent éviter d’appeler simplement `UNREGISTER("GENERIC.XLL")` dans cette fonction. Ce serait force annuler l’inscription de toutes les fonctions dans cette DLL, même s’ils sont enregistrés quelque part ailleurs. Annuler l’inscription au lieu de cela, les fonctions d’un à la fois. 
  
### <a name="example"></a>Exemple

Voir `\SAMPLES\GENERIC\GENERIC.C` pour le code source pour cette fonction. 
  
## <a name="see-also"></a>Voir aussi



[Fonctions de la DLL générique](functions-in-the-generic-dll.md)

