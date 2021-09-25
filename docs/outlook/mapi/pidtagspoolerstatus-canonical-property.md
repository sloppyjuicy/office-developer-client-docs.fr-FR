---
title: Propriété canonique PidTagSpoolerStatus
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.PidTagSpoolerStatus
api_type:
- COM
ms.assetid: a10d86fc-3a73-49dc-b974-ed852ec715e9
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 473f2745a6c3019db4994192fa4b138f1298b6cf
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59591408"
---
# <a name="pidtagspoolerstatus-canonical-property"></a>Propriété canonique PidTagSpoolerStatus

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient l’état du message en fonction des informations disponibles pour lepooler MAPI.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_SPOOLER_STATUS  <br/> |
|Identificateur :  <br/> |0x0E10  <br/> |
|Type de données :  <br/> |PT_LONG  <br/> |
|Domaine :  <br/> |MAPI non transmetteable  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété est calculée par MAPI sur les objets de message.
  
Cette propriété apparaît uniquement sur les messages entrants et est réservée dans tous les autres cas. Il indique si un message a été remis ou non à son emplacement final ou si un fournisseur de hooks de messagerie a potentiellement supprimé le message lors de son réroutage.
  
Les applications clientes ne doivent jamais définir cette propriété. Pour un message entrant, un client ou un fournisseur de services peut appeler [IMAPIProp::GetProps](imapiprop-getprops.md) sur cette propriété pour déterminer l’état du message. La valeur S_OK indique que le message a été correctement remis à la boutique de messages. La valeur MAPI_E_OBJECT_DELETED indique que le message a été supprimé et n’a jamais été engagé dans la boutique. 
  
Les fournisseurs de magasins de messages doivent prendre en charge cette propriété dans les messages, les tables des destinataires et la table des files d’attente sortantes. Les clients et les fournisseurs doivent être en mesure de définir des colonnes dans la table de files d’attente sortantes et de restreindre en fonction de cette propriété.
  
## <a name="related-resources"></a>Ressources connexes

### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
Mapitags.h
  
> Contient les définitions des propriétés répertoriées en tant que noms de remplacement.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

