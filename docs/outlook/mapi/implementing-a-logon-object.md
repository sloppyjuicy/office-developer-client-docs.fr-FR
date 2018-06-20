---
title: Implémentation d’un objet d’ouverture de session
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 41e5c88c-d79d-4e9f-81f4-c4365cfaa15d
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: e23c73931c9051b61d30b7ea7e9c54d06a4d9c33
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784157"
---
# <a name="implementing-a-logon-object"></a>Implémentation d’un objet d’ouverture de session

  
  
**S’applique à**: Outlook 
  
Chaque carnet d’adresses, la banque de messages et le fournisseur de transport instancie un objet d’ouverture de session dans le cadre de son implémentation de [IABProvider::Logon](iabprovider-logon.md), [IMSProvider::Logon](imsprovider-logon.md)ou [IXPProvider::TransportLogon](ixpprovider-transportlogon.md). Objets d’ouverture de session implémentent les méthodes qui aident les demandes des clients MAPI. Selon votre type de fournisseur de services, votre objet de connexion prendront en charge une des interfaces suivantes. 
  
|**Interface d’objet d’ouverture de session**|**Fournisseur de services**|
|:-----|:-----|
|[IABLogon : IUnknown](iablogoniunknown.md) <br/> |Fournisseur de carnet d’adresses  <br/> |
|[IMSLogon : IUnknown](imslogoniunknown.md) <br/> |Fournisseur de banque de messages  <br/> |
|[IXPLogon : IUnknown](ixplogoniunknown.md) <br/> |Fournisseur de transport  <br/> |
   
Message et le carnet d’adresses stockent implémentés par les fournisseurs dans leurs objets d’ouverture de session des fonctionnalités suivantes :
  
- Prise en charge de la notification d’événement (méthodes**Advise** et **Unadvise** ). Pour une vue d’ensemble de notification d’événement, voir la [Notification d’événement MAPI](event-notification-in-mapi.md). Pour plus d’informations sur la prise en charge de la notification dans votre objet de connexion, voir [Prise en charge de Notification d’événement](supporting-event-notification.md). 
    
- Comparaison d’identificateur d’entrée (méthode**CompareEntryIDs** ). Pour obtenir des informations générales sur les identificateurs d’entrée, voir [Identificateurs d’entrée MAPI](mapi-entry-identifiers.md). Pour plus d’informations sur la comparaison des identificateurs d’entrée dans la méthode de l’objet d’ouverture de session **CompareEntryIDs** , voir [prise en charge l’accès aux objets et comparaison](supporting-object-access-and-comparison.md).
    
- Accès aux informations d’erreur supplémentaires (méthode**GetLastError** ). Pour plus d’informations sur la gestion des erreurs dans MAPI, voir [Gestion des erreurs dans MAPI](error-handling-in-mapi.md). 
    
- Accès aux objets implémentés par le fournisseur de services (méthode**OpenEntry** ). Pour plus d’informations, voir [prise en charge l’accès aux objets et comparaison](supporting-object-access-and-comparison.md).
    
- Accès à un objet d’état (méthode**OpenStatusEntry** ). Pour obtenir des informations générales sur les objets d’état, voir [Les objets état MAPI](mapi-status-objects.md). Pour obtenir des informations spécifiques sur l’implémentation d’un objet d’état, voir [Implémentation d’objet état](status-object-implementation.md).
    
- Un processus de fermeture de session (méthode de**fermeture de session** ). Pour plus d’informations, voir [Arrêt vers le bas un fournisseur de services](shutting-down-a-service-provider.md).
    
Si votre fournisseur est un fournisseur de carnet d’adresses, vous allez également implémenter les méthodes suivantes et les fonctionnalités associées :
  
- [IABLogon::GetOneOffTable](iablogon-getoneofftable.md) pour fournir une liste des modèles que vous prenez en charge pour la création de nouveaux destinataires. Pour plus d’informations, voir [Tables uniques](one-off-tables.md) ou [l’implémentation d’une Table des fournisseurs d’uniques](implementing-a-provider-one-off-table.md).
    
- [IABLogon::OpenTemplateID](iablogon-opentemplateid.md) pour fournir l’accès à l’implémentation d’un destinataire dont les données se trouve dans un fournisseur de carnet d’adresses hôte. Pour plus d’informations, voir [agissant comme un fournisseur de carnet d’adresses étrangère](acting-as-a-foreign-address-book-provider.md). 
    
- [IABLogon::PrepareRecips](iablogon-preparerecips.md) pour vous assurer que les propriétés appropriées sont disponibles pour tous les destinataires dans une liste de destinataires. Pour plus d’informations, voir [IABLogon::PrepareRecips](iablogon-preparerecips.md). 
    
Objet d’ouverture de session d’un fournisseur de transport qui implémente [IXPLogon : IUnknown](ixplogoniunknown.md), est assez différente de l’ouverture de session objets implémentés par les autres types de fournisseurs de services. Propose des fonctionnalités uniquement deux points communs avec les autres objets d’ouverture de session : accès à un objet d’état par le biais de la méthode [IXPLogon::OpenStatusEntry](ixplogon-openstatusentry.md) et une opération de déconnexion par le biais de la méthode [IXPLogon::TransportLogoff](ixplogon-transportlogoff.md) . Fournisseurs de transport implémentent les fonctionnalités suivantes dans les objets d’ouverture de session : 
  
- Inscription pour les types d’adresses (méthode[IXPLogon::AddressTypes](ixplogon-addresstypes.md) ). Pour plus d’informations sur l’inscription d’un type d’adresse, voir [fournisseur de Transport et le modèle opérationnel du spouleur MAPI](transport-provider-and-mapi-spooler-operational-model.md).
    
- Contrôle de la transmission de message (méthodes[IXPLogon::StartMessage](ixplogon-startmessage.md), [IXPLogon::EndMessage](ixplogon-endmessage.md)et [IXPLogon::SubmitMessage](ixplogon-submitmessage.md) ). Pour plus d’informations, voir [Modèle de réception de Message](message-reception-model.md), [l’interaction avec le spouleur MAPI](interacting-with-the-mapi-spooler.md)et [Modèle d’envoi de Message](message-submission-model.md).
    
- Validation de l’état interne (méthode[IXPLogon::ValidateState](ixplogon-validatestate.md) ). 
    
- Possibilité de télécharger ou transférer des messages à la demande (méthode[IXPLogon::FlushQueues](ixplogon-flushqueues.md) ). Pour plus d’informations, voir [implémentation de la méthode FlushQueues](implementing-the-flushqueues-method.md).
    
- Possibilité de requête en attente de messages (méthode[IXPLogon::Poll](ixplogon-poll.md) ). Pour plus d’informations, voir [Modèle de réception de messages](message-reception-model.md).
    
- Détection de l’état est inactif (méthode[IXPLogon::Idle](ixplogon-idle.md) ). 
    
- Interaction avec le spouleur MAPI (méthode[IXPLogon::TransportNotify](ixplogon-transportnotify.md) ). 
    
## <a name="see-also"></a>Voir aussi



[L’implémentation du fournisseur de Service d’ouverture de session](implementing-service-provider-logon.md)

