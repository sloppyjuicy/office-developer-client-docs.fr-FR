---
title: Fournisseur de transport et modèle opérationnel de spouleur MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b0f8d8f0-fed7-4a7c-bc40-e935f159591d
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 26d9982248fde015a584eb79cc248bafc5afc6bb
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22594032"
---
# <a name="transport-provider-and-mapi-spooler-operational-model"></a>Fournisseur de transport et modèle opérationnel de spouleur MAPI

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Initialisation de fournisseur de transport, démarrage, traitement, l’arrêt et deinitialization sont effectuées par une série d’appels du spouleur MAPI vers le fournisseur de transport. Les appels sont classés comme suit :
  
1. Le spouleur MAPI appelle la fonction [XPProviderInit](xpproviderinit.md) , passe un objet de prise en charge, obtient l’objet de fournisseur et vérifie que le fournisseur de transport et le spouleur MAPI prennent en charge les numéros de version une plage compatible de MAPI. 
    
2. Le spouleur MAPI appelle la méthode [IXPProvider::TransportLogon](ixpprovider-transportlogon.md) de la [IXPProvider : IUnknown](ixpprovideriunknown.md) interface. Une session est établie entre le spouleur MAPI et le fournisseur de transport avec les informations d’identification dans la section du profil actuelle. Le fournisseur de transport renvoie un objet d’ouverture de session. 
    
3. Le spouleur MAPI appelle la méthode [IXPLogon::AddressTypes](ixplogon-addresstypes.md) . Le fournisseur de transport renvoie une liste des identificateurs uniques (UID) et des types d’adresse de messagerie qu’il accepte. 
    
4. Le fournisseur de transport appelle la méthode [IMAPISupport::ModifyStatusRow](imapisupport-modifystatusrow.md) pour créer une ligne dans la table d’état MAPI. 
    
5. Le spouleur MAPI appelle la méthode [IXPLogon::TransportNotify](ixplogon-transportnotify.md) pour activer la réception et transmission de message. 
    
6. Si vous avez demandé par le fournisseur de transport dans son retour pour l’appel de **TransportLogon** , le spouleur MAPI appelle régulièrement la méthode [IXPLogon::Idle](ixplogon-idle.md) . Traitement inactif est utile si le fournisseur de transport doit interroger le système de messagerie sous-jacent pour les nouveaux messages ou effectuer d’autres tâches de priorité basse. 
    
7. Le spouleur MAPI et le fournisseur de transport envoyer et recevoir des messages. Pour plus d’informations, voir [Modèle d’envoi de Message](message-submission-model.md) et le [Modèle de réception de messages](message-reception-model.md). Le spouleur MAPI de demandes de transport et appelle sur les objets de prise en charge, le message et des pièces jointes.
    
8. Le spouleur MAPI appelle la méthode **TransportNotify** pour désactiver la réception et transmission de message. 
    
9. Le spouleur MAPI libère les objets d’ouverture de session et le fournisseur. Pour plus d’informations, voir la méthode [IXPProvider::Shutdown](ixpprovider-shutdown.md) . 
    

