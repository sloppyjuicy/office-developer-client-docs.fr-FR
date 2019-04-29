---
title: Définition de l'ordre de transport
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4a140ec3-9520-4119-a975-0fb6c1049967
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: efa2d6ab9edbd50634093b5185ef9036689f1379
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433597"
---
# <a name="setting-transport-order"></a>Définition de l'ordre de transport

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Le spouleur MAPI affecte les responsabilités pour les messages sortants en fonction des types d'adresses et des identificateurs que les fournisseurs de transport déclare qu'ils peuvent gérer. Les fournisseurs de transport publient une liste de types d'adresses et d'identificateurs pris en charge, stockés dans les structures **MAPIUID** , lorsque MAPI appelle la méthode [IXPLogon:: AddressTypes](ixplogon-addresstypes.md) , directement après l'ouverture de session. Le type d'adresse d'un destinataire est stocké dans sa propriété **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)).
  
L'enregistrement pour un type d'adresse indique à MAPI que le fournisseur de transport peut fournir aux destinataires dont la propriété **PR_ADDRTYPE** est définie sur le type d'adresse enregistré. De même, l'enregistrement pour un **MAPIUID** indique que le fournisseur de transport peut fournir aux destinataires représentés par des identificateurs d'entrée avec le **MAPIUID**enregistré.
  
La plupart des fournisseurs de transport s'inscrivent pour un ou plusieurs types d'adresses; peu de registres par **MAPIUID**. Les fournisseurs de transport qui sont étroitement associés à un fournisseur de carnet d'adresses et qui comprennent son format d'identificateur d'entrée peuvent s'enregistrer pour gérer les messages par **MAPIUID**, ce qui améliore les performances. Ces fournisseurs de transport étroitement couplés peuvent extraire l'adresse de messagerie du destinataire et d'autres informations nécessaires de l'identificateur d'entrée sans avoir à l'ouvrir avec un appel **IMAPISupport:: OpenEntry** . 
  
MAPI gère une commande pour les fournisseurs de transport, utilisée lorsque plusieurs fournisseurs de transport ont été inscrits pour le même type d'adresse ou **MAPIUID**. Vous pouvez remplacer cette commande en appelant [IMsgServiceAdmin:: MsgServiceTransportOrder](imsgserviceadmin-msgservicetransportorder.md) et en passant une liste triée des **MAPIUID**s de tous les fournisseurs de transport actifs vers lesquels pointe le paramètre _lpUIDList_ : 
  
Pour récupérer la liste de tous les types d'adresses pouvant être gérés par l'un des fournisseurs de transport actifs, appelez [IMAPISession:: EnumAdrTypes](imapisession-enumadrtypes.md). **EnumAdrTypes** renvoie un tableau de chaînes qui décrit les types d'adresses pris en charge par les fournisseurs de transport qui sont actifs dans la session en cours. 
  

