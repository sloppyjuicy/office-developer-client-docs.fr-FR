---
title: Types d’adresses MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: eee97982-29be-4dcf-ae11-8a38f0080ea7
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 20eb429b2574f67e8b28ae96eeb96f42840123d0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784558"
---
# <a name="mapi-address-types"></a>Types d’adresses MAPI

  
  
**S’applique à**: Outlook 
  
Chaque utilisateur de messagerie est associé à un type d’adresse, une chaîne de caractères décrivant le format d’adresse de l’utilisateur qui est stocké dans la propriété **TYPEADR_PR** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)). Mappent les types d’adresses pour les formats d’adresse. Autrement dit, en examinant le type d’adresse d’un destinataire, applications clientes peuvent déterminer comment mettre en forme une adresse appropriée pour le destinataire. 
  
Par exemple, le `SMTP` type d’adresse spécifie l’adresse Internet standard : 
  
 `username@companyname.com.`
  
Et la `EX` type d’adresse spécifie une adresse de serveur Exchange. 
  
Toutes les entrées de carnet d’adresses doivent avoir un type d’adresse valide. Ils ont besoin de leurs utilisateurs spécifier un type d’adresse lors de la création d’un type de destinataire personnalisé non pris en charge par le fournisseur de carnet d’adresses. Les entrées prises en charge, les fournisseurs de carnet d’adresses sont requis pour fournir des types d’adresses. 
  
MAPI définit le type d’une seule adresse : MAPIPDL, ce qui signifie pour une liste de distribution personnelle.
  
Pour obtenir une liste des types d’adresse pris en charge par tous les fournisseurs de transport dans la session, les applications clientes appellent la méthode **IMAPISession::EnumAdrTypes** . Pour plus d’informations, voir [IMAPISession::EnumAdrTypes](imapisession-enumadrtypes.md).
  

