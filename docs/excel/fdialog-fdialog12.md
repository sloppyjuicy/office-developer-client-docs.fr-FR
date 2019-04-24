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
- fonction fdialog [Excel 2007], fonction fDialog12 [Excel 2007]
localization_priority: Normal
ms.assetid: a9a47408-07d1-4a00-9596-abc48b12392f
description: 'S�applique �: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 58d0df500c38534ec1315d2dab1517c1f5272ad5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32304066"
---
# <a name="fdialogfdialog12"></a>fDialog/fDialog12

 **S’applique à**: Excel 2013 | Office 2013 | Visual Studio 
  
Exemple de commande définie par l'utilisateur montrant comment créer une UDD Microsoft Excel (boîte de dialogue définie par l'utilisateur) dans une DLL à l'aide des fonctionnalités de la boîte de dialogue de l'API C. Lorsque GENERIC. xll est chargé, il crée un menu défini par l'utilisateur, générique, par le biais duquel cette commande est accédée.
  
```cs
int WINAPI fDialog(void);
```

## <a name="parameters"></a>Paramètres

La fonction ne prend aucun paramètre.
  
## <a name="property-valuereturn-value"></a>Valeur de propriété/valeur de renvoi

La fonction renvoie toujours 1.
  
### <a name="example"></a>Exemple

Voir `\SAMPLES\GENERIC\GENERIC.C` pour obtenir le code source de cette fonction. 
  
## <a name="see-also"></a>Voir aussi



[Fonctions dans le fichier DLL générique](functions-in-the-generic-dll.md)

