---
title: xlfGetDef
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
keywords:
- xlfgetdef
localization_priority: Normal
ms.assetid: 68f5edbd-9040-46d3-acd5-dd51ca82f6fa
description: 'S�applique �: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 030c4e501e8a9eb4b6ce29d7fe0e171324b50b5c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782238"
---
# <a name="xlfgetdef"></a>xlfGetDef

**S’applique à**: Excel 2013 | Office 2013 | Visual Studio 
  
Renvoie le nom, sous forme de texte, qui est défini pour une zone particulière, une valeur ou une formule dans un classeur. Dans Excel, cette valeur est affichée dans la colonne **nom** de la boîte de dialogue **Gestionnaire de noms** qui s’affiche lorsque vous cliquez sur **Gestionnaire de noms** dans la section **Noms définis** sous l’onglet **formules** utiliser **xlfGetDef** pour obtenir le nom qui correspond à une définition. Pour obtenir la définition d’un nom, utilisez [xlfGetName](xlfgetname.md).
  
```cpp
Excel12(xlfGetDef, LPXLOPER12 pxRes, 3, LPXLOPER12 pxDefText, LPXLOPER12 pxDocumentText, LPXLOPER12 pxTypeNum);
```

## <a name="parameters"></a>Paramètres

_pxDefText_ (**xltypeStr**)
  
Peut être tout ce que vous pouvez définir un nom pour faire référence à, y compris une référence, une valeur, un objet ou une formule.
  
Références doivent figurer dans le style R1C1, tel que `"R3C5"`. Si _pxDefText_ est une valeur ou une formule, il n’est pas nécessaire d’inclure le signe égal qui est affiché dans la colonne **Fait référence à** la boîte de dialogue **Gestionnaire de noms** . S’il existe plusieurs noms pour _pxDefText_, **xlfGetDef** renvoie le premier nom. Si aucun nom correspond à _pxDefText_, **xlfGetDef** renvoie la `#NAME?` valeur d’erreur. 
  
_pxDocumentText_ (**xltypeStr**)
  
Spécifie la feuille qui _pxDefText_ se trouve sur. Si _pxDocumentText_ est omis, il est supposé pour être la feuille active. 
  
_pxTypeNum_ (**xltypeNum**)
  
Nombre compris entre 1 et 3 spécifiant les types de noms sont retournés.
  
|**_pxTypeNum_**|**Renvoie**|
|:-----|:-----|
|1 ou aucune  <br/> |Noms normales uniquement.  <br/> |
|2  <br/> |Noms masqués.  <br/> |
|3  <br/> |Tous les noms.  <br/> |
   
## <a name="property-valuereturn-value"></a>Propriété valeur/valeur de retour

 _pxRes_ (**xltypeStr** ou **xltypeErr**)
  
Renvoie le nom associé à la définition spécifiée.
  
## <a name="remarks"></a>Remarques

Le tableau suivant répertorie les quatre exemples des valeurs renvoyées par un appel à **xlfGetDef** avec les arguments spécifiés. 
  
|**Nom défini dans Excel**|**_pxDefText_**|**_pxDocumentText_**|**_pxTypeNum_**|**Valeur renvoyée**|
|:-----|:-----|:-----|:-----|:-----|
|La plage spécifiée dans Sheet4 est nommée Ventes.  <br/> |« R2C2:R9C6 »  <br/> |« Sheet4 »  <br/> |\<omis\>  <br/> |« Ventes »  <br/> |
|La valeur 100 Sheet4 est définie comme constante.  <br/> |« 100 »  <br/> |« Sheet4 »  <br/> |\<omis\>  <br/> |« Constante »  <br/> |
|La formule spécifiée dans Sheet4 est nommée SumTotal.  <br/> |« SUM(R1C1:R10C1) »  <br/> |« Sheet4 »  <br/> |\<omis\>  <br/> |« SumTotal »  <br/> |
|3 est défini comme nom masqué compteur dans la feuille active.  <br/> |« 3 »  <br/> |\<omis\>  <br/> |2  <br/> |« Compteur »  <br/> |
   
## <a name="see-also"></a>Voir aussi

- [xlfGetName](xlfgetname.md)
- [Fonctions XLM API C essentielles et utiles](essential-and-useful-c-api-xlm-functions.md)

