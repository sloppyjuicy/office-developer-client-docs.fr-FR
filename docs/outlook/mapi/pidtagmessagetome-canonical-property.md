---
title: Propriété canonique PidTagMessageToMe
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMessageToMe
api_type:
- HeaderDef
ms.assetid: aeb0fa71-f471-46c5-ad9c-f8afb3fed533
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 42aec7a8d617bdf1abd385add30d903efa2b73d2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19786244"
---
# <a name="pidtagmessagetome-canonical-property"></a>Propriété canonique PidTagMessageToMe

  
  
**S’applique à**: Outlook 
  
Contient la valeur TRUE si cet utilisateur de messagerie est nommé spécifiquement comme (destinataire du message à) principale et ne fait pas partie d’une liste de distribution. 
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_MESSAGE_TO_ME  <br/> |
|Identificateur :  <br/> |0x0057  <br/> |
|Type de données :  <br/> |PT_BOOLEAN  <br/> |
|Zone :  <br/> |Général de messagerie  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété fournit un moyen pratique pour déterminer si le nom d’utilisateur apparaît explicitement dans la liste des destinataires principale sans examiner toutes les entrées de la liste. 
  
Cette propriété permet également de traitement automatisé des messages reçus au moment de la réception. Option du fournisseur de transport, cette propriété contient FALSE ou n’est pas incluse si l’utilisateur de messagerie ne figure pas directement dans la table de destinataires. 
  
Remise de messages résultant de l’extension des listes de distribution ou la désignation d’une copie carbone invisible n’entraîne pas cette propriété à définir. Le destinataire doit se nommer explicitement. 
  
Les messages ne définissent généralement pas cette propriété, **PR_MESSAGE_RECIP_ME** ([PidTagMessageRecipientMe](pidtagmessagerecipientme-canonical-property.md)) ou le **PR_MESSAGE_CC_ME** ([PidTagMessageCcMe](pidtagmessageccme-canonical-property.md)). Si elles sont présentes dans les messages de l’utilisateur peut accéder dans des magasins de messages publique, privé des autres utilisateurs magasins, dans les fichiers sur le disque, ou incorporé à l’intérieur d’autres messages reçus, ils contiennent généralement les valeurs à laquelle ils ont été définies lors de la dernière un fournisseur de transport remis le message. 
  
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

