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
ms.openlocfilehash: ccb04671e94879b2a7b4a961b6981ed89188c543
ms.sourcegitcommit: 193df57ebf141020852d2ebc8cf0931edb71574a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/25/2022
ms.locfileid: "62198477"
---
# <a name="initframework"></a>InitFramework

 **S’applique à**: Excel 2013 | Office 2013 | Visual Studio 
  
Fonction de bibliothèque d’infrastructure qui initialise la bibliothèque Framework, qui initialise simplement les structures de données mémoire /  **XLOPER XLOPER12** temporaires, libérant ainsi toute mémoire qui a déjà été allouée. 
  
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

