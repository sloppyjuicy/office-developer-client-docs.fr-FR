---
title: IAddrBookCreateOneOff
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAddrBook.CreateOneOff
api_type:
- COM
ms.assetid: bcacfbdf-edff-4810-a985-e6d2c9271901
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: ddb87af4b14be6d728bcceddb4d958ba49229ad4
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579038"
---
# <a name="iaddrbookcreateoneoff"></a><span data-ttu-id="b8f59-103">IAddrBook::CreateOneOff</span><span class="sxs-lookup"><span data-stu-id="b8f59-103">IAddrBook::CreateOneOff</span></span>

  
  
<span data-ttu-id="b8f59-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b8f59-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b8f59-105">Crée un identificateur d’entrée pour une adresse unique.</span><span class="sxs-lookup"><span data-stu-id="b8f59-105">Creates an entry identifier for a one-off address.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="b8f59-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b8f59-106">Parameters</span></span>

 <span data-ttu-id="b8f59-107">_Caractère_</span><span class="sxs-lookup"><span data-stu-id="b8f59-107">_lpszName_</span></span>
  
> <span data-ttu-id="b8f59-108">[in] Pointeur vers la valeur de la propriété du destinataire **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="b8f59-108">[in] A pointer to the value of the recipient's **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property.</span></span> <span data-ttu-id="b8f59-109">Le paramètre _le caractère_ peut être NULL.</span><span class="sxs-lookup"><span data-stu-id="b8f59-109">The  _lpszName_ parameter can be NULL.</span></span> 
    
 <span data-ttu-id="b8f59-110">_lpszAdrType_</span><span class="sxs-lookup"><span data-stu-id="b8f59-110">_lpszAdrType_</span></span>
  
> <span data-ttu-id="b8f59-111">[in] Pointeur vers le type d’adresse du destinataire, tel que FAX ou SMTP.</span><span class="sxs-lookup"><span data-stu-id="b8f59-111">[in] A pointer to the address type of the recipient, such as FAX or SMTP.</span></span> <span data-ttu-id="b8f59-112">Le paramètre _lpszAdrType_ ne peut pas être NULL.</span><span class="sxs-lookup"><span data-stu-id="b8f59-112">The  _lpszAdrType_ parameter cannot be NULL.</span></span> 
    
 <span data-ttu-id="b8f59-113">_lpszAddress_</span><span class="sxs-lookup"><span data-stu-id="b8f59-113">_lpszAddress_</span></span>
  
> <span data-ttu-id="b8f59-114">[in] Pointeur vers l’adresse du destinataire.</span><span class="sxs-lookup"><span data-stu-id="b8f59-114">[in] A pointer to the address of the recipient.</span></span> <span data-ttu-id="b8f59-115">Le paramètre _lpszAddress_ ne peut pas être NULL.</span><span class="sxs-lookup"><span data-stu-id="b8f59-115">The  _lpszAddress_ parameter cannot be NULL.</span></span> 
    
 <span data-ttu-id="b8f59-116">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="b8f59-116">_ulFlags_</span></span>
  
> <span data-ttu-id="b8f59-117">[in] Masque de bits d’indicateurs influençant le destinataire unique.</span><span class="sxs-lookup"><span data-stu-id="b8f59-117">[in] A bitmask of flags that affects the one-off recipient.</span></span> <span data-ttu-id="b8f59-118">Les indicateurs suivants peuvent être définis :</span><span class="sxs-lookup"><span data-stu-id="b8f59-118">The following flags can be set:</span></span>
    
<span data-ttu-id="b8f59-119">MAPI_SEND_NO_RICH_INFO</span><span class="sxs-lookup"><span data-stu-id="b8f59-119">MAPI_SEND_NO_RICH_INFO</span></span> 
  
