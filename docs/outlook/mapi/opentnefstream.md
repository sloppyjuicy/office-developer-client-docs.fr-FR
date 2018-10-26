---
title: OpenTnefStream
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.OpenTnefStream
api_type:
- COM
ms.assetid: 912d7799-53ce-42a7-9fbd-f9a6a3a56047
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: c5abd3a80a9736a4d71525805e4bc38289975c34
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22577806"
---
# <a name="opentnefstream"></a><span data-ttu-id="be90b-103">OpenTnefStream</span><span class="sxs-lookup"><span data-stu-id="be90b-103">OpenTnefStream</span></span>

<span data-ttu-id="be90b-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="be90b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="be90b-105">Appelée par un fournisseur de transport pour initier une session MAPI Neutral Encapsulation Format TNEF (Transport).</span><span class="sxs-lookup"><span data-stu-id="be90b-105">Called by a transport provider to initiate a MAPI Transport Neutral Encapsulation Format (TNEF) session.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="be90b-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="be90b-106">Header file:</span></span>  <br/> |<span data-ttu-id="be90b-107">TNEF.h</span><span class="sxs-lookup"><span data-stu-id="be90b-107">Tnef.h</span></span>  <br/> |
|<span data-ttu-id="be90b-108">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="be90b-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="be90b-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="be90b-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="be90b-110">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="be90b-110">Called by:</span></span>  <br/> |<span data-ttu-id="be90b-111">Fournisseurs de transport</span><span class="sxs-lookup"><span data-stu-id="be90b-111">Transport providers</span></span>  <br/> |
   
```cpp
HRESULT OpenTnefStream(
  LPVOID lpvSupport,
  LPSTREAM lpStream,
  LPSTR lpszStreamName, 
  ULONG ulFlags,
  LPMESSAGE lpMessage,
  WORD wKey,
  LPITNEF FAR * lppTNEF
);
```

## <a name="parameters"></a><span data-ttu-id="be90b-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="be90b-112">Parameters</span></span>

<span data-ttu-id="be90b-113">_lpvSupport_</span><span class="sxs-lookup"><span data-stu-id="be90b-113">_lpvSupport_</span></span>
  
> <span data-ttu-id="be90b-114">[in] Transmet un objet de prise en charge, ou passe NULL.</span><span class="sxs-lookup"><span data-stu-id="be90b-114">[in] Passes a support object, or passes in NULL.</span></span> 
    
<span data-ttu-id="be90b-115">_lpStream_</span><span class="sxs-lookup"><span data-stu-id="be90b-115">_lpStream_</span></span>
  
> <span data-ttu-id="be90b-116">[in] Pointeur vers une flux de données de stockage objet interface OLE **IStream** fournissant une source ou destination d’un message de flux TNEF.</span><span class="sxs-lookup"><span data-stu-id="be90b-116">[in] Pointer to a storage stream object OLE **IStream** interface providing a source or destination for a TNEF stream message.</span></span> 
    
<span data-ttu-id="be90b-117">_lpszStreamName_</span><span class="sxs-lookup"><span data-stu-id="be90b-117">_lpszStreamName_</span></span>
  
> <span data-ttu-id="be90b-118">[in] Pointeur vers le nom du flux de données qui utilise l’objet TNEF.</span><span class="sxs-lookup"><span data-stu-id="be90b-118">[in] Pointer to the name of the data stream that the TNEF object uses.</span></span> <span data-ttu-id="be90b-119">Si l’appelant a défini l’indicateur TNEF_ENCODE (paramètre _ulFlags_ ) l’appel vers **OpenTnefStream**, le paramètre de _caractère_ doit spécifier un pointeur non null à une chaîne non nulle constituée de caractères validités pour un fichier d’attribution de noms.</span><span class="sxs-lookup"><span data-stu-id="be90b-119">If the caller has set the TNEF_ENCODE flag ( _ulFlags_ parameter) in its call to **OpenTnefStream**, the  _lpszName_ parameter must specify a non-null pointer to a non-null string consisting of any characters considered valid for naming a file.</span></span> <span data-ttu-id="be90b-120">MAPI n’autorise pas les noms de chaîne, y compris les caractères « [ », «] », ou « : », même si le système de fichiers permet de leur utilisation.</span><span class="sxs-lookup"><span data-stu-id="be90b-120">MAPI does not allow string names including the characters "[", "]", or ":", even if the file system permits their use.</span></span> <span data-ttu-id="be90b-121">La taille de la chaîne transmise pour _le caractère_ ne doit pas dépasser la valeur de MAX_PATH, la longueur maximale d’une chaîne qui contient un nom de chemin d’accès.</span><span class="sxs-lookup"><span data-stu-id="be90b-121">The size of the string passed for  _lpszName_ must not exceed the value of MAX_PATH, the maximum length of a string that contains a path name.</span></span> 
    
