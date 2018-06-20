---
title: debugPrintf
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- debugPrintf
keywords:
- fonction debugprintf [excel 2007]
localization_priority: Normal
ms.assetid: 9ad541f6-0b35-4f50-926a-8940e3f8033a
description: 'S�applique �: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 25669cfc705e797b80be0fab590d809e8f1e3b5c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782015"
---
# <a name="debugprintf"></a>debugPrintf

**S’applique à**: Excel 2013 | Office 2013 | Visual Studio 
  
Fonction de bibliothèque Framework écrit une chaîne octet se terminant par null dans le débogueur actif via la fonction Windows SDK **OutputDebugStringA**. Si l’application ne possède aucun débogueur, le débogueur système affiche la chaîne. Si l’application ne possède aucun débogueur et le débogueur système n’est pas actif, **debugPrintf** est sans effet. 
  
Cette fonction ne retourne pas une valeur.
  
```cs
void WINAPI debugPrintf(LPSTR lpFormat, arguments);
```

## <a name="parameters"></a>Paramètres

 _lpFormat (LPSTR)_
  
La chaîne de format qui suit la syntaxe et les règles qui est utilisée avec la fonction **sprintf** . 
  
 _arguments_
  
Zéro ou plusieurs arguments pour la correspondance de la chaîne de format.
  
## <a name="example"></a>Exemple

Cette fonction imprime une chaîne pour indiquer que le contrôle a été passé à celui-ci. L’indicateur _DEBUG doit être définie avant la compilation, sinon cette fonction n’a aucun effet.
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI debugPrintfExample(void)
{
#ifdef _DEBUG
   debugPrintf("Made it!\r");
#endif
   return 1;
}

```

## <a name="see-also"></a>Voir aussi



[Fonctions de la bibliothèque Framework](functions-in-the-framework-library.md)

