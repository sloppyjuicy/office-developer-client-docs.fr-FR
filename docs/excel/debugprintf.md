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
ms.localizationpriority: medium
ms.assetid: 9ad541f6-0b35-4f50-926a-8940e3f8033a
ms.openlocfilehash: 402b3c4cd1e198c8da131c7f596f1acd8e5b6eb5
ms.sourcegitcommit: 193df57ebf141020852d2ebc8cf0931edb71574a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/25/2022
ms.locfileid: "62198701"
---
# <a name="debugprintf"></a>debugPrintf

**S’applique à**: Excel 2013 | Office 2013 | Visual Studio 
  
Fonction de bibliothèque d’infrastructure qui écrit une chaîne d’byte terminée par null dans le déboguer actif via la fonction Windows SDK **OutputDebugStringA**. Si l’application n’a pas de débompeur, le débogger système affiche la chaîne. Si l’application n’a pas de déboguer et que le déboguer système n’est pas actif, **debugPrintf ne** fait rien. 
  
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