<span data-ttu-id="be90b-122">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="be90b-122">_ulFlags_</span></span>
  
> <span data-ttu-id="be90b-123">[in] Masque de bits d’indicateurs utilisés pour indiquer le mode de la fonction.</span><span class="sxs-lookup"><span data-stu-id="be90b-123">[in] Bitmask of flags used to indicate the mode of the function.</span></span> <span data-ttu-id="be90b-124">Les indicateurs suivants peuvent être définis :</span><span class="sxs-lookup"><span data-stu-id="be90b-124">The following flags can be set:</span></span>
    
<span data-ttu-id="be90b-125">TNEF_BEST_DATA</span><span class="sxs-lookup"><span data-stu-id="be90b-125">TNEF_BEST_DATA</span></span> 
  
> <span data-ttu-id="be90b-126">Toutes les propriétés possibles sont mappées dans leurs attributs de bas niveau, mais lorsqu’il existe une perte de données possible en raison de la conversion à un attribut de bas niveau, la propriété est également codée dans l’encapsule.</span><span class="sxs-lookup"><span data-stu-id="be90b-126">All possible properties are mapped into their down-level attributes, but when there is a possible data loss due to the conversion to a down-level attribute, the property is also encoded in the encapsulations.</span></span> <span data-ttu-id="be90b-127">Notez que cette opération entraîne la duplication des informations sur le flux TNEF.</span><span class="sxs-lookup"><span data-stu-id="be90b-127">Note that this will cause the duplication of information in the TNEF stream.</span></span> <span data-ttu-id="be90b-128">TNEF_BEST_DATA est la valeur par défaut si aucun autre mode n’est spécifiés.</span><span class="sxs-lookup"><span data-stu-id="be90b-128">TNEF_BEST_DATA is the default if no other modes are specified.</span></span> 
    
<span data-ttu-id="be90b-129">TNEF_COMPATIBILITY</span><span class="sxs-lookup"><span data-stu-id="be90b-129">TNEF_COMPATIBILITY</span></span> 
  
> <span data-ttu-id="be90b-130">Fournit une compatibilité descendante avec le client antérieur des applications.</span><span class="sxs-lookup"><span data-stu-id="be90b-130">Provides backward compatibility with the older client applications.</span></span> <span data-ttu-id="be90b-131">Flux TNEF codés avec cet indicateur mappe toutes les propriétés possibles dans leur attribut de bas niveau correspondant.</span><span class="sxs-lookup"><span data-stu-id="be90b-131">TNEF streams encoded with this flag will map all possible properties into their corresponding down-level attribute.</span></span> <span data-ttu-id="be90b-132">Ce mode entraîne également l’utilisation par défaut de certaines propriétés requises par les clients de bas niveau.</span><span class="sxs-lookup"><span data-stu-id="be90b-132">This mode also causes the defaulting of some properties that are required by down-level clients.</span></span> 
    
  > [!CAUTION]
  > <span data-ttu-id="be90b-133">Cet indicateur est obsolète et ne doit pas être utilisé.</span><span class="sxs-lookup"><span data-stu-id="be90b-133">This flag is obsolete and should not be used.</span></span> 
  
<span data-ttu-id="be90b-134">TNEF_DECODE</span><span class="sxs-lookup"><span data-stu-id="be90b-134">TNEF_DECODE</span></span> 
  
