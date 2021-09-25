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
ms.localizationpriority: medium
ms.assetid: c472a14a-92a6-46f6-924c-db8d6199d6fb
description: 'S’applique à : Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 932d1a42c104b364d6f6d584e4e8848469405688
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59621429"
---
# <a name="initframework"></a>InitFramework

 **S’applique à**: Excel 2013 | Office 2013 | Visual Studio 
  
Fonction de la bibliothèque Framework qui initialise la bibliothèque Framework, qui initialise simplement les structures de données mémoire /  **XLOPER XLOPER12** temporaires, libérant ainsi toute mémoire déjà allouée. 
  
```cs
short WINAPI InitFramework(void);
```

## <a name="parameters"></a>Paramètres

Cette fonction ne prend aucun argument.
  
## <a name="return-value"></a>Valeur renvoyée

Cette fonction ne retourne pas de valeur.
  
## <a name="example"></a>Exemple

Cet exemple utilise la **fonction InitFramework** pour libérer toute la mémoire temporaire. 
  
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

