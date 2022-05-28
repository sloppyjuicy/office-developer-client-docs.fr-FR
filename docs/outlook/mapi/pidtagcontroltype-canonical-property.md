---
title: Propriété canonique PidTagControlType
description: Décrit la propriété canonique PidTagControlType, qui contient une valeur indiquant un type de contrôle pour un contrôle utilisé dans une boîte de dialogue.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagControlType
api_type:
- HeaderDef
ms.assetid: 7728fa2f-4a59-4e86-90f1-4384824598aa
ms.openlocfilehash: 335c70e389801bc98ef1cfb7d4b8f2ef87f52184
ms.sourcegitcommit: 8c8e4ac05a6612dd5c815ab18ba40e56a6ba839d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/28/2022
ms.locfileid: "65769430"
---
# <a name="pidtagcontroltype-canonical-property"></a>Propriété canonique PidTagControlType

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient une valeur indiquant un type de contrôle pour un contrôle utilisé dans une boîte de dialogue. 
  
|Propriété |Valeur |
|:-----|:-----|
|Propriétés associées :  <br/> |PR_CONTROL_TYPE  <br/> |
|Identificateur :  <br/> |0x3F02  <br/> |
|Type de données :  <br/> |PT_LONG  <br/> |
|Domaine :  <br/> |Table d’affichage MAPI  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété peut avoir exactement l’une des valeurs suivantes :
    
DTCT_LABEL (0x00000000)
  
> Étiquette de boîte de dialogue.
   
DTCT_EDIT (0x00000001)
  
> Boîte de dialogue modifier le texte.

DTCT_LBX (0x00000002)
  
> Boîte de dialogue de liste.
    
DTCT_COMBOBOX (0x00000003)
  
> Boîte de dialogue déroulante.

DTCT_DDLBX (0x00000004)
  
> Boîte de dialogue de liste déroulante.

DTCT_CHECKBOX (0x00000005)
  
> Case à cocher de boîte de dialogue.

DTCT_GROUPBOX (0x00000006)
  
> Boîte de dialogue de groupe.
  
DTCT_BUTTON (0x00000007)
  
> Contrôle de bouton de boîte de dialogue.
    
DTCT_PAGE (0x00000008)
  
> Page à onglets de boîte de dialogue.
    
DTCT_RADIOBUTTON (0x00000009)
  
> Une case d’option de boîte de dialogue.
    
DTCT_MVLISTBOX (0x0000000B)
  
> Zone de liste à valeurs multiples remplie par une propriété à valeurs multiples de type chaîne.
    
DTCT_MVDDLBX (0x0000000C)
  
> Zone de liste déroulante à valeurs multiples remplie par une propriété à valeurs multiples de chaîne de type.
    
## <a name="related-resources"></a>Ressources connexes

### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
mapitags.h
  
> Contient des définitions de propriétés répertoriées en tant que noms secondaires.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage de noms MAPI à des noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

