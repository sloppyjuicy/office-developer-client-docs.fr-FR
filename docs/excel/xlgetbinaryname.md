---
title: xlGetBinaryName
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlGetBinaryName
keywords:
- fonction xlgetbinaryname [excel 2007]
ms.localizationpriority: medium
ms.assetid: 66af3f78-65b5-42e0-82f9-ffd639d41751
ms.openlocfilehash: b922cb4ac6336c0f9334e1639f08cdd6680db7f3
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63381872"
---
# <a name="xlgetbinaryname"></a>xlGetBinaryName

**S’applique à**: Excel 2013 | Office 2013 | Visual Studio
  
Utilisé pour renvoyer un handle pour les données enregistrées par la fonction [xlDefineBinaryName](xldefinebinaryname.md). Les données avec un nom binaire défini sont enregistrées avec le workbook et sont accessibles par nom à tout moment. Pour plus d’informations, voir « Limite d’étendue du nom binaire » dans [Problèmes connus Excel développement XLL.](known-issues-in-excel-xll-development.md)
  
```cs
Excel12(xlGetBinaryName, LPXLOPER12 pxRes, 1, LPXLOPER12 pxName);
```

## <a name="parameters"></a>Paramètres

_pxRes_ (**xltypeBigData** ou **xltypeErr**)
  
Structure bigdata spécifiant les données récupérées ou une erreur indique que les données n’ont pas pu être récupérées ou que le nom n’est pas défini. Lorsque la fonction est de retour, le **membre hdata** de **la XLOPERXLOPER12**/  contient un handle pour les données nommées. _PxRes doit_ être libéré dans un appel à **xlFree** lorsque ce n’est plus nécessaire.
  
_pxName_ (**xltypeStr**)
  
Chaîne spécifiant le nom des données.
  
## <a name="remarks"></a>Remarques

Microsoft Excel la poignée de mémoire renvoyée en **hdata**. Dans Windows, le handle est un dent de mémoire global (alloué par la **fonction GlobalAlloc**).
  
## <a name="see-also"></a>Voir aussi

- [xlDefineBinaryName](xldefinebinaryname.md)
- [Fonctions de l’API C à appeler à partir d’un fichier DLL ou XLL](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)
