---
title: Propriété canonique PidTagStoreEntryId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagStoreEntryId
api_type:
- COM
ms.assetid: 0d705667-19f4-4eda-a068-e65ea8f00d9b
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: ffe4798c5e8ef200619b060a58e868cc4a1b2bc2
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22590070"
---
# <a name="pidtagstoreentryid-canonical-property"></a>Propriété canonique PidTagStoreEntryId

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Contient l’identificateur d’entrée unique de la banque de messages où un objet réside.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_STORE_ENTRYID  <br/> |
|Identificateur :  <br/> |0x0FFB  <br/> |
|Type de données :  <br/> |PT_BINARY  <br/> |
|Domaine :  <br/> |Propriétés ID  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété est utilisée pour ouvrir une banque de messages avec la méthode [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md) . Il est également utilisé pour ouvrir un objet appartenant à la banque de messages. 
  
Pour une banque de messages, cette propriété est identique à la propriété **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) de la banque. Une application cliente permet de comparer les deux propriétés à l’aide de la méthode [IMAPISession::CompareEntryIDs](imapisession-compareentryids.md) . 
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications du protocole

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications du protocole Exchange Server associées.
    
[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Gère les objets de message et la pièce jointe.
    
[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)
  
> La conversion entre IETF RFC2445, RFC2446, RFC2447 et rendez-vous et des objets de la conférence.
    
[[MS-OXOFLAG]](http://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)
  
> Spécifie les propriétés et les opérations liées aux marquage.
    
[[MS-OXSHARE]](http://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)
  
> Partage des dossiers de boîte aux lettres entre des clients.
    
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

