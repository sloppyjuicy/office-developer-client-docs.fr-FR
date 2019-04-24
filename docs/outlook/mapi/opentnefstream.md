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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 524b52026010b9a06d5822b48b7c04bbf90a113e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348922"
---
# <a name="opentnefstream"></a><span data-ttu-id="a01a3-103">OpenTnefStream</span><span class="sxs-lookup"><span data-stu-id="a01a3-103">OpenTnefStream</span></span>

<span data-ttu-id="a01a3-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a01a3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a01a3-105">Appelé par un fournisseur de transport pour lancer une session TNEF (Transport Neutral Encapsulation Format) MAPI.</span><span class="sxs-lookup"><span data-stu-id="a01a3-105">Called by a transport provider to initiate a MAPI Transport Neutral Encapsulation Format (TNEF) session.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a01a3-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="a01a3-106">Header file:</span></span>  <br/> |<span data-ttu-id="a01a3-107">TNEF. h</span><span class="sxs-lookup"><span data-stu-id="a01a3-107">Tnef.h</span></span>  <br/> |
|<span data-ttu-id="a01a3-108">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="a01a3-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="a01a3-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="a01a3-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="a01a3-110">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="a01a3-110">Called by:</span></span>  <br/> |<span data-ttu-id="a01a3-111">Fournisseurs de transport</span><span class="sxs-lookup"><span data-stu-id="a01a3-111">Transport providers</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="a01a3-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a01a3-112">Parameters</span></span>

<span data-ttu-id="a01a3-113">_lpvSupport_</span><span class="sxs-lookup"><span data-stu-id="a01a3-113">_lpvSupport_</span></span>
  
> <span data-ttu-id="a01a3-114">dans Transmet un objet support ou transmet une valeur NULL.</span><span class="sxs-lookup"><span data-stu-id="a01a3-114">[in] Passes a support object, or passes in NULL.</span></span> 
    
<span data-ttu-id="a01a3-115">_lpStream_</span><span class="sxs-lookup"><span data-stu-id="a01a3-115">_lpStream_</span></span>
  
> <span data-ttu-id="a01a3-116">dans Pointeur vers une interface OLE **IStream** d'objet de flux de stockage fournissant une source ou une destination pour un message de flux TNEF.</span><span class="sxs-lookup"><span data-stu-id="a01a3-116">[in] Pointer to a storage stream object OLE **IStream** interface providing a source or destination for a TNEF stream message.</span></span> 
    
<span data-ttu-id="a01a3-117">_lpszStreamName_</span><span class="sxs-lookup"><span data-stu-id="a01a3-117">_lpszStreamName_</span></span>
  
> <span data-ttu-id="a01a3-118">dans Pointeur vers le nom du flux de données que l'objet TNEF utilise.</span><span class="sxs-lookup"><span data-stu-id="a01a3-118">[in] Pointer to the name of the data stream that the TNEF object uses.</span></span> <span data-ttu-id="a01a3-119">Si l'appelant a défini l'indicateur TNEF_ENCODE (paramètre _ulFlags_ ) dans son appel à **OpenTnefStream**, le paramètre _lpszName_ doit spécifier un pointeur non null vers une chaîne non null constituée de tous les caractères considérés comme valides pour l'attribution d'un nom à un fichier.</span><span class="sxs-lookup"><span data-stu-id="a01a3-119">If the caller has set the TNEF_ENCODE flag ( _ulFlags_ parameter) in its call to **OpenTnefStream**, the  _lpszName_ parameter must specify a non-null pointer to a non-null string consisting of any characters considered valid for naming a file.</span></span> <span data-ttu-id="a01a3-120">MAPI n'autorise pas les noms de chaînes, y compris les caractères «[», «]» ou «:», même si le système de fichiers autorise leur utilisation.</span><span class="sxs-lookup"><span data-stu-id="a01a3-120">MAPI does not allow string names including the characters "[", "]", or ":", even if the file system permits their use.</span></span> <span data-ttu-id="a01a3-121">La taille de la chaîne transmise pour _lpszName_ ne doit pas dépasser la valeur de MAX_PATH, la longueur maximale d'une chaîne contenant un nom de chemin d'accès.</span><span class="sxs-lookup"><span data-stu-id="a01a3-121">The size of the string passed for  _lpszName_ must not exceed the value of MAX_PATH, the maximum length of a string that contains a path name.</span></span> 
    
