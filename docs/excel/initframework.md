---
title: InitFramework
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- InitFramework
keywords:
- fonction InitFramework [Excel 2007]
localization_priority: Normal
ms.assetid: c472a14a-92a6-46f6-924c-db8d6199d6fb
description: 'S’applique à : Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 34fe8f4a606956b90a0d005b0bc523cea460153f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420752"
---
# <a name="initframework"></a>InitFramework

 **S’applique à** : Excel 2013 | Office 2013 | Visual Studio 
  
Fonction de bibliothèque d'infrastructure qui initialise la bibliothèque d'infrastructure, qui initialise simplement les structures de données de mémoire de la mémoire de la bibliothèque **XLOPER**/ **** temporaire, en libérant toute mémoire déjà allouée. 
  
```cs
short WINAPI InitFramework(void);
```

## <a name="parameters"></a>Paramètres

Cette fonction ne prend aucun argument.
  
## <a name="return-value"></a>Valeur renvoyée

Cette fonction ne renvoie pas de valeur.
  
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

