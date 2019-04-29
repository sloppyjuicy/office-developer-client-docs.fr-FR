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
ms.openlocfilehash: ca42e91528cdb7e61ae3620989c4a89966db1061
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424608"
---
# <a name="imessagegetrecipienttable"></a><span data-ttu-id="af669-103">IMessage::GetRecipientTable</span><span class="sxs-lookup"><span data-stu-id="af669-103">IMessage::GetRecipientTable</span></span>

  
  
<span data-ttu-id="af669-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="af669-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="af669-105">Renvoie la table de destinataires du message.</span><span class="sxs-lookup"><span data-stu-id="af669-105">Returns the message's recipient table.</span></span>
  
```cpp
HRESULT GetRecipientTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a><span data-ttu-id="af669-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="af669-106">Parameters</span></span>

 <span data-ttu-id="af669-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="af669-107">_ulFlags_</span></span>
  
> <span data-ttu-id="af669-108">dans Masque de des indicateurs qui contrôle le retour de la table.</span><span class="sxs-lookup"><span data-stu-id="af669-108">[in] Bitmask of flags that controls the return of the table.</span></span> <span data-ttu-id="af669-109">Les indicateurs suivants peuvent être définis:</span><span class="sxs-lookup"><span data-stu-id="af669-109">The following flags can be set:</span></span>
    
<span data-ttu-id="af669-110">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="af669-110">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="af669-111">Permet à **GetRecipientTable** de retourner correctement, éventuellement avant que la table soit entièrement disponible pour le client appelant.</span><span class="sxs-lookup"><span data-stu-id="af669-111">Allows **GetRecipientTable** to return successfully, possibly before the table is fully available to the calling client.</span></span> <span data-ttu-id="af669-112">Si la table n'est pas disponible, un appel ultérieur de celle-ci peut entraîner une erreur.</span><span class="sxs-lookup"><span data-stu-id="af669-112">If the table is not available, making a subsequent call to it can cause an error.</span></span> 
    
<span data-ttu-id="af669-113">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="af669-113">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="af669-114">Les colonnes de chaîne doivent être au format Unicode.</span><span class="sxs-lookup"><span data-stu-id="af669-114">String columns should be in Unicode format.</span></span> <span data-ttu-id="af669-115">Si l'indicateur MAPI_UNICODE n'est pas défini, les colonnes de chaîne doivent être au format ANSI.</span><span class="sxs-lookup"><span data-stu-id="af669-115">If the MAPI_UNICODE flag is not set, the string columns should be in ANSI format.</span></span>
    
 <span data-ttu-id="af669-116">_lppTable_</span><span class="sxs-lookup"><span data-stu-id="af669-116">_lppTable_</span></span>
  
> <span data-ttu-id="af669-117">remarquer Pointeur vers un pointeur vers le tableau de destinataires.</span><span class="sxs-lookup"><span data-stu-id="af669-117">[out] Pointer to a pointer to the recipient table.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="af669-118">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="af669-118">Return value</span></span>

<span data-ttu-id="af669-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="af669-119">S_OK</span></span> 
  
> <span data-ttu-id="af669-120">La table de destinataires a été renvoyée avec succès.</span><span class="sxs-lookup"><span data-stu-id="af669-120">The recipient table was returned successfully.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="af669-121">Remarques</span><span class="sxs-lookup"><span data-stu-id="af669-121">Remarks</span></span>

<span data-ttu-id="af669-122">La méthode **IMessage:: GetRecipientTable** renvoie un pointeur vers la table de destinataires du message, qui inclut des informations sur tous les destinataires du message.</span><span class="sxs-lookup"><span data-stu-id="af669-122">The **IMessage::GetRecipientTable** method returns a pointer to the message's recipient table, which includes information about all of the recipients for the message.</span></span> <span data-ttu-id="af669-123">Il y a une ligne pour chaque destinataire.</span><span class="sxs-lookup"><span data-stu-id="af669-123">There is one row for every recipient.</span></span> 
  
<span data-ttu-id="af669-124">Les tables de destinataires ont un jeu de colonnes différent selon que le message a été envoyé ou non.</span><span class="sxs-lookup"><span data-stu-id="af669-124">Recipient tables have a different column set depending on whether the message has been submitted.</span></span> <span data-ttu-id="af669-125">Pour obtenir la liste complète des colonnes d'un tableau de destinataires, consultez la rubrique [tables](recipient-tables.md)des destinataires.</span><span class="sxs-lookup"><span data-stu-id="af669-125">For a complete list of the columns in a recipient table, see [Recipient Tables](recipient-tables.md).</span></span>
  
<span data-ttu-id="af669-126">Certaines tables de destinataires prennent en charge un large éventail de restrictions; d'autres non.</span><span class="sxs-lookup"><span data-stu-id="af669-126">Some recipient tables support a wide variety of restrictions; others do not.</span></span> <span data-ttu-id="af669-127">La prise en charge des restrictions dépend de l'implémentation du fournisseur de banque de messages.</span><span class="sxs-lookup"><span data-stu-id="af669-127">Support for restrictions depends on the message store provider's implementation.</span></span> 
  
<span data-ttu-id="af669-128">La définition de l'indicateur MAPI_UNICODE dans le paramètre _ulFlags_ affecte les appels suivants à la table de destinataires:</span><span class="sxs-lookup"><span data-stu-id="af669-128">Setting the MAPI_UNICODE flag in the  _ulFlags_ parameter affects the following calls to the recipient table:</span></span> 
  
- <span data-ttu-id="af669-129">[IMAPITable:: QueryColumns](imapitable-querycolumns.md) pour récupérer le jeu de colonnes.</span><span class="sxs-lookup"><span data-stu-id="af669-129">[IMAPITable::QueryColumns](imapitable-querycolumns.md) to retrieve the column set.</span></span> 
    
- <span data-ttu-id="af669-130">[IMAPITable:: QueryRows](imapitable-queryrows.md) pour extraire des lignes.</span><span class="sxs-lookup"><span data-stu-id="af669-130">[IMAPITable::QueryRows](imapitable-queryrows.md) to retrieve rows.</span></span> 
    
- <span data-ttu-id="af669-131">[IMAPITable:: QuerySortOrder](imapitable-querysortorder.md) pour récupérer l'ordre de tri.</span><span class="sxs-lookup"><span data-stu-id="af669-131">[IMAPITable::QuerySortOrder](imapitable-querysortorder.md) to retrieve the sort order.</span></span> 
    
<span data-ttu-id="af669-132">Définition des demandes d'indicateur Unicode pour que les informations de toutes les colonnes de chaînes renvoyées à partir de ces appels soient au format Unicode.</span><span class="sxs-lookup"><span data-stu-id="af669-132">Setting the Unicode flag requests that the information for any string columns returned from these calls be in Unicode format.</span></span> <span data-ttu-id="af669-133">Toutefois, étant donné que tous les fournisseurs de banques de messages ne prennent pas en charge Unicode, la définition de cet indicateur n'est qu'une requête.</span><span class="sxs-lookup"><span data-stu-id="af669-133">However, because not all message store providers support Unicode, setting this flag is only a request.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="af669-134">Remarques pour les appelants</span><span class="sxs-lookup"><span data-stu-id="af669-134">Notes to callers</span></span>

<span data-ttu-id="af669-135">Vous pouvez modifier une table de destinataires lorsqu'elle est ouverte en appelant la méthode [IMessage:: ModifyRecipients](imessage-modifyrecipients.md) .</span><span class="sxs-lookup"><span data-stu-id="af669-135">You can change a recipient table while it is open by calling the [IMessage::ModifyRecipients](imessage-modifyrecipients.md) method.</span></span> <span data-ttu-id="af669-136">**ModifyRecipients** ajoute des destinataires, supprime des destinataires ou modifie les propriétés des destinataires.</span><span class="sxs-lookup"><span data-stu-id="af669-136">**ModifyRecipients** adds recipients, deletes recipients, or modifies recipient properties.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="af669-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="af669-137">See also</span></span>



[<span data-ttu-id="af669-138">IMAPIProp::SaveChanges</span><span class="sxs-lookup"><span data-stu-id="af669-138">IMAPIProp::SaveChanges</span></span>](imapiprop-savechanges.md)
  
[<span data-ttu-id="af669-139">IMAPITable::QueryRows</span><span class="sxs-lookup"><span data-stu-id="af669-139">IMAPITable::QueryRows</span></span>](imapitable-queryrows.md)
  
[<span data-ttu-id="af669-140">IMessage::ModifyRecipients</span><span class="sxs-lookup"><span data-stu-id="af669-140">IMessage::ModifyRecipients</span></span>](imessage-modifyrecipients.md)
  
[<span data-ttu-id="af669-141">IMessage : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="af669-141">IMessage : IMAPIProp</span></span>](imessageimapiprop.md)

