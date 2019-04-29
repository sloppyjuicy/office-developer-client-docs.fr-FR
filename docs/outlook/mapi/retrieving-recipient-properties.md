---
title: Récupération des propriétés d’un destinataire
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 358f892b-54a7-4213-b3c0-94f28f99716f
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 38063cebe70b153decce6713ac5fc31d6916dbf6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426673"
---
# <a name="retrieving-recipient-properties"></a><span data-ttu-id="9e515-103">Récupération des propriétés d’un destinataire</span><span class="sxs-lookup"><span data-stu-id="9e515-103">Retrieving recipient properties</span></span>
  
<span data-ttu-id="9e515-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9e515-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
### <a name="to-access-one-or-more-properties-of-an-address-book-entry"></a><span data-ttu-id="9e515-105">Pour accéder à une ou plusieurs propriétés d'une entrée de carnet d'adresses</span><span class="sxs-lookup"><span data-stu-id="9e515-105">To access one or more properties of an address book entry</span></span>
  
1. <span data-ttu-id="9e515-106">Pour chaque entrée de carnet d'adresses qui vous intéresse, appelez [IAddrBook:: OpenEntry](iaddrbook-openentry.md), en transmettant l'identificateur d'entrée de l'utilisateur de messagerie cible ou de la liste de distribution.</span><span class="sxs-lookup"><span data-stu-id="9e515-106">For each address book entry of interest, call [IAddrBook::OpenEntry](iaddrbook-openentry.md), passing the entry identifier of the target messaging user or distribution list.</span></span>
    
2. <span data-ttu-id="9e515-107">Effectuez ensuite l'une des opérations suivantes:</span><span class="sxs-lookup"><span data-stu-id="9e515-107">Then do one of the following:</span></span>
    
   - <span data-ttu-id="9e515-108">Appelez la méthode [IMAPIProp:: GetProps](imapiprop-getprops.md) de la liste de distribution ou de l'utilisateur de messagerie pour chaque entrée de carnet d'adresses présentant un intérêt, avec une liste d'une ou plusieurs propriétés à récupérer.</span><span class="sxs-lookup"><span data-stu-id="9e515-108">Call the messaging user or distribution list's [IMAPIProp::GetProps](imapiprop-getprops.md) method for each address book entry of interest, with a list of the one or more properties to retrieve.</span></span> 
    
   - <span data-ttu-id="9e515-109">Appelez [IAddrBook::P reparerecips](iaddrbook-preparerecips.md), en transmettant une structure [ADRLIST](adrlist.md) qui contient toutes les propriétés de toutes les entrées de carnet d'adresses souhaitées.</span><span class="sxs-lookup"><span data-stu-id="9e515-109">Call [IAddrBook::PrepareRecips](iaddrbook-preparerecips.md), passing an [ADRLIST](adrlist.md) structure that holds all of the properties for all of the desired address book entries.</span></span> <span data-ttu-id="9e515-110">Étant donné qu'un appel à **PrepareRecips** peut retourner des informations pour plusieurs entrées de carnet d'adresses, il s'agit de la stratégie préférable lorsque vous vous intéressez à plusieurs destinataires.</span><span class="sxs-lookup"><span data-stu-id="9e515-110">Because one call to **PrepareRecips** can return information for multiple address book entries, it is the preferable strategy when you are interested in more than one recipient.</span></span> 
    

