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
ms.localizationpriority: medium
ms.assetid: d85685fa-df70-45bb-b629-a9d43b5cb926
description: 'S’applique à : Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 8a355955d2d31247fce1d5b875472b0e749e554b
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59617236"
---
# <a name="fexit"></a>fExit

 **S’applique à**: Excel 2013 | Office 2013 | Visual Studio 
  
Exemple de commande définie par l’utilisateur qui décharge GENERIC.xll. Lorsque GENERIC.xll est chargé, il crée un menu défini par l’utilisateur, Generic, via lequel cette commande est accessible. 
  
```cs
int WINAPI fExit(void);
```

## <a name="parameters"></a>Paramètres

La fonction ne prend aucun paramètre.
  
## <a name="property-valuereturn-value"></a>Valeur de propriété/valeur de renvoi

La fonction renvoie toujours 1.
  
## <a name="remarks"></a>Remarques

Il s’agit d’une routine initiée par l’utilisateur pour quitter GENERIC.xll Vous devez éviter  `UNREGISTER("GENERIC.XLL")` d’appeler simplement dans cette fonction. Cela désinsèrerait de force toutes les fonctions dans cette DLL, même si elles sont enregistrées ailleurs. Au lieu de cela, désinsser les fonctions une par une. 
  
### <a name="example"></a>Exemple

Voir  `\SAMPLES\GENERIC\GENERIC.C` le code source pour cette fonction. 
  
## <a name="see-also"></a>Voir aussi



[Fonctions dans le fichier DLL générique](functions-in-the-generic-dll.md)