> <span data-ttu-id="be90b-135">L’objet TNEF sur le flux indiqué est ouvert avec accès en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="be90b-135">The TNEF object on the indicated stream is opened with read-only access.</span></span> <span data-ttu-id="be90b-136">Le fournisseur de transport doit définir cet indicateur s’il veut que la fonction pour initialiser l’objet de décodage suivantes.</span><span class="sxs-lookup"><span data-stu-id="be90b-136">The transport provider must set this flag if it wants the function to initialize the object for subsequent decoding.</span></span>
    
<span data-ttu-id="be90b-137">TNEF_ENCODE</span><span class="sxs-lookup"><span data-stu-id="be90b-137">TNEF_ENCODE</span></span> 
  
> <span data-ttu-id="be90b-138">Ouverture de l’objet TNEF sur le flux indiqué pour l’autorisation en lecture-écriture.</span><span class="sxs-lookup"><span data-stu-id="be90b-138">The TNEF object on the indicated stream is opened for read/write permission.</span></span> <span data-ttu-id="be90b-139">Le fournisseur de transport doit définir cet indicateur s’il veut que la fonction pour initialiser l’objet de codage suivantes.</span><span class="sxs-lookup"><span data-stu-id="be90b-139">The transport provider must set this flag if it wants the function to initialize the object for subsequent encoding.</span></span>
    
<span data-ttu-id="be90b-140">TNEF_PURE</span><span class="sxs-lookup"><span data-stu-id="be90b-140">TNEF_PURE</span></span> 
  
> <span data-ttu-id="be90b-141">Code toutes les propriétés dans les blocs d’encapsulation MAPI.</span><span class="sxs-lookup"><span data-stu-id="be90b-141">Encodes all properties into the MAPI encapsulation blocks.</span></span> <span data-ttu-id="be90b-142">Par conséquent, un fichier TNEF « pur » sera composée, au plus, attMAPIProps, attAttachment, attRenddata et attRecipTable.</span><span class="sxs-lookup"><span data-stu-id="be90b-142">Therefore, a "pure" TNEF file will consist of, at most, attMAPIProps, attAttachment, attRenddata, and attRecipTable.</span></span> <span data-ttu-id="be90b-143">Ce mode est idéal pour une utilisation lorsque aucune compatibilité descendante n’est nécessaire.</span><span class="sxs-lookup"><span data-stu-id="be90b-143">This mode is ideal for use when no backward compatibility is required.</span></span>
    
<span data-ttu-id="be90b-144">_lpMessage_</span><span class="sxs-lookup"><span data-stu-id="be90b-144">_lpMessage_</span></span>
  
> <span data-ttu-id="be90b-145">[in] Pointeur vers un objet de message comme une destination d’un message décodée avec les pièces jointes ou d’une source d’un message codé avec les pièces jointes.</span><span class="sxs-lookup"><span data-stu-id="be90b-145">[in] Pointer to a message object as a destination for a decoded message with attachments or a source for an encoded message with attachments.</span></span> <span data-ttu-id="be90b-146">Toutes les propriétés d’un message de destination peuvent être remplacées par les propriétés d’un message codé.</span><span class="sxs-lookup"><span data-stu-id="be90b-146">Any properties of a destination message might be overwritten by the properties of an encoded message.</span></span>
    
<span data-ttu-id="be90b-147">_wKey_</span><span class="sxs-lookup"><span data-stu-id="be90b-147">_wKey_</span></span>
  
> <span data-ttu-id="be90b-148">[in] Une clé de recherche que l’objet TNEF utilise pour la correspondance de pièces jointes sur les balises de texte insérés dans le texte du message.</span><span class="sxs-lookup"><span data-stu-id="be90b-148">[in] A search key that the TNEF object uses to match attachments to the text tags inserted in the message text.</span></span> <span data-ttu-id="be90b-149">Cette valeur doit être relativement unique sur les messages.</span><span class="sxs-lookup"><span data-stu-id="be90b-149">This value should be relatively unique across messages.</span></span>
    
