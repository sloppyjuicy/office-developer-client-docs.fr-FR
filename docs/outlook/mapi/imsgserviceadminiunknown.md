---
title: IMsgServiceAdmin IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgServiceAdmin
api_type:
- COM
ms.assetid: 5905b9e9-c462-451d-a49f-1f3a8aa506a6
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 21889bf626d7f9128d1e01b3e6a15b5fa0d2e696
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784266"
---
# <a name="imsgserviceadmin--iunknown"></a>IMsgServiceAdmin : IUnknown

  
  
**S’applique à**: Outlook 
  
Modifie un service de message dans un profil.
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |MapiX.h  <br/> |
|Exposés par :  <br/> |Objets d’administration de service de message  <br/> |
|Implémentée par :  <br/> |MAPI  <br/> |
|Appelée par :  <br/> |Applications clientes  <br/> |
|Identificateur de l’interface :  <br/> |IID_IMsgServiceAdmin  <br/> |
|Type de pointeur :  <br/> |LPSERVICEADMIN  <br/> |
   
## <a name="vtable-order"></a>Ordre vtable

|||
|:-----|:-----|
|[GetLastError](imsgserviceadmin-getlasterror.md) <br/> |Retourne une structure [MAPIERROR](mapierror.md) qui contient des informations sur la dernière erreur générée par un objet de l’administration de service de message.  <br/> |
|[GetMsgServiceTable](imsgserviceadmin-getmsgservicetable.md) <br/> |Permet d’accéder à la table de service de message, une liste des services dans le profil de message.  <br/> |
|[CreateMsgService](imsgserviceadmin-createmsgservice.md) <br/> |Ajoute un service de message pour le profil actuel.  <br/> <br/>**Remarque**: cette méthode est déconseillée. Utilisez plutôt [IMsgServiceAdmin2::CreateMsgServiceEx](imsgserviceadmin2-createmsgserviceex.md) .           |
|[DeleteMsgService](imsgserviceadmin-deletemsgservice.md) <br/> |Supprime un service de message d’un profil.  <br/> |
|[CopyMsgService](imsgserviceadmin-copymsgservice.md) <br/> |Copie un service de message dans un profil.  <br/> |
|[RenameMsgService](imsgserviceadmin-renamemsgservice.md) <br/> |Déconseillé. Affecte un nouveau nom à un service de message.  <br/> |
|[ConfigureMsgService](imsgserviceadmin-configuremsgservice.md) <br/> |RECONFIGURE un service de message.  <br/> |
|[OpenProfileSection](imsgserviceadmin-openprofilesection.md) <br/> |Ouvre une section du profil actuel et retourne un pointeur [IProfSect](iprofsectimapiprop.md) pour davantage d’accès.  <br/> |
|[MsgServiceTransportOrder](imsgserviceadmin-msgservicetransportorder.md) <br/> |Définit l’ordre dans les transports fournisseurs sont appelées pour remettre un message.  <br/> |
|[AdminProviders](imsgserviceadmin-adminproviders.md) <br/> |Renvoie un pointeur qui fournit l’accès à un objet de l’administration du fournisseur.  <br/> |
|[SetPrimaryIdentity](imsgserviceadmin-setprimaryidentity.md) <br/> |Désigne un service de message pour être le fournisseur de l’identité principale pour le profil.  <br/> |
|[GetProviderTable](imsgserviceadmin-getprovidertable.md) <br/> |Permet d’accéder à la table fournisseurs, une liste des fournisseurs de services dans le profil.  <br/> |
   
## <a name="remarks"></a>Remarques

Une implémentation peut obtenir un pointeur vers une interface **IMsgServiceAdmin** de deux manières : en appelant la méthode [IMAPISession::AdminServices](imapisession-adminservices.md) ou en appelant la méthode [IProfAdmin::AdminServices](iprofadmin-adminservices.md) . Pour les clients principalement avec la configuration de profil, **IProfAdmin::AdminServices** est le meilleur moyen d’obtenir l’interface **IMsgServiceAdmin** , car il n’enregistre pas sur les fournisseurs de la session MAPI. Si un client nécessite la possibilité d’apporter des modifications au profil actif, **IMAPISession::AdminServices** doit être appelée pour obtenir le pointeur **IMsgServiceAdmin** . Sachez que bien que MAPI ne permet pas d’un profil qui est en cours d’utilisation d’être supprimé, il n’existe aucune protection pour empêcher la suppression de tous les services de message dans le profil d’un client. 
  
## <a name="see-also"></a>Voir aussi



[Interfaces MAPI](mapi-interfaces.md)

