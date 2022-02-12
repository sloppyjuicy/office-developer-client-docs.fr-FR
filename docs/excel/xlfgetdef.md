---
title: xlfGetDef
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
keywords:
- xlfgetdef
ms.localizationpriority: medium
ms.assetid: 68f5edbd-9040-46d3-acd5-dd51ca82f6fa
ms.openlocfilehash: d664b31be4dc279bc5bfe0024db51e1f0b47dbed
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62776731"
---
# <a name="xlfgetdef"></a>xlfGetDef

**S’applique à**: Excel 2013 | Office 2013 | Visual Studio 
  
Renvoie le nom, en tant que texte, qui est défini pour une zone, une valeur ou une formule particulière dans un workbook. Dans Excel, cette valeur est affichée dans la colonne Nom de  la boîte de dialogue  Gestionnaire de noms, qui s’affiche lorsque vous cliquez sur  Gestionnaire de noms dans **la section Noms** définis sous l’onglet **Formules**. Utilisez **xlfGetDef** pour obtenir le nom qui correspond à une définition. Pour obtenir la définition d’un nom, utilisez [xlfGetName](xlfgetname.md).
  
```cpp
Excel12(xlfGetDef, LPXLOPER12 pxRes, 3, LPXLOPER12 pxDefText, LPXLOPER12 pxDocumentText, LPXLOPER12 pxTypeNum);
```

## <a name="parameters"></a>Paramètres

_pxDefText_ (**xltypeStr**)
  
Il peut s’agit de tout ce à quoi vous pouvez définir un nom à référencer, y compris une référence, une valeur, un objet ou une formule.
  
Les références doivent être données dans le style R1C1, par exemple  `"R3C5"`. Si  _pxDefText_ est une valeur ou une formule, il n’est pas nécessaire d’inclure le signe égal affiché dans la colonne **Références** dans la boîte de dialogue **Gestionnaire** de noms. S’il existe plusieurs noms pour  _pxDefText_, **xlfGetDef** renvoie le prénom. Si aucun nom ne correspond  _à pxDefText_, **xlfGetDef** renvoie la valeur d’erreur  `#NAME?` . 
  
_pxDocumentText_ (**xltypeStr**)
  
Spécifie la feuille sur qui  _se trouve pxDefText_ . Si  _pxDocumentText_ est omis, il est supposé être la feuille active. 
  
_pxTypeNum_ (**xltypeNum**)
  
Nombre de 1 à 3 spécifiant les types de noms renvoyés.
  
|**_pxTypeNum_**|**Renvoie**|
|:-----|:-----|
|1 ou aucune  <br/> |Noms normaux uniquement. |
|2  <br/> |Noms masqués uniquement. |
|3  <br/> |Tous les noms. |
   
## <a name="property-valuereturn-value"></a>Valeur de propriété/valeur de renvoi

 _pxRes_ (**xltypeStr** ou **xltypeErr**)
  
Renvoie le nom associé à la définition spécifiée.
  
## <a name="remarks"></a>Remarques

Le tableau suivant répertorie quatre exemples de valeurs renvoyées par un appel à **xlfGetDef** avec les arguments spécifiés. 
  
|**Nom défini dans Excel**|**_pxDefText_**|**_pxDocumentText_**|**_pxTypeNum_**|**Valeur renvoyée**|
|:-----|:-----|:-----|:-----|:-----|
|La plage spécifiée dans la feuille Sheet4 est nommée Ventes. |« R2C2:R9C6 »  <br/> |« Sheet4 »  <br/> |\<omitted\>  <br/> |« Ventes »  <br/> |
|La valeur 100 dans la feuille Sheet4 est définie comme Constante. |"100"  <br/> |« Sheet4 »  <br/> |\<omitted\>  <br/> |« Constante »  <br/> |
|La formule spécifiée dans la feuille Sheet4 est nommée SumTotal. |« SUM(R1C1:R10C1) »  <br/> |« Sheet4 »  <br/> |\<omitted\>  <br/> |« SumTotal »  <br/> |
|3 est défini comme le compteur de nom masqué dans la feuille active. |"3"  <br/> |\<omitted\>  <br/> |2  <br/> |« Counter »  <br/> |
   
## <a name="see-also"></a>Voir aussi

- [xlfGetName](xlfgetname.md)
- [Fonctions XLM essentielles et utiles de l’API C](essential-and-useful-c-api-xlm-functions.md)

