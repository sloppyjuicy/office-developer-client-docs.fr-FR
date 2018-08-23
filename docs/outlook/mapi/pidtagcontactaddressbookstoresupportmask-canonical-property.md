---
title: Propriété canonique PidTagContactAddressBookStoreSupportMask
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagContactAddressBookStoreSupportMask
api_type:
- HeaderDef
ms.assetid: 34f649c8-29bf-470f-9b05-31b69d069259
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 7219a8936381c498e7b27898f5efae8e40697b59
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565612"
---
# <a name="pidtagcontactaddressbookstoresupportmask-canonical-property"></a>Propriété canonique PidTagContactAddressBookStoreSupportMask

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Contient la propriété **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagcontactaddressbookstoresupportmask-canonical-property.md)) obtenue à partir de la banque stockant le dossier Contacts.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_CONTAB_STORE_SUPPORT_MASK  <br/> |
|Identificateur :  <br/> |0x6611  <br/> |
|Type de données :  <br/> |PT_LONG  <br/> |
|Domaine :  <br/> |Carnet d’adresses de contacts  <br/> |
   
## <a name="remarks"></a>Remarques

Le fournisseur de carnet d’adresses de contacts utilise cette propriété pour évaluer l’adéquation des fonctionnalités prises en charge de la banque. Il s’agit d’une propriété sur un conteneur de carnet d’adresses de contacts et une colonne dans la table des conteneurs du carnet d’adresses de contacts.
  
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

