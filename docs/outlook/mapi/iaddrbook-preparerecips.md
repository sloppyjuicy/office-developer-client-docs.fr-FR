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
ms.openlocfilehash: db1c23f33e604d6aafdd8a046566c7390c281ad8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414276"
---
# <a name="iaddrbookpreparerecips"></a><span data-ttu-id="fad20-103">IAddrBook::PrepareRecips</span><span class="sxs-lookup"><span data-stu-id="fad20-103">IAddrBook::PrepareRecips</span></span>

  
  
<span data-ttu-id="fad20-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fad20-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fad20-105">Prépare une liste de destinataires pour une utilisation ultérieure par le système de messagerie.</span><span class="sxs-lookup"><span data-stu-id="fad20-105">Prepares a recipient list for later use by the messaging system.</span></span> 
  
```cpp
HRESULT PrepareRecips(
  ULONG ulFlags,
  LPSPropTagArray lpSPropTagArray,
  LPADRLIST lpRecipList
);
```

## <a name="parameters"></a><span data-ttu-id="fad20-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="fad20-106">Parameters</span></span>

 <span data-ttu-id="fad20-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="fad20-107">_ulFlags_</span></span>
  
> <span data-ttu-id="fad20-108">[in] Masque de bits d’indicateurs qui contrôle la façon dont l’entrée est ouverte.</span><span class="sxs-lookup"><span data-stu-id="fad20-108">[in] A bitmask of flags that controls how the entry is opened.</span></span> <span data-ttu-id="fad20-109">L’indicateur suivant peut être définie :</span><span class="sxs-lookup"><span data-stu-id="fad20-109">The following flag can be set:</span></span>
    
<span data-ttu-id="fad20-110">MAPI_CACHE_ONLY</span><span class="sxs-lookup"><span data-stu-id="fad20-110">MAPI_CACHE_ONLY</span></span>
  
> <span data-ttu-id="fad20-111">Utilisez uniquement le carnet d’adresses en mode hors connexion pour effectuer la résolution de noms.</span><span class="sxs-lookup"><span data-stu-id="fad20-111">Use only the offline address book to perform name resolution.</span></span> <span data-ttu-id="fad20-112">Par exemple, vous pouvez utiliser cet indicateur pour permettre à une application cliente d’ouvrir la liste d’adresses globale (LAL) en mode Exchange mis en cache et d’accéder à une entrée dans ce carnet d’adresses à partir du cache sans créer de trafic entre le client et le serveur.</span><span class="sxs-lookup"><span data-stu-id="fad20-112">For example, you can use this flag to allow a client application to open the global address list (GAL) in cached exchange mode and to access an entry in that address book from the cache without creating traffic between the client and the server.</span></span> <span data-ttu-id="fad20-113">Cet indicateur est pris en charge uniquement par le fournisseur de carnet d’adresses Exchange.</span><span class="sxs-lookup"><span data-stu-id="fad20-113">This flag is supported only by the Exchange Address Book Provider.</span></span>
    
 <span data-ttu-id="fad20-114">_lpSPropTagArray_</span><span class="sxs-lookup"><span data-stu-id="fad20-114">_lpSPropTagArray_</span></span>
  
> <span data-ttu-id="fad20-115">[in] Pointeur vers une structure [SPropTagArray](sproptagarray.md) qui contient un tableau de balises de propriétés qui indiquent les propriétés, le cas contraire, qui nécessitent une mise à jour.</span><span class="sxs-lookup"><span data-stu-id="fad20-115">[in] A pointer to an [SPropTagArray](sproptagarray.md) structure that contains an array of property tags that indicate the properties, if any, that require updating.</span></span> <span data-ttu-id="fad20-116">Le  _paramètre lpSPropTagArray_ peut être NULL.</span><span class="sxs-lookup"><span data-stu-id="fad20-116">The  _lpSPropTagArray_ parameter can be NULL.</span></span> 
    
 <span data-ttu-id="fad20-117">_lpRecipList_</span><span class="sxs-lookup"><span data-stu-id="fad20-117">_lpRecipList_</span></span>
  
> <span data-ttu-id="fad20-118">[in] Pointeur vers une structure [ADRLIST](adrlist.md) qui contient la liste des destinataires.</span><span class="sxs-lookup"><span data-stu-id="fad20-118">[in] A pointer to an [ADRLIST](adrlist.md) structure that contains the list of recipients.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="fad20-119">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="fad20-119">Return value</span></span>

<span data-ttu-id="fad20-120">S_OK</span><span class="sxs-lookup"><span data-stu-id="fad20-120">S_OK</span></span> 
  
> <span data-ttu-id="fad20-121">La liste des destinataires a été préparée avec succès.</span><span class="sxs-lookup"><span data-stu-id="fad20-121">The recipient list was successfully prepared.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="fad20-122">Remarques</span><span class="sxs-lookup"><span data-stu-id="fad20-122">Remarks</span></span>

<span data-ttu-id="fad20-123">Les clients et les fournisseurs de services appellent **la méthode PrepareRecips** pour :</span><span class="sxs-lookup"><span data-stu-id="fad20-123">Clients and service providers call the **PrepareRecips** method to do the following:</span></span> 
  
