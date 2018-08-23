---
title: Suppression d’un destinataire
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f7495030-e3b8-4c7c-9e19-284ba820e846
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 03917ad52f1dc1ce4d0b59cd54fe33f58f352061
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22582944"
---
# <a name="deleting-a-recipient"></a><span data-ttu-id="2c850-103">Suppression d’un destinataire</span><span class="sxs-lookup"><span data-stu-id="2c850-103">Deleting a Recipient</span></span>

  
  
<span data-ttu-id="2c850-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2c850-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="2c850-105">**Pour supprimer une ou plusieurs entrées de carnet d’adresses d’un conteneur modifiable**</span><span class="sxs-lookup"><span data-stu-id="2c850-105">**To remove one or more address book entries from a modifiable container**</span></span>
  
- <span data-ttu-id="2c850-106">Appelez la méthode [IABContainer::DeleteEntries](iabcontainer-deleteentries.md) , en passant un tableau d’identificateurs d’entrée qui représentent les entrées de carnet d’adresses à supprimer.</span><span class="sxs-lookup"><span data-stu-id="2c850-106">Call the [IABContainer::DeleteEntries](iabcontainer-deleteentries.md) method, passing an array of entry identifiers that represent the address book entries to be deleted.</span></span> <span data-ttu-id="2c850-107">**DeleteEntries** peut renvoyer un avertissement MAPI_W_PARTIAL_COMPLETION se produit, pour indiquer qu’il n’a pas pu supprimer un ou plusieurs des entrées.</span><span class="sxs-lookup"><span data-stu-id="2c850-107">**DeleteEntries** can return a warning, MAPI_W_PARTIAL_COMPLETION, to indicate that it couldn't delete one or more of the entries.</span></span> <span data-ttu-id="2c850-108">Testez pour cette valeur de retour à la macro **HR_FAILED** et appeler la méthode de [IMAPIProp::GetLastError](imapiprop-getlasterror.md) du conteneur si plus d’informations sur le problème n’est nécessaire.</span><span class="sxs-lookup"><span data-stu-id="2c850-108">Test for this return value with the **HR_FAILED** macro and call the container's [IMAPIProp::GetLastError](imapiprop-getlasterror.md) method if more information about the problem is needed.</span></span> 
    
<span data-ttu-id="2c850-109">Lorsque vous maintenez un pointeur vers la structure [ADRENTRY](adrentry.md) d’une entrée supprimée dans le cache, vous serez toujours en mesure de récupérer les propriétés à l’aide de son identificateur d’entrée.</span><span class="sxs-lookup"><span data-stu-id="2c850-109">When you hold a pointer to a deleted entry's [ADRENTRY](adrentry.md) structure in your cache, you will still be able to retrieve properties using its entry identifier.</span></span> <span data-ttu-id="2c850-110">Il s’agit, car l’entrée est uniquement marquée pour suppression.</span><span class="sxs-lookup"><span data-stu-id="2c850-110">This is because the entry is only marked for deletion.</span></span> <span data-ttu-id="2c850-111">MAPI conserve un niveau d’accès à ces entrées marquées par sa conception.</span><span class="sxs-lookup"><span data-stu-id="2c850-111">MAPI maintains a level of access to these marked entries by design.</span></span> 
  

