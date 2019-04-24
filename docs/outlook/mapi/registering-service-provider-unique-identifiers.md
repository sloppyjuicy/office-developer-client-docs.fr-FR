---
title: Inscription des identificateurs uniques des fournisseurs de services
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 964fceb4-8a1c-46c1-98e1-a325c9259f8b
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 9f4acbb06f85a88a6c057da263ae95e09f72e0bb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328398"
---
# <a name="registering-service-provider-unique-identifiers"></a>Inscription des identificateurs uniques des fournisseurs de services

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Le carnet d'adresses, la Banque de messages et les fournisseurs de transport utilisent un identificateur unique appelé [MAPIUID](mapiuid.md) pour s'inscrire aux objets de service de différents types. Un **MAPIUID** est un identificateur de 16 octets qui contient un GUID. Vous pouvez créer un **MAPIUID** à l'aide de la procédure suivante: 
  
1. Définissez une constante.
    
2. Appelez l'outil de*création de GUID** Visual Studio. 
    
Par exemple, un fournisseur de carnet d'adresses peut inclure la constante suivante dans un fichier d'en-tête pour définir un **MAPIUID**:
  
 `#define AB_UID_PROVIDER { 0Xe3, 0x3c, 0x67, 0xa0, \ 0xc8, 0x1f, 0x11, 0xce, \ 0xb2, 0xe4, 0x0, 0xaa, \ 0x0, 0x51, 0xe, 0x3b }`
  
 **Pour enregistrer un MAPIUID si votre fournisseur est un carnet d'adresses ou un fournisseur de banque de messages**
  
1. Appelez [IMAPISupport:: SetProviderUID](imapisupport-setprovideruid.md).
    
2. Inscrivez un **MAPIUID** pour chaque objet d'ouverture de session que vous instanciez et incluez cette **MAPIUID** dans les 16 premiers octets du membre **AB** de chaque identificateur d'entrée que vous créez. MAPI utilise des structures **MAPIUID** pour associer des objets à des fournisseurs de services. Lorsqu'un client appelle la méthode [IMAPISession:: OpenEntry](imapisession-openentry.md) pour ouvrir un objet, MAPI examine la partie **MAPIUID** de l'identificateur d'entrée, en la comparant à la **MAPIUID**enregistrée, afin de déterminer l'objet d'ouverture de session qui doit recevoir l'élément Open. sollicit.
    
3. Si votre fournisseur est un transport, enregistrez une ou plusieurs structures **MAPIUID** lorsque MAPI appelle votre méthode **IXPLogon:: AddressTypes** . MAPI utilise les structures **MAPIUID** enregistrées par les fournisseurs de transport pour affecter la responsabilité de la remise des messages. 
    
Bien que les fournisseurs de services inscrivent généralement un seul **MAPIUID**, vous pouvez enregistrer plusieurs structures **MAPIUID** . Si votre carnet d'adresses ou votre fournisseur de banque de messages prend en charge plusieurs objets d'ouverture de session, par exemple, en permettant à un utilisateur d'ajouter plusieurs instances de votre fournisseur à son profil, vous pouvez implémenter un autre **MAPIUID** pour chaque objet d'ouverture de session. Il existe d'autres raisons de prendre en charge plusieurs **MAPIUID**:
  
- Vous devez prendre en charge plusieurs versions de votre fournisseur et les identificateurs d'entrée doivent représenter la version appropriée. Affectez une autre **MAPIUID** pour chaque version. 
    
- Vous souhaitez faire la distinction entre les types d'objets que vous prenez en charge. Par exemple, un fournisseur de carnet d'adresses peut souhaiter enregistrer un **MAPIUID** à utiliser dans les identificateurs d'entrée de ses objets utilisateur de messagerie et un autre **MAPIUID** à utiliser pour les listes de distribution. 
    
Lorsque plusieurs objets d'ouverture de session sont actifs simultanément, il est logique d'avoir des structures **MAPIUID** uniques pour chacune d'elles. Cela augmente la précision avec laquelle MAPI établit une correspondance entre les identificateurs d'entrée et les fournisseurs de services et enregistre le travail. Lorsque chaque objet Logon a son propre identificateur unique, MAPI peut garantir que toute requête qu'il dirige vers un objet Logon peut être gérée par cet objet. Lorsque les objets d'ouverture de session partagent des structures **MAPIUID** , MAPI achemine la demande vers le premier objet ouverture de session qui est identifié par l' **MAPIUID**. Si l'un de vos objets d'ouverture de session reçoit une demande qu'il ne peut pas traiter, car il ne gère pas l'identificateur d'entrée, transmettez la demande à votre prochain objet d'ouverture de session avant de renvoyer une erreur.
  
## <a name="see-also"></a>Voir aussi



[Implémentation de la connexion au fournisseur de services](implementing-service-provider-logon.md)

