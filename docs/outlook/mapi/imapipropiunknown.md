---
title: IMAPIProp IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProp
api_type:
- COM
ms.assetid: 3c9e4e05-cd3a-4b56-9dff-879e33ff6fd5
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 6b0a8923ee5efe22584170ce9853698885527ee8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407661"
---
# <a name="imapiprop--iunknown"></a><span data-ttu-id="6bea3-103">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="6bea3-103">IMAPIProp : IUnknown</span></span>

  
  
<span data-ttu-id="6bea3-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6bea3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6bea3-105">Permet aux clients, aux fournisseurs de services et à MAPI de travailler avec les propriétés.</span><span class="sxs-lookup"><span data-stu-id="6bea3-105">Enables clients, service providers, and MAPI to work with properties.</span></span> <span data-ttu-id="6bea3-106">Tous les objets qui prennent en charge les propriétés implémentent cette interface.</span><span class="sxs-lookup"><span data-stu-id="6bea3-106">All objects that support properties implement this interface.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="6bea3-107">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="6bea3-107">Header file:</span></span>  <br/> |<span data-ttu-id="6bea3-108">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="6bea3-108">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="6bea3-109">Exposé par:</span><span class="sxs-lookup"><span data-stu-id="6bea3-109">Exposed by:</span></span>  <br/> |<span data-ttu-id="6bea3-110">Aucun objet n'expose directement cette interface.</span><span class="sxs-lookup"><span data-stu-id="6bea3-110">No object exposes this interface directly.</span></span>  <br/> |
|<span data-ttu-id="6bea3-111">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="6bea3-111">Implemented by:</span></span>  <br/> |<span data-ttu-id="6bea3-112">Fournisseurs de services et MAPI</span><span class="sxs-lookup"><span data-stu-id="6bea3-112">Service providers and MAPI</span></span>  <br/> |
|<span data-ttu-id="6bea3-113">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="6bea3-113">Called by:</span></span>  <br/> |<span data-ttu-id="6bea3-114">Applications clientes, fournisseurs de services et MAPI</span><span class="sxs-lookup"><span data-stu-id="6bea3-114">Client applications, service providers, and MAPI</span></span>  <br/> |
|<span data-ttu-id="6bea3-115">Identificateur de l'interface:</span><span class="sxs-lookup"><span data-stu-id="6bea3-115">Interface identifier:</span></span>  <br/> |<span data-ttu-id="6bea3-116">IID_IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="6bea3-116">IID_IMAPIProp</span></span>  <br/> |
|<span data-ttu-id="6bea3-117">Type de pointeur:</span><span class="sxs-lookup"><span data-stu-id="6bea3-117">Pointer type:</span></span>  <br/> |<span data-ttu-id="6bea3-118">LPMAPIPROP</span><span class="sxs-lookup"><span data-stu-id="6bea3-118">LPMAPIPROP</span></span>  <br/> |
|<span data-ttu-id="6bea3-119">Modèle de transaction:</span><span class="sxs-lookup"><span data-stu-id="6bea3-119">Transaction model:</span></span>  <br/> |<span data-ttu-id="6bea3-120">Classe abstraite, jamais implémentée</span><span class="sxs-lookup"><span data-stu-id="6bea3-120">Abstract class, never implemented</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="6bea3-121">Ordre vtable</span><span class="sxs-lookup"><span data-stu-id="6bea3-121">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="6bea3-122">Généré</span><span class="sxs-lookup"><span data-stu-id="6bea3-122">GetLastError</span></span>](imapiprop-getlasterror.md) <br/> |<span data-ttu-id="6bea3-123">Renvoie une structure [MAPIERROR](mapierror.md) qui contient des informations sur l'erreur précédente.</span><span class="sxs-lookup"><span data-stu-id="6bea3-123">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous error.</span></span>  <br/> |
|[<span data-ttu-id="6bea3-124">SaveChanges</span><span class="sxs-lookup"><span data-stu-id="6bea3-124">SaveChanges</span></span>](imapiprop-savechanges.md) <br/> |<span data-ttu-id="6bea3-125">Rend permanentes toutes les modifications qui ont été apportées à un objet depuis la dernière opération d'enregistrement.</span><span class="sxs-lookup"><span data-stu-id="6bea3-125">Makes permanent any changes that were made to an object since the last save operation.</span></span>  <br/> |
|[<span data-ttu-id="6bea3-126">GetProps</span><span class="sxs-lookup"><span data-stu-id="6bea3-126">GetProps</span></span>](imapiprop-getprops.md) <br/> |<span data-ttu-id="6bea3-127">Récupère la valeur de propriété d'une ou de plusieurs propriétés d'un objet.</span><span class="sxs-lookup"><span data-stu-id="6bea3-127">Retrieves the property value of one or more properties of an object.</span></span>  <br/> |
|[<span data-ttu-id="6bea3-128">GetPropList</span><span class="sxs-lookup"><span data-stu-id="6bea3-128">GetPropList</span></span>](imapiprop-getproplist.md) <br/> |<span data-ttu-id="6bea3-129">Renvoie les balises de propriété pour toutes les propriétés.</span><span class="sxs-lookup"><span data-stu-id="6bea3-129">Returns property tags for all properties.</span></span>  <br/> |
|[<span data-ttu-id="6bea3-130">OpenProperty</span><span class="sxs-lookup"><span data-stu-id="6bea3-130">OpenProperty</span></span>](imapiprop-openproperty.md) <br/> |<span data-ttu-id="6bea3-131">Renvoie un pointeur vers une interface qui peut être utilisée pour accéder à une propriété.</span><span class="sxs-lookup"><span data-stu-id="6bea3-131">Returns a pointer to an interface that can be used to access a property.</span></span>  <br/> |
|[<span data-ttu-id="6bea3-132">SetProps</span><span class="sxs-lookup"><span data-stu-id="6bea3-132">SetProps</span></span>](imapiprop-setprops.md) <br/> |<span data-ttu-id="6bea3-133">Met à jour une ou plusieurs propriétés.</span><span class="sxs-lookup"><span data-stu-id="6bea3-133">Updates one or more properties.</span></span>  <br/> |
|[<span data-ttu-id="6bea3-134">DeleteProps</span><span class="sxs-lookup"><span data-stu-id="6bea3-134">DeleteProps</span></span>](imapiprop-deleteprops.md) <br/> |<span data-ttu-id="6bea3-135">Supprime une ou plusieurs propriétés d'un objet.</span><span class="sxs-lookup"><span data-stu-id="6bea3-135">Deletes one or more properties from an object.</span></span>  <br/> |
|[<span data-ttu-id="6bea3-136">CopyTo</span><span class="sxs-lookup"><span data-stu-id="6bea3-136">CopyTo</span></span>](imapiprop-copyto.md) <br/> |<span data-ttu-id="6bea3-137">Copie ou déplace toutes les propriétés, à l'exception des propriétés spécifiquement exclues.</span><span class="sxs-lookup"><span data-stu-id="6bea3-137">Copies or moves all properties, except for specifically excluded properties.</span></span>  <br/> |
|[<span data-ttu-id="6bea3-138">CopyProps</span><span class="sxs-lookup"><span data-stu-id="6bea3-138">CopyProps</span></span>](imapiprop-copyprops.md) <br/> |<span data-ttu-id="6bea3-139">Copie ou déplace les propriétés sélectionnées.</span><span class="sxs-lookup"><span data-stu-id="6bea3-139">Copies or moves selected properties.</span></span>  <br/> |
|[<span data-ttu-id="6bea3-140">GetNamesFromIDs</span><span class="sxs-lookup"><span data-stu-id="6bea3-140">GetNamesFromIDs</span></span>](imapiprop-getnamesfromids.md) <br/> |<span data-ttu-id="6bea3-141">Fournit les noms de propriétés qui correspondent à un ou plusieurs identificateurs de propriété.</span><span class="sxs-lookup"><span data-stu-id="6bea3-141">Provides the property names that correspond to one or more property identifiers.</span></span>  <br/> |
|[<span data-ttu-id="6bea3-142">GetIDsFromNames</span><span class="sxs-lookup"><span data-stu-id="6bea3-142">GetIDsFromNames</span></span>](imapiprop-getidsfromnames.md) <br/> |<span data-ttu-id="6bea3-143">Fournit les identificateurs de propriété qui correspondent à un ou plusieurs noms de propriétés.</span><span class="sxs-lookup"><span data-stu-id="6bea3-143">Provides the property identifiers that correspond to one or more property names.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6bea3-144">Remarques</span><span class="sxs-lookup"><span data-stu-id="6bea3-144">Remarks</span></span>

 <span data-ttu-id="6bea3-145">**IMAPIProp** est l'interface de base pour les interfaces suivantes:</span><span class="sxs-lookup"><span data-stu-id="6bea3-145">**IMAPIProp** is the base interface for the following interfaces:</span></span> 
  
