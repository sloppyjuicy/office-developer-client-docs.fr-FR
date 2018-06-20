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
ms.openlocfilehash: e184fd0933295984af97258d785df92306160a6d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19786924"
---
# <a name="pidtagtransportmessageheaders-canonical-property"></a>Propriété canonique PidTagTransportMessageHeaders

  
  
**S’applique à**: Outlook 
  
Contient des informations d’enveloppe de message de transport spécifique.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_TRANSPORT_MESSAGE_HEADERS, PR_TRANSPORT_MESSAGE_HEADERS_A, PR_TRANSPORT_MESSAGE_HEADERS_W  <br/> |
|Identificateur :  <br/> |0x007D  <br/> |
|Type de données :  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Zone :  <br/> |Courier électronique  <br/> |
   
## <a name="remarks"></a>Remarques

Le fournisseur de transport peut générer les informations d’en-tête de message pour les messages entrants.
  
Ces propriétés offrent une alternative doivent précéder au texte du message ou en supprimant les informations d’en-tête de message transport. Le client peut choisir s’il faut afficher les informations.
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications du protocole

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications du protocole Exchange Server associées.
    
[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Spécifie les propriétés et les opérations qui sont autorisées sur les objets de message électronique.
    
[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)
  
> Convertit des conventions de messagerie standard Internet aux objets de message.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
MAPITAGS.h
  
> Contient les définitions des propriétés répertoriées en tant que d’autres noms.
    
## <a name="see-also"></a>Voir aussi



[Propriété canonique PidTagBody](pidtagbody-canonical-property.md)


[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage de noms de propriété canonique aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage de noms MAPI pour les noms de propriété canonique](mapping-mapi-names-to-canonical-property-names.md)