<span data-ttu-id="a01a3-122">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="a01a3-122">_ulFlags_</span></span>
  
> <span data-ttu-id="a01a3-123">dans Masque de des indicateurs utilisé pour indiquer le mode de la fonction.</span><span class="sxs-lookup"><span data-stu-id="a01a3-123">[in] Bitmask of flags used to indicate the mode of the function.</span></span> <span data-ttu-id="a01a3-124">Les indicateurs suivants peuvent être définis:</span><span class="sxs-lookup"><span data-stu-id="a01a3-124">The following flags can be set:</span></span>
    
<span data-ttu-id="a01a3-125">TNEF_BEST_DATA</span><span class="sxs-lookup"><span data-stu-id="a01a3-125">TNEF_BEST_DATA</span></span> 
  
> <span data-ttu-id="a01a3-126">Toutes les propriétés possibles sont mappées dans leurs attributs de bas niveau, mais en cas de perte de données possible en raison de la conversion en un attribut de bas niveau, la propriété est également codée dans les encapsulations.</span><span class="sxs-lookup"><span data-stu-id="a01a3-126">All possible properties are mapped into their down-level attributes, but when there is a possible data loss due to the conversion to a down-level attribute, the property is also encoded in the encapsulations.</span></span> <span data-ttu-id="a01a3-127">Notez que cette opération entraînera la duplication des informations dans le flux TNEF.</span><span class="sxs-lookup"><span data-stu-id="a01a3-127">Note that this will cause the duplication of information in the TNEF stream.</span></span> <span data-ttu-id="a01a3-128">TNEF_BEST_DATA est la valeur par défaut si aucun autre mode n'est spécifié.</span><span class="sxs-lookup"><span data-stu-id="a01a3-128">TNEF_BEST_DATA is the default if no other modes are specified.</span></span> 
    
<span data-ttu-id="a01a3-129">TNEF_COMPATIBILITY</span><span class="sxs-lookup"><span data-stu-id="a01a3-129">TNEF_COMPATIBILITY</span></span> 
  
> <span data-ttu-id="a01a3-130">Fournit une compatibilité descendante avec les applications clientes plus anciennes.</span><span class="sxs-lookup"><span data-stu-id="a01a3-130">Provides backward compatibility with the older client applications.</span></span> <span data-ttu-id="a01a3-131">Les flux TNEF codés avec cet indicateur mappent toutes les propriétés possibles dans leur attribut de bas niveau correspondant.</span><span class="sxs-lookup"><span data-stu-id="a01a3-131">TNEF streams encoded with this flag will map all possible properties into their corresponding down-level attribute.</span></span> <span data-ttu-id="a01a3-132">Ce mode provoque également la valeur par défaut de certaines propriétés requises par les clients de bas niveau.</span><span class="sxs-lookup"><span data-stu-id="a01a3-132">This mode also causes the defaulting of some properties that are required by down-level clients.</span></span> 
    
  > [!CAUTION]
  > <span data-ttu-id="a01a3-133">Cet indicateur est obsolète et ne doit pas être utilisé.</span><span class="sxs-lookup"><span data-stu-id="a01a3-133">This flag is obsolete and should not be used.</span></span> 
  
<span data-ttu-id="a01a3-134">TNEF_DECODE</span><span class="sxs-lookup"><span data-stu-id="a01a3-134">TNEF_DECODE</span></span> 
  