- <span data-ttu-id="fad20-124">Assurez-vous que tous les destinataires du  _paramètre lpRecipList_ ont des identificateurs d’entrée à long terme.</span><span class="sxs-lookup"><span data-stu-id="fad20-124">Ensure that all recipients in the  _lpRecipList_ parameter have long-term entry identifiers.</span></span> 
    
- <span data-ttu-id="fad20-125">Assurez-vous que chaque destinataire du paramètre  _lpRecipList_ possède les propriétés répertoriées dans le paramètre  _lpSPropTagArray_ et que ces propriétés apparaissent au début de la liste des destinataires.</span><span class="sxs-lookup"><span data-stu-id="fad20-125">Ensure that each recipient in the  _lpRecipList_ parameter has the properties listed in the  _lpSPropTagArray_ parameter and that these properties appear at the start of the recipient list.</span></span> 
    
<span data-ttu-id="fad20-126">MAPI convertit les identificateurs d’entrée à court terme de chaque destinataire en identificateurs d’entrée à long terme.</span><span class="sxs-lookup"><span data-stu-id="fad20-126">MAPI converts each recipient's short-term entry identifiers to long-term entry identifiers.</span></span> <span data-ttu-id="fad20-127">Si nécessaire, les identificateurs d’entrée à long terme des destinataires sont extraits du fournisseur de carnet d’adresses approprié et toutes les propriétés supplémentaires sont demandées.</span><span class="sxs-lookup"><span data-stu-id="fad20-127">If necessary, recipients' long-term entry identifiers are retrieved from the appropriate address book provider and any additional properties are requested.</span></span>
  
<span data-ttu-id="fad20-128">Dans une entrée de destinataire individuelle, les propriétés demandées sont d’abord ordre, suivies de toutes les propriétés déjà présentes pour l’entrée.</span><span class="sxs-lookup"><span data-stu-id="fad20-128">In an individual recipient entry, the requested properties are ordered first, followed by any properties that were already present for the entry.</span></span> <span data-ttu-id="fad20-129">Si une ou plusieurs des propriétés demandées dans le paramètre  _lpSPropTagArray_ ne sont pas gérées par le fournisseur de carnet d’adresses approprié, leurs types de propriétés sont PT_ERROR.</span><span class="sxs-lookup"><span data-stu-id="fad20-129">If one or more of the requested properties in the  _lpSPropTagArray_ parameter are not handled by the appropriate address book provider, their property types will be set to PT_ERROR.</span></span> <span data-ttu-id="fad20-130">Leurs valeurs de propriété sont définies sur MAPI_E_NOT_FOUND ou sur une autre valeur qui donne une raison plus spécifique pour laquelle les propriétés ne sont pas disponibles.</span><span class="sxs-lookup"><span data-stu-id="fad20-130">Their property values will be set to either to MAPI_E_NOT_FOUND or to another value that gives a more specific reason why the properties are not available.</span></span> <span data-ttu-id="fad20-131">Chaque structure [SPropValue](spropvalue.md) incluse dans le paramètre  _lpRecipList_ doit être allouée séparément à l’aide des fonctions [MAPIAllocateBuffer](mapiallocatebuffer.md) et [MAPIAllocateMore](mapiallocatemore.md) afin qu’elle puisse être libérée individuellement.</span><span class="sxs-lookup"><span data-stu-id="fad20-131">Each [SPropValue](spropvalue.md) structure included in the  _lpRecipList_ parameter must be separately allocated by using the [MAPIAllocateBuffer](mapiallocatebuffer.md) and [MAPIAllocateMore](mapiallocatemore.md) functions so that it can be freed individually.</span></span> 
  
<span data-ttu-id="fad20-132">Pour plus d’informations PT_ERROR, voir [Types de propriétés.](property-types.md)</span><span class="sxs-lookup"><span data-stu-id="fad20-132">For information about PT_ERROR, see [Property Types](property-types.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="fad20-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fad20-133">See also</span></span>



[<span data-ttu-id="fad20-134">ADRLIST</span><span class="sxs-lookup"><span data-stu-id="fad20-134">ADRLIST</span></span>](adrlist.md)
  
[<span data-ttu-id="fad20-135">IMAPIProp::GetProps</span><span class="sxs-lookup"><span data-stu-id="fad20-135">IMAPIProp::GetProps</span></span>](imapiprop-getprops.md)
  
[<span data-ttu-id="fad20-136">IMessage::ModifyRecipients</span><span class="sxs-lookup"><span data-stu-id="fad20-136">IMessage::ModifyRecipients</span></span>](imessage-modifyrecipients.md)
  
[<span data-ttu-id="fad20-137">Propriété canonique PidTagEntryId</span><span class="sxs-lookup"><span data-stu-id="fad20-137">PidTagEntryId Canonical Property</span></span>](pidtagentryid-canonical-property.md)
  
[<span data-ttu-id="fad20-138">SPropValue</span><span class="sxs-lookup"><span data-stu-id="fad20-138">SPropValue</span></span>](spropvalue.md)
  
[<span data-ttu-id="fad20-139">SRowSet</span><span class="sxs-lookup"><span data-stu-id="fad20-139">SRowSet</span></span>](srowset.md)
  
[<span data-ttu-id="fad20-140">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="fad20-140">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)

