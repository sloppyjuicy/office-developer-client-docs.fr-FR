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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 02d2b136ed1437ba53ce1e54a202d70a48b2abe9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783919"
---
# <a name="imapiprop--iunknown"></a><span data-ttu-id="30055-103">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="30055-103">IMAPIProp : IUnknown</span></span>

  
  
<span data-ttu-id="30055-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="30055-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="30055-105">Permet de clients, fournisseurs de services et MAPI travailler avec les propriétés.</span><span class="sxs-lookup"><span data-stu-id="30055-105">Enables clients, service providers, and MAPI to work with properties.</span></span> <span data-ttu-id="30055-106">Tous les objets qui prennent en charge les propriétés implémentent cette interface.</span><span class="sxs-lookup"><span data-stu-id="30055-106">All objects that support properties implement this interface.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="30055-107">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="30055-107">Header file:</span></span>  <br/> |<span data-ttu-id="30055-108">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="30055-108">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="30055-109">Exposés par :</span><span class="sxs-lookup"><span data-stu-id="30055-109">Exposed by:</span></span>  <br/> |<span data-ttu-id="30055-110">Aucun objet n’expose cette interface directement.</span><span class="sxs-lookup"><span data-stu-id="30055-110">No object exposes this interface directly.</span></span>  <br/> |
|<span data-ttu-id="30055-111">Implémentée par :</span><span class="sxs-lookup"><span data-stu-id="30055-111">Implemented by:</span></span>  <br/> |<span data-ttu-id="30055-112">Fournisseurs de services et MAPI</span><span class="sxs-lookup"><span data-stu-id="30055-112">Service providers and MAPI</span></span>  <br/> |
|<span data-ttu-id="30055-113">Appelée par :</span><span class="sxs-lookup"><span data-stu-id="30055-113">Called by:</span></span>  <br/> |<span data-ttu-id="30055-114">Applications clientes et fournisseurs de services MAPI</span><span class="sxs-lookup"><span data-stu-id="30055-114">Client applications, service providers, and MAPI</span></span>  <br/> |
|<span data-ttu-id="30055-115">Identificateur de l’interface :</span><span class="sxs-lookup"><span data-stu-id="30055-115">Interface identifier:</span></span>  <br/> |<span data-ttu-id="30055-116">IID_IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="30055-116">IID_IMAPIProp</span></span>  <br/> |
|<span data-ttu-id="30055-117">Type de pointeur :</span><span class="sxs-lookup"><span data-stu-id="30055-117">Pointer type:</span></span>  <br/> |<span data-ttu-id="30055-118">LPMAPIPROP</span><span class="sxs-lookup"><span data-stu-id="30055-118">LPMAPIPROP</span></span>  <br/> |
|<span data-ttu-id="30055-119">Modèle de transaction :</span><span class="sxs-lookup"><span data-stu-id="30055-119">Transaction model:</span></span>  <br/> |<span data-ttu-id="30055-120">Classe abstraite, jamais implémentée</span><span class="sxs-lookup"><span data-stu-id="30055-120">Abstract class, never implemented</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="30055-121">Ordre vtable</span><span class="sxs-lookup"><span data-stu-id="30055-121">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="30055-122">GetLastError</span><span class="sxs-lookup"><span data-stu-id="30055-122">GetLastError</span></span>](imapiprop-getlasterror.md) <br/> |<span data-ttu-id="30055-123">Retourne une structure [MAPIERROR](mapierror.md) qui contient des informations sur l’erreur précédente.</span><span class="sxs-lookup"><span data-stu-id="30055-123">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous error.</span></span>  <br/> |
|[<span data-ttu-id="30055-124">SaveChanges</span><span class="sxs-lookup"><span data-stu-id="30055-124">SaveChanges</span></span>](imapiprop-savechanges.md) <br/> |<span data-ttu-id="30055-125">Rend permanentes toutes les modifications qui ont été apportées à un objet depuis la dernière opération d’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="30055-125">Makes permanent any changes that were made to an object since the last save operation.</span></span>  <br/> |
|[<span data-ttu-id="30055-126">GetProps</span><span class="sxs-lookup"><span data-stu-id="30055-126">GetProps</span></span>](imapiprop-getprops.md) <br/> |<span data-ttu-id="30055-127">Récupère la valeur de propriété d’une ou plusieurs propriétés d’un objet.</span><span class="sxs-lookup"><span data-stu-id="30055-127">Retrieves the property value of one or more properties of an object.</span></span>  <br/> |
|[<span data-ttu-id="30055-128">GetPropList</span><span class="sxs-lookup"><span data-stu-id="30055-128">GetPropList</span></span>](imapiprop-getproplist.md) <br/> |<span data-ttu-id="30055-129">Renvoie les balises de propriété pour toutes les propriétés.</span><span class="sxs-lookup"><span data-stu-id="30055-129">Returns property tags for all properties.</span></span>  <br/> |
|[<span data-ttu-id="30055-130">OpenProperty</span><span class="sxs-lookup"><span data-stu-id="30055-130">OpenProperty</span></span>](imapiprop-openproperty.md) <br/> |<span data-ttu-id="30055-131">Retourne un pointeur vers une interface qui peut être utilisée pour accéder à une propriété.</span><span class="sxs-lookup"><span data-stu-id="30055-131">Returns a pointer to an interface that can be used to access a property.</span></span>  <br/> |
|[<span data-ttu-id="30055-132">SetProps</span><span class="sxs-lookup"><span data-stu-id="30055-132">SetProps</span></span>](imapiprop-setprops.md) <br/> |<span data-ttu-id="30055-133">Met à jour une ou plusieurs propriétés.</span><span class="sxs-lookup"><span data-stu-id="30055-133">Updates one or more properties.</span></span>  <br/> |
|[<span data-ttu-id="30055-134">DeleteProps</span><span class="sxs-lookup"><span data-stu-id="30055-134">DeleteProps</span></span>](imapiprop-deleteprops.md) <br/> |<span data-ttu-id="30055-135">Supprime une ou plusieurs propriétés d’un objet.</span><span class="sxs-lookup"><span data-stu-id="30055-135">Deletes one or more properties from an object.</span></span>  <br/> |
|[<span data-ttu-id="30055-136">CopyTo</span><span class="sxs-lookup"><span data-stu-id="30055-136">CopyTo</span></span>](imapiprop-copyto.md) <br/> |<span data-ttu-id="30055-137">Copie ou déplace toutes les propriétés, à l’exception de spécifiquement des propriétés exclues.</span><span class="sxs-lookup"><span data-stu-id="30055-137">Copies or moves all properties, except for specifically excluded properties.</span></span>  <br/> |
|[<span data-ttu-id="30055-138">CopyProps</span><span class="sxs-lookup"><span data-stu-id="30055-138">CopyProps</span></span>](imapiprop-copyprops.md) <br/> |<span data-ttu-id="30055-139">Copie ou déplace des propriétés sélectionnées.</span><span class="sxs-lookup"><span data-stu-id="30055-139">Copies or moves selected properties.</span></span>  <br/> |
|[<span data-ttu-id="30055-140">GetNamesFromIDs</span><span class="sxs-lookup"><span data-stu-id="30055-140">GetNamesFromIDs</span></span>](imapiprop-getnamesfromids.md) <br/> |<span data-ttu-id="30055-141">Fournit les noms des propriétés qui correspondent à un ou plusieurs identificateurs de propriété.</span><span class="sxs-lookup"><span data-stu-id="30055-141">Provides the property names that correspond to one or more property identifiers.</span></span>  <br/> |
|[<span data-ttu-id="30055-142">GetIDsFromNames</span><span class="sxs-lookup"><span data-stu-id="30055-142">GetIDsFromNames</span></span>](imapiprop-getidsfromnames.md) <br/> |<span data-ttu-id="30055-143">Fournit les identificateurs de propriété qui correspondent à un ou plusieurs noms de propriété.</span><span class="sxs-lookup"><span data-stu-id="30055-143">Provides the property identifiers that correspond to one or more property names.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="30055-144">Remarques</span><span class="sxs-lookup"><span data-stu-id="30055-144">Remarks</span></span>

 <span data-ttu-id="30055-145">**IMAPIProp** est l’interface de base pour les interfaces suivantes :</span><span class="sxs-lookup"><span data-stu-id="30055-145">**IMAPIProp** is the base interface for the following interfaces:</span></span> 
  
