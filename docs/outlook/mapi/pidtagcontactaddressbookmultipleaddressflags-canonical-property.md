---
title: Propriété canonique PidTagContactAddressBookMultipleAddressFlags
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagContactAddressBookMultipleAddressFlags
api_type:
- HeaderDef
ms.assetid: ed3bc585-13f6-46a5-9e71-9c8513ddfc0a
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: b783a624ef5358a69d65dd52785b285db1a70df7
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588670"
---
# <a name="pidtagcontactaddressbookmultipleaddressflags-canonical-property"></a>Propriété canonique PidTagContactAddressBookMultipleAddressFlags

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Contient des indicateurs qui indique si les fournisseurs prendra en charge plusieurs e-mail addresses par élément de contact.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_CONTAB_MULTI_ADDR_FLAGS  <br/> |
|Identificateur :  <br/> |0x6625  <br/> |
|Type de données :  <br/> |PT_MV_LONG  <br/> |
|Domaine :  <br/> |Carnet d’adresses de contacts  <br/> |
   
## <a name="remarks"></a>Remarques

Si les indicateurs de cette propriété soient TRUE, le fournisseur n’inclut pas les contacts sans les adresses de messagerie. Uniquement l’adresse de messagerie principale sera respectée. Il s’agit d’une propriété sur une section de profil du carnet d’adresses de contacts.
  
## <a name="related-resources"></a>Ressources connexes

### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
MAPITAGS.h
  
> Contient les définitions des propriétés répertoriées en tant que propriétés associées.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

