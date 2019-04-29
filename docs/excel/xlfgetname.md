---
title: xlfGetName
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
keywords:
- xlfGetName
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
  
Renvoie la définition d'un nom tel qu'il apparaît dans la colonne **fait référence à** de la boîte de dialogue **Gestionnaire de noms** , qui s'affiche lorsque vous cliquez sur **Gestionnaire de noms** dans la section **noms définis** sous l'onglet **formules** . Si la définition contient des références, celles-ci sont indiquées sous forme de références de style R1C1. Utilisez **xlfGetName** pour vérifier la valeur définie par un nom. Pour obtenir le nom qui correspond à une définition, utilisez [xlfGetDef](xlfgetdef.md).
  
```cpp
Excel12(xlfGetName, LPXLOPER12 pxRes, 2, LPXLOPER12 pxNameText, LPXLOPER12 pxInfoType);
```

## <a name="parameters"></a>Paramètres

_pxNameText_ (**xltypeStr**)
  
Peut être un nom défini sur la feuille; référence externe à un nom défini dans le classeur actif, par exemple, `"!Sales"`; ou une référence externe à un nom défini sur un classeur ouvert particulier, par exemple `"[Book1]SHEET1!Sales"`.  _pxNameText_ peut également être un nom masqué. 
  
_pxInfoType_ (**xltypeBool**)
  
Spécifie le type d'informations à renvoyer sur le nom. Si la **valeur** est false ou omise, la définition est renvoyée. Si la **valeur est true**, renvoie **true** si le nom est défini pour la seule feuille, **false** si le nom est défini pour l'intégralité du classeur. 
  
## <a name="property-valuereturn-value"></a>Valeur de propriété/valeur de renvoi

_pxRes_ (**xltypeStr**, **xltypeBool**ou **xltypeErr**)
  
En fonction de la valeur transmise pour _pxInfoType_, renvoie la définition du nom spécifié (**XltypeStr**) ou **true** ou **false** (**xltypeBool**).
  
## <a name="remarks"></a>Remarques

Si la case à cocher **protéger la feuille de calcul et le contenu des cellules verrouillées** a été activée dans la boîte de dialogue **protéger la feuille** pour protéger le classeur contenant le nom, **xlfGetName** renvoie la `#N/A` valeur d'erreur. Pour afficher la boîte de dialogue **protéger la feuille** , cliquez sur **protéger la feuille** dans la section **modifications** de l'onglet **révision** . 
  
Le tableau suivant répertorie trois exemples de valeurs renvoyées par un appel à **xlfGetDef** avec l'argument _pxNameText_ spécifié. 
  
|**Définition dans Excel**|**_pxNameText_**|**Valeur renvoyée**|
|:-----|:-----|:-----|
|Le nom ventes sur une feuille est défini comme le numéro 523.  <br/> |Ventes  <br/> |«= 523»  <br/> |
|La marge de la feuille active est définie en tant que formule = ventes-coûts.  <br/> |"! Bénéficier  <br/> |«= Ventes-coûts»  <br/> |
|La base de données de noms de la feuille active est définie en tant que plage a1: F500.  <br/> |"! Database  <br/> |"= L1C1: R500C6"  <br/> |
   
## <a name="see-also"></a>Voir aussi

- [xlfGetDef](xlfgetdef.md)
- [Fonctions XLM essentielles et utiles de l’API C](essential-and-useful-c-api-xlm-functions.md)