- [<span data-ttu-id="6bea3-146">IAttach</span><span class="sxs-lookup"><span data-stu-id="6bea3-146">IAttach</span></span>](iattachimapiprop.md)
    
- [<span data-ttu-id="6bea3-147">IMailUser</span><span class="sxs-lookup"><span data-stu-id="6bea3-147">IMailUser</span></span>](imailuserimapiprop.md)
    
- [<span data-ttu-id="6bea3-148">IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="6bea3-148">IMAPIContainer</span></span>](imapicontainerimapiprop.md)
    
- [<span data-ttu-id="6bea3-149">IMAPIFormInfo</span><span class="sxs-lookup"><span data-stu-id="6bea3-149">IMAPIFormInfo</span></span>](imapiforminfoimapiprop.md)
    
- [<span data-ttu-id="6bea3-150">IMAPIStatus</span><span class="sxs-lookup"><span data-stu-id="6bea3-150">IMAPIStatus</span></span>](imapistatusimapiprop.md)
    
- [<span data-ttu-id="6bea3-151">IMessage</span><span class="sxs-lookup"><span data-stu-id="6bea3-151">IMessage</span></span>](imessageimapiprop.md)
    
- [<span data-ttu-id="6bea3-152">IMsgStore</span><span class="sxs-lookup"><span data-stu-id="6bea3-152">IMsgStore</span></span>](imsgstoreimapiprop.md)
    
- [<span data-ttu-id="6bea3-153">IProfSect</span><span class="sxs-lookup"><span data-stu-id="6bea3-153">IProfSect</span></span>](iprofsectimapiprop.md)
    
- [<span data-ttu-id="6bea3-154">IPropData</span><span class="sxs-lookup"><span data-stu-id="6bea3-154">IPropData</span></span>](ipropdataimapiprop.md)
    
## <a name="see-also"></a><span data-ttu-id="6bea3-155">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6bea3-155">See also</span></span>



[<span data-ttu-id="6bea3-156">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="6bea3-156">MAPI Interfaces</span></span>](mapi-interfaces.md)

