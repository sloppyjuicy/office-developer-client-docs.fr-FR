---
title: xlfGetName
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
keywords:
- xlfgetname
localization_priority: Normal
ms.assetid: 65780435-aaa2-47af-b44f-07be7aa769ee
description: 'S’applique à : Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: fdee0146ae2199097828e98abb96ffe43a64fc80
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436628"
---
# <a name="xlfgetname"></a>xlfGetName

**S’applique à** : Excel 2013 | Office 2013 | Visual Studio 
  
Renvoie la définition d’un nom tel qu’il  apparaît dans la colonne **Références**  de la boîte de dialogue Gestionnaire de noms, qui s’affiche lorsque vous cliquez sur Gestionnaire de noms dans la **section** Noms définis sous l’onglet **Formules.** Si la définition contient des références, elles sont données en tant que références de style R1C1. Utilisez **xlfGetName pour vérifier** la valeur définie par un nom. Pour obtenir le nom qui correspond à une définition, utilisez [xlfGetDef](xlfgetdef.md).
  
```cpp
Excel12(xlfGetName, LPXLOPER12 pxRes, 2, LPXLOPER12 pxNameText, LPXLOPER12 pxInfoType);
```

## <a name="parameters"></a>Parameters

_pxNameText_ (**xltypeStr**)
  
Il peut s’agit d’un nom défini dans la feuille . une référence externe à un nom défini dans le livre de travail actif, par exemple, ou une référence externe à un nom défini sur un workbook ouvert  `"!Sales"` particulier, par exemple,  `"[Book1]SHEET1!Sales"` .  _pxNameText_ peut également être un nom masqué. 
  
_pxInfoType_ (**xltypeBool**)
  
Spécifie le type d’informations à renvoyer sur le nom. Si **false** ou omis, la définition est renvoyée. Si **true**, renvoie **TRUE** si le nom est défini uniquement pour la feuille, **FALSE** si le nom est défini pour l’ensemble du workbook. 
  
## <a name="property-valuereturn-value"></a>Valeur de propriété/valeur de renvoi

_pxRes_ (**xltypeStr**, **xltypeBool** ou **xltypeErr**)
  
En fonction de la valeur passée pour  _pxInfoType_, renvoie la définition du nom spécifié (**xltypeStr**), ou **TRUE** ou **FALSE** (**xltypeBool**).
  
## <a name="remarks"></a>Remarques

Si  la case à cocher Protéger la feuille de  calcul et le contenu des cellules verrouillées a été sélectionnée dans la boîte de dialogue Protéger la feuille pour protéger le workbook contenant le nom, **xlfGetName** renvoie la valeur `#N/A` d’erreur. Pour voir la boîte **de dialogue Protéger la feuille,** cliquez sur Protéger la **feuille** dans la section **Modifications** de **l’onglet** Révision. 
  
Le tableau suivant répertorie trois exemples de valeurs renvoyées par un appel à **xlfGetDef** avec l’argument  _pxNameText_ spécifié. 
  
|**Définition dans Excel**|**_pxNameText_**|**Valeur renvoyée**|
|:-----|:-----|:-----|
|Le nom Ventes sur une feuille est défini comme le numéro 523.  <br/> |« Ventes »  <br/> |« =523 »  <br/> |
|Le nom Profit de la feuille active est défini comme la formule =Sales-Costs.  <br/> |"! Profit »  <br/> |« =Sales-Costs »  <br/> |
|Le nom Base de données de la feuille active est défini comme la plage A1:F500.  <br/> |"! Base de données »  <br/> |« =R1C1:R500C6 »  <br/> |
   
## <a name="see-also"></a>Voir aussi

- [xlfGetDef](xlfgetdef.md)
- [Fonctions XLM essentielles et utiles de l’API C](essential-and-useful-c-api-xlm-functions.md)

