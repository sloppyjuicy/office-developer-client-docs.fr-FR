---
title: Suppression d'un destinataire
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f7495030-e3b8-4c7c-9e19-284ba820e846
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: bd01c66d9fff7c94ffb1ce9f956f1951bc482020
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316813"
---
# <a name="deleting-a-recipient"></a><span data-ttu-id="fc714-103">Suppression d'un destinataire</span><span class="sxs-lookup"><span data-stu-id="fc714-103">Deleting a Recipient</span></span>

  
  
<span data-ttu-id="fc714-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fc714-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="fc714-105">**Pour supprimer une ou plusieurs entrées de carnet d'adresses d'un conteneur modifiable**</span><span class="sxs-lookup"><span data-stu-id="fc714-105">**To remove one or more address book entries from a modifiable container**</span></span>
  
- <span data-ttu-id="fc714-106">Appelez la méthode [IABContainer::D eleteentries](iabcontainer-deleteentries.md) , en passant un tableau d'identificateurs d'entrée qui représentent les entrées de carnet d'adresses à supprimer.</span><span class="sxs-lookup"><span data-stu-id="fc714-106">Call the [IABContainer::DeleteEntries](iabcontainer-deleteentries.md) method, passing an array of entry identifiers that represent the address book entries to be deleted.</span></span> <span data-ttu-id="fc714-107">**DeleteEntries** peut renvoyer un avertissement, MAPI_W_PARTIAL_COMPLETION, pour indiquer qu'il n'a pas pu supprimer une ou plusieurs entrées.</span><span class="sxs-lookup"><span data-stu-id="fc714-107">**DeleteEntries** can return a warning, MAPI_W_PARTIAL_COMPLETION, to indicate that it couldn't delete one or more of the entries.</span></span> <span data-ttu-id="fc714-108">Testez cette valeur de retour avec la macro **HR_FAILED** et appelez la méthode [IMAPIProp:: GetLastError](imapiprop-getlasterror.md) du conteneur si davantage d'informations sur le problème sont nécessaires.</span><span class="sxs-lookup"><span data-stu-id="fc714-108">Test for this return value with the **HR_FAILED** macro and call the container's [IMAPIProp::GetLastError](imapiprop-getlasterror.md) method if more information about the problem is needed.</span></span> 
    
<span data-ttu-id="fc714-109">Lorsque vous placez un pointeur sur la structure [ADRENTRY](adrentry.md) d'une entrée supprimée dans votre cache, vous pouvez toujours récupérer les propriétés à l'aide de son identificateur d'entrée.</span><span class="sxs-lookup"><span data-stu-id="fc714-109">When you hold a pointer to a deleted entry's [ADRENTRY](adrentry.md) structure in your cache, you will still be able to retrieve properties using its entry identifier.</span></span> <span data-ttu-id="fc714-110">Cela est dû au fait que l'entrée est uniquement marquée pour suppression.</span><span class="sxs-lookup"><span data-stu-id="fc714-110">This is because the entry is only marked for deletion.</span></span> <span data-ttu-id="fc714-111">MAPI conserve un niveau d'accès à ces entrées marquées par la conception.</span><span class="sxs-lookup"><span data-stu-id="fc714-111">MAPI maintains a level of access to these marked entries by design.</span></span> 
  

