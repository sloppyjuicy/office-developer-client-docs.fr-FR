---
title: Ordre de Transport de paramètre
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4a140ec3-9520-4119-a975-0fb6c1049967
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 71d7ebf2bc8c7bbf3b5ee6ce60959fdeee79abe3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787141"
---
# <a name="setting-transport-order"></a>Ordre de Transport de paramètre

  
  
**S’applique à**: Outlook 
  
Le spouleur MAPI attribue la responsabilité pour les messages sortants en fonction des types d’adresses et identificateurs de fournisseurs de transport déclarer qu’ils peuvent gérer. Fournisseurs de transport publient une liste des types d’adresse pris en charge et les identificateurs, stockées dans des structures **MAPIUID** — lorsque MAPI appelle leur méthode [IXPLogon::AddressTypes](ixplogon-addresstypes.md) , directement après l’ouverture de session. Type d’adresse d’un destinataire est stocké dans sa propriété **TYPEADR_PR** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)).
  
Inscription pour un type d’adresse indique à MAPI que le fournisseur de transport peut remettre aux destinataires dont la propriété **TYPEADR_PR** définie sur le type d’adresse enregistrée. De même, l’enregistrement pour un **MAPIUID** indique que le fournisseur de transport peut remettre à des destinataires qui sont représentées par les identificateurs d’entrée avec la inscrits **MAPIUID**.
  
La plupart des fournisseurs de transport s’inscrire pour un ou plusieurs types d’adresses ; peu inscrire par **MAPIUID**. Fournisseurs de transport qui sont étroitement liés à un fournisseur de carnet d’adresses et de comprennent son format d’identificateur d’entrée peuvent s’inscrire pour gérer les messages par **MAPIUID**, ce qui améliore les performances. Ces fournisseurs de transport étroitement couplés extraire adresse de messagerie du destinataire et d’autres informations nécessaires à partir de l’identificateur d’entrée sans avoir à ouvrir avec un appel **IMAPISupport::OpenEntry** . 
  
MAPI gère une commande pour les fournisseurs de transport, utilisée lorsque plusieurs fournisseurs de transport ont enregistré pour le même type d’adresse ou **MAPIUID**. Vous pouvez remplacer cet ordre en appelant [IMsgServiceAdmin::MsgServiceTransportOrder](imsgserviceadmin-msgservicetransportorder.md) et en transmettant une liste triée des s **MAPIUID**de tous les fournisseurs de transport actif vers laquelle pointe le paramètre _lpUIDList_ . : 
  
Pour récupérer une liste de tous les types d’adresses qui peuvent être gérés par un des fournisseurs de transport actif, appelez [IMAPISession::EnumAdrTypes](imapisession-enumadrtypes.md). **EnumAdrTypes** renvoie un tableau de chaînes qui décrit les types d’adresse pris en charge par les fournisseurs de transport qui sont actifs dans la session active. 
  

