---
title: Définition de l’ordre de transport
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 4a140ec3-9520-4119-a975-0fb6c1049967
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: dc1ead1b58ed92c67ffba888ee19b589eee6de3f
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59566688"
---
# <a name="setting-transport-order"></a>Définition de l’ordre de transport

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Lepooler MAPI attribue la responsabilité des messages sortants en fonction des types d’adresses et des identificateurs que les fournisseurs de transport déclarent qu’ils peuvent gérer. Les fournisseurs de transport publient une liste de types d’adresses et d’identificateurs pris en charge , stockés dans des structures **MAPIUID,** lorsque MAPI appelle leur méthode [IXPLogon::AddressTypes,](ixplogon-addresstypes.md) directement après l’ouverture de messagerie. Le type d’adresse d’un destinataire est stocké dans **sa propriété PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)).
  
L’inscription à un type d’adresse indique à MAPI que le fournisseur de transport peut remettre aux destinataires avec leur propriété **PR_ADDRTYPE** définie sur le type d’adresse enregistré. De même, l’inscription à **un MAPIUID** indique que le fournisseur de transport peut remettre à des destinataires représentés par des identificateurs d’entrée avec le **MAPIUID enregistré.**
  
La plupart des fournisseurs de transport s’inscrivent pour un ou plusieurs types d’adresses ; quelques inscrits **par MAPIUID**. Les fournisseurs de transport étroitement associés à un fournisseur de carnet d’adresses et qui comprennent son format d’identificateur d’entrée peuvent s’inscrire pour gérer les messages par **MAPIUID,** améliorant ainsi les performances. Ces fournisseurs de transport étroitement couplés peuvent extraire l’adresse e-mail du destinataire et d’autres informations nécessaires de l’identificateur d’entrée sans avoir à l’ouvrir avec un appel **IMAPISupport::OpenEntry.** 
  
MAPI maintient une commande pour les fournisseurs de transport, utilisée lorsque plusieurs fournisseurs de transport se sont inscrits pour le même type d’adresse ou **MAPIUID**. Vous pouvez remplacer cet ordre en appelant [IMsgServiceAdmin::MsgServiceTransportOrder](imsgserviceadmin-msgservicetransportorder.md) et en passant une liste triée des **MAPIUID** de tous les fournisseurs de transport actifs pointés par le paramètre  _lpUIDList_ : 
  
Pour récupérer une liste de tous les types d’adresses qui peuvent être gérés par l’un des fournisseurs de transport actifs, appelez [IMAPISession::EnumAdrTypes](imapisession-enumadrtypes.md). **EnumAdrTypes renvoie** un tableau de chaînes qui décrit les types d’adresses pris en charge par les fournisseurs de transport actifs dans la session active. 
  

