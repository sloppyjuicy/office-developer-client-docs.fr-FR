---
title: IMAPISupportCreateOneOff
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.CreateOneOff
api_type:
- COM
ms.assetid: ee57d6e0-9de0-4427-97ce-371c1c01f3de
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 1526ed54fd3773856b009c7c3570064f5a66df28
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22594942"
---
# <a name="imapisupportcreateoneoff"></a><span data-ttu-id="f9f91-103">IMAPISupport::CreateOneOff</span><span class="sxs-lookup"><span data-stu-id="f9f91-103">IMAPISupport::CreateOneOff</span></span>

  
  
<span data-ttu-id="f9f91-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f9f91-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f9f91-105">Crée un identificateur d’entrée pour une adresse unique.</span><span class="sxs-lookup"><span data-stu-id="f9f91-105">Creates an entry identifier for a one-off address.</span></span>
  
```cpp
HRESULT CreateOneOff(
  LPSTR lpszName,
  LPSTR lpszAdrType,
  LPSTR lpszAddress,
  ULONG ulFlags,
  ULONG FAR * lpcbEntryID,
  LPENTRYID FAR * lppEntryID
);
```

## <a name="parameters"></a><span data-ttu-id="f9f91-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f9f91-106">Parameters</span></span>

 <span data-ttu-id="f9f91-107">_Caractère_</span><span class="sxs-lookup"><span data-stu-id="f9f91-107">_lpszName_</span></span>
  
> <span data-ttu-id="f9f91-108">[in] Pointeur vers le nom complet du destinataire de la propriété **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="f9f91-108">[in] A pointer to the display name of the recipient the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property.</span></span> <span data-ttu-id="f9f91-109">Le paramètre _le caractère_ peut être NULL.</span><span class="sxs-lookup"><span data-stu-id="f9f91-109">The  _lpszName_ parameter can be NULL.</span></span> 
    
 <span data-ttu-id="f9f91-110">_lpszAdrType_</span><span class="sxs-lookup"><span data-stu-id="f9f91-110">_lpszAdrType_</span></span>
  
> <span data-ttu-id="f9f91-111">[in] Pointeur vers le type d’adresse du destinataire (telles que télécopie, SMTP ou X500).</span><span class="sxs-lookup"><span data-stu-id="f9f91-111">[in] A pointer to the address type (such as FAX, SMTP, or X500) of the recipient.</span></span> <span data-ttu-id="f9f91-112">Le paramètre _lpszAdrType_ ne peut pas être NULL.</span><span class="sxs-lookup"><span data-stu-id="f9f91-112">The  _lpszAdrType_ parameter cannot be NULL.</span></span> 
    
 <span data-ttu-id="f9f91-113">_lpszAddress_</span><span class="sxs-lookup"><span data-stu-id="f9f91-113">_lpszAddress_</span></span>
  
> <span data-ttu-id="f9f91-114">[in] Pointeur vers l’adresse de messagerie du destinataire.</span><span class="sxs-lookup"><span data-stu-id="f9f91-114">[in] A pointer to the messaging address of the recipient.</span></span> <span data-ttu-id="f9f91-115">Le paramètre _lpszAddress_ ne peut pas être NULL.</span><span class="sxs-lookup"><span data-stu-id="f9f91-115">The  _lpszAddress_ parameter cannot be NULL.</span></span> 
    
 <span data-ttu-id="f9f91-116">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="f9f91-116">_ulFlags_</span></span>
  
> <span data-ttu-id="f9f91-117">[in] Masque de bits d’indicateurs influençant le destinataire unique.</span><span class="sxs-lookup"><span data-stu-id="f9f91-117">[in] A bitmask of flags that affects the one-off recipient.</span></span> <span data-ttu-id="f9f91-118">Les indicateurs suivants peuvent être définis :</span><span class="sxs-lookup"><span data-stu-id="f9f91-118">The following flags can be set:</span></span>
    
<span data-ttu-id="f9f91-119">MAPI_SEND_NO_RICH_INFO</span><span class="sxs-lookup"><span data-stu-id="f9f91-119">MAPI_SEND_NO_RICH_INFO</span></span> 
  
> <span data-ttu-id="f9f91-120">Le destinataire ne peut pas gérer le contenu des messages mis en forme.</span><span class="sxs-lookup"><span data-stu-id="f9f91-120">The recipient cannot handle formatted message content.</span></span> <span data-ttu-id="f9f91-121">Si MAPI_SEND_NO_RICH_INFO est défini, MAPI définit la propriété du destinataire **PR_SEND_RICH_INFO** ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)) sur FALSE.</span><span class="sxs-lookup"><span data-stu-id="f9f91-121">If MAPI_SEND_NO_RICH_INFO is set, MAPI sets the recipient's **PR_SEND_RICH_INFO** ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)) property to FALSE.</span></span> <span data-ttu-id="f9f91-122">Si MAPI_SEND_NO_RICH_INFO n’est pas définie, MAPI définit cette propriété sur TRUE, sauf si l’adresse de messagerie du destinataire désigné par _lpszAddress_ est interprétée comme une adresse Internet.</span><span class="sxs-lookup"><span data-stu-id="f9f91-122">If MAPI_SEND_NO_RICH_INFO is not set, MAPI sets this property to TRUE unless the recipient's messaging address pointed to by  _lpszAddress_ is interpreted to be an Internet address.</span></span> <span data-ttu-id="f9f91-123">Dans ce cas, MAPI définit **PR_SEND_RICH_INFO** sur FALSE.</span><span class="sxs-lookup"><span data-stu-id="f9f91-123">In this case, MAPI sets **PR_SEND_RICH_INFO** to FALSE.</span></span> 
    
