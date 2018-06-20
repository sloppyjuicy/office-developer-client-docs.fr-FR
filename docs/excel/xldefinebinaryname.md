---
title: xlDefineBinaryName
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlDefineBinaryName
keywords:
- fonction xlDefineBinaryName [excel 2007]
localization_priority: Normal
ms.assetid: e3e8f91b-cc31-4f09-9941-f950ae96820a
description: 'S�applique �: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 14515cc262ea398a9f200c0de3a1f6b64c758b3d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782208"
---
# <a name="xldefinebinaryname"></a>xlDefineBinaryName

 **S’applique à**: Excel 2013 | Office 2013 | Visual Studio 
  
Utilisé pour allouer un stockage persistant pour un **xltypeBigData** **XLOPER**/ **XLOPER12**. Données avec un nom défini binaire sont enregistrées avec le classeur et est accessible par un nom à tout moment. Pour plus d’informations, voir « Limitation d’étendue nom binaire » dans [Les problèmes connus dans le développement de XLL Excel](known-issues-in-excel-xll-development.md).
  
```cs
Excel12(xlDefineBinaryName, 0, 2, LPXLOPER12 pxName, LPXLOPER12 pxData);
```

## <a name="parameters"></a>Paramètres

 _pxName_ (**xltypeStr**)
  
Chaîne spécifiant le nom des données. La chaîne est soumis aux mêmes restrictions de dénomination noms définis comme.
  
 _pxData_ (**xltypeBigData**)
  
Structure Bigdata spécifiant les données à stocker. Lorsque vous appelez cette fonction, le membre **lpbData** de la structure **bigdata** doit pointer sur les données pour lequel le nom est défini, et le membre **cbData** doit contenir la longueur des données en octets. 
  
Si l’argument _pxData_ n’est pas spécifié (**xltypeMissing**), l’allocation nommée spécifiée par _pxName_ est supprimée. 
  
## <a name="see-also"></a>Voir aussi



[xlGetBinaryName](xlgetbinaryname.md)


[Fonctions de l’API C qui peuvent être appelées uniquement à partir d’une DLL ou XLL](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)
  
[Problèmes connus concernant le développement de XLL Excel](known-issues-in-excel-xll-development.md)

