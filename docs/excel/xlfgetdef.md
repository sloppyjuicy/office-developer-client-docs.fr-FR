---
title: xlfGetDef
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
keywords:
- xlfGetDef
localization_priority: Normal
ms.assetid: 68f5edbd-9040-46d3-acd5-dd51ca82f6fa
description: 'S�applique �: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 014db553156849d84bd07e0e416f8cb3fefb4e0b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310240"
---
# <a name="xlfgetdef"></a>xlfGetDef

**S’applique à**: Excel 2013 | Office 2013 | Visual Studio 
  
Renvoie le nom, sous forme de texte, qui est défini pour une zone, une valeur ou une formule particulière dans un classeur. Dans Excel, cette valeur est affichée dans la colonne **nom** de la boîte de dialogue **Gestionnaire de noms** , qui s'affiche lorsque vous cliquez sur gestionnaire de **noms** dans la section **noms définis** de l'onglet **formules** . Utilisez **xlfGetDef** pour obtenir le nom qui correspond à une définition. Pour obtenir la définition d'un nom, utilisez [xlfGetName](xlfgetname.md).
  
```cpp
Excel12(xlfGetDef, LPXLOPER12 pxRes, 3, LPXLOPER12 pxDefText, LPXLOPER12 pxDocumentText, LPXLOPER12 pxTypeNum);
```

## <a name="parameters"></a>Paramètres

_pxDefText_ (**xltypeStr**)
  
Peut être tout ce que vous pouvez définir un nom auquel faire référence, y compris une référence, une valeur, un objet ou une formule.
  
Les références doivent être indiquées au format `"R3C5"`L1C1, comme. Si _pxDefText_ est une valeur ou une formule, il n'est pas nécessaire d'inclure le signe égal qui est affiché dans la colonne **fait référence à** dans la boîte de dialogue **Gestionnaire de noms** . S'il existe plusieurs noms pour _pxDefText_, **xlfGetDef** renvoie le prénom. Si aucun nom ne correspond à _pxDefText_, **xlfGetDef** renvoie la `#NAME?` valeur d'erreur. 
  
_pxDocumentText_ (**xltypeStr**)
  
Spécifie la feuille sur laquelle se trouve _pxDefText_ . Si _pxDocumentText_ est omis, il est supposé être la feuille active. 
  
_pxTypeNum_ (**xltypeNum**)
  
Un nombre compris entre 1 et 3 spécifiant les types de noms qui sont renvoyés.
  
|**_pxTypeNum_**|**Renvoie**|
|:-----|:-----|
|1 ou aucune  <br/> |Noms normaux uniquement.  <br/> |
|n°2  <br/> |Noms masqués uniquement.  <br/> |
|3  <br/> |Tous les noms.  <br/> |
   
## <a name="property-valuereturn-value"></a>Valeur de propriété/valeur de renvoi

 _pxRes_ (**xltypeStr** ou **xltypeErr**)
  
Renvoie le nom associé à la définition spécifiée.
  
## <a name="remarks"></a>Remarques

Le tableau suivant répertorie quatre exemples de valeurs renvoyées par un appel à **xlfGetDef** avec les arguments spécifiés. 
  
|**Nom défini dans Excel**|**_pxDefText_**|**_pxDocumentText_**|**_pxTypeNum_**|**Valeur renvoyée**|
|:-----|:-----|:-----|:-----|:-----|
|La plage spécifiée dans Sheet4 est nommée Sales.  <br/> |«R2C2: R9C6»  <br/> |Sheet4  <br/> |\<omis\>  <br/> |Ventes  <br/> |
|La valeur 100 dans Sheet4 est définie comme constante.  <br/> |«100»  <br/> |Sheet4  <br/> |\<omis\>  <br/> |Permanente  <br/> |
|La formule spécifiée dans Sheet4 est nommée SumTotal.  <br/> |"SUM (R1C1: R10C1)"  <br/> |Sheet4  <br/> |\<omis\>  <br/> |«SumTotal»  <br/> |
|3 est défini comme le compteur de nom masqué sur la feuille active.  <br/> |3  <br/> |\<omis\>  <br/> |n°2  <br/> |Lutte  <br/> |
   
## <a name="see-also"></a>Voir aussi

- [xlfGetName](xlfgetname.md)
- [Fonctions XLM essentielles et utiles de l’API C](essential-and-useful-c-api-xlm-functions.md)

