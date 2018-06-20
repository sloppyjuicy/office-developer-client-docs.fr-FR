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
# <a name="retrieving-recipient-properties"></a><span data-ttu-id="5395c-103">Récupération des propriétés de destinataire</span><span class="sxs-lookup"><span data-stu-id="5395c-103">Retrieving recipient properties</span></span>
  
<span data-ttu-id="5395c-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="5395c-104">**Applies to**: Outlook</span></span> 
  
### <a name="to-access-one-or-more-properties-of-an-address-book-entry"></a><span data-ttu-id="5395c-105">Pour accéder à une ou plusieurs propriétés d’une entrée de carnet d’adresses</span><span class="sxs-lookup"><span data-stu-id="5395c-105">To access one or more properties of an address book entry</span></span>
  
1. <span data-ttu-id="5395c-106">Pour chaque entrée de carnet d’adresse d’intérêt, appelez [IAddrBook::OpenEntry](iaddrbook-openentry.md), en passant l’identificateur d’entrée de l’utilisateur ou liste de distribution de messagerie cible.</span><span class="sxs-lookup"><span data-stu-id="5395c-106">For each address book entry of interest, call [IAddrBook::OpenEntry](iaddrbook-openentry.md), passing the entry identifier of the target messaging user or distribution list.</span></span>
    
2. <span data-ttu-id="5395c-107">Puis effectuez l’une des options suivantes :</span><span class="sxs-lookup"><span data-stu-id="5395c-107">Then do one of the following:</span></span>
    
   - <span data-ttu-id="5395c-108">Appelez la méthode [IMAPIProp::GetProps](imapiprop-getprops.md) de liste de distribution ou de l’utilisateur de messagerie pour chaque entrée de carnet d’adresse d’intérêt, avec une liste des propriétés pour récupérer un ou plusieurs.</span><span class="sxs-lookup"><span data-stu-id="5395c-108">Call the messaging user or distribution list's [IMAPIProp::GetProps](imapiprop-getprops.md) method for each address book entry of interest, with a list of the one or more properties to retrieve.</span></span> 
    
   - <span data-ttu-id="5395c-109">Appelez [IAddrBook::PrepareRecips](iaddrbook-preparerecips.md), en passant une structure [ADRLIST](adrlist.md) qui conserve toutes les propriétés de toutes les entrées de carnet d’adresses de votre choix.</span><span class="sxs-lookup"><span data-stu-id="5395c-109">Call [IAddrBook::PrepareRecips](iaddrbook-preparerecips.md), passing an [ADRLIST](adrlist.md) structure that holds all of the properties for all of the desired address book entries.</span></span> <span data-ttu-id="5395c-110">Un appel à **PrepareRecips** peut retourner des informations d’adresse plusieurs entrées de carnet de, il est la stratégie préférable lorsque vous êtes intéressé par plusieurs destinataires.</span><span class="sxs-lookup"><span data-stu-id="5395c-110">Because one call to **PrepareRecips** can return information for multiple address book entries, it is the preferable strategy when you are interested in more than one recipient.</span></span> 
    

