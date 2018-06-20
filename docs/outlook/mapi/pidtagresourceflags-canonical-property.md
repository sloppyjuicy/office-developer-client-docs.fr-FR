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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: dae917b3e536aee5f24879edc3ccf0736e7c9f34
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19786599"
---
# <a name="pidtagresourceflags-canonical-property"></a>Propriété canonique PidTagResourceFlags

  
  
**S’applique à**: Outlook 
  
Contient un masque de bits d’indicateurs pour les fournisseurs et les services de messagerie.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_RESOURCE_FLAGS  <br/> |
|Identificateur :  <br/> |0x3009  <br/> |
|Type de données :  <br/> |PT_LONG  <br/> |
|Zone :  <br/> |MAPI courantes  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété décrit les caractéristiques d’un service de message, un fournisseur de services ou un objet d’état. Les indicateurs qui sont définis pour cette propriété dépendant de son contexte. Par exemple, certains indicateurs sont valides uniquement pour les objets d’état et d’autres indicateurs uniquement pour les colonnes dans la table de service de message. 
  
Les indicateurs sont de trois classes : modifiable, statiques et dynamiques. Indicateurs statiques sont définis par MAPI à partir des données dans le fichier MAPISVC.inf. INF et n’a jamais été modifié. Modifiables indicateurs sont définis par MAPI à partir du fichier MAPISVC.inf. INF mais peut être modifiée par la suite. Indicateurs dynamiques pouvant être définies et réinitialiser par les méthodes MAPI.
  
Pour un service de message, un ou plusieurs des indicateurs suivants peuvent être défini dans cette propriété :
  
SERVICE_CREATE_WITH_STORE 
  
> Réservé. Ne pas utiliser.
    
SERVICE_DEFAULT_STORE 
  
> Dynamique. Le service de message contient la banque par défaut. Une interface utilisateur doit être affichée demander à l’utilisateur de confirmer la suppression ou le déplacement de ce service s’en déconnecter le profil. 
    
SERVICE_NO_PRIMARY_IDENTITY 
  
> Statique. L’indicateur au niveau de service qui doit être défini pour indiquer qu’aucun des fournisseurs dans le service de message peut être utilisée pour fournir une identité. Cet indicateur ou SERVICE_PRIMARY_IDENTITY doit être ensemble, mais pas les deux.
    
SERVICE_PRIMARY_IDENTITY 
  
> Modifiable. Le service de message correspondant contient le fournisseur utilisé pour l’identité du principale pour cette session. [IMsgServiceAdmin::SetPrimaryIdentity](imsgserviceadmin-setprimaryidentity.md) permet de définir cet indicateur. Cet indicateur ou SERVICE_NO_PRIMARY_IDENTITY doit être ensemble, mais pas les deux. 
    
SERVICE_SINGLE_COPY 
  
> Statique. Toute tentative pour créer ou copier ce service de message dans un profil dans lequel le service existe déjà échouera. Pour créer une copie unique service de message ajouter la propriété **PR_RESOURCE_FLAGS** à la section du service dans le fichier MAPISVC.inf. INF et de définir cet indicateur. 
    
Pour un fournisseur de services, un ou plusieurs des indicateurs suivants peuvent être définies dans **PR_RESOURCE_FLAGS**:
  
HOOK_INBOUND 
  
> Statique. Le crochet spouleur doit traiter les messages entrants.
    
HOOK_OUTBOUND 
  
> Statique. Le crochet spouleur doit traiter les messages sortants. 
    
STATUS_DEFAULT_OUTBOUND 
  
> Modifiable. Ce paramètre identity doit être appliqué aux messages sortants si le profil contient plusieurs instances de ce fournisseur de transport. Cela peut se produire si plusieurs instances d’un fournisseur de transport unique s’affichent dans le profil.
    
STATUS_DEFAULT_STORE 
  
> Modifiable. Cette banque de messages est la banque par défaut pour le profil. 
    
STATUS_NEED_IPM_TREE 
  
> Dynamique. Les dossiers standards dans cette banque de messages, y compris le dossier racine du message interpersonnel (IPM), n’ont pas encore été vérifiées. MAPI Active et désactive cet indicateur. 
    
STATUS_NO_DEFAULT_STORE 
  
> Statique. Cette banque de messages est incapable de devenir la banque de messages par défaut pour le profil.
    
STATUS_NO_PRIMARY_IDENTITY 
  
> Statique. Ce fournisseur ne pas de fournir une identité dans sa ligne d’état. Cet indicateur ou STATUS_PRIMARY_IDENTITY doit être défini.
    
STATUS_OWN_STORE 
  
> Statique. Ce fournisseur de transport fortement couplé à une banque de messages et fournit la propriété **PR_OWN_STORE_ENTRYID** ([PidTagOwnStoreEntryId](pidtagownstoreentryid-canonical-property.md)) dans la ligne d’état.
    
STATUS_PRIMARY_IDENTITY 
  
> Modifiable. Ce fournisseur fournit l’identité du principale pour la session ; l’identificateur d’entrée pour l’objet fournissant l’identité est renvoyé à partir de [IMAPISession::QueryIdentity](imapisession-queryidentity.md). Cet indicateur ou **STATUS_NO_PRIMARY_IDENTITY** doit être défini. 
    
STATUS_PRIMARY_STORE 
  
> Modifiable. Cette banque de messages doit être utilisé lorsqu’une application cliente se connecte. Une fois ouvert, ce magasin doit être défini en tant que la banque par défaut pour le profil. 
    
STATUS_SECONDARY_STORE 
  
> Modifiable. Cette banque de messages doit être utilisé si la banque principale n’est pas disponible lorsqu’une application cliente se connecte. Une fois ouvert, ce magasin doit être défini en tant que la banque par défaut pour le profil. 
    
STATUS_SIMPLE_STORE 
  
> Dynamique. Permettra de cette banque de messages par l’interface Simple MAPI en tant que la banque de messages par défaut.
    
STATUS_TEMP_SECTION 
  
> Dynamique. Cette banque de messages ne doit pas être publiée dans la table et du profil est supprimée après la fermeture de session. 
    
STATUS_XP_PREFER_LAST 
  
> Statique. Ce transport est censé être le dernier transport sélectionné pour envoyer un message lorsque plusieurs fournisseurs de transport sont en mesure de transmettre le message.
    
## <a name="related-resources"></a>Ressources connexes

### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
MAPITAGS.h
  
> Contient les définitions des propriétés répertoriées en tant que d’autres noms.
    
## <a name="see-also"></a>Voir aussi



[IMsgServiceAdmin::MsgServiceTransportOrder](imsgserviceadmin-msgservicetransportorder.md)
  
[Propriété canonique PidTagIdentityEntryId](pidtagidentityentryid-canonical-property.md)


[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage de noms de propriété canonique aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage de noms MAPI pour les noms de propriété canonique](mapping-mapi-names-to-canonical-property-names.md)

