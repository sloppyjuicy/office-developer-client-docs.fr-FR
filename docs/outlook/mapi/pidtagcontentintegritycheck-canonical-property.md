---
title: Propriété canonique PidTagContentIntegrityCheck
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagContentIntegrityCheck
api_type:
- HeaderDef
ms.assetid: c7f10b8a-6b20-44cf-bde6-8d2b711c1c14
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 2082db4ccd107fcd02e37882707e4e3ee697695d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19785858"
---
# <a name="pidtagcontentintegritycheck-canonical-property"></a>Propriété canonique PidTagContentIntegrityCheck

  
  
**S’applique à**: Outlook 
  
Contient une valeur de vérification de l’intégrité du contenu ASN.1 qui permet à un expéditeur du message protéger le contenu des messages de divulgation à des destinataires non autorisés.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_CONTENT_INTEGRITY_CHECK  <br/> |
|Identificateur :  <br/> |0x0c00  <br/> |
|Type de données :  <br/> |PT_BINARY  <br/> |
|Zone :  <br/> |Exchange  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété fournit pour la non-répudiation du contenu du message. Conjointement avec **PR_MESSAGE_TOKEN** ([PidTagMessageToken](pidtagmessagetoken-canonical-property.md)), elle garantit que le contenu d’un message arrive à sa destination inchangée.
  
## <a name="related-resources"></a>Ressources connexes

### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
MAPITAGS.h
  
> Contient les définitions des propriétés répertoriées en tant que propriétés associées.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage de noms de propriété canonique aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage de noms MAPI pour les noms de propriété canonique](mapping-mapi-names-to-canonical-property-names.md)

