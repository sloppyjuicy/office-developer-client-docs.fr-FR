---
title: InitFramework
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- InitFramework
keywords:
- fonction initframework [excel 2007]
localization_priority: Normal
ms.assetid: c472a14a-92a6-46f6-924c-db8d6199d6fb
description: 'S�applique �: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 2d7e3286d794d6f21da9ef83ca44d18ec242c063
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782125"
---
# <a name="initframework"></a>InitFramework

 **S’applique à**: Excel 2013 | Office 2013 | Visual Studio 
  
Fonction de bibliothèque Framework initialise la bibliothèque Framework qui initialise simplement le temporaire **XLOPER**/ **XLOPER12** mémoire des structures de données libérer toute mémoire qui a déjà été attribuée. 
  
```cs
short WINAPI InitFramework(void);
```

## <a name="parameters"></a>Paramètres

Cette fonction prend aucun argument.
  
## <a name="return-value"></a>Valeur renvoy�e

Cette fonction ne retourne pas une valeur.
  
## <a name="example"></a>Exemple

Cet exemple utilise la fonction **InitFramework** pour libérer toute la mémoire temporaire. 
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI InitFrameworkExample(void)
{
    InitFramework();
    return 1;
}
```

## <a name="see-also"></a>Voir aussi



[Fonctions de la bibliothèque Framework](functions-in-the-framework-library.md)

