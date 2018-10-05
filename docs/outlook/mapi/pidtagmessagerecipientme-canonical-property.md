---
title: Propriété canonique PidTagMessageRecipientMe
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMessageRecipientMe
api_type:
- HeaderDef
ms.assetid: 90333258-8913-4f98-aefb-4cc2ab34abcf
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 78423e874becdfc232b0dd964b32ae0c4530d19e
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25382462"
---
# <a name="pidtagmessagerecipientme-canonical-property"></a>Propriété canonique PidTagMessageRecipientMe

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient la valeur TRUE si cet utilisateur de messagerie est nommé spécifiquement comme principale (To), copie carbone (CC) ou au destinataire de copie carbone invisible (Cci) du message et ne fait pas partie d’une liste de distribution. 
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_MESSAGE_RECIP_ME  <br/> |
|Identificateur :  <br/> |0x0059  <br/> |
|Type de données :  <br/> |PT_BOOLEAN  <br/> |
|Domaine :  <br/> |Général de messagerie  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété fournit un moyen pratique pour déterminer si le nom d’utilisateur apparaît explicitement dans la liste des destinataires, sans examiner toutes les entrées de la liste. La valeur représente l’opération **OR** logique des propriétés **PR_MESSAGE_CC_ME** ([PidTagMessageCcMe](pidtagmessageccme-canonical-property.md)) et **PR_MESSAGE_TO_ME** ([PidTagMessageToMe](pidtagmessagetome-canonical-property.md)) et les informations Cci (qui n’apparaît pas dans le cas contraire dans un propriété). 
  
Cette propriété permet de traitement automatisé des messages reçus au moment de la réception. Option du fournisseur de transport, cette propriété contient FALSE ou n’est pas incluse si l’utilisateur de messagerie ne figure pas directement dans la table de destinataires. 
  
Remise de messages qui résulte de l’extension des listes de distribution n’entraîne pas cette propriété à définir. Le destinataire doit se nommer explicitement. 
  
Les messages ne définissent généralement pas cette propriété, **PR_MESSAGE_CC_ME**ou **PR_MESSAGE_TO_ME**. Si elles sont présentes dans les messages de l’utilisateur peut accéder dans des magasins de messages publique, privé des autres utilisateurs magasins, dans les fichiers sur le disque, ou incorporé à l’intérieur d’autres messages reçus, ils contiennent généralement les valeurs à laquelle ils ont été définies lors de la dernière un fournisseur de transport remis le message. 
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications du protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications du protocole Exchange Server associées.
    
[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Spécifie les propriétés et les opérations qui sont autorisées sur les objets de message électronique.
    
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

