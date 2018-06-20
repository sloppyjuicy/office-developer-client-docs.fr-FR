---
title: xlfSetName
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlfSetName
keywords:
- fonction xlfSetName [excel 2007]
localization_priority: Normal
ms.assetid: ea7fd713-7c1b-4648-a609-3334f595c61a
description: 'S�applique �: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 48ce927f6bcb328a90779948a660cf9d0b460205
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782218"
---
# <a name="xlfsetname"></a>xlfSetName

**S’applique à**: Excel 2013 | Office 2013 | Visual Studio 
  
Permet de créer et supprimer des noms définis associés à la DLL.
  
```cs
Excel12(xlfSetName, LPXLOPER12 pxRes, 2, LPXLOPER12 pxNameText, LPXLOPER12 pxNameDefinition);
```

## <a name="parameters"></a>Paramètres

_pxNameText_ (**xltypeStr**)
  
Le nom de la plage qui doit être conforme aux limites habituelles dans Microsoft Excel sur les noms valides.
  
_pxNameDefinition_ (**xltypeStr**, **xltypeNum**, **xltypeBool**, **xltypeErr**, **xltypeMulti**, **xltypeSRef**, **xltypeRef**ou **xltypeInt**)
  
(Facultatif). La valeur, l’ensemble de valeurs, cellule ou plage de cellules que _pxNameText_ est défini en tant que. En cas d’omission, le nom est supprimé. 
  
## <a name="property-valuereturn-value"></a>Propriété valeur/valeur de retour

_pxRes_ (**xltypeBool** ou **xltypeErr**)
  
TRUE si l’opération a réussi, ou FALSE si le nom ne peut pas créer ou supprimer. Propriété renvoie #VALUE ! Si un ou plusieurs des arguments n’est pas valide.
  
## <a name="remarks"></a>Remarques

Lorsqu’une fonction ou une commande est enregistrée à l’aide de **xlfRegister** avec un argument valide _pxFunctionText_ , Excel crée un nom associé à la DLL de ressource. Lorsque votre DLL est déchargé, ces noms doivent être supprimés à l’aide de la [fonction xlfSetName](xlfsetname.md). Toutefois, en raison d’un problème connu dans Excel, cette opération de suppression échoue. Pour plus d�informations, consultez [Probl�mes connus concernant le d�veloppement de XLL Excel](known-issues-in-excel-xll-development.md).
  
### <a name="example"></a>Exemple

Voir le code de la fonction **xlAutoClose** dans `\SAMPLES\GENERIC\GENERIC.C`.
  
## <a name="see-also"></a>Voir aussi

- [Fonctions XLM API C essentielles et utiles](essential-and-useful-c-api-xlm-functions.md)

