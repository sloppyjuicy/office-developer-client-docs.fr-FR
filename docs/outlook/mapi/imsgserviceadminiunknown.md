---
title: IMsgServiceAdmin IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMsgServiceAdmin
api_type:
- COM
ms.assetid: 5905b9e9-c462-451d-a49f-1f3a8aa506a6
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: e2be100506babac0e519a9bb4cd88cd6ba2e903b
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62774929"
---
# <a name="imsgserviceadmin--iunknown"></a>IMsgServiceAdmin : IUnknown

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Modifie un service de message dans un profil.
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |MapiX.h  <br/> |
|Exposé par :  <br/> |Objets d’administration de service de message  <br/> |
|Implémenté par :  <br/> |MAPI  <br/> |
|Appelé par :  <br/> |Applications clientes  <br/> |
|Identificateur d’interface :  <br/> |IID_IMsgServiceAdmin  <br/> |
|Type de pointeur :  <br/> |LPSERVICEADMIN  <br/> |
   
## <a name="vtable-order"></a>Ordre des vtables

|||
|:-----|:-----|
|[GetLastError](imsgserviceadmin-getlasterror.md) <br/> |Renvoie une structure [MAPIERROR](mapierror.md) qui contient des informations sur la dernière erreur générée par un objet d’administration de service de message. |
|[GetMsgServiceTable](imsgserviceadmin-getmsgservicetable.md) <br/> |Permet d’accéder à la table des services de message, liste des services de message dans le profil. |
|[CreateMsgService](imsgserviceadmin-createmsgservice.md) <br/> |Ajoute un service de message au profil actuel. <br/>**REMARQUE** : cette méthode est dépréciée. Utilisez [IMsgServiceAdmin2::CreateMsgServiceEx](imsgserviceadmin2-createmsgserviceex.md) à la place.           |
|[DeleteMsgService](imsgserviceadmin-deletemsgservice.md) <br/> |Supprime un service de message d’un profil. |
|[CopyMsgService](imsgserviceadmin-copymsgservice.md) <br/> |Copie un service de message dans un profil. |
|[RenameMsgService](imsgserviceadmin-renamemsgservice.md) <br/> |Déconseillé. Attribue un nouveau nom à un service de message. |
|[ConfigureMsgService](imsgserviceadmin-configuremsgservice.md) <br/> |Reconfigure un service de message. |
|[OpenProfileSection](imsgserviceadmin-openprofilesection.md) <br/> |Ouvre une section du profil actuel et renvoie un [pointeur IProfSect](iprofsectimapiprop.md) pour un accès supplémentaire. |
|[MsgServiceTransportOrder](imsgserviceadmin-msgservicetransportorder.md) <br/> |Définit l’ordre dans lequel les fournisseurs de transport sont appelés pour remettre un message. |
|[AdminProviders](imsgserviceadmin-adminproviders.md) <br/> |Renvoie un pointeur qui donne accès à un objet d’administration de fournisseur. |
|[SetPrimaryIdentity](imsgserviceadmin-setprimaryidentity.md) <br/> |Désigne un service de message comme fournisseur de l’identité principale du profil. |
|[GetProviderTable](imsgserviceadmin-getprovidertable.md) <br/> |Permet d’accéder à la table des fournisseurs, qui répertorie les fournisseurs de services dans le profil. |
   
## <a name="remarks"></a>Remarques

Une implémentation peut obtenir un pointeur vers une interface **IMsgServiceAdmin de deux manières** : en appelant la méthode [IMAPISession::AdminServices](imapisession-adminservices.md) ou en appelant la méthode [IProfAdmin::AdminServices](iprofadmin-adminservices.md) . Pour les clients principalement concernés par la configuration de profil, **IProfAdmin::AdminServices** est le moyen préféré pour obtenir l’interface **IMsgServiceAdmin** , car il ne se connecte pas aux fournisseurs à la session MAPI. Si un client nécessite la possibilité d’apporter des modifications au profil actif, **IMAPISession::AdminServices** doit être appelé pour obtenir le pointeur **IMsgServiceAdmin** . Notez que même si MAPI n’autorise pas la suppression d’un profil en cours d’utilisation, il n’existe aucune protection pour empêcher un client de supprimer tous les services de message du profil. 
  
## <a name="see-also"></a>Voir aussi



[Interfaces MAPI](mapi-interfaces.md)

