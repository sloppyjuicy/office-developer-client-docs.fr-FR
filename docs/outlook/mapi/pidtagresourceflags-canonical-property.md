---
title: Propriété canonique PidTagResourceFlags
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagResourceFlags
api_type:
- COM
ms.assetid: 69be9ad3-006a-459e-9cd4-eb3f609d71ad
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 2fb9eed0beaf7269ac90a021dae650355484ebc2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436229"
---
# <a name="pidtagresourceflags-canonical-property"></a>Propriété canonique PidTagResourceFlags

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient un masque de bits d’indicateurs pour les fournisseurs et les services de messagerie.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_RESOURCE_FLAGS  <br/> |
|Identificateur :  <br/> |0x3009  <br/> |
|Type de données :  <br/> |PT_LONG  <br/> |
|Domaine :  <br/> |MAPI courant  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété décrit les caractéristiques d’un service de messagerie, d’un fournisseur de services ou d’un objet d’état. Les indicateurs qui sont définies pour cette propriété dépendent de son contexte. Par exemple, certains indicateurs sont valides uniquement pour les objets d’état et d’autres indicateurs uniquement pour les colonnes dans la table de service de message. 
  
Les indicateurs sont de trois classes : statique, modifiable et dynamique. Les indicateurs statiques sont définies par MAPI à partir de données dans MAPISVC. INF et jamais modifié. Les indicateurs modifiables sont définies par MAPI à partir de MAPISVC. INF, mais peut être modifié par la suite. Les indicateurs dynamiques peuvent être définies et réinitialisées par les méthodes MAPI.
  
Pour un service de message, un ou plusieurs des indicateurs suivants peuvent être définies dans cette propriété :
  
SERVICE_CREATE_WITH_STORE 
  
> Réservé. Ne pas utiliser.
    
SERVICE_DEFAULT_STORE 
  
> Dynamique. Le service de message contient la boutique par défaut. Une interface utilisateur doit s’afficher et invite l’utilisateur à confirmer la suppression ou le déplacement de ce service hors du profil. 
    
SERVICE_NO_PRIMARY_IDENTITY 
  
> Statique. Indicateur de niveau de service qui doit être définie pour indiquer qu’aucun des fournisseurs du service de messagerie ne peut être utilisé pour fournir une identité. Cet indicateur ou cet SERVICE_PRIMARY_IDENTITY doit être définie, mais pas les deux.
    
SERVICE_PRIMARY_IDENTITY 
  
> Modifiable. Le service de message correspondant contient le fournisseur utilisé pour l’identité principale de cette session. Utilisez [IMsgServiceAdmin::SetPrimaryIdentity](imsgserviceadmin-setprimaryidentity.md) pour définir cet indicateur. Cet indicateur ou cet SERVICE_NO_PRIMARY_IDENTITY doit être définie, mais pas les deux. 
    
SERVICE_SINGLE_COPY 
  
> Statique. Toute tentative de création ou de copie de ce service de message dans un profil où le service existe déjà échouera. Pour créer un service de message à copie **unique, ajoutez la propriété PR_RESOURCE_FLAGS** à la section du service dans MAPISVC. INF et définissez cet indicateur. 
    
Pour un fournisseur de services, un ou plusieurs des indicateurs suivants peuvent être PR_RESOURCE_FLAGS **:**
  
HOOK_INBOUND 
  
> Statique. Le hook dupooler doit traiter les messages entrants.
    
HOOK_OUTBOUND 
  
> Statique. Le hook dupooler doit traiter les messages sortants. 
    
STATUS_DEFAULT_OUTBOUND 
  
> Modifiable. Cette identité doit être appliquée aux messages sortants si le profil contient plusieurs instances de ce fournisseur de transport. Cela peut se produire si plusieurs instances d’un seul fournisseur de transport apparaissent dans le profil.
    
STATUS_DEFAULT_STORE 
  
> Modifiable. Cette magasin de messages est la boutique par défaut pour le profil. 
    
STATUS_NEED_IPM_TREE 
  
> Dynamique. Les dossiers standard de cette magasin de messages, y compris le dossier racine de message interpersonnel (IPM), n’ont pas encore été vérifiés. MAPI définit et effacer cet indicateur. 
    
STATUS_NO_DEFAULT_STORE 
  
> Statique. Cette magasin de messages ne peut pas devenir la boutique de messages par défaut pour le profil.
    
STATUS_NO_PRIMARY_IDENTITY 
  
> Statique. Ce fournisseur ne fournit pas d’identité dans sa ligne d’état. Cet indicateur ou cet STATUS_PRIMARY_IDENTITY doit être définie.
    
STATUS_OWN_STORE 
  
> Statique. Ce fournisseur de transport est étroitement associé à une magasin de messages et fournit la propriété **PR_OWN_STORE_ENTRYID** ([PidTagOwnStoreEntryId](pidtagownstoreentryid-canonical-property.md)) dans sa ligne d’état.
    
STATUS_PRIMARY_IDENTITY 
  
> Modifiable. Ce fournisseur fournit l’identité principale de la session . l’identificateur d’entrée pour la fourniture de l’objet l’identité est renvoyée par [IMAPISession::QueryIdentity](imapisession-queryidentity.md). Cet indicateur ou **cet STATUS_NO_PRIMARY_IDENTITY** doit être définie. 
    
STATUS_PRIMARY_STORE 
  
> Modifiable. Ce magasin de messages doit être utilisé lorsqu’une application cliente se connecte. Une fois ouvert, cette boutique doit être définie comme magasin par défaut pour le profil. 
    
STATUS_SECONDARY_STORE 
  
> Modifiable. Ce magasin de messages doit être utilisé si le magasin principal n’est pas disponible lorsqu’une application cliente se connecte. Une fois ouvert, cette boutique doit être définie comme magasin par défaut pour le profil. 
    
STATUS_SIMPLE_STORE 
  
> Dynamique. Cette magasin de messages sera utilisée par Simple MAPI comme magasin de messages par défaut.
    
STATUS_TEMP_SECTION 
  
> Dynamique. Cette magasin de messages ne doit pas être publiée dans la table de la boutique de messages et sera supprimée du profil après la décoff. 
    
STATUS_XP_PREFER_LAST 
  
> Statique. Ce transport s’attend à être le dernier transport sélectionné pour envoyer un message lorsque plusieurs fournisseurs de transport sont en mesure de transmettre le message.
    
## <a name="related-resources"></a>Ressources connexes

### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
Mapitags.h
  
> Contient les définitions des propriétés répertoriées en tant que noms de remplacement.
    
## <a name="see-also"></a>Voir aussi



[IMsgServiceAdmin::MsgServiceTransportOrder](imsgserviceadmin-msgservicetransportorder.md)
  
[Propriété canonique PidTagIdentityEntryId](pidtagidentityentryid-canonical-property.md)


[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

