---
title: Propriété canonique PidTagContactAddressBookStoreSupportMask
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagContactAddressBookStoreSupportMask
api_type:
- HeaderDef
ms.assetid: 34f649c8-29bf-470f-9b05-31b69d069259
description: Contient la PR_STORE_SUPPORT_MASK de données obtenue à partir de la boutique contenant le dossier Contacts.
ms.openlocfilehash: fc198a99a296d504c55986eb5f7896ba3930c9b5
ms.sourcegitcommit: 0a067f44281eddabff15fff565fb80eaa543b660
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/23/2022
ms.locfileid: "63764642"
---
# <a name="pidtagcontactaddressbookstoresupportmask-canonical-property"></a>Propriété canonique PidTagContactAddressBookStoreSupportMask

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient la **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagcontactaddressbookstoresupportmask-canonical-property.md)) obtenue à partir de la boutique qui contient le dossier Contacts.
  
|Propriété |Valeur |
|:-----|:-----|
|Propriétés associées :  <br/> |PR_CONTAB_STORE_SUPPORT_MASK  <br/> |
|Identificateur :  <br/> |0x6611  <br/> |
|Type de données :  <br/> |PT_LONG  <br/> |
|Domaine :  <br/> |Carnet d’adresses de contact  <br/> |
   
## <a name="remarks"></a>Remarques

Le fournisseur de carnet d’adresses de contact utilise cette propriété pour évaluer l’adéquation des fonctionnalités du magasin pris en charge. Il s’agit d’une propriété d’un conteneur de carnet d’adresses de contact et d’une colonne dans la table des conteneurs de carnet d’adresses de contact.
  
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