- [<span data-ttu-id="30055-146">IAttach</span><span class="sxs-lookup"><span data-stu-id="30055-146">IAttach</span></span>](iattachimapiprop.md)
    
- [<span data-ttu-id="30055-147">IMailUser</span><span class="sxs-lookup"><span data-stu-id="30055-147">IMailUser</span></span>](imailuserimapiprop.md)
    
- [<span data-ttu-id="30055-148">IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="30055-148">IMAPIContainer</span></span>](imapicontainerimapiprop.md)
    
- [<span data-ttu-id="30055-149">IMAPIFormInfo</span><span class="sxs-lookup"><span data-stu-id="30055-149">IMAPIFormInfo</span></span>](imapiforminfoimapiprop.md)
    
- [<span data-ttu-id="30055-150">IMAPIStatus</span><span class="sxs-lookup"><span data-stu-id="30055-150">IMAPIStatus</span></span>](imapistatusimapiprop.md)
    
- [<span data-ttu-id="30055-151">IMessage</span><span class="sxs-lookup"><span data-stu-id="30055-151">IMessage</span></span>](imessageimapiprop.md)
    
- [<span data-ttu-id="30055-152">IMsgStore</span><span class="sxs-lookup"><span data-stu-id="30055-152">IMsgStore</span></span>](imsgstoreimapiprop.md)
    
- [<span data-ttu-id="30055-153">IProfSect</span><span class="sxs-lookup"><span data-stu-id="30055-153">IProfSect</span></span>](iprofsectimapiprop.md)
    
- [<span data-ttu-id="30055-154">IPropData</span><span class="sxs-lookup"><span data-stu-id="30055-154">IPropData</span></span>](ipropdataimapiprop.md)
    
## <a name="see-also"></a><span data-ttu-id="30055-155">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="30055-155">See also</span></span>



[<span data-ttu-id="30055-156">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="30055-156">MAPI Interfaces</span></span>](mapi-interfaces.md)

