---
title: IAddrBookPrepareRecips
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAddrBook.PrepareRecips
api_type:
- COM
ms.assetid: d423f7b5-23b8-44dd-bca3-6590182dc42d
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 004498ac94aadaa075d87d4dd3c675c8cd5f4feb
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22563876"
---
# <a name="iaddrbookpreparerecips"></a><span data-ttu-id="fbd50-103">IAddrBook::PrepareRecips</span><span class="sxs-lookup"><span data-stu-id="fbd50-103">IAddrBook::PrepareRecips</span></span>

  
  
<span data-ttu-id="fbd50-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fbd50-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fbd50-105">Prépare une liste de destinataires pour une utilisation ultérieure par le système de messagerie.</span><span class="sxs-lookup"><span data-stu-id="fbd50-105">Prepares a recipient list for later use by the messaging system.</span></span> 
  
```cpp
HRESULT PrepareRecips(
  ULONG ulFlags,
  LPSPropTagArray lpSPropTagArray,
  LPADRLIST lpRecipList
);
```

## <a name="parameters"></a><span data-ttu-id="fbd50-106">Param�tres</span><span class="sxs-lookup"><span data-stu-id="fbd50-106">Parameters</span></span>

 <span data-ttu-id="fbd50-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="fbd50-107">_ulFlags_</span></span>
  
> <span data-ttu-id="fbd50-108">[in] Masque de bits d’indicateurs qui contrôle la façon dont l’entrée est ouvert.</span><span class="sxs-lookup"><span data-stu-id="fbd50-108">[in] A bitmask of flags that controls how the entry is opened.</span></span> <span data-ttu-id="fbd50-109">Vous pouvez définir l’indicateur suivant :</span><span class="sxs-lookup"><span data-stu-id="fbd50-109">The following flag can be set:</span></span>
    
<span data-ttu-id="fbd50-110">MAPI_CACHE_ONLY</span><span class="sxs-lookup"><span data-stu-id="fbd50-110">MAPI_CACHE_ONLY</span></span>
  
> <span data-ttu-id="fbd50-111">Utilisez uniquement le carnet d’adresses en mode hors connexion pour effectuer la résolution de noms.</span><span class="sxs-lookup"><span data-stu-id="fbd50-111">Use only the offline address book to perform name resolution.</span></span> <span data-ttu-id="fbd50-112">Par exemple, vous pouvez utiliser cet indicateur pour autoriser une application cliente pour ouvrir la liste d’adresses globale (LAG) en mode exchange mis en cache et d’accéder à une entrée dans ce carnet d’adresses à partir du cache sans le trafic entre le client et le serveur de création.</span><span class="sxs-lookup"><span data-stu-id="fbd50-112">For example, you can use this flag to allow a client application to open the global address list (GAL) in cached exchange mode and to access an entry in that address book from the cache without creating traffic between the client and the server.</span></span> <span data-ttu-id="fbd50-113">Cet indicateur est pris en charge uniquement par le fournisseur de carnet d’adresses Exchange.</span><span class="sxs-lookup"><span data-stu-id="fbd50-113">This flag is supported only by the Exchange Address Book Provider.</span></span>
    
 <span data-ttu-id="fbd50-114">_lpSPropTagArray_</span><span class="sxs-lookup"><span data-stu-id="fbd50-114">_lpSPropTagArray_</span></span>
  
> <span data-ttu-id="fbd50-115">[in] Un pointeur vers une structure [SPropTagArray](sproptagarray.md) qui contient un tableau de balises de propriétés qui indiquent les propriétés, le cas échéant, qui nécessitent la mise à jour.</span><span class="sxs-lookup"><span data-stu-id="fbd50-115">[in] A pointer to an [SPropTagArray](sproptagarray.md) structure that contains an array of property tags that indicate the properties, if any, that require updating.</span></span> <span data-ttu-id="fbd50-116">Le paramètre _lpSPropTagArray_ peut être NULL.</span><span class="sxs-lookup"><span data-stu-id="fbd50-116">The  _lpSPropTagArray_ parameter can be NULL.</span></span> 
    
 <span data-ttu-id="fbd50-117">_lpRecipList_</span><span class="sxs-lookup"><span data-stu-id="fbd50-117">_lpRecipList_</span></span>
  
> <span data-ttu-id="fbd50-118">[in] Pointeur vers une structure [ADRLIST](adrlist.md) qui contient la liste des destinataires.</span><span class="sxs-lookup"><span data-stu-id="fbd50-118">[in] A pointer to an [ADRLIST](adrlist.md) structure that contains the list of recipients.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="fbd50-119">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="fbd50-119">Return value</span></span>

<span data-ttu-id="fbd50-120">S_OK</span><span class="sxs-lookup"><span data-stu-id="fbd50-120">S_OK</span></span> 
  
> <span data-ttu-id="fbd50-121">La liste de destinataires a été correctement préparée.</span><span class="sxs-lookup"><span data-stu-id="fbd50-121">The recipient list was successfully prepared.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="fbd50-122">Remarques</span><span class="sxs-lookup"><span data-stu-id="fbd50-122">Remarks</span></span>

<span data-ttu-id="fbd50-123">Clients et fournisseurs de services appellent la méthode **PrepareRecips** pour effectuer les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="fbd50-123">Clients and service providers call the **PrepareRecips** method to do the following:</span></span> 
  
