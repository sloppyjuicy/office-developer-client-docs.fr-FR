---
title: Propriété canonique PidTagValidFolderMask
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.PidTagValidFolderMask
api_type:
- COM
ms.assetid: 83a44aee-5269-42a8-8078-4bc063bb6e29
description: Contient un masque de bits d’indicateurs qui indique la validité des identificateurs d’entrée des dossiers d’une magasin de messages.
ms.openlocfilehash: 0a9368eb1d1c5fd32fddb5a59b88e1db732b7bb9
ms.sourcegitcommit: 331e2bc18fb14cc9868d28ca29cb5eda85c8f154
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/25/2022
ms.locfileid: "64455978"
---
# <a name="pidtagvalidfoldermask-canonical-property"></a>Propriété canonique PidTagValidFolderMask

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient un masque de bits d’indicateurs qui indique la validité des identificateurs d’entrée des dossiers d’une magasin de messages.
  
|Propriété |Valeur |
|:-----|:-----|
|Propriétés associées :  <br/> |PR_VALID_FOLDER_MASK  <br/> |
|Identificateur :  <br/> |0x35DF  <br/> |
|Type de données :  <br/> |PT_LONG  <br/> |
|Domaine :  <br/> |Magasin de messages MAPI  <br/> |
   
## <a name="remarks"></a>Remarques

L’identificateur d’entrée d’un dossier peut devenir non valide si un utilisateur supprime le dossier ou si la magasin de messages est endommagée.
  
Un ou plusieurs des indicateurs suivants peuvent être définies pour le masque de bits : 
  
FOLDER_COMMON_VIEWS_VALID 
  
> Le dossier Affichages communs possède un identificateur d’entrée valide. Voir **PR_COMMON_VIEWS_ENTRYID** ([PidTagCommonViewsEntryId](pidtagcommonviewsentryid-canonical-property.md)).
    
FOLDER_FINDER_VALID 
  
> Le dossier de recherche possède un identificateur d’entrée valide. Voir **PR_FINDER_ENTRYID** ([PidTagFinderEntryId](pidtagfinderentryid-canonical-property.md)). 
    
FOLDER_IPM_INBOX_VALID 
  
> Le dossier de réception du message interpersonnel (IPM) possède un identificateur d’entrée valide. Voir [IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md). 
    
FOLDER_IPM_OUTBOX_VALID 
  
> Le dossier de la boîte d’envoi IPM possède un identificateur d’entrée valide. Voir **PR_IPM_OUTBOX_ENTRYID** ([PidTagIpmOutboxEntryId](pidtagipmoutboxentryid-canonical-property.md)). 
    
FOLDER_IPM_SENTMAIL_VALID 
  
> Le dossier Éléments envoyés IPM possède un identificateur d’entrée valide. Voir **PR_IPM_SENTMAIL_ENTRYID** ([PidTagIpmSentMailEntryId](pidtagipmsentmailentryid-canonical-property.md)).
    
FOLDER_IPM_SUBTREE_VALID 
  
> La sous-arbre du dossier IPM possède un identificateur d’entrée valide. Voir **PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md)).
    
FOLDER_IPM_WASTEBASKET_VALID 
  
> Le dossier Éléments supprimés IPM possède un identificateur d’entrée valide. Voir **PR_IPM_WASTEBASKET_ENTRYID** ([PidTagIpmWastebasketEntryId](pidtagipmwastebasketentryid-canonical-property.md)).
    
FOLDER_VIEWS_VALID 
  
> Le dossier Vues possède un identificateur d’entrée valide. Voir **PR_VIEWS_ENTRYID** ([PidTagViewsEntryId](pidtagviewsentryid-canonical-property.md)).
    
## <a name="related-resources"></a>Ressources connexes

### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
Mapitags.h
  
> Contient les définitions des propriétés répertoriées en tant que noms de remplacement.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

