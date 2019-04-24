---
title: Récupération des propriétés d’un destinataire
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 358f892b-54a7-4213-b3c0-94f28f99716f
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 38063cebe70b153decce6713ac5fc31d6916dbf6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32279593"
---
# <a name="retrieving-recipient-properties"></a>Récupération des propriétés d’un destinataire
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
### <a name="to-access-one-or-more-properties-of-an-address-book-entry"></a>Pour accéder à une ou plusieurs propriétés d'une entrée de carnet d'adresses
  
1. Pour chaque entrée de carnet d'adresses qui vous intéresse, appelez [IAddrBook:: OpenEntry](iaddrbook-openentry.md), en transmettant l'identificateur d'entrée de l'utilisateur de messagerie cible ou de la liste de distribution.
    
2. Effectuez ensuite l'une des opérations suivantes:
    
   - Appelez la méthode [IMAPIProp:: GetProps](imapiprop-getprops.md) de la liste de distribution ou de l'utilisateur de messagerie pour chaque entrée de carnet d'adresses présentant un intérêt, avec une liste d'une ou plusieurs propriétés à récupérer. 
    
   - Appelez [IAddrBook::P reparerecips](iaddrbook-preparerecips.md), en transmettant une structure [ADRLIST](adrlist.md) qui contient toutes les propriétés de toutes les entrées de carnet d'adresses souhaitées. Étant donné qu'un appel à **PrepareRecips** peut retourner des informations pour plusieurs entrées de carnet d'adresses, il s'agit de la stratégie préférable lorsque vous vous intéressez à plusieurs destinataires. 
    

