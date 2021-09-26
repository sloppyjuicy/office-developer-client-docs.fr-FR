---
title: Récupération des propriétés d’un destinataire
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 358f892b-54a7-4213-b3c0-94f28f99716f
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: ecf340bcf63048ad8d29ba411aa3553e4890bf78
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59599115"
---
# <a name="retrieving-recipient-properties"></a>Récupération des propriétés d’un destinataire
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
### <a name="to-access-one-or-more-properties-of-an-address-book-entry"></a>Pour accéder à une ou plusieurs propriétés d’une entrée de carnet d’adresses
  
1. Pour chaque entrée de carnet d’adresses qui vous intéresse, appelez [IAddrBook::OpenEntry](iaddrbook-openentry.md), en passant l’identificateur d’entrée de l’utilisateur de messagerie cible ou de la liste de distribution.
    
2. Ensuite, faites l’une des choses suivantes :
    
   - Appelez la méthode [IMAPIProp::GetProps](imapiprop-getprops.md) de l’utilisateur de messagerie ou de la liste de distribution pour chaque entrée de carnet d’adresses qui vous intéresse, avec une liste des propriétés à récupérer. 
    
   - Appelez [IAddrBook::P repareRecips](iaddrbook-preparerecips.md), en passant une structure [ADRLIST](adrlist.md) qui contient toutes les propriétés de toutes les entrées de carnet d’adresses souhaitées. Étant donné qu’un appel à **PrepareRecips** peut renvoyer des informations pour plusieurs entrées de carnet d’adresses, il s’agit de la stratégie préférable lorsque vous êtes intéressé par plusieurs destinataires. 
    