> <span data-ttu-id="a01a3-135">L'objet TNEF sur le flux indiqué est ouvert avec un accès en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="a01a3-135">The TNEF object on the indicated stream is opened with read-only access.</span></span> <span data-ttu-id="a01a3-136">Le fournisseur de transport doit définir cet indicateur s'il souhaite que la fonction initialise l'objet pour un décodage ultérieur.</span><span class="sxs-lookup"><span data-stu-id="a01a3-136">The transport provider must set this flag if it wants the function to initialize the object for subsequent decoding.</span></span>
    
<span data-ttu-id="a01a3-137">TNEF_ENCODE</span><span class="sxs-lookup"><span data-stu-id="a01a3-137">TNEF_ENCODE</span></span> 
  
> <span data-ttu-id="a01a3-138">L'objet TNEF sur le flux indiqué est ouvert en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="a01a3-138">The TNEF object on the indicated stream is opened for read/write permission.</span></span> <span data-ttu-id="a01a3-139">Le fournisseur de transport doit définir cet indicateur s'il souhaite que la fonction initialise l'objet pour le codage suivant.</span><span class="sxs-lookup"><span data-stu-id="a01a3-139">The transport provider must set this flag if it wants the function to initialize the object for subsequent encoding.</span></span>
    
<span data-ttu-id="a01a3-140">TNEF_PURE</span><span class="sxs-lookup"><span data-stu-id="a01a3-140">TNEF_PURE</span></span> 
  
> <span data-ttu-id="a01a3-141">Encode toutes les propriétés dans les blocs d'encapsulation MAPI.</span><span class="sxs-lookup"><span data-stu-id="a01a3-141">Encodes all properties into the MAPI encapsulation blocks.</span></span> <span data-ttu-id="a01a3-142">Par conséquent, un fichier TNEF «pur» se compose au plus des attMAPIProps, attAttachment, attRenddata et attRecipTable.</span><span class="sxs-lookup"><span data-stu-id="a01a3-142">Therefore, a "pure" TNEF file will consist of, at most, attMAPIProps, attAttachment, attRenddata, and attRecipTable.</span></span> <span data-ttu-id="a01a3-143">Ce mode est idéal pour une utilisation sans compatibilité descendante.</span><span class="sxs-lookup"><span data-stu-id="a01a3-143">This mode is ideal for use when no backward compatibility is required.</span></span>
    
<span data-ttu-id="a01a3-144">_lpMessage_</span><span class="sxs-lookup"><span data-stu-id="a01a3-144">_lpMessage_</span></span>
  
> <span data-ttu-id="a01a3-145">dans Pointeur vers un objet message comme destination d'un message décodé avec des pièces jointes ou une source pour un message encodé avec des pièces jointes.</span><span class="sxs-lookup"><span data-stu-id="a01a3-145">[in] Pointer to a message object as a destination for a decoded message with attachments or a source for an encoded message with attachments.</span></span> <span data-ttu-id="a01a3-146">Toutes les propriétés d'un message de destination peuvent être remplacées par les propriétés d'un message encodé.</span><span class="sxs-lookup"><span data-stu-id="a01a3-146">Any properties of a destination message might be overwritten by the properties of an encoded message.</span></span>
    
<span data-ttu-id="a01a3-147">_wKey_</span><span class="sxs-lookup"><span data-stu-id="a01a3-147">_wKey_</span></span>
  
> <span data-ttu-id="a01a3-148">dans Clé de recherche utilisée par l'objet TNEF pour faire correspondre les pièces jointes aux balises de texte insérées dans le texte du message.</span><span class="sxs-lookup"><span data-stu-id="a01a3-148">[in] A search key that the TNEF object uses to match attachments to the text tags inserted in the message text.</span></span> <span data-ttu-id="a01a3-149">Cette valeur doit être relativement unique dans les messages.</span><span class="sxs-lookup"><span data-stu-id="a01a3-149">This value should be relatively unique across messages.</span></span>
    
<span data-ttu-id="a01a3-150">_lppTNEF_</span><span class="sxs-lookup"><span data-stu-id="a01a3-150">_lppTNEF_</span></span>
  
