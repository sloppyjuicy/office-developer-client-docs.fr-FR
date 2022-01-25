---
title: fDialog/fDialog12
manager: lindalu
ms.date: 1/24/2022
ms.audience: Developer
ms.topic: reference
f1_keywords:
- fDialog
- fDialog12
keywords:
- fonction fdialog [excel 2007]
- fonction fDialog12 [Excel 2007]
ms.localizationpriority: medium
ms.assetid: a9a47408-07d1-4a00-9596-abc48b12392f
ms.openlocfilehash: f70634fa7c865b934d28a72a22199881949f99de
ms.sourcegitcommit: 193df57ebf141020852d2ebc8cf0931edb71574a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/25/2022
ms.locfileid: "62198344"
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

Voir `\SAMPLES\GENERIC\GENERIC.C` le code source pour cette fonction.
  
## <a name="see-also"></a>Voir aussi

[Fonctions dans le fichier DLL générique](functions-in-the-generic-dll.md)
