---
title: Propriété canonique PidTagTransportMessageHeaders
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagTransportMessageHeaders
api_type:
- COM
ms.assetid: 9f8e3f20-6454-4dfd-9b35-e0401abac6b3
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 7ad9048a19123b94c10afaddcbedb7f54e8fe477
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360759"
---
# <a name="pidtagtransportmessageheaders-canonical-property"></a>Propriété canonique PidTagTransportMessageHeaders

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient des informations d'enveloppe de message propres au transport.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_TRANSPORT_MESSAGE_HEADERS, PR_TRANSPORT_MESSAGE_HEADERS_A, PR_TRANSPORT_MESSAGE_HEADERS_W  <br/> |
|Identificateur :  <br/> |0x007D  <br/> |
|Type de données :  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Domaine :  <br/> |E-mail  <br/> |
   
## <a name="remarks"></a>Remarques

Le fournisseur de transport peut générer les informations d'en-tête de message pour les messages entrants.
  
Ces propriétés offrent une alternative à la possibilité d'ignorer les informations d'en-tête de message de transport ou de l'en faire glisser vers le texte du message. Le client peut choisir d'afficher ou non les informations.
  
## <a name="related-resources"></a>Ressources associées

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références à des spécifications de protocole Exchange Server connexes.
    
[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Spécifie les propriétés et les opérations qui sont autorisées pour les objets message électronique.
    
[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)
  
> ConVertit des conventions de messagerie standard Internet en objets message.
    
### <a name="header-files"></a>Fichiers d'en-tête

Mapidefs. h
  
> Fournit des définitions de type de données.
    
Mapitags. h
  
> Contient les définitions des propriétés figurant en tant que noms de substitution.
    
## <a name="see-also"></a>Voir aussi



[Propriété canonique PidTagBody](pidtagbody-canonical-property.md)


[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

