---
title: Propriété canonique PidTagContactAddressBookMultipleAddressFlags
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagContactAddressBookMultipleAddressFlags
api_type:
- HeaderDef
ms.assetid: ed3bc585-13f6-46a5-9e71-9c8513ddfc0a
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 72cf1ee919ce9bc49792712f9e0b441d23f1ae01
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59566842"
---
# <a name="pidtagcontactaddressbookmultipleaddressflags-canonical-property"></a>Propriété canonique PidTagContactAddressBookMultipleAddressFlags

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient des indicateurs qui indiquent si les fournisseurs vont prendre en charge plusieurs adresses de messagerie par élément de contact.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_CONTAB_MULTI_ADDR_FLAGS  <br/> |
|Identificateur :  <br/> |0x6625  <br/> |
|Type de données :  <br/> |PT_MV_LONG  <br/> |
|Domaine :  <br/> |Carnet d’adresses de contact  <br/> |
   
## <a name="remarks"></a>Remarques

Si les indicateurs de cette propriété sont TRUE, le fournisseur n’inclut pas les contacts sans adresse de messagerie. Seule l’adresse de messagerie principale sera honorée. Il s’agit d’une propriété d’une section de profil de carnet d’adresses de contact.
  
## <a name="related-resources"></a>Ressources connexes

### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
Mapitags.h
  
> Contient les définitions des propriétés répertoriées en tant que propriétés associées.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

