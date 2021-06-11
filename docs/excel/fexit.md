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
description: 'S’applique à : Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 97f0a1ec797176fb51c87c58f94e46a323ae5b32
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429914"
---
# <a name="fexit"></a>fExit

 **S’applique à** : Excel 2013 | Office 2013 | Visual Studio 
  
Exemple de commande définie par l’utilisateur qui décharge GENERIC.xll. Lorsque GENERIC.xll est chargé, il crée un menu défini par l’utilisateur, Generic, via lequel cette commande est accessible. 
  
```cs
int WINAPI fExit(void);
```

## <a name="parameters"></a>Parameters

La fonction ne prend aucun paramètre.
  
## <a name="property-valuereturn-value"></a>Valeur de propriété/valeur de renvoi

La fonction renvoie toujours 1.
  
## <a name="remarks"></a>Remarques

Il s’agit d’une routine initiée par l’utilisateur pour quitter GENERIC.xll Vous devez éviter  `UNREGISTER("GENERIC.XLL")` d’appeler simplement dans cette fonction. Cela désinsèrerait de force toutes les fonctions dans cette DLL, même si elles sont enregistrées ailleurs. Au lieu de cela, désinsser les fonctions une par une. 
  
### <a name="example"></a>Exemple

Voir  `\SAMPLES\GENERIC\GENERIC.C` le code source pour cette fonction. 
  
## <a name="see-also"></a>Voir aussi



[Fonctions dans le fichier DLL générique](functions-in-the-generic-dll.md)

