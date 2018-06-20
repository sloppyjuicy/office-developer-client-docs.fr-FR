---
title: Inscription des identificateurs uniques de fournisseur de Service
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 964fceb4-8a1c-46c1-98e1-a325c9259f8b
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 80d2e4fd353f0746349563fd911e0af09a658b35
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19786983"
---
# <a name="registering-service-provider-unique-identifiers"></a>Inscription des identificateurs uniques de fournisseur de Service

  
  
**S’applique à**: Outlook 
  
Carnet d’adresses, banque de messages et les fournisseurs de transport permet d’un identificateur unique, appelé un [MAPIUID](mapiuid.md) pour enregistrer aux objets de différents types de service. Un **MAPIUID** est un identificateur de 16 octets qui contient un GUID. Vous pouvez créer un **MAPIUID** à l’aide de la procédure suivante : 
  
1. Définir une constante.
    
2. Appeler le Visual Studio*Create GUID** outil. 
    
Par exemple, un fournisseur de carnet d’adresses peut inclure la constante suivante dans un fichier d’en-tête pour définir un **MAPIUID**:
  
 `#define AB_UID_PROVIDER { 0Xe3, 0x3c, 0x67, 0xa0, \ 0xc8, 0x1f, 0x11, 0xce, \ 0xb2, 0xe4, 0x0, 0xaa, \ 0x0, 0x51, 0xe, 0x3b }`
  
 **Pour inscrire un MAPIUID si votre fournisseur est un fournisseur de magasin de message ou de carnet d’adresses**
  
1. Appelez [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md).
    
2. Inscrire un **MAPIUID** pour chaque ouverture de session d’objet que vous instanciez et incluez ce **MAPIUID** dans les premier 16 octets du membre **ab** de chaque identificateur d’entrée que vous créez. MAPI utilise des structures **MAPIUID** pour associer des objets à des fournisseurs de services. Lorsqu’un client appelle la méthode [IMAPISession::OpenEntry](imapisession-openentry.md) pour ouvrir un objet, MAPI examine la partie **MAPIUID** de l’identificateur d’entrée, l’associer à l’inscrits **MAPIUID**, pour déterminer l’objet d’ouverture de session doit recevoir l’ouvrir demande.
    
3. Si votre fournisseur est un type de transport, enregistrez une ou plusieurs structures **MAPIUID** lorsque MAPI appelle votre méthode **IXPLogon::AddressTypes** . MAPI utilise les structures **MAPIUID** enregistrés par des fournisseurs de transport pour affecter la responsabilité de la remise du message. 
    
Bien que les fournisseurs de services généralement enregistrement un seul **MAPIUID**, vous pouvez inscrire plusieurs structures **MAPIUID** . Si votre carnet d’adresses ou un message magasins fournisseur prend en charge plusieurs objets de l’ouverture de session, peut-être en permettant à un utilisateur pour ajouter plusieurs instances de votre fournisseur à leur profil, vous souhaitez implémenter une autre **MAPIUID** pour chaque objet d’ouverture de session. Il existe quelques autres raisons pour prendre en charge de plusieurs **MAPIUID**:
  
- À prendre en charge plusieurs versions de votre fournisseur et les identificateurs d’entrée doivent représenter la version appropriée. Affecter un autre **MAPIUID** pour chaque version. 
    
- Vous souhaitez faire la distinction entre les types d’objets que vous prenez en charge. Par exemple, un fournisseur de carnet d’adresses souhaiterez inscrire un **MAPIUID** à utiliser dans les identificateurs d’entrée de ses objets utilisateur de messagerie et un autre **MAPIUID** à utiliser pour les listes de distribution. 
    
Lorsqu’il existe plusieurs objets d’ouverture de session qui sont actifs simultanément, il est judicieux ont des structures **MAPIUID** uniques pour chacune d’elles. Cela permet d’augmenter la précision qui établit une correspondance avec les identificateurs d’entrée aux fournisseurs de services MAPI et enregistre un travail. Lorsque tous les objets d’ouverture de session a son propre identificateur unique, MAPI peut garantir que toute demande elle dirige vers un objet d’ouverture de session peut être gérés par l’objet. Lorsque vous partagez des structures **MAPIUID** objets d’ouverture de session, MAPI achemine la demande au premier objet identifié par l' **MAPIUID**d’ouverture de session. Si un de vos objets d’ouverture de session reçoit une demande qu’il ne peut pas traiter, car il ne gère pas l’identificateur d’entrée, transmettez la demande à votre objet d’ouverture de session suivant avant qu’une erreur.
  
## <a name="see-also"></a>Voir aussi



[L’implémentation du fournisseur de Service d’ouverture de session](implementing-service-provider-logon.md)

