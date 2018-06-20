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
ms.openlocfilehash: df52f668e91b707c0436b394186b27fdbb3a5dbf
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19786820"
---
# <a name="pidtagspoolerstatus-canonical-property"></a>Propriété canonique PidTagSpoolerStatus

  
  
**S’applique à**: Outlook 
  
Indique le statut du message en fonction des informations qui est disponibles pour le spouleur MAPI.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_SPOOLER_STATUS  <br/> |
|Identificateur :  <br/> |0x0E10  <br/> |
|Type de données :  <br/> |PT_LONG  <br/> |
|Zone :  <br/> |MAPI non transmissible  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété est calculée par MAPI sur les objets de message.
  
Cette propriété s’affiche uniquement les messages entrants et est réservée dans tous les autres cas. Il indique si un message a été remis à son emplacement final ou si un fournisseur de messagerie crochet potentiellement a supprimé le message lors de son réacheminement.
  
Applications clientes ne doivent jamais définir cette propriété. Pour un message entrant, un client ou fournisseur de services peut appeler [IMAPIProp::GetProps](imapiprop-getprops.md) sur cette propriété pour déterminer le statut du message. La valeur S_OK indique que le message a bien été remis à la banque de messages. La valeur MAPI_E_OBJECT_DELETED indique que le message a été supprimé et n’a jamais validé dans le magasin. 
  
Fournisseurs de magasins de message doivent prendre en charge cette propriété dans les messages, les tables de destinataires et la table sortant de la file d’attente. Fournisseurs et clients doivent être en mesure de définir les colonnes de la table sortant de la file d’attente et de restreindre en fonction de cette propriété.
  
## <a name="related-resources"></a>Ressources connexes

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

