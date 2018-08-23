---
title: Propriété canonique PidTagValidFolderMask
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagValidFolderMask
api_type:
- COM
ms.assetid: 83a44aee-5269-42a8-8078-4bc063bb6e29
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 605e2f528ea0afc1a35348320abaffeb142d9921
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22590721"
---
# <a name="pidtagvalidfoldermask-canonical-property"></a>Propriété canonique PidTagValidFolderMask

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Contient un masque binaire composé des indicateurs qui influencent la validité des identificateurs d’entrée des dossiers dans une banque de messages.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_VALID_FOLDER_MASK  <br/> |
|Identificateur :  <br/> |0x35DF  <br/> |
|Type de données :  <br/> |PT_LONG  <br/> |
|Domaine :  <br/> |Banque de messages MAPI  <br/> |
   
## <a name="remarks"></a>Remarques

Identificateur d’entrée d’un dossier peut devenir non valide si un utilisateur supprime le dossier ou si la banque de messages est corrompue.
  
Un ou plusieurs des indicateurs suivants peuvent être définies pour le masque de bits : 
  
FOLDER_COMMON_VIEWS_VALID 
  
> Le dossier views courantes possède un identificateur d’entrée valide. Voir **PR_COMMON_VIEWS_ENTRYID** ([PidTagCommonViewsEntryId](pidtagcommonviewsentryid-canonical-property.md)).
    
FOLDER_FINDER_VALID 
  
> Le dossier de recherche a un identificateur d’entrée valide. Voir **PR_FINDER_ENTRYID** ([PidTagFinderEntryId](pidtagfinderentryid-canonical-property.md)). 
    
FOLDER_IPM_INBOX_VALID 
  
> Recevoir le message interpersonnel (IPM) dossier possède un identificateur d’entrée valide. Voir [IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md). 
    
FOLDER_IPM_OUTBOX_VALID 
  
> Le dossier boîte d’envoi de l’IPM possède un identificateur d’entrée valide. Voir **PR_IPM_OUTBOX_ENTRYID** ([PidTagIpmOutboxEntryId](pidtagipmoutboxentryid-canonical-property.md)). 
    
FOLDER_IPM_SENTMAIL_VALID 
  
> Le dossier éléments envoyés de IPM possède un identificateur d’entrée valide. Voir **PR_IPM_SENTMAIL_ENTRYID** ([PidTagIpmSentMailEntryId](pidtagipmsentmailentryid-canonical-property.md)).
    
FOLDER_IPM_SUBTREE_VALID 
  
> La sous-arborescence de dossier IPM possède un identificateur d’entrée valide. Voir **PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md)).
    
FOLDER_IPM_WASTEBASKET_VALID 
  
> Le dossier éléments supprimés de IPM possède un identificateur d’entrée valide. Voir **PR_IPM_WASTEBASKET_ENTRYID** ([PidTagIpmWastebasketEntryId](pidtagipmwastebasketentryid-canonical-property.md)).
    
FOLDER_VIEWS_VALID 
  
> Le dossier views possède un identificateur d’entrée valide. Voir **PR_VIEWS_ENTRYID** ([PidTagViewsEntryId](pidtagviewsentryid-canonical-property.md)).
    
## <a name="related-resources"></a>Ressources connexes

### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
MAPITAGS.h
  
> Contient les définitions des propriétés répertoriées en tant que d’autres noms.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

