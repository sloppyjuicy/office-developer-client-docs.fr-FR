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
description: 'S�applique �: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 63bfc6e94950a621c2367b2d35d25e3de48b344f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782217"
---
# <a name="xlfgetname"></a>xlfGetName

**S’applique à**: Excel 2013 | Office 2013 | Visual Studio 
  
Renvoie la définition d’un nom tel qu’il apparaît dans la colonne **fait référence à** de la boîte de dialogue **Gestionnaire de noms** qui s’affiche lorsque vous cliquez sur **Gestionnaire de noms** dans la section **Noms définis** sous l’onglet **formules** . Si la définition contient des références, ils sont indiqués sous forme de références de style R1C1. Utilisez **xlfGetName** pour vérifier la valeur définie par un nom. Pour obtenir le nom qui correspond à une définition, utilisez [xlfGetDef](xlfgetdef.md).
  
```cpp
Excel12(xlfGetName, LPXLOPER12 pxRes, 2, LPXLOPER12 pxNameText, LPXLOPER12 pxInfoType);
```

## <a name="parameters"></a>Paramètres

_pxNameText_ (**xltypeStr**)
  
Un nom peut être défini sur la feuille. une référence à un nom défini dans le classeur actif, par exemple, `"!Sales"`; ou une référence à un nom défini dans un classeur ouvert particulier, par exemple, `"[Book1]SHEET1!Sales"`.  _pxNameText_ peut également être un nom masqué. 
  
_pxInfoType_ (**xltypeBool**)
  
Spécifie le type d’informations à renvoyer sur le nom. Si **FALSE** ou omis, la définition est retournée. Si **la valeur TRUE**, renvoie **la valeur TRUE** si le nom est défini pour simplement la feuille, **FALSE** si le nom est défini pour l’intégralité du classeur. 
  
## <a name="property-valuereturn-value"></a>Propriété valeur/valeur de retour

_pxRes_ (**xltypeStr**, **xltypeBool**ou **xltypeErr**)
  
Selon la valeur passée pour _pxInfoType_, renvoie la définition du nom spécifié (**xltypeStr**), ou **la valeur TRUE** ou **FALSE** (**xltypeBool**).
  
## <a name="remarks"></a>Remarques

Si la case à cocher **protéger la feuille et le contenu des cellules verrouillées** a été sélectionnée dans la boîte de dialogue **Protéger la feuille** pour protéger le classeur contenant le nom, **xlfGetName** renvoie la `#N/A` valeur d’erreur. Pour afficher la boîte de dialogue **Protéger la feuille** , cliquez sur **Protéger la feuille** dans la section **modifications** de l’onglet **révision** . 
  
Le tableau suivant répertorie les trois exemples de valeurs retournées par un appel à **xlfGetDef** avec l’argument spécifié _pxNameText_ . 
  
|**Définition dans Excel**|**_pxNameText_**|**Valeur renvoyée**|
|:-----|:-----|:-----|
|Le nom de ventes sur une feuille est défini comme numéro 523.  <br/> |« Ventes »  <br/> |« = 523 »  <br/> |
|Le nom bénéficiaire de la feuille active est défini en tant que la formule = ventes-coûts.  <br/> |"! Profit »  <br/> |« = Ventes-coûts »  <br/> |
|Le nom de base de données de la feuille active est défini comme la plage A1:F500.  <br/> |"! Base de données »  <br/> |« = R1C1:R500C6 »  <br/> |
   
## <a name="see-also"></a>Voir aussi

- [xlfGetDef](xlfgetdef.md)
- [Fonctions XLM API C essentielles et utiles](essential-and-useful-c-api-xlm-functions.md)

