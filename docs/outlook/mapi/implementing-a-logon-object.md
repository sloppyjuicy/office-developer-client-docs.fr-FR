---
title: Implémentation d'un objet d'ouverture de session
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 41e5c88c-d79d-4e9f-81f4-c4365cfaa15d
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: f9d77313012c2d133dc9352707ebc5e0c69c9973
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433044"
---
# <a name="implementing-a-logon-object"></a>Implémentation d'un objet d'ouverture de session

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Tous les carnets d'adresses, banques de messages et fournisseurs de transport instancient un objet d'ouverture de session dans le cadre de son implémentation de [IABProvider:: Logon](iabprovider-logon.md), [IMSProvider:: Logon](imsprovider-logon.md)ou [IXPProvider:: TransportLogon](ixpprovider-transportlogon.md). Les objets d'ouverture de session implémentent des méthodes qui aident les demandes client de service MAPI. En fonction de votre type de fournisseur de services, votre objet d'ouverture de session prendra en charge l'une des interfaces suivantes. 
  
|**Interface de l'objet Logon**|**Fournisseur de services**|
|:-----|:-----|
|[IABLogon : IUnknown](iablogoniunknown.md) <br/> |Fournisseur de carnets d'adresses  <br/> |
|[IMSLogon : IUnknown](imslogoniunknown.md) <br/> |Fournisseur de banque de messages  <br/> |
|[IXPLogon : IUnknown](ixplogoniunknown.md) <br/> |Fournisseur de transport  <br/> |
   
Les fournisseurs de carnet d'adresses et de banque de messages implémentent les fonctionnalités suivantes dans leurs objets d'ouverture de session:
  
- Prise en charge des notifications d'événements (méthodes**Advise** et Unadvise). **** Pour obtenir une vue d'ensemble de la notification d'événement, consultez la rubrique notifications d' [événements dans MAPI](event-notification-in-mapi.md). Pour plus d'informations sur la prise en charge de la notification dans votre objet Logon, consultez la rubrique [prise en charge](supporting-event-notification.md)des notifications d'événements. 
    
- Comparaison d'identificateur d'entrée (méthode**CompareEntryIDs** ). Pour obtenir des informations générales sur les identificateurs d'entrée, consultez la rubrique [MAPI Entry Identifiers](mapi-entry-identifiers.md). Pour plus d'informations sur la comparaison des identificateurs d'entrée dans la méthode **CompareEntryIDs** de l'objet Logon, voir [prise en charge de la comparaison et de l'accès aux objets](supporting-object-access-and-comparison.md).
    
- Accès aux informations supplémentaires sur l'erreur (méthode**GetLastError** ). Pour plus d'informations sur la gestion des erreurs dans MAPI, consultez la rubrique [gestion des erreurs dans MAPI](error-handling-in-mapi.md). 
    
- Accès aux objets implémentés par le fournisseur de services (méthode**OpenEntry** ). Pour plus d'informations, consultez la rubrique [prise en charge de l'accès aux objets et comparaison](supporting-object-access-and-comparison.md).
    
- Accès à un objet état (méthode**OpenStatusEntry** ). Pour obtenir des informations générales sur les objets d'État, voir [MAPI Status Objects](mapi-status-objects.md). Pour plus d'informations sur l'implémentation d'un objet Status, voir [Status implémentation Object](status-object-implementation.md).
    
- Un processus de fermeture de session (méthode de**fermeture de session** ). Pour plus d'informations, consultez la rubrique [arrêt d'un fournisseur de services](shutting-down-a-service-provider.md).
    
Si votre fournisseur est un fournisseur de carnets d'adresses, vous implémentez également les méthodes suivantes et les fonctionnalités associées:
  
- [IABLogon:: GetOneOffTable](iablogon-getoneofftable.md) pour fournir une liste des modèles que vous prenez en charge pour la création de nouveaux destinataires. Pour plus d'informations, consultez la rubrique [tables One-Off](one-off-tables.md) ou [implémentation d'une table ponctuelle de fournisseur](implementing-a-provider-one-off-table.md).
    
- [IABLogon:: OpenTemplateID](iablogon-opentemplateid.md) pour fournir l'accès à l'implémentation d'un destinataire dont les données résident dans un fournisseur de carnet d'adresses hôte. Pour plus d'informations, consultez [la rubrique agir en tant que fournisseur de carnet d'adresses étranger](acting-as-a-foreign-address-book-provider.md). 
    
- [IABLogon::P reparerecips](iablogon-preparerecips.md) pour vous assurer que les propriétés appropriées sont disponibles pour tous les destinataires d'une liste de destinataires. Pour plus d'informations, consultez la rubrique [IABLogon::P reparerecips](iablogon-preparerecips.md). 
    
L'objet d'ouverture de session d'un fournisseur de transport, qui implémente [IXPLogon: IUnknown](ixplogoniunknown.md), est très différent des objets d'ouverture de session implémentés par les autres types de fournisseurs de services. Il n'a que deux fonctionnalités en commun avec les autres objets Logon: l'accès à un objet Status via la méthode [IXPLogon:: OpenStatusEntry](ixplogon-openstatusentry.md) et une opération de fermeture de session via la méthode [IXPLogon:: TransportLogoff](ixplogon-transportlogoff.md) . Les fournisseurs de transport implémentent les fonctionnalités uniques suivantes dans leurs objets d'ouverture de session: 
  
- Inscription pour les types d'adresse (méthode[IXPLogon:: AddressTypes](ixplogon-addresstypes.md) ). Pour plus d'informations sur l'inscription d'un type d'adresse, consultez la rubrique [fournisseur de transport et modèle opérationnel de spouleUR MAPI](transport-provider-and-mapi-spooler-operational-model.md).
    
- Contrôle de la transmission des messages ([IXPLogon:: StartMessage](ixplogon-startmessage.md), [IXPLogon:: EndMessage](ixplogon-endmessage.md)et [IXPLogon:: SubmitMessage](ixplogon-submitmessage.md) méthodes). Pour plus d'informations, consultez la rubrique [modèle de réception des messages](message-reception-model.md), [interaction avec le spouleur MAPI](interacting-with-the-mapi-spooler.md)et [modèle de dépôt de messages](message-submission-model.md).
    
- Validation de l'état interne (méthode[IXPLogon:: ValidateState](ixplogon-validatestate.md) ). 
    
- Possibilité de télécharger ou de télécharger des messages à la demande (méthode[IXPLogon:: FlushQueues](ixplogon-flushqueues.md) ). Pour plus d'informations, consultez [la rubrique implémentation de la méthode FlushQueues](implementing-the-flushqueues-method.md).
    
- Possibilité d'interroger les messages en attente ([IXPLogon::P méthode oll](ixplogon-poll.md) ). Pour plus d'informations, consultez la rubrique [modèle de réception des messages](message-reception-model.md).
    
- Détection d'État inActif (méthode[IXPLogon:: Idle](ixplogon-idle.md) ). 
    
- Interaction avec le spouleur MAPI (méthode[IXPLogon:: TransportNotify](ixplogon-transportnotify.md) ). 
    
## <a name="see-also"></a>Voir aussi



[Implémentation de la connexion au fournisseur de services](implementing-service-provider-logon.md)

