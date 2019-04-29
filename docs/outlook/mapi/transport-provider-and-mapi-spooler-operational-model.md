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
ms.openlocfilehash: 5987111844f087801c63989b905992900ff6909c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426624"
---
# <a name="transport-provider-and-mapi-spooler-operational-model"></a>Fournisseur de transport et modèle opérationnel de spouleur MAPI

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
L'initialisation, le démarrage, le traitement, l'arrêt et la désinitialisation des fournisseurs de transport sont effectués par une série d'appels depuis le spouleur MAPI vers le fournisseur de transport. Les appels sont séquencés comme suit:
  
1. Le spouleur MAPI appelle la fonction [XPProviderInit](xpproviderinit.md) , transmet un objet de prise en charge, obtient l'objet fournisseur et vérifie que le fournisseur de transport et le spouleur MAPI prennent en charge une plage de numéros de version MAPI compatible. 
    
2. Le spouleur MAPI appelle la méthode [IXPProvider:: TransportLogon](ixpprovider-transportlogon.md) de l'interface [IXPProvider: IUnknown](ixpprovideriunknown.md) . Une session est établie entre le spouleur MAPI et le fournisseur de transport avec les informations d'identification dans la section actuelle du profil. Le fournisseur de transport renvoie un objet Logon. 
    
3. Le spouleur MAPI appelle la méthode [IXPLogon:: AddressTypes](ixplogon-addresstypes.md) . Le fournisseur de transport renvoie une liste des identificateurs uniques (UID) et des types d'adresses de messagerie qu'il accepte. 
    
4. Le fournisseur de transport appelle la méthode [IMAPISupport:: ModifyStatusRow](imapisupport-modifystatusrow.md) pour créer sa ligne dans la table d'État MAPI. 
    
5. Le spouleur MAPI appelle la méthode [IXPLogon:: TransportNotify](ixplogon-transportnotify.md) pour activer la transmission et la réception des messages. 
    
6. Si le fournisseur de transport le demande, le spouleur **** MAPI appelle régulièrement la méthode [IXPLogon:: Idle](ixplogon-idle.md) . Le traitement inActif est utile si le fournisseur de transport doit interroger le système de messagerie sous-jacent pour les nouveaux messages ou effectuer d'autres tâches de faible priorité. 
    
7. Le fournisseur de transport et le spouleur MAPI envoient et reçoivent les messages. Pour plus d'informations, voir modèle d' [envoi de messages](message-submission-model.md) et modèle de [réception des messages](message-reception-model.md). Les services de spouleur MAPI transportent les demandes et les appels sur les objets de support, de message et de pièce jointe.
    
8. Le spouleur MAPI appelle la méthode **TransportNotify** pour désactiver la transmission et la réception des messages. 
    
9. Le spouleur MAPI libère les objets Logon et Provider. Pour plus d'informations, reportez-vous à la méthode [IXPProvider:: Shutdown](ixpprovider-shutdown.md) . 
    

