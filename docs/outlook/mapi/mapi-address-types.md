---
title: Types d’adresse MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: eee97982-29be-4dcf-ae11-8a38f0080ea7
ms.openlocfilehash: ddb4c540b5e78b9b3fc4934b18e5e36132658cd7
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63371834"
---
# <a name="mapi-address-types"></a>Types d’adresse MAPI

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Chaque utilisateur de messagerie est associé à un type d’adresse, une chaîne de caractères décrivant le format de l’adresse de l’utilisateur qui est stocké dans la propriété **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)). Les types d’adresses sont map to address formats. Autrement dit, en regardant le type d’adresse d’un destinataire, les applications clientes peuvent déterminer comment mettre en forme une adresse appropriée pour le destinataire. 
  
Par exemple, le  `SMTP` type d’adresse spécifie l’adresse Internet standard : 
  
 `username@companyname.com.`
  
De plus, le `EX` type d’adresse spécifie une Exchange Server de l’adresse. 
  
Toutes les entrées de carnet d’adresses doivent avoir un type d’adresse valide. Les clients exigent que leurs utilisateurs spécifient un type d’adresse lors de la création d’un type de destinataire personnalisé non pris en compte par le fournisseur de carnet d’adresses. Pour les entrées qu’ils prendre en charge, les fournisseurs de carnets d’adresses doivent fournir des types d’adresses valides. 
  
MAPI définit un seul type d’adresse : MAPIPDL, qui signifie liste de distribution personnelle.
  
Pour obtenir la liste des types d’adresses pris en charge par tous les fournisseurs de transport dans la session, les applications clientes appellent la méthode **IMAPISession::EnumAdrTypes** . Pour plus d’informations, [voir IMAPISession::EnumAdrTypes](imapisession-enumadrtypes.md).
  

