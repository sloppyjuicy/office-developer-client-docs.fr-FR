---
title: Propriété canonique PidTagStoreRecordKey
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagStoreRecordKey
api_type:
- COM
ms.assetid: 27347302-bd52-4f62-98f1-6c37f9a66463
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: d6f858a9f1d3d4620a86621e3f5ecb4ad4609691
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25401082"
---
# <a name="pidtagstorerecordkey-canonical-property"></a>Propriété canonique PidTagStoreRecordKey

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient l’identificateur unique comparable binaire (clé d’enregistrement) de la banque de messages dans lequel réside un objet.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_STORE_RECORD_KEY  <br/> |
|Identificateur :  <br/> |0x0FFA  <br/> |
|Type de données :  <br/> |PT_BINARY  <br/> |
|Domaine :  <br/> |Propriétés ID  <br/> |
   
## <a name="remarks"></a>Remarques

Pour une banque de messages, cette propriété est identique à la propriété **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)) de la banque.
  
La relation entre cette propriété et la **PR_RECORD_KEY** est la même que la relation entre **PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md)) et **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)).
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications du protocole

[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Gère les objets de message et la pièce jointe.
    
[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)
  
> La conversion entre IETF RFC2445, RFC2446, RFC2447 et rendez-vous et des objets de la conférence.
    
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