> <span data-ttu-id="b8f59-120">Le destinataire ne peut pas gérer le contenu des messages mis en forme.</span><span class="sxs-lookup"><span data-stu-id="b8f59-120">The recipient cannot handle formatted message content.</span></span> <span data-ttu-id="b8f59-121">Si MAPI_SEND_NO_RICH_INFO est défini, MAPI définit la propriété du destinataire **PR_SEND_RICH_INFO** ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)) sur FALSE.</span><span class="sxs-lookup"><span data-stu-id="b8f59-121">If MAPI_SEND_NO_RICH_INFO is set, MAPI sets the recipient's **PR_SEND_RICH_INFO** ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)) property to FALSE.</span></span> <span data-ttu-id="b8f59-122">Si MAPI_SEND_NO_RICH_INFO n’est pas définie, MAPI définit cette propriété sur TRUE, sauf si l’adresse de messagerie du destinataire désigné par _lpszAddress_ est interprétée comme une adresse Internet.</span><span class="sxs-lookup"><span data-stu-id="b8f59-122">If MAPI_SEND_NO_RICH_INFO is not set, MAPI sets this property to TRUE unless the recipient's messaging address pointed to by  _lpszAddress_ is interpreted to be an Internet address.</span></span> <span data-ttu-id="b8f59-123">Dans ce cas, MAPI définit **PR_SEND_RICH_INFO** sur FALSE.</span><span class="sxs-lookup"><span data-stu-id="b8f59-123">In this case, MAPI sets **PR_SEND_RICH_INFO** to FALSE.</span></span> 
    
<span data-ttu-id="b8f59-124">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="b8f59-124">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="b8f59-125">Le nom complet, le type d’adresse et l’adresse sont au format Unicode.</span><span class="sxs-lookup"><span data-stu-id="b8f59-125">The display name, address type, and address are in Unicode format.</span></span> <span data-ttu-id="b8f59-126">Si l’indicateur MAPI_UNICODE n’est pas défini, ces chaînes sont au format ANSI.</span><span class="sxs-lookup"><span data-stu-id="b8f59-126">If the MAPI_UNICODE flag is not set, these strings are in ANSI format.</span></span>
    
 <span data-ttu-id="b8f59-127">_lpcbEntryID_</span><span class="sxs-lookup"><span data-stu-id="b8f59-127">_lpcbEntryID_</span></span>
  
> <span data-ttu-id="b8f59-128">[out] Pointeur vers le nombre d’octets dans l’identificateur d’entrée indiqué par le paramètre _lppEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="b8f59-128">[out] A pointer to the byte count in the entry identifier pointed to by the  _lppEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="b8f59-129">_lppEntryID_</span><span class="sxs-lookup"><span data-stu-id="b8f59-129">_lppEntryID_</span></span>
  
> <span data-ttu-id="b8f59-130">[out] Pointeur vers un pointeur vers l’identificateur d’entrée pour le destinataire unique.</span><span class="sxs-lookup"><span data-stu-id="b8f59-130">[out] A pointer to a pointer to the entry identifier for the one-off recipient.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="b8f59-131">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="b8f59-131">Return value</span></span>

<span data-ttu-id="b8f59-132">S_OK</span><span class="sxs-lookup"><span data-stu-id="b8f59-132">S_OK</span></span> 
  
> <span data-ttu-id="b8f59-133">L’identificateur d’entrée unique a été créé avec succès.</span><span class="sxs-lookup"><span data-stu-id="b8f59-133">The one-off entry identifier was created successfully.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="b8f59-134">Remarques</span><span class="sxs-lookup"><span data-stu-id="b8f59-134">Remarks</span></span>

<span data-ttu-id="b8f59-135">Les clients appeler la méthode **CreateOneOff** pour créer un identificateur d’entrée pour un destinataire unique, un destinataire qui n’appartient pas à tous les conteneurs à partir des fournisseurs de carnet d’adresses actuellement chargée.</span><span class="sxs-lookup"><span data-stu-id="b8f59-135">Clients call the **CreateOneOff** method to create an entry identifier for a one-off recipient — a recipient that does not belong to any of the containers from any of the currently loaded address book providers.</span></span> <span data-ttu-id="b8f59-136">Destinataires uniques peuvent avoir n’importe quel type d’adresse est prise en charge par un des fournisseurs de carnet d’adresses actif pour la session.</span><span class="sxs-lookup"><span data-stu-id="b8f59-136">One-off recipients can have any kind of address that is supported by one of the active address book providers for the session.</span></span> 
  
<span data-ttu-id="b8f59-137">Destinataires uniques sont généralement créés avec un modèle pour leur type d’adresse spécifique.</span><span class="sxs-lookup"><span data-stu-id="b8f59-137">One-off recipients are typically created with a template for their particular address type.</span></span> <span data-ttu-id="b8f59-138">Le fournisseur de carnet d’adresses qui prend en charge le type d’adresse fournit le modèle.</span><span class="sxs-lookup"><span data-stu-id="b8f59-138">The address book provider that supports the address type supplies the template.</span></span> <span data-ttu-id="b8f59-139">Un utilisateur d’une application cliente entre les informations appropriées dans le modèle.</span><span class="sxs-lookup"><span data-stu-id="b8f59-139">A user of a client application enters the relevant information into the template.</span></span>
  
