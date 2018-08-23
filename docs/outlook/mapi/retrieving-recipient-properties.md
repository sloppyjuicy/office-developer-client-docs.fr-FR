---
title: Récupération des propriétés de destinataire
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 358f892b-54a7-4213-b3c0-94f28f99716f
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: a48c6a8e043062bc6b48e09934fded1dccb507b2
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22585436"
---
# <a name="retrieving-recipient-properties"></a>Récupération des propriétés de destinataire
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
### <a name="to-access-one-or-more-properties-of-an-address-book-entry"></a>Pour accéder à une ou plusieurs propriétés d’une entrée de carnet d’adresses
  
1. Pour chaque entrée de carnet d’adresse d’intérêt, appelez [IAddrBook::OpenEntry](iaddrbook-openentry.md), en passant l’identificateur d’entrée de l’utilisateur ou liste de distribution de messagerie cible.
    
2. Puis effectuez l’une des options suivantes :
    
   - Appelez la méthode [IMAPIProp::GetProps](imapiprop-getprops.md) de liste de distribution ou de l’utilisateur de messagerie pour chaque entrée de carnet d’adresse d’intérêt, avec une liste des propriétés pour récupérer un ou plusieurs. 
    
   - Appelez [IAddrBook::PrepareRecips](iaddrbook-preparerecips.md), en passant une structure [ADRLIST](adrlist.md) qui conserve toutes les propriétés de toutes les entrées de carnet d’adresses de votre choix. Un appel à **PrepareRecips** peut retourner des informations d’adresse plusieurs entrées de carnet de, il est la stratégie préférable lorsque vous êtes intéressé par plusieurs destinataires. 
    