<span data-ttu-id="f9f91-124">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="f9f91-124">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="f9f91-125">Le nom complet, le type d’adresse et l’adresse sont au format Unicode.</span><span class="sxs-lookup"><span data-stu-id="f9f91-125">The display name, address type, and address are in Unicode format.</span></span> <span data-ttu-id="f9f91-126">Si l’indicateur MAPI_UNICODE n’est pas défini, ces chaînes sont au format ANSI.</span><span class="sxs-lookup"><span data-stu-id="f9f91-126">If the MAPI_UNICODE flag is not set, these strings are in ANSI format.</span></span>
    
 <span data-ttu-id="f9f91-127">_lpcbEntryID_</span><span class="sxs-lookup"><span data-stu-id="f9f91-127">_lpcbEntryID_</span></span>
  
> <span data-ttu-id="f9f91-128">[out] Un pointeur vers le nombre d’octets de l’identificateur d’entrée indiqué par le paramètre _lppEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="f9f91-128">[out] A pointer to the count of bytes in the entry identifier pointed to by the  _lppEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="f9f91-129">_lppEntryID_</span><span class="sxs-lookup"><span data-stu-id="f9f91-129">_lppEntryID_</span></span>
  
> <span data-ttu-id="f9f91-130">[out] Pointeur vers un pointeur vers l’identificateur d’entrée pour le destinataire unique.</span><span class="sxs-lookup"><span data-stu-id="f9f91-130">[out] A pointer to a pointer to the entry identifier for the one-off recipient.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="f9f91-131">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="f9f91-131">Return value</span></span>

<span data-ttu-id="f9f91-132">S_OK</span><span class="sxs-lookup"><span data-stu-id="f9f91-132">S_OK</span></span> 
  
> <span data-ttu-id="f9f91-133">L’identificateur d’entrée unique a été créé avec succès.</span><span class="sxs-lookup"><span data-stu-id="f9f91-133">The one-off entry identifier was successfully created.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="f9f91-134">Remarques</span><span class="sxs-lookup"><span data-stu-id="f9f91-134">Remarks</span></span>

<span data-ttu-id="f9f91-135">La méthode **IMAPISupport::CreateOneOff** est implémentée pour tous les objets de prise en charge de fournisseur de service.</span><span class="sxs-lookup"><span data-stu-id="f9f91-135">The **IMAPISupport::CreateOneOff** method is implemented for all service provider support objects.</span></span> <span data-ttu-id="f9f91-136">Fournisseurs de services d’appel **CreateOneOff** pour créer un identificateur d’entrée pour un destinataire unique (un destinataire qui n’appartient pas à tous les conteneurs à partir des fournisseurs de carnet d’adresses actuellement chargée).</span><span class="sxs-lookup"><span data-stu-id="f9f91-136">Service providers call **CreateOneOff** to create an entry identifier for a one-off recipient (a recipient that does not belong to any of the containers from any of the currently loaded address book providers).</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="f9f91-137">Notes aux appelants</span><span class="sxs-lookup"><span data-stu-id="f9f91-137">Notes to callers</span></span>

<span data-ttu-id="f9f91-138">Lorsque vous avez terminé à l’aide de l’identificateur d’entrée renvoyée par **CreateOneOff**, libérer de la mémoire allouée à l’identificateur d’entrée à l’aide de la fonction [MAPIFreeBuffer](mapifreebuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="f9f91-138">When you are finished using the entry identifier returned by **CreateOneOff**, free the memory allocated for the entry identifier by using the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> 
  
## <a name="notes-to-transport-providers"></a><span data-ttu-id="f9f91-139">Remarques pour les fournisseurs de Transport</span><span class="sxs-lookup"><span data-stu-id="f9f91-139">Notes to Transport Providers</span></span>

<span data-ttu-id="f9f91-140">Prend en charge le Transport Neutral Encapsulation Format TNEF () et la valeur de la propriété **PR_SEND_RICH_INFO** pour déterminer s’il faut utiliser le format TNEF lorsque vous un message de transport.</span><span class="sxs-lookup"><span data-stu-id="f9f91-140">Support the Transport Neutral Encapsulation Format (TNEF) and use the value of the **PR_SEND_RICH_INFO** property to determine whether to use TNEF when you transport a message.</span></span> <span data-ttu-id="f9f91-141">Ne pas de prise en charge TNEF ou ne pas envoyer un message dans ce format, lorsqu’elle est demandée peut être un problème pour les clients basés sur les formulaires ou les clients qui requièrent des propriétés MAPI personnalisées.</span><span class="sxs-lookup"><span data-stu-id="f9f91-141">Not supporting TNEF or not sending a message in this format when it is requested can be a problem for form-based clients or clients that require custom MAPI properties.</span></span> <span data-ttu-id="f9f91-142">Il s’agit, car le format TNEF est généralement utilisé pour envoyer des propriétés personnalisées pour les classes de message personnalisées.</span><span class="sxs-lookup"><span data-stu-id="f9f91-142">This is because TNEF is typically used to send custom properties for custom message classes.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="f9f91-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f9f91-143">See also</span></span>



[<span data-ttu-id="f9f91-144">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="f9f91-144">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="f9f91-145">Propriété canonique PidTagDisplayName</span><span class="sxs-lookup"><span data-stu-id="f9f91-145">PidTagDisplayName Canonical Property</span></span>](pidtagdisplayname-canonical-property.md)
  
[<span data-ttu-id="f9f91-146">Propriété canonique PidTagSendRichInfo</span><span class="sxs-lookup"><span data-stu-id="f9f91-146">PidTagSendRichInfo Canonical Property</span></span>](pidtagsendrichinfo-canonical-property.md)
  
[<span data-ttu-id="f9f91-147">IMAPISupport : IUnknown</span><span class="sxs-lookup"><span data-stu-id="f9f91-147">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