<span data-ttu-id="b8f59-140">MAPI prend en charge les chaînes de caractères Unicode pour le nom complet, type d’adresse et les paramètres d’adresse de **CreateOneOff**.</span><span class="sxs-lookup"><span data-stu-id="b8f59-140">MAPI supports Unicode character strings for the display name, address type, and address parameters of **CreateOneOff**.</span></span>
  
<span data-ttu-id="b8f59-141">L’indicateur MAPI_SEND_NO_RICH_INFO contrôle si le texte mis en forme au format RTF (RICH Text Format) est envoyé avec chaque message.</span><span class="sxs-lookup"><span data-stu-id="b8f59-141">The MAPI_SEND_NO_RICH_INFO flag controls whether formatted text in Rich Text Format (RTF) is sent along with each message.</span></span> <span data-ttu-id="b8f59-142">Le Neutral Encapsulation Format TNEF (Transport) : un format qui est utilisé pour la transmission de texte mis en forme — envoyée par la plupart des fournisseurs de transport, quelle que soit la façon dont le destinataire définit sa propriété **PR_SEND_RICH_INFO** .</span><span class="sxs-lookup"><span data-stu-id="b8f59-142">The Transport Neutral Encapsulation Format (TNEF) — a format that is used for transmitting formatted text — is sent by most transport providers, regardless of how the recipient sets its **PR_SEND_RICH_INFO** property.</span></span> <span data-ttu-id="b8f59-143">Il n’est pas un problème pour les clients qui fonctionnent avec les messages interpersonnels de messagerie.</span><span class="sxs-lookup"><span data-stu-id="b8f59-143">This is not an issue for messaging clients that work with interpersonal messages.</span></span> <span data-ttu-id="b8f59-144">Toutefois, étant donné que TNEF est généralement utilisé pour envoyer des propriétés personnalisées pour les classes de message personnalisées, non prise en charge peut être un problème pour les clients basés sur les formulaires ou les clients qui requièrent des propriétés MAPI personnalisées.</span><span class="sxs-lookup"><span data-stu-id="b8f59-144">However, because TNEF is typically used to send custom properties for custom message classes, not supporting it can be a problem for form-based clients or clients that require custom MAPI properties.</span></span> <span data-ttu-id="b8f59-145">Pour plus d’informations, consultez [Envoi de Messages avec TNEF](sending-messages-with-tnef.md).</span><span class="sxs-lookup"><span data-stu-id="b8f59-145">For more information, see [Sending Messages with TNEF](sending-messages-with-tnef.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="b8f59-146">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="b8f59-146">MFCMAPI reference</span></span>

<span data-ttu-id="b8f59-147">Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="b8f59-147">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="b8f59-148">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="b8f59-148">**File**</span></span>|<span data-ttu-id="b8f59-149">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="b8f59-149">**Function**</span></span>|<span data-ttu-id="b8f59-150">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="b8f59-150">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="b8f59-151">Mapiabfunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="b8f59-151">Mapiabfunctions.cpp</span></span>  <br/> |<span data-ttu-id="b8f59-152">AddOneOffAddress</span><span class="sxs-lookup"><span data-stu-id="b8f59-152">AddOneOffAddress</span></span>  <br/> |<span data-ttu-id="b8f59-153">MFCMAPI utilise la méthode **CreateOneOff** pour créer un ID d’entrée pour une adresse qui ne figure pas dans un carnet d’adresses.</span><span class="sxs-lookup"><span data-stu-id="b8f59-153">MFCMAPI uses the **CreateOneOff** method to create an entry ID for an address that is not found in any address book.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b8f59-154">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b8f59-154">See also</span></span>



[<span data-ttu-id="b8f59-155">IMAPISupport::CreateOneOff</span><span class="sxs-lookup"><span data-stu-id="b8f59-155">IMAPISupport::CreateOneOff</span></span>](imapisupport-createoneoff.md)
  
[<span data-ttu-id="b8f59-156">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="b8f59-156">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)


[<span data-ttu-id="b8f59-157">MFCMAPI comme un exemple de Code</span><span class="sxs-lookup"><span data-stu-id="b8f59-157">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

