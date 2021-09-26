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
description: 'S’applique à : Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: c6f3f8de3fc3a4fcc3c6ade8d3378e578f4fb193
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59611195"
---
# <a name="xlfgetdef"></a>xlfGetDef

**S’applique à**: Excel 2013 | Office 2013 | Visual Studio 
  
Renvoie le nom, en tant que texte, qui est défini pour une zone, une valeur ou une formule particulière dans un workbook. Dans Excel, cette valeur s’affiche dans la  colonne Nom de la boîte de  dialogue Gestionnaire de noms, qui s’affiche lorsque vous cliquez sur Gestionnaire de noms dans la **section** Noms définis sous l’onglet **Formules.**  Utilisez **xlfGetDef** pour obtenir le nom qui correspond à une définition. Pour obtenir la définition d’un nom, utilisez [xlfGetName](xlfgetname.md).
  
```cpp
Excel12(xlfGetDef, LPXLOPER12 pxRes, 3, LPXLOPER12 pxDefText, LPXLOPER12 pxDocumentText, LPXLOPER12 pxTypeNum);
```

## <a name="parameters"></a>Paramètres

_pxDefText_ (**xltypeStr**)
  
Il peut s’agit de tout ce à quoi vous pouvez définir un nom à référencer, y compris une référence, une valeur, un objet ou une formule.
  
Les références doivent être données dans le style R1C1, par  `"R3C5"` exemple. Si  _pxDefText_ est une valeur ou une formule, il n’est pas nécessaire d’inclure le signe égal affiché dans la colonne **Références** dans la boîte de dialogue **Gestionnaire** de noms. S’il existe plusieurs noms  _pour pxDefText,_ **xlfGetDef** renvoie le prénom. Si aucun nom ne correspond  _à pxDefText_, **xlfGetDef** renvoie la valeur  `#NAME?` d’erreur. 
  
_pxDocumentText_ (**xltypeStr**)
  
Spécifie la feuille sur qui se trouve _pxDefText._ Si  _pxDocumentText_ est omis, il est supposé être la feuille active. 
  
_pxTypeNum_ (**xltypeNum**)
  
Nombre de 1 à 3 spécifiant les types de noms renvoyés.
  
|**_pxTypeNum_**|**Renvoie**|
|:-----|:-----|
|1 ou aucune  <br/> |Noms normaux uniquement.  <br/> |
|2  <br/> |Noms masqués uniquement.  <br/> |
|3  <br/> |Tous les noms.  <br/> |
   
## <a name="property-valuereturn-value"></a>Valeur de propriété/valeur de renvoi

 _pxRes_ (**xltypeStr** ou **xltypeErr**)
  
Renvoie le nom associé à la définition spécifiée.
  
## <a name="remarks"></a>Remarques

Le tableau suivant répertorie quatre exemples de valeurs renvoyées par un appel à **xlfGetDef** avec les arguments spécifiés. 
  
|**Nom défini dans Excel**|**_pxDefText_**|**_pxDocumentText_**|**_pxTypeNum_**|**Valeur renvoyée**|
|:-----|:-----|:-----|:-----|:-----|
|La plage spécifiée dans la feuille Sheet4 est nommée Ventes.  <br/> |« R2C2:R9C6 »  <br/> |« Sheet4 »  <br/> |\<omitted\>  <br/> |« Ventes »  <br/> |
|La valeur 100 dans la feuille Sheet4 est définie comme Constante.  <br/> |"100"  <br/> |« Sheet4 »  <br/> |\<omitted\>  <br/> |« Constante »  <br/> |
|La formule spécifiée dans la feuille Sheet4 est nommée SumTotal.  <br/> |« SUM(R1C1:R10C1) »  <br/> |« Sheet4 »  <br/> |\<omitted\>  <br/> |« SumTotal »  <br/> |
|3 est défini comme le nom masqué Counter de la feuille active.  <br/> |"3"  <br/> |\<omitted\>  <br/> |2  <br/> |« Counter »  <br/> |
   
## <a name="see-also"></a>Voir aussi

- [xlfGetName](xlfgetname.md)
- [Fonctions XLM essentielles et utiles de l’API C](essential-and-useful-c-api-xlm-functions.md)

