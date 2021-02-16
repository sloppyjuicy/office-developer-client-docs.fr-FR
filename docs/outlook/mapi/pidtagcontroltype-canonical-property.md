---
title: Propriété canonique PidTagControlType
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagControlType
api_type:
- HeaderDef
ms.assetid: 7728fa2f-4a59-4e86-90f1-4384824598aa
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 7bdb02f72ba14a36c8a4c218cd5f0631e7145e6a
ms.sourcegitcommit: 0419850d5c1b3439d9da59070201fb4952ca5d07
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/28/2020
ms.locfileid: "49734202"
---
# <a name="pidtagcontroltype-canonical-property"></a>Propriété canonique PidTagControlType

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient une valeur indiquant un type de contrôle pour un contrôle utilisé dans une boîte de dialogue. 
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_CONTROL_TYPE  <br/> |
|Identificateur :  <br/> |0x3F02  <br/> |
|Type de données :  <br/> |PT_LONG  <br/> |
|Domaine :  <br/> |Tableau d’affichage MAPI  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété peut avoir exactement l’une des valeurs suivantes :
    
DTCT_LABEL (0x00000000)
  
> Étiquette de boîte de dialogue.
   
DTCT_EDIT (0x00000001)
  
> Boîte de dialogue de modification de texte.

DTCT_LBX (0x00000002)
  
> Boîte de dialogue.
    
DTCT_COMBOBOX (0x00000003)
  
> Zone de liste déroulante de boîte de dialogue.

DTCT_DDLBX (0x00000004)
  
> Boîte de dialogue de liste.

DTCT_CHECKBOX (0x00000005)
  
> Une case à cocher de boîte de dialogue.

DTCT_GROUPBOX (0x00000006)
  
> Boîte de dialogue de groupe.
  
DTCT_BUTTON (0x00000007)
  
> Contrôle de bouton de boîte de dialogue.
    
DTCT_PAGE (0x00000008)
  
> Page à onglets de boîte de dialogue.
    
DTCT_RADIOBUTTON (0x00000009)
  
> Une boîte de dialogue.
    
DTCT_MVLISTBOX (0x0000000B)
  
> Zone de liste à valeurs multiples remplie par une propriété à valeurs multiples de type chaîne.
    
DTCT_MVDDLBX (0x0000000C)
  
> Zone de listes listes à valeurs multiples remplie par une propriété à valeurs multiples de type chaîne.
    
## <a name="related-resources"></a>Ressources connexes

### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
mapitags.h
  
> Contient les définitions des propriétés répertoriées en tant que noms de remplacement.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

