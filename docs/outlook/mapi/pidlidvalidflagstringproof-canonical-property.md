---
title: Propriété canonique PidLidValidFlagStringProof
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidValidFlagStringProof
api_type:
- COM
ms.assetid: e5a94968-7e84-4faf-8104-9ea36d35fa1a
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: dfe3b57c246e247eda365bed46af2e0f35f0e54b
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25391954"
---
# <a name="pidlidvalidflagstringproof-canonical-property"></a>Propriété canonique PidLidValidFlagStringProof

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Vérifie si la valeur de la propriété **dispidRequest** ([PidLidFlagRequest](pidlidflagrequest-canonical-property.md)) a été définie par un agent qui avait la valeur de la propriété **PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md)).
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |dispidValidFlagStringProof  <br/> |
|Jeu de propriétés :  <br/> |PSETID_Common  <br/> |
|ID de type long (capot) :  <br/> |0x000085BF  <br/> |
|Type de données :  <br/> |PT_SYSTIME  <br/> |
|Domaine :  <br/> |Task  <br/> |
   
## <a name="remarks"></a>Remarques

Sur les objets non expédiable (trafic entrant et objets extérieurs à la messagerie), les clients doivent définir cette valeur à la valeur de **PR_MESSAGE_DELIVERY_TIME** lors de la modification **dispidRequest**.
  
Dans la mesure où la valeur de **PR_MESSAGE_DELIVERY_TIME** ne peut pas être prévue par l’expéditeur, si la valeur de cette propriété est égale à la valeur de **PR_MESSAGE_DELIVERY_TIME**, il est certain que la valeur de **dispidRequest** n’a pas issus de l’expéditeur du message. Un client peut décider comment présenter la valeur de **dispidRequest** pour l’utilisateur final en fonction du résultat de cette comparaison conformément à la stratégie de sécurité spécifiques du client. Si la valeur de **dispidRequest** est ignorée en raison de la présence d’une valeur pour **dispidFlagStringEnum** ([PidLidFlagString](pidlidflagstring-canonical-property.md)), cette propriété doit être ignorée.
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications du protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des définitions de jeu de propriétés et des références aux spécifications du protocole Exchange Server connexes.
    
[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)
  
> Spécifie les propriétés et les opérations liées aux marquage.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
## <a name="see-also"></a>Voir aussi



[Propriété canonique PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md)


[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

