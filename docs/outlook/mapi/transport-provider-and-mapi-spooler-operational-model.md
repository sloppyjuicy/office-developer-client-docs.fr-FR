---
title: Fournisseur de transport et modèle opérationnel du spooler MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: b0f8d8f0-fed7-4a7c-bc40-e935f159591d
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 9613c46ee105d24317c6c902f8d5f122cf4689cb
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59619595"
---
# <a name="transport-provider-and-mapi-spooler-operational-model"></a>Fournisseur de transport et modèle opérationnel du spooler MAPI

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
L’initialisation, le démarrage, le traitement, l’arrêt et la désinitialisation du fournisseur de transport sont effectués par une série d’appels dupooler MAPI au fournisseur de transport. Les appels sont séquencés comme suit :
  
1. Lepooler MAPI appelle la fonction [XPProviderInit,](xpproviderinit.md) transmet un objet de support, obtient l’objet fournisseur et vérifie que le fournisseur de transport et lepooler MAPI prend en charge une plage compatible de numéros de version MAPI. 
    
2. Lepooler MAPI appelle la méthode [IXPProvider::TransportLogon](ixpprovider-transportlogon.md) de l’interface [IXPProvider : IUnknown.](ixpprovideriunknown.md) Une session est établie entre lepooler MAPI et le fournisseur de transport avec les informations d’identification dans la section actuelle du profil. Le fournisseur de transport renvoie un objet d’accès. 
    
3. Lepooler MAPI appelle la [méthode IXPLogon::AddressTypes.](ixplogon-addresstypes.md) Le fournisseur de transport renvoie une liste des identificateurs uniques (IUD) et des types d’adresse de messagerie qu’il acceptera. 
    
4. Le fournisseur de transport appelle la méthode [IMAPISupport::ModifyStatusRow](imapisupport-modifystatusrow.md) pour créer sa ligne dans la table d’état MAPI. 
    
5. Lepooler MAPI appelle la méthode [IXPLogon::TransportNotify](ixplogon-transportnotify.md) pour activer la transmission et la réception des messages. 
    
6. Si le fournisseur de transport le demande dans son retour pour l’appel **TransportLogon,** lepooler MAPI appelle régulièrement la méthode [IXPLogon::Idle.](ixplogon-idle.md) Le traitement inactif est utile si le fournisseur de transport doit sondé le système de messagerie sous-jacent à la recherche de nouveaux messages ou effectuer d’autres tâches de faible priorité. 
    
7. Le fournisseur de transport et lepooler MAPI envoient et reçoivent des messages. Pour plus d’informations, [voir modèle de dépôt de message](message-submission-model.md) et modèle de réception de [message.](message-reception-model.md) Lepooler MAPI traite les demandes de transport et les appels sur les objets de support, de message et de pièce jointe.
    
8. Lepooler MAPI appelle la **méthode TransportNotify** pour désactiver la transmission et la réception des messages. 
    
9. Lepooler MAPI libère les objets d’accès et de fournisseur. Pour plus d’informations, voir la [méthode IXPProvider::Shutdown.](ixpprovider-shutdown.md) 
    

