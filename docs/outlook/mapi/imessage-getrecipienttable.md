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
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 90ae9cee915296475d7fe64952b40ab7344e89e2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784136"
---
# <a name="imessagegetrecipienttable"></a><span data-ttu-id="1fd6c-103">IMessage::GetRecipientTable</span><span class="sxs-lookup"><span data-stu-id="1fd6c-103">IMessage::GetRecipientTable</span></span>

  
  
<span data-ttu-id="1fd6c-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="1fd6c-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="1fd6c-105">Renvoie un tableau de destinataire du message.</span><span class="sxs-lookup"><span data-stu-id="1fd6c-105">Returns the message's recipient table.</span></span>
  
```cpp
HRESULT GetRecipientTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a><span data-ttu-id="1fd6c-106">Param�tres</span><span class="sxs-lookup"><span data-stu-id="1fd6c-106">Parameters</span></span>

 <span data-ttu-id="1fd6c-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="1fd6c-107">_ulFlags_</span></span>
  
> <span data-ttu-id="1fd6c-108">[in] Masque de bits d’indicateurs qui contrôle le retour de la table.</span><span class="sxs-lookup"><span data-stu-id="1fd6c-108">[in] Bitmask of flags that controls the return of the table.</span></span> <span data-ttu-id="1fd6c-109">Les indicateurs suivants peuvent être définis :</span><span class="sxs-lookup"><span data-stu-id="1fd6c-109">The following flags can be set:</span></span>
    
<span data-ttu-id="1fd6c-110">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="1fd6c-110">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="1fd6c-111">Permet de **GetRecipientTable** renvoyer avec succès, éventuellement, avant de la table est totalement disponible au client appelant.</span><span class="sxs-lookup"><span data-stu-id="1fd6c-111">Allows **GetRecipientTable** to return successfully, possibly before the table is fully available to the calling client.</span></span> <span data-ttu-id="1fd6c-112">Si le tableau n’est pas disponible, vous appelez suivante lui peut provoquer une erreur.</span><span class="sxs-lookup"><span data-stu-id="1fd6c-112">If the table is not available, making a subsequent call to it can cause an error.</span></span> 
    
<span data-ttu-id="1fd6c-113">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="1fd6c-113">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="1fd6c-114">Colonnes de la chaîne doivent être au format Unicode.</span><span class="sxs-lookup"><span data-stu-id="1fd6c-114">String columns should be in Unicode format.</span></span> <span data-ttu-id="1fd6c-115">Si l’indicateur MAPI_UNICODE n’est pas définie, les colonnes de la chaîne doivent être au format ANSI.</span><span class="sxs-lookup"><span data-stu-id="1fd6c-115">If the MAPI_UNICODE flag is not set, the string columns should be in ANSI format.</span></span>
    
 <span data-ttu-id="1fd6c-116">_lppTable_</span><span class="sxs-lookup"><span data-stu-id="1fd6c-116">_lppTable_</span></span>
  
> <span data-ttu-id="1fd6c-117">[out] Pointeur vers un pointeur vers la table de destinataires.</span><span class="sxs-lookup"><span data-stu-id="1fd6c-117">[out] Pointer to a pointer to the recipient table.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="1fd6c-118">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="1fd6c-118">Return value</span></span>

<span data-ttu-id="1fd6c-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="1fd6c-119">S_OK</span></span> 
  
> <span data-ttu-id="1fd6c-120">La table de destinataires a été renvoyée avec succès.</span><span class="sxs-lookup"><span data-stu-id="1fd6c-120">The recipient table was returned successfully.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="1fd6c-121">Remarques</span><span class="sxs-lookup"><span data-stu-id="1fd6c-121">Remarks</span></span>

<span data-ttu-id="1fd6c-122">La méthode **IMessage::GetRecipientTable** retourne un pointeur vers la table des destinataires du message, qui consacrée des informations sur tous les destinataires du message.</span><span class="sxs-lookup"><span data-stu-id="1fd6c-122">The **IMessage::GetRecipientTable** method returns a pointer to the message's recipient table, which includes information about all of the recipients for the message.</span></span> <span data-ttu-id="1fd6c-123">Il existe une ligne pour chaque destinataire.</span><span class="sxs-lookup"><span data-stu-id="1fd6c-123">There is one row for every recipient.</span></span> 
  
<span data-ttu-id="1fd6c-124">Tables de destinataires ont une colonne différente selon que le message a été envoyé.</span><span class="sxs-lookup"><span data-stu-id="1fd6c-124">Recipient tables have a different column set depending on whether the message has been submitted.</span></span> <span data-ttu-id="1fd6c-125">Pour obtenir une liste complète des colonnes dans une table de destinataires, voir [Les Tables de destinataire](recipient-tables.md).</span><span class="sxs-lookup"><span data-stu-id="1fd6c-125">For a complete list of the columns in a recipient table, see [Recipient Tables](recipient-tables.md).</span></span>
  
<span data-ttu-id="1fd6c-126">Certaines tables de destinataires de prendre en charge une grande variété de restrictions ; d’autres ne le sont pas.</span><span class="sxs-lookup"><span data-stu-id="1fd6c-126">Some recipient tables support a wide variety of restrictions; others do not.</span></span> <span data-ttu-id="1fd6c-127">Prise en charge des restrictions dépend de l’implémentation du fournisseur de banque de messages.</span><span class="sxs-lookup"><span data-stu-id="1fd6c-127">Support for restrictions depends on the message store provider's implementation.</span></span> 
  
<span data-ttu-id="1fd6c-128">Définition de l’indicateur MAPI_UNICODE dans le paramètre _ulFlags_ affecte les appels suivants de la table de destinataires :</span><span class="sxs-lookup"><span data-stu-id="1fd6c-128">Setting the MAPI_UNICODE flag in the  _ulFlags_ parameter affects the following calls to the recipient table:</span></span> 
  
- <span data-ttu-id="1fd6c-129">[IMAPITable::QueryColumns](imapitable-querycolumns.md) pour extraire l’ensemble de colonnes.</span><span class="sxs-lookup"><span data-stu-id="1fd6c-129">[IMAPITable::QueryColumns](imapitable-querycolumns.md) to retrieve the column set.</span></span> 
    
- <span data-ttu-id="1fd6c-130">[IMAPITable::QueryRows](imapitable-queryrows.md) pour récupérer des lignes.</span><span class="sxs-lookup"><span data-stu-id="1fd6c-130">[IMAPITable::QueryRows](imapitable-queryrows.md) to retrieve rows.</span></span> 
    
- <span data-ttu-id="1fd6c-131">[IMAPITable::QuerySortOrder](imapitable-querysortorder.md) pour récupérer l’ordre de tri.</span><span class="sxs-lookup"><span data-stu-id="1fd6c-131">[IMAPITable::QuerySortOrder](imapitable-querysortorder.md) to retrieve the sort order.</span></span> 
    
<span data-ttu-id="1fd6c-132">Si les demandes d’indicateur Unicode que les informations des colonnes de la chaîne retournée par ces appels au format Unicode.</span><span class="sxs-lookup"><span data-stu-id="1fd6c-132">Setting the Unicode flag requests that the information for any string columns returned from these calls be in Unicode format.</span></span> <span data-ttu-id="1fd6c-133">Toutefois, étant donné que tous les fournisseurs de banque de messages prennent en charge Unicode, définition de cet indicateur est uniquement une demande.</span><span class="sxs-lookup"><span data-stu-id="1fd6c-133">However, because not all message store providers support Unicode, setting this flag is only a request.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="1fd6c-134">Notes aux appelants</span><span class="sxs-lookup"><span data-stu-id="1fd6c-134">Notes to callers</span></span>

<span data-ttu-id="1fd6c-135">Vous pouvez modifier une table de destinataires lorsqu’il est ouvert en appelant la méthode [IMessage::ModifyRecipients](imessage-modifyrecipients.md) .</span><span class="sxs-lookup"><span data-stu-id="1fd6c-135">You can change a recipient table while it is open by calling the [IMessage::ModifyRecipients](imessage-modifyrecipients.md) method.</span></span> <span data-ttu-id="1fd6c-136">**ModifyRecipients** ajoute des destinataires, supprime les destinataires ou modifie les propriétés de destinataire.</span><span class="sxs-lookup"><span data-stu-id="1fd6c-136">**ModifyRecipients** adds recipients, deletes recipients, or modifies recipient properties.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="1fd6c-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1fd6c-137">See also</span></span>



[<span data-ttu-id="1fd6c-138">IMAPIProp::SaveChanges</span><span class="sxs-lookup"><span data-stu-id="1fd6c-138">IMAPIProp::SaveChanges</span></span>](imapiprop-savechanges.md)
  
[<span data-ttu-id="1fd6c-139">IMAPITable::QueryRows</span><span class="sxs-lookup"><span data-stu-id="1fd6c-139">IMAPITable::QueryRows</span></span>](imapitable-queryrows.md)
  
[<span data-ttu-id="1fd6c-140">IMessage::ModifyRecipients</span><span class="sxs-lookup"><span data-stu-id="1fd6c-140">IMessage::ModifyRecipients</span></span>](imessage-modifyrecipients.md)
  
[<span data-ttu-id="1fd6c-141">IMessage : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="1fd6c-141">IMessage : IMAPIProp</span></span>](imessageimapiprop.md)