- <span data-ttu-id="fbd50-124">Assurez-vous que tous les destinataires dans le paramètre _lpRecipList_ ont des identificateurs d’entrée à long terme.</span><span class="sxs-lookup"><span data-stu-id="fbd50-124">Ensure that all recipients in the  _lpRecipList_ parameter have long-term entry identifiers.</span></span> 
    
- <span data-ttu-id="fbd50-125">Vérifiez que chaque destinataire dans le paramètre _lpRecipList_ possède les propriétés répertoriées dans le paramètre _lpSPropTagArray_ et que ces propriétés s’affichent au début de la liste des destinataires.</span><span class="sxs-lookup"><span data-stu-id="fbd50-125">Ensure that each recipient in the  _lpRecipList_ parameter has the properties listed in the  _lpSPropTagArray_ parameter and that these properties appear at the start of the recipient list.</span></span> 
    
<span data-ttu-id="fbd50-126">MAPI convertit les identificateurs d’entrée de chaque destinataire à court terme des identificateurs d’entrée à long terme.</span><span class="sxs-lookup"><span data-stu-id="fbd50-126">MAPI converts each recipient's short-term entry identifiers to long-term entry identifiers.</span></span> <span data-ttu-id="fbd50-127">Si nécessaire, les identificateurs d’entrée à long terme des destinataires sont récupérées à partir du fournisseur de carnet d’adresse appropriée et des propriétés supplémentaires sont demandées.</span><span class="sxs-lookup"><span data-stu-id="fbd50-127">If necessary, recipients' long-term entry identifiers are retrieved from the appropriate address book provider and any additional properties are requested.</span></span>
  
<span data-ttu-id="fbd50-128">Dans une entrée individuelle de destinataire, les propriétés demandées sont triées tout d’abord, suivie de toutes les propriétés qui étaient déjà présentes pour l’entrée.</span><span class="sxs-lookup"><span data-stu-id="fbd50-128">In an individual recipient entry, the requested properties are ordered first, followed by any properties that were already present for the entry.</span></span> <span data-ttu-id="fbd50-129">Si une ou plusieurs des propriétés demandées dans le paramètre _lpSPropTagArray_ ne sont pas gérés par le fournisseur de carnet d’adresse appropriée, leurs types de propriétés définira PT_ERROR.</span><span class="sxs-lookup"><span data-stu-id="fbd50-129">If one or more of the requested properties in the  _lpSPropTagArray_ parameter are not handled by the appropriate address book provider, their property types will be set to PT_ERROR.</span></span> <span data-ttu-id="fbd50-130">Les valeurs de propriété seront fixés à MAPI_E_NOT_FOUND ou une autre valeur qui fournit la raison plus spécifique pourquoi les propriétés ne sont pas disponibles.</span><span class="sxs-lookup"><span data-stu-id="fbd50-130">Their property values will be set to either to MAPI_E_NOT_FOUND or to another value that gives a more specific reason why the properties are not available.</span></span> <span data-ttu-id="fbd50-131">Chaque structure [SPropValue](spropvalue.md) inclus dans le paramètre _lpRecipList_ doit être alloué séparément en utilisant les fonctions [MAPIAllocateBuffer](mapiallocatebuffer.md) et [MAPIAllocateMore](mapiallocatemore.md) afin qu’elle peut être libérée individuellement.</span><span class="sxs-lookup"><span data-stu-id="fbd50-131">Each [SPropValue](spropvalue.md) structure included in the  _lpRecipList_ parameter must be separately allocated by using the [MAPIAllocateBuffer](mapiallocatebuffer.md) and [MAPIAllocateMore](mapiallocatemore.md) functions so that it can be freed individually.</span></span> 
  
<span data-ttu-id="fbd50-132">Pour plus d’informations sur PT_ERROR, reportez-vous à [Types de propriété](property-types.md).</span><span class="sxs-lookup"><span data-stu-id="fbd50-132">For information about PT_ERROR, see [Property Types](property-types.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="fbd50-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fbd50-133">See also</span></span>



[<span data-ttu-id="fbd50-134">ADRLIST</span><span class="sxs-lookup"><span data-stu-id="fbd50-134">ADRLIST</span></span>](adrlist.md)
  
[<span data-ttu-id="fbd50-135">IMAPIProp::GetProps</span><span class="sxs-lookup"><span data-stu-id="fbd50-135">IMAPIProp::GetProps</span></span>](imapiprop-getprops.md)
  
[<span data-ttu-id="fbd50-136">IMessage::ModifyRecipients</span><span class="sxs-lookup"><span data-stu-id="fbd50-136">IMessage::ModifyRecipients</span></span>](imessage-modifyrecipients.md)
  
[<span data-ttu-id="fbd50-137">Propriété canonique PidTagEntryId</span><span class="sxs-lookup"><span data-stu-id="fbd50-137">PidTagEntryId Canonical Property</span></span>](pidtagentryid-canonical-property.md)
  
[<span data-ttu-id="fbd50-138">SPropValue</span><span class="sxs-lookup"><span data-stu-id="fbd50-138">SPropValue</span></span>](spropvalue.md)
  
[<span data-ttu-id="fbd50-139">SRowSet</span><span class="sxs-lookup"><span data-stu-id="fbd50-139">SRowSet</span></span>](srowset.md)
  
[<span data-ttu-id="fbd50-140">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="fbd50-140">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)

