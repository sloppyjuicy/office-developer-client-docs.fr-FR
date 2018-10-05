---
title: Propriété canonique PidTagMessageCcMe
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMessageCcMe
api_type:
- HeaderDef
ms.assetid: 7310a0f2-a109-40a4-99bf-e963d754a067
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 7605739dd6d0f0205a1a4f09eb8c45d235c0c179
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25389770"
---
# <a name="pidtagmessageccme-canonical-property"></a>Propriété canonique PidTagMessageCcMe

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient la valeur TRUE si cet utilisateur de messagerie est nommé spécifiquement comme destinataire du message en copie carbone (CC) et ne fait pas partie d’une liste de distribution. 
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_MESSAGE_CC_ME  <br/> |
|Identificateur :  <br/> |0x0058  <br/> |
|Type de données :  <br/> |PT_BOOLEAN  <br/> |
|Domaine :  <br/> |Général de messagerie  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété fournit un moyen pratique pour déterminer si le nom d’utilisateur apparaît explicitement dans la liste des destinataires en copie carbone, sans examiner toutes les entrées de la liste. 
  
Cette propriété permet également de traitement automatisé des messages reçus au moment de la réception. Option du fournisseur de transport, cette propriété contient FALSE ou n’est pas définie si l’utilisateur de messagerie ne figure pas directement dans la table de destinataires. 
  
Remise de messages résultant de l’extension des listes de distribution ou la désignation d’une copie carbone invisible n’entraîne pas cette propriété à définir. Le destinataire doit se nommer explicitement. 
  
Généralement, les messages non envoyés ne définissent pas cette propriété, **PR_MESSAGE_RECIP_ME** ([PidTagMessageRecipientMe](pidtagmessagerecipientme-canonical-property.md)) ou **PR_MESSAGE_TO_ME** ([PidTagMessageToMe](pidtagmessagetome-canonical-property.md)). Si elles sont présentes dans les messages de l’utilisateur peut accéder dans des magasins de messages publique, privé des autres utilisateurs magasins, dans les fichiers sur le disque, ou incorporé à l’intérieur d’autres messages reçus, ils contiennent généralement les valeurs à laquelle ils ont été définies lors de la dernière un fournisseur de transport remis le message. 
  
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

