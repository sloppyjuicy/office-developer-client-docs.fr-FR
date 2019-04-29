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
  
Contient un masque de réindicateur des indicateurs pour les services de messagerie et les fournisseurs.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_RESOURCE_FLAGS  <br/> |
|Identificateur :  <br/> |0x3009  <br/> |
|Type de données :  <br/> |PT_LONG  <br/> |
|Domaine :  <br/> |MAPI commun  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété décrit les caractéristiques d'un service de messagerie, d'un fournisseur de services ou d'un objet d'État. Les indicateurs définis pour cette propriété dépendent de son contexte. Par exemple, certains indicateurs ne sont valides que pour les objets d'État et les autres indicateurs uniquement pour les colonnes du tableau de service de message. 
  
Les indicateurs sont de trois classes: statique, modifiable et dynamique. Les indicateurs statiques sont définis par MAPI à partir de données dans MAPISVC. INF et jamais modifié. Les indicateurs modifiables sont définis par MAPI à partir de MAPISVC. INF, mais peut être modifié par la suite. Les indicateurs dynamiques peuvent être définis et réinitialisés par des méthodes MAPI.
  
Pour un service de messagerie, un ou plusieurs des indicateurs suivants peuvent être définis dans cette propriété:
  
SERVICE_CREATE_WITH_STORE 
  
> Réservé. Ne pas utiliser.
    
SERVICE_DEFAULT_STORE 
  
> Dynamique. Le service de messagerie contient le magasin par défaut. Une interface utilisateur doit s'afficher pour inviter l'utilisateur à confirmer avant de supprimer ou de retirer ce service du profil. 
    
SERVICE_NO_PRIMARY_IDENTITY 
  
> Liée. Indicateur de niveau de service qui doit être défini pour indiquer qu'aucun des fournisseurs dans le service de messagerie ne peut être utilisé pour fournir une identité. Cet indicateur ou SERVICE_PRIMARY_IDENTITY doit être défini, mais pas les deux.
    
SERVICE_PRIMARY_IDENTITY 
  
> Modifiable. Le service de messagerie correspondant contient le fournisseur utilisé pour l'identité principale de cette session. Utilisez [IMsgServiceAdmin:: SetPrimaryIdentity](imsgserviceadmin-setprimaryidentity.md) pour définir cet indicateur. Cet indicateur ou SERVICE_NO_PRIMARY_IDENTITY doit être défini, mais pas les deux. 
    
SERVICE_SINGLE_COPY 
  
> Liée. Toute tentative de création ou de copie de ce service de messagerie dans un profil où le service existe déjà échouera. Pour créer un service de messagerie à copie unique, ajoutez la propriété **PR_RESOURCE_FLAGS** à la section du service dans MAPISVC. INF et définissez cet indicateur. 
    
Pour un fournisseur de services, un ou plusieurs des indicateurs suivants peuvent être définis dans **PR_RESOURCE_FLAGS**:
  
HOOK_INBOUND 
  
> Liée. Le hook de spouleur doit traiter les messages entrants.
    
HOOK_OUTBOUND 
  
> Liée. Le hook de spouleur doit traiter les messages sortants. 
    
STATUS_DEFAULT_OUTBOUND 
  
> Modifiable. Cette identité doit être appliquée aux messages sortants si le profil contient plusieurs instances de ce fournisseur de transport. Cela peut se produire si plusieurs instances d'un fournisseur de transport unique apparaissent dans le profil.
    
STATUS_DEFAULT_STORE 
  
> Modifiable. Il s'agit de la Banque de messages par défaut pour le profil. 
    
STATUS_NEED_IPM_TREE 
  
> Dynamique. Les dossiers standard de cette banque de messages, y compris le dossier racine de message, n'ont pas encore été vérifiés. MAPI définit et efface cet indicateur. 
    
STATUS_NO_DEFAULT_STORE 
  
> Liée. Cette banque de messages ne peut pas devenir la Banque de messages par défaut pour le profil.
    
STATUS_NO_PRIMARY_IDENTITY 
  
> Liée. Ce fournisseur ne fournit pas d'identité dans sa ligne d'État. Cet indicateur ou STATUS_PRIMARY_IDENTITY doit être défini.
    
STATUS_OWN_STORE 
  
> Liée. Ce fournisseur de transport est étroitement couplé à une banque de messages et fournit la propriété **PR_OWN_STORE_ENTRYID** ([PidTagOwnStoreEntryId](pidtagownstoreentryid-canonical-property.md)) dans sa ligne d'État.
    
STATUS_PRIMARY_IDENTITY 
  
> Modifiable. Ce fournisseur fournit l'identité principale pour la session; l'identificateur d'entrée pour l'objet qui fournit l'identité est renvoyé depuis [IMAPISession:: QueryIdentity](imapisession-queryidentity.md). Cet indicateur ou **STATUS_NO_PRIMARY_IDENTITY** doit être défini. 
    
STATUS_PRIMARY_STORE 
  
> Modifiable. Cette banque de messages doit être utilisée lorsqu'une application cliente se connecte. Une fois ouvert, ce magasin doit être défini comme magasin par défaut pour le profil. 
    
STATUS_SECONDARY_STORE 
  
> Modifiable. Cette banque de messages doit être utilisée si le magasin principal n'est pas disponible lorsqu'une application cliente se connecte. Une fois ouvert, ce magasin doit être défini comme magasin par défaut pour le profil. 
    
STATUS_SIMPLE_STORE 
  
> Dynamique. Cette banque de messages sera utilisée par le simple MAPI comme banque de messages par défaut.
    
STATUS_TEMP_SECTION 
  
> Dynamique. Cette banque de messages ne doit pas être publiée dans la table de banque de messages et sera supprimée du profil après la fermeture de session. 
    
STATUS_XP_PREFER_LAST 
  
> Liée. Ce transport s'attend à être le dernier transport sélectionné pour envoyer un message lorsque plusieurs fournisseurs de transport peuvent transmettre le message.
    
## <a name="related-resources"></a>Ressources connexes

### <a name="header-files"></a>Fichiers d'en-tête

Mapidefs. h
  
> Fournit des définitions de type de données.
    
Mapitags. h
  
> Contient les définitions des propriétés figurant en tant que noms de substitution.
    
## <a name="see-also"></a>Voir aussi



[IMsgServiceAdmin::MsgServiceTransportOrder](imsgserviceadmin-msgservicetransportorder.md)
  
[Propriété canonique PidTagIdentityEntryId](pidtagidentityentryid-canonical-property.md)


[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

