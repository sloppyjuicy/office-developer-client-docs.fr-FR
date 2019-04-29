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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: aba61d4acf7c1f9a5d91fa15f1ca6b16f173bcb2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426134"
---
# <a name="imsgserviceadmin--iunknown"></a>IMsgServiceAdmin : IUnknown

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Apporte des modifications à un service de messagerie dans un profil.
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |MapiX. h  <br/> |
|Exposé par:  <br/> |Objets d'administration du service de messagerie  <br/> |
|Implémenté par :  <br/> |MAPI  <br/> |
|Appelé par :  <br/> |Applications clientes  <br/> |
|Identificateur de l'interface:  <br/> |IID_IMsgServiceAdmin  <br/> |
|Type de pointeur:  <br/> |LPSERVICEADMIN  <br/> |
   
## <a name="vtable-order"></a>Ordre vtable

|||
|:-----|:-----|
|[Généré](imsgserviceadmin-getlasterror.md) <br/> |Renvoie une structure [MAPIERROR](mapierror.md) qui contient des informations sur la dernière erreur générée par un objet d'administration de service de messagerie.  <br/> |
|[GetMsgServiceTable](imsgserviceadmin-getmsgservicetable.md) <br/> |Fournit l'accès à la table de service de messagerie, une liste des services de messagerie dans le profil.  <br/> |
|[CreateMsgService](imsgserviceadmin-createmsgservice.md) <br/> |Ajoute un service de messagerie au profil actif.  <br/> <br/>**Remarque**: cette méthode est déconseillée. Utilisez [IMsgServiceAdmin2:: CreateMsgServiceEx](imsgserviceadmin2-createmsgserviceex.md) à la place.           |
|[DeleteMsgService](imsgserviceadmin-deletemsgservice.md) <br/> |Supprime un service de messagerie d'un profil.  <br/> |
|[CopyMsgService](imsgserviceadmin-copymsgservice.md) <br/> |Copie un service de messagerie dans un profil.  <br/> |
|[RenameMsgService](imsgserviceadmin-renamemsgservice.md) <br/> |Déconseillé. Affecte un nouveau nom à un service de messagerie.  <br/> |
|[ConfigureMsgService](imsgserviceadmin-configuremsgservice.md) <br/> |Reconfigure un service de messagerie.  <br/> |
|[OpenProfileSection](imsgserviceadmin-openprofilesection.md) <br/> |Ouvre une section du profil actif et renvoie un pointeur [IProfSect](iprofsectimapiprop.md) pour un accès supplémentaire.  <br/> |
|[MsgServiceTransportOrder](imsgserviceadmin-msgservicetransportorder.md) <br/> |Définit l'ordre dans lequel les fournisseurs de transport sont appelés pour la remise d'un message.  <br/> |
|[AdminProviders](imsgserviceadmin-adminproviders.md) <br/> |Renvoie un pointeur qui fournit l'accès à un objet d'administration de fournisseur.  <br/> |
|[SetPrimaryIdentity](imsgserviceadmin-setprimaryidentity.md) <br/> |Désigne un service de messagerie en tant que fournisseur de l'identité principale pour le profil.  <br/> |
|[GetProviderTable](imsgserviceadmin-getprovidertable.md) <br/> |Fournit l'accès à la table du fournisseur, une liste des fournisseurs de services dans le profil.  <br/> |
   
## <a name="remarks"></a>Remarques

Une implémentation peut obtenir un pointeur vers une interface **IMsgServiceAdmin** de deux manières: en appelant la méthode [IMAPISession:: AdminServices](imapisession-adminservices.md) ou en appelant la méthode [IProfAdmin:: AdminServices](iprofadmin-adminservices.md) . Pour les clients qui concernent principalement la configuration de profil, **IProfAdmin:: AdminServices** est le meilleur moyen d'obtenir l'interface **IMsgServiceAdmin** , car il ne se connecte pas aux fournisseurs dans la session MAPI. Si un client a besoin de pouvoir apporter des modifications au profil actif, **IMAPISession:: AdminServices** doit être appelé pour obtenir le pointeur **IMsgServiceAdmin** . N'oubliez pas que, bien que MAPI n'autorise pas la suppression d'un profil en cours d'utilisation, il n'existe aucune protection pour empêcher un client de supprimer tous les services de messagerie dans le profil. 
  
## <a name="see-also"></a>Voir aussi



[Interfaces MAPI](mapi-interfaces.md)

