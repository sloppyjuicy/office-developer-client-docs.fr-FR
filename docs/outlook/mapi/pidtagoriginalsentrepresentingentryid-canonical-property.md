---
title: Propriété canonique PidTagOriginalSentRepresentingEntryId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginalSentRepresentingEntryId
api_type:
- COM
ms.assetid: ece3df57-47f3-4d27-854f-b511c920ac75
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 92300733d32f021bb0ab8ab29a9676b740eeda12
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19786349"
---
# <a name="pidtagoriginalsentrepresentingentryid-canonical-property"></a>Propriété canonique PidTagOriginalSentRepresentingEntryId

  
  
**S’applique à**: Outlook 
  
Contient l’identificateur d’entrée de l’utilisateur de messagerie pour le compte duquel le message d’origine a été envoyé.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_ORIGINAL_SENT_REPRESENTING_ENTRYID  <br/> |
|Identificateur :  <br/> |0x005E  <br/> |
|Type de données :  <br/> |PT_BINARY  <br/> |
|Zone :  <br/> |Général de messagerie  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété est une des propriétés d’adresse de l’expéditeur d’origine représenté d’un message. Il est utilisé dans un thread de conversation.
  
Une application cliente envoie un message de la part d’un autre client doit définir cette propriété à la valeur de la propriété **PR_SENT_REPRESENTING_ENTRYID** ([PidTagSentRepresentingEntryId](pidtagsentrepresentingentryid-canonical-property.md)) à la première soumission du message. Une fois définies, il doit jamais être modifié.
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications du protocole

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications du protocole Exchange Server associées.
    
[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Spécifie les propriétés et les opérations qui sont autorisées sur les objets de message électronique.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
MAPITAGS.h
  
> Contient les définitions des propriétés répertoriées en tant que d’autres noms.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage de noms de propriété canonique aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage de noms MAPI pour les noms de propriété canonique](mapping-mapi-names-to-canonical-property-names.md)