> <span data-ttu-id="a01a3-151">remarquer Pointeur vers le nouvel objet TNEF.</span><span class="sxs-lookup"><span data-stu-id="a01a3-151">[out] Pointer to the new TNEF object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="a01a3-152">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="a01a3-152">Return value</span></span>

<span data-ttu-id="a01a3-153">S_OK</span><span class="sxs-lookup"><span data-stu-id="a01a3-153">S_OK</span></span> 
  
> <span data-ttu-id="a01a3-154">L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.</span><span class="sxs-lookup"><span data-stu-id="a01a3-154">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="a01a3-155">Remarques</span><span class="sxs-lookup"><span data-stu-id="a01a3-155">Remarks</span></span>

<span data-ttu-id="a01a3-156">Un objet TNEF créé par la fonction **OpenTnefStream** appelle ensuite la méthode OLE **IUnknown:: AddRef** pour ajouter des références pour l'objet de prise en charge, l'objet Stream et l'objet message.</span><span class="sxs-lookup"><span data-stu-id="a01a3-156">A TNEF object created by the **OpenTnefStream** function later calls the OLE method **IUnknown::AddRef** to add references for the support object, the stream object, and the message object.</span></span> <span data-ttu-id="a01a3-157">Le fournisseur de transport peut libérer les références pour les trois objets avec un seul appel à la méthode OLE **IUnknown:: Release** sur l'objet TNEF.</span><span class="sxs-lookup"><span data-stu-id="a01a3-157">The transport provider can release the references for all three objects with a single call to the OLE method **IUnknown::Release** on the TNEF object.</span></span> 
  
<span data-ttu-id="a01a3-158">**OpenTnefStream** alloue et Initialise une interface **ITNEF** d'objets TNEF que le fournisseur doit utiliser pour coder une interface **IMessage** de message MAPI en un message de flux TNEF.</span><span class="sxs-lookup"><span data-stu-id="a01a3-158">**OpenTnefStream** allocates and initializes a TNEF object **ITnef** interface for the provider to use in encoding a MAPI message **IMessage** interface into a TNEF stream message.</span></span> <span data-ttu-id="a01a3-159">La fonction peut également configurer l'objet pour le fournisseur à utiliser dans les appels ultérieurs à [ITnef:: ExtractProps](itnef-extractprops.md) pour décoder un message TNEF en flux TNEF dans un message MAPI.</span><span class="sxs-lookup"><span data-stu-id="a01a3-159">Alternatively, the function can set up the object for the provider to use in subsequent calls to [ITnef::ExtractProps](itnef-extractprops.md) to decode a TNEF stream message into a MAPI message.</span></span> <span data-ttu-id="a01a3-160">Pour libérer l'objet TNEF et fermer la session, le fournisseur de transport doit appeler la méthode **IUnknown:: Release** héritée sur l'objet.</span><span class="sxs-lookup"><span data-stu-id="a01a3-160">To free the TNEF object and close the session, the transport provider must call the inherited **IUnknown::Release** method on the object.</span></span> 
  
<span data-ttu-id="a01a3-161">Cette fonction est le point d'entrée d'origine pour l'accès TNEF et a été remplacée par [OpenTnefStreamEx](opentnefstreamex.md) mais est toujours utilisée pour la compatibilité pour ceux qui utilisent déjà TNEF.</span><span class="sxs-lookup"><span data-stu-id="a01a3-161">This function is the original entry point for TNEF access and has been replaced by [OpenTnefStreamEx](opentnefstreamex.md) but is still used for compatibility for those already using TNEF.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="a01a3-162">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a01a3-162">See also</span></span>

- [<span data-ttu-id="a01a3-163">IMAPISupport : IUnknown</span><span class="sxs-lookup"><span data-stu-id="a01a3-163">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)
- [<span data-ttu-id="a01a3-164">IXPProvider::TransportLogon</span><span class="sxs-lookup"><span data-stu-id="a01a3-164">IXPProvider::TransportLogon</span></span>](ixpprovider-transportlogon.md)

