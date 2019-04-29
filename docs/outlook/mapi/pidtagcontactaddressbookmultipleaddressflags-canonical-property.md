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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: ecd795490d953f1aa237dfbd77585ba79c8b3234
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429249"
---
# <a name="pidtagcontactaddressbookmultipleaddressflags-canonical-property"></a>Propriété canonique PidTagContactAddressBookMultipleAddressFlags

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient des indicateurs qui indiquent si les fournisseurs prendront en charge plusieurs adresses de messagerie par élément de contact.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_CONTAB_MULTI_ADDR_FLAGS  <br/> |
|Identificateur :  <br/> |0x6625  <br/> |
|Type de données :  <br/> |PT_MV_LONG  <br/> |
|Domaine :  <br/> |Carnet d'adresses des contacts  <br/> |
   
## <a name="remarks"></a>Remarques

Si les indicateurs de cette propriété ont la valeur TRUE, le fournisseur n'inclut pas de contacts sans adresse de messagerie. Seule l'adresse de messagerie principale sera honorée. Il s'agit d'une propriété dans la section profil de carnet d'adresses de contacts.
  
## <a name="related-resources"></a>Ressources connexes

### <a name="header-files"></a>Fichiers d'en-tête

Mapidefs. h
  
> Fournit des définitions de type de données.
    
Mapitags. h
  
> Contient les définitions des propriétés indiquées en tant que propriétés associées.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

