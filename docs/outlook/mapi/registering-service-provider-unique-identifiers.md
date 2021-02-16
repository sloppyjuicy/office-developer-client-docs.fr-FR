---
title: Inscription des identificateurs uniques du fournisseur de services
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 964fceb4-8a1c-46c1-98e1-a325c9259f8b
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 9f4acbb06f85a88a6c057da263ae95e09f72e0bb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410174"
---
# <a name="registering-service-provider-unique-identifiers"></a>Inscription des identificateurs uniques du fournisseur de services

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Les fournisseurs de carnet d’adresses, de magasin de messages et de transport utilisent un identificateur unique appelé [MAPIUID](mapiuid.md) pour s’inscrire aux objets de service de différents types. **MapIUID est** un identificateur de 16 byte qui contient un GUID. Vous pouvez créer un **MAPIUID** à l’aide de la procédure suivante : 
  
1. Définissez une constante.
    
2. Invoke the Visual Studio *Create GUID** tool. 
    
Par exemple, un fournisseur de carnet d’adresses peut inclure la constante suivante dans un fichier d’en-tête pour définir un **MAPIUID**:
  
 `#define AB_UID_PROVIDER { 0Xe3, 0x3c, 0x67, 0xa0, \ 0xc8, 0x1f, 0x11, 0xce, \ 0xb2, 0xe4, 0x0, 0xaa, \ 0x0, 0x51, 0xe, 0x3b }`
  
 **Pour inscrire un MAPIUID si votre fournisseur est un fournisseur de carnet d’adresses ou de magasin de messages**
  
1. Appelez [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md).
    
2. Inscrivez un **MAPIUID** pour chaque objet d’inscription que vous inséziez et incluez ce **MAPIUID** dans les 16 premiers octets du membre **ab** de chaque identificateur d’entrée que vous créez. MAPI utilise des structures **MAPIUID** pour associer des objets à des fournisseurs de services. Lorsqu’un client appelle la méthode [IMAPISession::OpenEntry](imapisession-openentry.md) pour ouvrir un objet, MAPI examine la partie **MAPIUID** de l’identificateur d’entrée, en la faisant correspondre à l’identificateur **MAPIUID** enregistré, pour déterminer quel objet d’ouverture doit recevoir la demande d’ouverture.
    
3. Si votre fournisseur est un transport, inscrivez une ou plusieurs structures **MAPIUID** lorsque MAPI appelle votre **méthode IXPLogon::AddressTypes.** MAPI utilise les structures **MAPIUID** enregistrées par les fournisseurs de transport pour attribuer la responsabilité de la remise des messages. 
    
Bien que les fournisseurs de services enregistrent généralement un **seul MAPIUID,** vous pouvez inscrire plusieurs structures **MAPIUID.** Si votre carnet d’adresses ou votre fournisseur de magasins de messages prend en charge plusieurs objets d’ouverture de page, par exemple en permettant à un utilisateur d’ajouter plusieurs instances de votre fournisseur à son profil, vous pouvez implémenter un **MAPIUID** différent pour chaque objet d’ouverture de page. Il existe quelques autres raisons de prendre en charge plusieurs **MAPIUID**:
  
- Vous devez prendre en charge plusieurs versions de votre fournisseur et les identificateurs d’entrée doivent représenter la version appropriée. Affectez un **MAPIUID différent** pour chaque version. 
    
- Vous souhaitez faire la distinction entre les types d’objets que vous prendrez en charge. Par exemple, un fournisseur de carnet d’adresses peut inscrire un **MAPIUID** à utiliser dans les identificateurs d’entrée de ses objets utilisateur de messagerie et un **autre MAPIUID** à utiliser pour les listes de distribution. 
    
Lorsqu’il existe plusieurs objets de session qui sont actifs simultanément, il est logique d’avoir des structures **MAPIUID** uniques pour chacun d’eux. Cela augmente la précision avec laquelle MAPI fait la correspondance entre les identificateurs d’entrée et les fournisseurs de services et enregistre du travail. Lorsque chaque objet d' logon possède son propre identificateur unique, MAPI peut garantir que toute demande qu’il a route vers un objet d’logon peut être gérée par cet objet. Lorsque des objets d' logon partagent des structures **MAPIUID,** MAPI a pour effet d’approvisionnement la demande vers le premier objet d' logon qui est identifié par **mapIUID**. Si l’un de vos objets d’inscription reçoit une demande qu’il ne peut pas traiter car elle ne gère pas l’identificateur d’entrée, passez la demande à votre prochain objet d’inscription avant de renvoyer une erreur.
  
## <a name="see-also"></a>Voir aussi



[Mise en œuvre de l’logo du fournisseur de services](implementing-service-provider-logon.md)

