---
title: fDialog/fDialog12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- fDialog
- fDialog12
keywords:
- fdialog function [excel 2007],fDialog12 function [Excel 2007]
ms.localizationpriority: medium
ms.assetid: a9a47408-07d1-4a00-9596-abc48b12392f
description: 'S’applique à : Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: afcf924e04f833ff823647eef603824652347e5d
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59568193"
---
# <a name="fdialogfdialog12"></a>fDialog/fDialog12

 **S’applique à**: Excel 2013 | Office 2013 | Visual Studio 
  
Exemple de commande définie par l’utilisateur qui montre comment créer un UDD Microsoft Excel (boîte de dialogue définie par l’utilisateur) dans une DLL à l’aide des fonctionnalités de la boîte de dialogue dans l’API C. Lorsque GENERIC.xll est chargé, il crée un menu défini par l’utilisateur, Generic, via lequel cette commande est accessible.
  
```cs
int WINAPI fDialog(void);
```

## <a name="parameters"></a>Paramètres

La fonction ne prend aucun paramètre.
  
## <a name="property-valuereturn-value"></a>Valeur de propriété/valeur de renvoi

La fonction renvoie toujours 1.
  
### <a name="example"></a>Exemple

Voir  `\SAMPLES\GENERIC\GENERIC.C` le code source pour cette fonction. 
  
## <a name="see-also"></a>Voir aussi



[Fonctions dans le fichier DLL générique](functions-in-the-generic-dll.md)

