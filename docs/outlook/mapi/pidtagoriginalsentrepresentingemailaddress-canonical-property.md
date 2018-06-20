---
title: Propriété canonique PidTagOriginalSentRepresentingEmailAddress
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_type:
- COM
ms.assetid: e2c3d2c3-5451-45cb-b0ec-bdbf5b39a0ba
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: bfb771c4c5972a770910936b6220c9e11b24e355
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19786326"
---
# <a name="pidtagoriginalsentrepresentingemailaddress-canonical-property"></a>Propriété canonique PidTagOriginalSentRepresentingEmailAddress

  
  
**S’applique à**: Outlook 
  
Contient l’adresse de messagerie de l’utilisateur de messagerie pour le compte duquel le message d’origine a été envoyé.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_ORIGINAL_SENT_REPRESENTING_EMAIL_ADDRESS, PR_ORIGINAL_SENT_REPRESENTING_EMAIL_ADDRESS_A, PR_ORIGINAL_SENT_REPRESENTING_EMAIL_ADDRESS_W  <br/> |
|Identificateur :  <br/> |0x0069  <br/> |
|Type de données :  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Zone :  <br/> |Général de messagerie  <br/> |
   
## <a name="remarks"></a>Remarques

Ces propriétés sont des exemples de propriétés d’adresse de l’expéditeur d’origine représenté d’un message. Il est utilisé dans un thread de conversation.
  
Une application cliente envoie un message de la part d’un autre client doit définir ces propriétés à la valeur de la propriété **PR_SENT_REPRESENTING_EMAIL_ADDRESS** ([PidTagSentRepresentingEmailAddress](pidtagsentrepresentingemailaddress-canonical-property.md)) à la première soumission du message. Une fois définies, il doit jamais être modifié.
  
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

