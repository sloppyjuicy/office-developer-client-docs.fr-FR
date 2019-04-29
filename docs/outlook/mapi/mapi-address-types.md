---
title: Types d'adresses MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: eee97982-29be-4dcf-ae11-8a38f0080ea7
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: b0ff4ecff7a6e834f1e017adc11244657896db03
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405435"
---
# <a name="mapi-address-types"></a>Types d'adresses MAPI

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Chaque utilisateur de messagerie est associé à un type d'adresse, une chaîne de caractères décrivant le format de l'adresse de l'utilisateur qui est stockée dans la propriété **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)). Les types d'adresses correspondent aux formats d'adresse. En regardant le type d'adresse d'un destinataire, les applications clientes peuvent déterminer comment mettre en forme une adresse appropriée pour le destinataire. 
  
Par exemple, le `SMTP` type d'adresse spécifie l'adresse Internet standard: 
  
 `username@companyname.com.`
  
Et le `EX` type d'adresse spécifie une adresse de serveur Exchange. 
  
Toutes les entrées de carnet d'adresses doivent avoir un type d'adresse valide. Les clients exigent que leurs utilisateurs spécifient un type d'adresse lors de la création d'un type de destinataire personnalisé non pris en charge par le fournisseur de carnet d'adresses. Pour les entrées qu'ils prennent en charge, les fournisseurs de carnet d'adresses doivent fournir des types d'adresses valides. 
  
MAPI définit un seul type d'adresse: MAPIPDL, qui correspond à la liste de distribution personnelle.
  
Pour obtenir la liste des types d'adresses pris en charge par tous les fournisseurs de transport dans la session, les applications clientes appellent la méthode **IMAPISession:: EnumAdrTypes** . Pour plus d'informations, voir [IMAPISession:: EnumAdrTypes](imapisession-enumadrtypes.md).
  

