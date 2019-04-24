---
title: Propriété canonique PidTagSpoolerStatus
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSpoolerStatus
api_type:
- COM
ms.assetid: a10d86fc-3a73-49dc-b974-ed852ec715e9
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 426d26cae147faf3f843ac547de9d205d766ac44
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348208"
---
# <a name="pidtagspoolerstatus-canonical-property"></a>Propriété canonique PidTagSpoolerStatus

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient l'état du message en fonction des informations qui sont disponibles pour le spouleur MAPI.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_SPOOLER_STATUS  <br/> |
|Identificateur :  <br/> |0x0E10  <br/> |
|Type de données :  <br/> |PT_LONG  <br/> |
|Domaine :  <br/> |MAPI non transmissible  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété est calculée par MAPI sur les objets message.
  
Cette propriété s'affiche sur les messages entrants uniquement et est réservée dans tous les autres cas. Il indique si un message a été remis ou non à son emplacement final ou si un fournisseur de service de raccordement de messagerie peut avoir supprimé le message lors de son reroutage.
  
Les applications clientes ne doivent jamais définir cette propriété. Pour un message entrant, un client ou un fournisseur de services peut appeler [IMAPIProp:: GetProps](imapiprop-getprops.md) sur cette propriété pour déterminer l'état du message. La valeur S_OK indique que le message a bien été remis à la Banque de messages. La valeur MAPI_E_OBJECT_DELETED indique que le message a été supprimé et qu'il n'a jamais été validé dans la Banque. 
  
Les fournisseurs de banques de messages doivent prendre en charge cette propriété sur les messages, les tables de destinataires et la table de file d'attente sortante. Les clients et les fournisseurs doivent être en mesure de définir des colonnes sur la table de file d'attente sortante et de restreindre en fonction de cette propriété.
  
## <a name="related-resources"></a>Ressources associées

### <a name="header-files"></a>Fichiers d'en-tête

Mapidefs. h
  
> Fournit des définitions de type de données.
    
Mapitags. h
  
> Contient les définitions des propriétés figurant en tant que noms de substitution.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

