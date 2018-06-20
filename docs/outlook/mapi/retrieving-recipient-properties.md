---
title: Récupération des propriétés de destinataire
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 358f892b-54a7-4213-b3c0-94f28f99716f
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: a7bdcf133b8b2b5d8eb906cc0f5b5803838e27a3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787008"
---
# <a name="retrieving-recipient-properties"></a>Récupération des propriétés de destinataire
  
**S’applique à**: Outlook 
  
### <a name="to-access-one-or-more-properties-of-an-address-book-entry"></a>Pour accéder à une ou plusieurs propriétés d’une entrée de carnet d’adresses
  
1. Pour chaque entrée de carnet d’adresse d’intérêt, appelez [IAddrBook::OpenEntry](iaddrbook-openentry.md), en passant l’identificateur d’entrée de l’utilisateur ou liste de distribution de messagerie cible.
    
2. Puis effectuez l’une des options suivantes :
    
   - Appelez la méthode [IMAPIProp::GetProps](imapiprop-getprops.md) de liste de distribution ou de l’utilisateur de messagerie pour chaque entrée de carnet d’adresse d’intérêt, avec une liste des propriétés pour récupérer un ou plusieurs. 
    
   - Appelez [IAddrBook::PrepareRecips](iaddrbook-preparerecips.md), en passant une structure [ADRLIST](adrlist.md) qui conserve toutes les propriétés de toutes les entrées de carnet d’adresses de votre choix. Un appel à **PrepareRecips** peut retourner des informations d’adresse plusieurs entrées de carnet de, il est la stratégie préférable lorsque vous êtes intéressé par plusieurs destinataires. 
    