<span data-ttu-id="be90b-150">_lppTNEF_</span><span class="sxs-lookup"><span data-stu-id="be90b-150">_lppTNEF_</span></span>
  
> <span data-ttu-id="be90b-151">[out] Pointeur vers le nouvel objet TNEF.</span><span class="sxs-lookup"><span data-stu-id="be90b-151">[out] Pointer to the new TNEF object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="be90b-152">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="be90b-152">Return value</span></span>

<span data-ttu-id="be90b-153">S_OK</span><span class="sxs-lookup"><span data-stu-id="be90b-153">S_OK</span></span> 
  
> <span data-ttu-id="be90b-154">L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.</span><span class="sxs-lookup"><span data-stu-id="be90b-154">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="be90b-155">Remarques</span><span class="sxs-lookup"><span data-stu-id="be90b-155">Remarks</span></span>

<span data-ttu-id="be90b-156">Un objet TNEF créé ultérieurement par la fonction **OpenTnefStream** appelle la méthode OLE **IUnknown::AddRef** pour ajouter des références pour l’objet de prise en charge, l’objet stream et l’objet du message.</span><span class="sxs-lookup"><span data-stu-id="be90b-156">A TNEF object created by the **OpenTnefStream** function later calls the OLE method **IUnknown::AddRef** to add references for the support object, the stream object, and the message object.</span></span> <span data-ttu-id="be90b-157">Le fournisseur de transport permettre libérer les références pour tous les trois objets avec un seul appel à la méthode OLE **IUnknown::Release** sur l’objet TNEF.</span><span class="sxs-lookup"><span data-stu-id="be90b-157">The transport provider can release the references for all three objects with a single call to the OLE method **IUnknown::Release** on the TNEF object.</span></span> 
  
<span data-ttu-id="be90b-158">**OpenTnefStream** alloue et initialise une interface de **ITnef** objet TNEF pour le fournisseur à utiliser dans une interface **IMessage** de message MAPI le codage dans un message de flux TNEF.</span><span class="sxs-lookup"><span data-stu-id="be90b-158">**OpenTnefStream** allocates and initializes a TNEF object **ITnef** interface for the provider to use in encoding a MAPI message **IMessage** interface into a TNEF stream message.</span></span> <span data-ttu-id="be90b-159">La fonction peut également définir l’objet pour le fournisseur à utiliser dans les appels suivants à [ITnef::ExtractProps](itnef-extractprops.md) pour décoder un message de flux TNEF dans un message MAPI.</span><span class="sxs-lookup"><span data-stu-id="be90b-159">Alternatively, the function can set up the object for the provider to use in subsequent calls to [ITnef::ExtractProps](itnef-extractprops.md) to decode a TNEF stream message into a MAPI message.</span></span> <span data-ttu-id="be90b-160">Pour libérer de l’objet TNEF, fermez la session, le fournisseur de transport doit appeler la méthode **IUnknown::Release** héritée sur l’objet.</span><span class="sxs-lookup"><span data-stu-id="be90b-160">To free the TNEF object and close the session, the transport provider must call the inherited **IUnknown::Release** method on the object.</span></span> 
  
<span data-ttu-id="be90b-161">Cette fonction est le point d’entrée d’origine pour l’accès TNEF et a été remplacée par [OpenTnefStreamEx](opentnefstreamex.md) , mais est toujours utilisée pour la compatibilité pour ceux déjà à l’aide de TNEF.</span><span class="sxs-lookup"><span data-stu-id="be90b-161">This function is the original entry point for TNEF access and has been replaced by [OpenTnefStreamEx](opentnefstreamex.md) but is still used for compatibility for those already using TNEF.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="be90b-162">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="be90b-162">See also</span></span>

- [<span data-ttu-id="be90b-163">IMAPISupport : IUnknown</span><span class="sxs-lookup"><span data-stu-id="be90b-163">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)
- [<span data-ttu-id="be90b-164">IXPProvider::TransportLogon</span><span class="sxs-lookup"><span data-stu-id="be90b-164">IXPProvider::TransportLogon</span></span>](ixpprovider-transportlogon.md)

