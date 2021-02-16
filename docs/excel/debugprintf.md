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
description: 'S’applique à : Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 08bde61573874c137b18856fd24d23b324a35328
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424797"
---
# <a name="debugprintf"></a>debugPrintf

**S’applique à** : Excel 2013 | Office 2013 | Visual Studio 
  
Fonction de bibliothèque d’infrastructure qui écrit une chaîne d’byte terminée par null dans le déboguer actif via la fonction SDK Windows **OutputDebugStringA**. Si l’application n’a pas de débompeur, le débogger système affiche la chaîne. Si l’application n’a pas de déboguer et que le déboguer système n’est pas actif, **debugPrintf ne** fait rien. 
  
Cette fonction ne retourne pas de valeur.
  
```cs
void WINAPI debugPrintf(LPSTR lpFormat, arguments);
```

## <a name="parameters"></a>Paramètres

 _lpFormat (LPSTR)_
  
Chaîne de format, qui suit la syntaxe et les règles de celle utilisée avec la **fonction sprintf.** 
  
 _arguments_
  
Zéro ou plusieurs arguments pour correspondre à la chaîne de format.
  
## <a name="example"></a>Exemple

Cette fonction imprime une chaîne pour montrer que le contrôle lui a été passé. L_DEBUG de base doit être défini avant la compilation, sinon cette fonction ne fait rien.
  
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

