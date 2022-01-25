---
title: xlfSetName
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlfSetName
keywords:
- fonction xlfsetname [excel 2007]
ms.localizationpriority: medium
ms.assetid: ea7fd713-7c1b-4648-a609-3334f595c61a
ms.openlocfilehash: 096c71fa2d96d516b6e0f3f6b1ed3d7e65984f55
ms.sourcegitcommit: 193df57ebf141020852d2ebc8cf0931edb71574a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/25/2022
ms.locfileid: "62199699"
---
# <a name="xlfsetname"></a>xlfSetName

**S’applique à**: Excel 2013 | Office 2013 | Visual Studio 
  
Utilisé pour créer et supprimer des noms définis associés à la DLL.
  
```cs
Excel12(xlfSetName, LPXLOPER12 pxRes, 2, LPXLOPER12 pxNameText, LPXLOPER12 pxNameDefinition);
```

## <a name="parameters"></a>Paramètres

_pxNameText_ (**xltypeStr**)
  
Nom de la plage, qui doit être conforme aux limitations habituelles dans Microsoft Excel sur les noms valides.
  
_pxNameDefinition_ (**xltypeStr**, **xltypeNum**, **xltypeBool**, **xltypeErr**, **xltypeMulti**, **xltypeSRef**, **xltypeRef** ou **xltypeInt**)
  
(Facultatif). Valeur, ensemble de valeurs, cellule ou plage de cellules définies par _pxNameText._ S’il est omis, le nom est supprimé. 
  
## <a name="property-valuereturn-value"></a>Valeur de propriété/valeur de renvoi

_pxRes_ (**xltypeBool** ou **xltypeErr**)
  
TRUE si l’opération a réussi ou FALSE si le nom n’a pas pu être créé ou supprimé. Renvoie #VALUE ! si un ou plusieurs arguments n’étaient pas valides.
  
## <a name="remarks"></a>Remarques

Lorsqu’une fonction ou une commande est enregistrée à l’aide de **xlfRegister** avec un argument _pxFunctionText_ valide, Excel crée un nom associé à la ressource DLL. Lorsque votre DLL est déchargée, ces noms doivent être supprimés à l’aide de la [fonction xlfSetName](xlfsetname.md). Toutefois, en raison d’un problème connu dans Excel, cette opération de suppression échoue. Pour plus d’informations, reportez-vous à la rubrique [Problèmes connus concernant le développement de XLL Excel](known-issues-in-excel-xll-development.md).
  
### <a name="example"></a>Exemple

Voir le code de la **fonction xlAutoClose** dans  `\SAMPLES\GENERIC\GENERIC.C` .
  
## <a name="see-also"></a>Voir aussi

- [Fonctions XLM essentielles et utiles de l’API C](essential-and-useful-c-api-xlm-functions.md)

