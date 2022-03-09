---
title: Récupération des propriétés d’un destinataire
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 358f892b-54a7-4213-b3c0-94f28f99716f
ms.openlocfilehash: 7be305fb5f5d2f5909254c157891262f56105b4f
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63371442"
---
# <a name="retrieving-recipient-properties"></a>Récupération des propriétés d’un destinataire
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
### <a name="to-access-one-or-more-properties-of-an-address-book-entry"></a>Pour accéder à une ou plusieurs propriétés d’une entrée de carnet d’adresses
  
1. Pour chaque entrée de carnet d’adresses qui vous intéresse, appelez [IAddrBook::OpenEntry](iaddrbook-openentry.md), en passant l’identificateur d’entrée de l’utilisateur de messagerie cible ou de la liste de distribution.
    
2. Ensuite, faites l’une des choses suivantes :
    
   - Appelez la méthode [IMAPIProp::GetProps](imapiprop-getprops.md) de l’utilisateur de messagerie ou de la liste de distribution pour chaque entrée de carnet d’adresses qui vous intéresse, avec une liste des propriétés à récupérer. 
    
   - Appelez [IAddrBook::P repareRecips](iaddrbook-preparerecips.md), en passant une structure [ADRLIST](adrlist.md) qui contient toutes les propriétés de toutes les entrées de carnet d’adresses souhaitées. Étant donné qu’un appel à **PrepareRecips** peut renvoyer des informations pour plusieurs entrées de carnet d’adresses, il est préférable de mettre en place une stratégie lorsque plusieurs destinataires vous intéressent. 
    

