---
title: Propriété canonique PidLidValidFlagStringProof
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidLidValidFlagStringProof
api_type:
- COM
ms.assetid: e5a94968-7e84-4faf-8104-9ea36d35fa1a
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 28f405493b919fb1e8a49a39575e0a75767a98be
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59604396"
---
# <a name="pidlidvalidflagstringproof-canonical-property"></a>Propriété canonique PidLidValidFlagStringProof

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Valide si la valeur de la propriété **dispidRequest** ([PidLidFlagRequest](pidlidflagrequest-canonical-property.md)) a été définie par un agent qui connaît la valeur de la propriété **PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md)).
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |dispidValidFlagStringProof  <br/> |
|Jeu de propriétés :  <br/> |PSETID_Common  <br/> |
|ID long (LID) :  <br/> |0x000085BF  <br/> |
|Type de données :  <br/> |PT_SYSTIME  <br/> |
|Domaine :  <br/> |Tâche  <br/> |
   
## <a name="remarks"></a>Remarques

Sur les objets non sendables (objets de courrier et non-courrier reçus), les clients doivent définir cette valeur sur la valeur **de PR_MESSAGE_DELIVERY_TIME** lors de la modification **de dispidRequest**.
  
Étant donné que la valeur de **PR_MESSAGE_DELIVERY_TIME** ne peut pas être prévue par l’expéditeur, si la valeur de cette propriété est égale à la valeur de **PR_MESSAGE_DELIVERY_TIME,** il est raisonnablement certain que la valeur de **dispidRequest** n’a pas été issue de l’expéditeur du message. Un client peut décider comment présenter la valeur de **dispidRequest** à l’utilisateur final en fonction du résultat de cette comparaison conformément à la stratégie de sécurité spécifique du client. Si la valeur de **dispidRequest** est ignorée en raison de la présence d’une valeur pour **dispidFlagStringEnum** ([PidLidFlagString](pidlidflagstring-canonical-property.md)), cette propriété doit être ignorée.
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des définitions de jeu de propriétés et des références aux spécifications Exchange Server protocole.
    
[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)
  
> Spécifie les propriétés et les opérations liées au marquage.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
## <a name="see-also"></a>Voir aussi



[Propriété canonique PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md)


[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

