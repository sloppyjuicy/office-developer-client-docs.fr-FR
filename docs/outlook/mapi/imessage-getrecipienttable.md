---
title: IMessageGetRecipientTable
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMessage.GetRecipientTable
api_type:
- COM
ms.assetid: a335dfca-44da-452e-b16f-25d314b1758f
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 5908069f5fa887fd9d2e3f8c0df75f2e3d69515c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579535"
---
# <a name="imessagegetrecipienttable"></a><span data-ttu-id="70e02-103">IMessage::GetRecipientTable</span><span class="sxs-lookup"><span data-stu-id="70e02-103">IMessage::GetRecipientTable</span></span>

  
  
<span data-ttu-id="70e02-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="70e02-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="70e02-105">Renvoie un tableau de destinataire du message.</span><span class="sxs-lookup"><span data-stu-id="70e02-105">Returns the message's recipient table.</span></span>
  
```cpp
HRESULT GetRecipientTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a><span data-ttu-id="70e02-106">Param�tres</span><span class="sxs-lookup"><span data-stu-id="70e02-106">Parameters</span></span>

 <span data-ttu-id="70e02-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="70e02-107">_ulFlags_</span></span>
  
> <span data-ttu-id="70e02-108">[in] Masque de bits d’indicateurs qui contrôle le retour de la table.</span><span class="sxs-lookup"><span data-stu-id="70e02-108">[in] Bitmask of flags that controls the return of the table.</span></span> <span data-ttu-id="70e02-109">Les indicateurs suivants peuvent être définis :</span><span class="sxs-lookup"><span data-stu-id="70e02-109">The following flags can be set:</span></span>
    
<span data-ttu-id="70e02-110">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="70e02-110">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="70e02-111">Permet de **GetRecipientTable** renvoyer avec succès, éventuellement, avant de la table est totalement disponible au client appelant.</span><span class="sxs-lookup"><span data-stu-id="70e02-111">Allows **GetRecipientTable** to return successfully, possibly before the table is fully available to the calling client.</span></span> <span data-ttu-id="70e02-112">Si le tableau n’est pas disponible, vous appelez suivante lui peut provoquer une erreur.</span><span class="sxs-lookup"><span data-stu-id="70e02-112">If the table is not available, making a subsequent call to it can cause an error.</span></span> 
    
<span data-ttu-id="70e02-113">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="70e02-113">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="70e02-114">Colonnes de la chaîne doivent être au format Unicode.</span><span class="sxs-lookup"><span data-stu-id="70e02-114">String columns should be in Unicode format.</span></span> <span data-ttu-id="70e02-115">Si l’indicateur MAPI_UNICODE n’est pas définie, les colonnes de la chaîne doivent être au format ANSI.</span><span class="sxs-lookup"><span data-stu-id="70e02-115">If the MAPI_UNICODE flag is not set, the string columns should be in ANSI format.</span></span>
    
 <span data-ttu-id="70e02-116">_lppTable_</span><span class="sxs-lookup"><span data-stu-id="70e02-116">_lppTable_</span></span>
  
> <span data-ttu-id="70e02-117">[out] Pointeur vers un pointeur vers la table de destinataires.</span><span class="sxs-lookup"><span data-stu-id="70e02-117">[out] Pointer to a pointer to the recipient table.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="70e02-118">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="70e02-118">Return value</span></span>

<span data-ttu-id="70e02-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="70e02-119">S_OK</span></span> 
  
> <span data-ttu-id="70e02-120">La table de destinataires a été renvoyée avec succès.</span><span class="sxs-lookup"><span data-stu-id="70e02-120">The recipient table was returned successfully.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="70e02-121">Remarques</span><span class="sxs-lookup"><span data-stu-id="70e02-121">Remarks</span></span>

<span data-ttu-id="70e02-122">La méthode **IMessage::GetRecipientTable** retourne un pointeur vers la table des destinataires du message, qui consacrée des informations sur tous les destinataires du message.</span><span class="sxs-lookup"><span data-stu-id="70e02-122">The **IMessage::GetRecipientTable** method returns a pointer to the message's recipient table, which includes information about all of the recipients for the message.</span></span> <span data-ttu-id="70e02-123">Il existe une ligne pour chaque destinataire.</span><span class="sxs-lookup"><span data-stu-id="70e02-123">There is one row for every recipient.</span></span> 
  
<span data-ttu-id="70e02-124">Tables de destinataires ont une colonne différente selon que le message a été envoyé.</span><span class="sxs-lookup"><span data-stu-id="70e02-124">Recipient tables have a different column set depending on whether the message has been submitted.</span></span> <span data-ttu-id="70e02-125">Pour obtenir une liste complète des colonnes dans une table de destinataires, voir [Les Tables de destinataire](recipient-tables.md).</span><span class="sxs-lookup"><span data-stu-id="70e02-125">For a complete list of the columns in a recipient table, see [Recipient Tables](recipient-tables.md).</span></span>
  
<span data-ttu-id="70e02-126">Certaines tables de destinataires de prendre en charge une grande variété de restrictions ; d’autres ne le sont pas.</span><span class="sxs-lookup"><span data-stu-id="70e02-126">Some recipient tables support a wide variety of restrictions; others do not.</span></span> <span data-ttu-id="70e02-127">Prise en charge des restrictions dépend de l’implémentation du fournisseur de banque de messages.</span><span class="sxs-lookup"><span data-stu-id="70e02-127">Support for restrictions depends on the message store provider's implementation.</span></span> 
  
<span data-ttu-id="70e02-128">Définition de l’indicateur MAPI_UNICODE dans le paramètre _ulFlags_ affecte les appels suivants de la table de destinataires :</span><span class="sxs-lookup"><span data-stu-id="70e02-128">Setting the MAPI_UNICODE flag in the  _ulFlags_ parameter affects the following calls to the recipient table:</span></span> 
  
- <span data-ttu-id="70e02-129">[IMAPITable::QueryColumns](imapitable-querycolumns.md) pour extraire l’ensemble de colonnes.</span><span class="sxs-lookup"><span data-stu-id="70e02-129">[IMAPITable::QueryColumns](imapitable-querycolumns.md) to retrieve the column set.</span></span> 
    
- <span data-ttu-id="70e02-130">[IMAPITable::QueryRows](imapitable-queryrows.md) pour récupérer des lignes.</span><span class="sxs-lookup"><span data-stu-id="70e02-130">[IMAPITable::QueryRows](imapitable-queryrows.md) to retrieve rows.</span></span> 
    
- <span data-ttu-id="70e02-131">[IMAPITable::QuerySortOrder](imapitable-querysortorder.md) pour récupérer l’ordre de tri.</span><span class="sxs-lookup"><span data-stu-id="70e02-131">[IMAPITable::QuerySortOrder](imapitable-querysortorder.md) to retrieve the sort order.</span></span> 
    
<span data-ttu-id="70e02-132">Si les demandes d’indicateur Unicode que les informations des colonnes de la chaîne retournée par ces appels au format Unicode.</span><span class="sxs-lookup"><span data-stu-id="70e02-132">Setting the Unicode flag requests that the information for any string columns returned from these calls be in Unicode format.</span></span> <span data-ttu-id="70e02-133">Toutefois, étant donné que tous les fournisseurs de banque de messages prennent en charge Unicode, définition de cet indicateur est uniquement une demande.</span><span class="sxs-lookup"><span data-stu-id="70e02-133">However, because not all message store providers support Unicode, setting this flag is only a request.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="70e02-134">Notes aux appelants</span><span class="sxs-lookup"><span data-stu-id="70e02-134">Notes to callers</span></span>

<span data-ttu-id="70e02-135">Vous pouvez modifier une table de destinataires lorsqu’il est ouvert en appelant la méthode [IMessage::ModifyRecipients](imessage-modifyrecipients.md) .</span><span class="sxs-lookup"><span data-stu-id="70e02-135">You can change a recipient table while it is open by calling the [IMessage::ModifyRecipients](imessage-modifyrecipients.md) method.</span></span> <span data-ttu-id="70e02-136">**ModifyRecipients** ajoute des destinataires, supprime les destinataires ou modifie les propriétés de destinataire.</span><span class="sxs-lookup"><span data-stu-id="70e02-136">**ModifyRecipients** adds recipients, deletes recipients, or modifies recipient properties.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="70e02-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="70e02-137">See also</span></span>



[<span data-ttu-id="70e02-138">IMAPIProp::SaveChanges</span><span class="sxs-lookup"><span data-stu-id="70e02-138">IMAPIProp::SaveChanges</span></span>](imapiprop-savechanges.md)
  
[<span data-ttu-id="70e02-139">IMAPITable::QueryRows</span><span class="sxs-lookup"><span data-stu-id="70e02-139">IMAPITable::QueryRows</span></span>](imapitable-queryrows.md)
  
[<span data-ttu-id="70e02-140">IMessage::ModifyRecipients</span><span class="sxs-lookup"><span data-stu-id="70e02-140">IMessage::ModifyRecipients</span></span>](imessage-modifyrecipients.md)
  
[<span data-ttu-id="70e02-141">IMessage : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="70e02-141">IMessage : IMAPIProp</span></span>](imessageimapiprop.md)

