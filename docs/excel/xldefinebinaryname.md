---
title: xlDefineBinaryName
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlDefineBinaryName
keywords:
- fonction xldefinebinaryname [excel 2007]
ms.localizationpriority: medium
ms.assetid: e3e8f91b-cc31-4f09-9941-f950ae96820a
ms.openlocfilehash: 8fe7ce996dffa826d6cd6cd2870a9781e59be85a
ms.sourcegitcommit: 193df57ebf141020852d2ebc8cf0931edb71574a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/25/2022
ms.locfileid: "62199184"
---
# <a name="xldefinebinaryname"></a>xlDefineBinaryName

 **S’applique à**: Excel 2013 | Office 2013 | Visual Studio 
  
Utilisé pour allouer un stockage persistant pour **un xltypeBigData** **XLOPER** /  **XLOPER12**. Les données avec un nom binaire défini sont enregistrées avec le workbook et sont accessibles par nom à tout moment. Pour plus d’informations, voir « Limitation de l’étendue du nom binaire » dans Problèmes connus [Excel développement XLL.](known-issues-in-excel-xll-development.md)
  
```cs
Excel12(xlDefineBinaryName, 0, 2, LPXLOPER12 pxName, LPXLOPER12 pxData);
```

## <a name="parameters"></a>Paramètres

 _pxName_ (**xltypeStr**)
  
Chaîne spécifiant le nom des données. La chaîne est soumise aux mêmes restrictions d’attribution de noms que les noms définis.
  
 _pxData_ (**xltypeBigData**)
  
Structure bigdata spécifiant les données à stocker. Lorsque vous appelez cette fonction, le membre **lpbData** de la structure **bigdata** doit pointer vers les données pour lesquelles le nom est défini et le membre **cbData** doit contenir la longueur des données en octets. 
  
Si  _l’argument pxData_ n’est pas spécifié (**xltypeMissing**), l’allocation nommée spécifiée par  _pxName_ est supprimée. 
  
## <a name="see-also"></a>Voir aussi



[xlGetBinaryName](xlgetbinaryname.md)


[Fonctions de l’API C à appeler à partir d’un fichier DLL ou XLL](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)
  
[Problèmes connus dans le développement Excel XLL](known-issues-in-excel-xll-development.md)

