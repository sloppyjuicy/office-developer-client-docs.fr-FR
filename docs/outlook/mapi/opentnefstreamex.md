---
title: OpenTnefStreamEx
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.OpenTnefStreamEx
api_type:
- COM
ms.assetid: eb84c408-2d8b-453b-92f4-5fd8851b84ca
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 178ab67875d8fb442500dd412dbafe4403deee16
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406240"
---
# <a name="opentnefstreamex"></a><span data-ttu-id="2bfb5-103">OpenTnefStreamEx</span><span class="sxs-lookup"><span data-stu-id="2bfb5-103">OpenTnefStreamEx</span></span>

<span data-ttu-id="2bfb5-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2bfb5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2bfb5-105">Crée un objet TNEF (Transport-Neutral Encapsulation Format) qui peut être utilisé pour encoder ou décoder un objet message dans un flux de données TNEF à des fins d'utilisation par les transports ou les passerelles et les banques de messages.</span><span class="sxs-lookup"><span data-stu-id="2bfb5-105">Creates a Transport-Neutral Encapsulation Format (TNEF) object that can be used to encode or decode a message object into a TNEF data stream for use by transports or gateways and message stores.</span></span> <span data-ttu-id="2bfb5-106">Il s'agit du point d'entrée pour l'accès TNEF.</span><span class="sxs-lookup"><span data-stu-id="2bfb5-106">This is the entry point for TNEF access.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="2bfb5-107">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="2bfb5-107">Header file:</span></span>  <br/> |<span data-ttu-id="2bfb5-108">TNEF. h</span><span class="sxs-lookup"><span data-stu-id="2bfb5-108">Tnef.h</span></span>  <br/> |
|<span data-ttu-id="2bfb5-109">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="2bfb5-109">Implemented by:</span></span>  <br/> |<span data-ttu-id="2bfb5-110">MAPI</span><span class="sxs-lookup"><span data-stu-id="2bfb5-110">MAPI</span></span>  <br/> |
|<span data-ttu-id="2bfb5-111">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="2bfb5-111">Called by:</span></span>  <br/> |<span data-ttu-id="2bfb5-112">Fournisseurs de transport</span><span class="sxs-lookup"><span data-stu-id="2bfb5-112">Transport providers</span></span>  <br/> |
   
```cpp
HRESULT OpenTnefStreamEx(
  LPVOID lpvSupport,
  LPSTREAM lpStream,
  LPSTR lpszStreamName,
  ULONG ulFlags,
  LPMESSAGE lpMessage,
  WORD wKeyVal,
  LPADDRESSBOOK lpAddressBook,
  LPITNEF FAR * lppTNEF
);
```

## <a name="parameters"></a><span data-ttu-id="2bfb5-113">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2bfb5-113">Parameters</span></span>

<span data-ttu-id="2bfb5-114">_lpvSupport_</span><span class="sxs-lookup"><span data-stu-id="2bfb5-114">_lpvSupport_</span></span>
  
> <span data-ttu-id="2bfb5-115">dans Transmet un objet support ou transmet une valeur NULL.</span><span class="sxs-lookup"><span data-stu-id="2bfb5-115">[in] Passes a support object, or passes in NULL.</span></span> <span data-ttu-id="2bfb5-116">Si la valeur est NULL, le paramètre _lpAddressBook_ doit être non null.</span><span class="sxs-lookup"><span data-stu-id="2bfb5-116">If NULL, the  _lpAddressBook_ parameter should be non-null.</span></span> 
    
<span data-ttu-id="2bfb5-117">_lpStream_</span><span class="sxs-lookup"><span data-stu-id="2bfb5-117">_lpStream_</span></span>
  
> <span data-ttu-id="2bfb5-118">dans Pointeur vers un objet de flux de stockage, tel qu'une interface OLE **IStream** , qui fournit une source ou une destination pour un message de flux TNEF.</span><span class="sxs-lookup"><span data-stu-id="2bfb5-118">[in] Pointer to a storage stream object, such as an OLE **IStream** interface, providing a source or destination for a TNEF stream message.</span></span> 
    
<span data-ttu-id="2bfb5-119">_lpszStreamName_</span><span class="sxs-lookup"><span data-stu-id="2bfb5-119">_lpszStreamName_</span></span>
  
> <span data-ttu-id="2bfb5-120">dans Pointeur vers le nom du flux de données que l'objet TNEF utilise.</span><span class="sxs-lookup"><span data-stu-id="2bfb5-120">[in] Pointer to the name of the data stream that the TNEF object uses.</span></span> <span data-ttu-id="2bfb5-121">Si l'appelant a défini l'indicateur TNEF_ENCODE (paramètre _ulFlags_ ) dans son appel à **OpenTnefStream**, le paramètre _lpszName_ doit spécifier un pointeur non null vers une chaîne non null constituée de tous les caractères considérés comme valides pour l'attribution d'un nom à un fichier.</span><span class="sxs-lookup"><span data-stu-id="2bfb5-121">If the caller has set the TNEF_ENCODE flag ( _ulFlags_ parameter) in its call to **OpenTnefStream**, the  _lpszName_ parameter must specify a non-null pointer to a non-null string consisting of any characters considered valid for naming a file.</span></span> <span data-ttu-id="2bfb5-122">MAPI n'autorise pas les noms de chaînes, y compris les caractères «[», «]» ou «:», même si le système de fichiers autorise leur utilisation.</span><span class="sxs-lookup"><span data-stu-id="2bfb5-122">MAPI does not allow string names including the characters "[", "]", or ":", even if the file system permits their use.</span></span> <span data-ttu-id="2bfb5-123">La taille de la chaîne transmise pour le paramètre _lpszName_ ne doit pas dépasser la valeur de MAX_PATH, la longueur maximale d'une chaîne contenant un nom de chemin d'accès.</span><span class="sxs-lookup"><span data-stu-id="2bfb5-123">The size of the string passed for the  _lpszName_ parameter must not exceed the value of MAX_PATH, the maximum length of a string that contains a path name.</span></span> 
    
<span data-ttu-id="2bfb5-124">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="2bfb5-124">_ulFlags_</span></span>
  
> <span data-ttu-id="2bfb5-125">dans Masque de des indicateurs utilisé pour indiquer le mode de la fonction.</span><span class="sxs-lookup"><span data-stu-id="2bfb5-125">[in] Bitmask of flags used to indicate the mode of the function.</span></span> <span data-ttu-id="2bfb5-126">Les indicateurs suivants peuvent être définis:</span><span class="sxs-lookup"><span data-stu-id="2bfb5-126">The following flags can be set:</span></span>
    
<span data-ttu-id="2bfb5-127">TNEF_BEST_DATA</span><span class="sxs-lookup"><span data-stu-id="2bfb5-127">TNEF_BEST_DATA</span></span> 
  
> <span data-ttu-id="2bfb5-128">Toutes les propriétés possibles sont mappées dans leurs attributs de bas niveau, mais en cas de perte de données possible en raison de la conversion en un attribut de bas niveau, la propriété est également codée dans les encapsulations.</span><span class="sxs-lookup"><span data-stu-id="2bfb5-128">All possible properties are mapped into their down-level attributes, but when there is a possible data loss due to the conversion to a down-level attribute, the property is also encoded in the encapsulations.</span></span> <span data-ttu-id="2bfb5-129">Notez que cette opération entraînera la duplication des informations dans le flux TNEF.</span><span class="sxs-lookup"><span data-stu-id="2bfb5-129">Note that this will cause the duplication of information in the TNEF stream.</span></span> <span data-ttu-id="2bfb5-130">TNEF_BEST_DATA est la valeur par défaut si aucun autre mode n'est spécifié.</span><span class="sxs-lookup"><span data-stu-id="2bfb5-130">TNEF_BEST_DATA is the default if no other modes are specified.</span></span> 
    
<span data-ttu-id="2bfb5-131">TNEF_COMPATIBILITY</span><span class="sxs-lookup"><span data-stu-id="2bfb5-131">TNEF_COMPATIBILITY</span></span> 
  
> <span data-ttu-id="2bfb5-132">Fournit une compatibilité descendante avec les applications clientes plus anciennes.</span><span class="sxs-lookup"><span data-stu-id="2bfb5-132">Provides backward compatibility with older client applications.</span></span> <span data-ttu-id="2bfb5-133">Les flux TNEF codés avec cet indicateur mappent toutes les propriétés possibles dans leur attribut de bas niveau correspondant.</span><span class="sxs-lookup"><span data-stu-id="2bfb5-133">TNEF streams encoded with this flag will map all possible properties into their corresponding down-level attribute.</span></span> <span data-ttu-id="2bfb5-134">Ce mode provoque également la valeur par défaut de certaines propriétés requises par les clients de bas niveau.</span><span class="sxs-lookup"><span data-stu-id="2bfb5-134">This mode also causes the defaulting of some properties that are required by down-level clients.</span></span> 
    
  > [!CAUTION]
  > <span data-ttu-id="2bfb5-135">Cet indicateur est obsolète et ne doit pas être utilisé.</span><span class="sxs-lookup"><span data-stu-id="2bfb5-135">This flag is obsolete and should not be used.</span></span> 
  
<span data-ttu-id="2bfb5-136">TNEF_DECODE</span><span class="sxs-lookup"><span data-stu-id="2bfb5-136">TNEF_DECODE</span></span> 
  
> <span data-ttu-id="2bfb5-137">L'objet TNEF sur le flux indiqué est ouvert avec un accès en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="2bfb5-137">The TNEF object on the indicated stream is opened with read-only access.</span></span> <span data-ttu-id="2bfb5-138">Le fournisseur de transport doit définir cet indicateur si la fonction est d'initialiser l'objet pour un décodage ultérieur.</span><span class="sxs-lookup"><span data-stu-id="2bfb5-138">The transport provider must set this flag if the function is to initialize the object for subsequent decoding.</span></span>
    
<span data-ttu-id="2bfb5-139">TNEF_ENCODE</span><span class="sxs-lookup"><span data-stu-id="2bfb5-139">TNEF_ENCODE</span></span> 
  
> <span data-ttu-id="2bfb5-140">L'objet TNEF sur le flux indiqué est ouvert en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="2bfb5-140">The TNEF object on the indicated stream is opened for read/write permission.</span></span> <span data-ttu-id="2bfb5-141">Le fournisseur de transport doit définir cet indicateur si la fonction est d'initialiser l'objet pour le codage suivant.</span><span class="sxs-lookup"><span data-stu-id="2bfb5-141">The transport provider must set this flag if the function is to initialize the object for subsequent encoding.</span></span>
    
<span data-ttu-id="2bfb5-142">TNEF_PURE</span><span class="sxs-lookup"><span data-stu-id="2bfb5-142">TNEF_PURE</span></span> 
  
> <span data-ttu-id="2bfb5-143">Encode toutes les propriétés dans les blocs d'encapsulation MAPI.</span><span class="sxs-lookup"><span data-stu-id="2bfb5-143">Encodes all properties into the MAPI encapsulation blocks.</span></span> <span data-ttu-id="2bfb5-144">Par conséquent, un fichier TNEF «pur» se compose au plus des attributs attMAPIProps, attAttachment, attRenddata et attRecipTable.</span><span class="sxs-lookup"><span data-stu-id="2bfb5-144">Therefore, a "pure" TNEF file will consist of, at most, the attributes attMAPIProps, attAttachment, attRenddata, and attRecipTable.</span></span> <span data-ttu-id="2bfb5-145">Ce mode est idéal pour une utilisation sans compatibilité descendante.</span><span class="sxs-lookup"><span data-stu-id="2bfb5-145">This mode is ideal for use when no backward compatibility is required.</span></span>
    
<span data-ttu-id="2bfb5-146">_lpMessage_</span><span class="sxs-lookup"><span data-stu-id="2bfb5-146">_lpMessage_</span></span>
  
> <span data-ttu-id="2bfb5-147">dans Pointeur vers un objet message comme destination d'un message décodé avec des pièces jointes ou une source pour un message encodé avec des pièces jointes.</span><span class="sxs-lookup"><span data-stu-id="2bfb5-147">[in] Pointer to a message object as a destination for a decoded message with attachments or a source for an encoded message with attachments.</span></span> <span data-ttu-id="2bfb5-148">Toutes les propriétés d'un message de destination peuvent être remplacées par les propriétés d'un message encodé.</span><span class="sxs-lookup"><span data-stu-id="2bfb5-148">Any properties of a destination message can be overwritten by the properties of an encoded message.</span></span>
    
<span data-ttu-id="2bfb5-149">_wKeyVal_</span><span class="sxs-lookup"><span data-stu-id="2bfb5-149">_wKeyVal_</span></span>
  
> <span data-ttu-id="2bfb5-150">dans Clé de recherche utilisée par l'objet TNEF pour faire correspondre les pièces jointes aux balises de texte insérées dans le texte du message.</span><span class="sxs-lookup"><span data-stu-id="2bfb5-150">[in] A search key that the TNEF object uses to match attachments to the text tags inserted in the message text.</span></span> <span data-ttu-id="2bfb5-151">Cette valeur doit être relativement unique dans les messages.</span><span class="sxs-lookup"><span data-stu-id="2bfb5-151">This value should be relatively unique across messages.</span></span> 
    
<span data-ttu-id="2bfb5-152">_lpAddressBook_</span><span class="sxs-lookup"><span data-stu-id="2bfb5-152">_lpAddressBook_</span></span>
  
> <span data-ttu-id="2bfb5-153">dans Pointeur vers un objet de carnet d'adresses utilisé pour obtenir des informations d'adressage pour les identificateurs d'entrée.</span><span class="sxs-lookup"><span data-stu-id="2bfb5-153">[in] Pointer to an address book object used to get addressing information for entry identifiers.</span></span> 
    
<span data-ttu-id="2bfb5-154">_lppTNEF_</span><span class="sxs-lookup"><span data-stu-id="2bfb5-154">_lppTNEF_</span></span>
  
> <span data-ttu-id="2bfb5-155">remarquer Pointeur vers le nouvel objet TNEF.</span><span class="sxs-lookup"><span data-stu-id="2bfb5-155">[out] Pointer to the new TNEF object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="2bfb5-156">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="2bfb5-156">Return value</span></span>

<span data-ttu-id="2bfb5-157">S_OK</span><span class="sxs-lookup"><span data-stu-id="2bfb5-157">S_OK</span></span> 
  
> <span data-ttu-id="2bfb5-158">L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.</span><span class="sxs-lookup"><span data-stu-id="2bfb5-158">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="2bfb5-159">Remarques</span><span class="sxs-lookup"><span data-stu-id="2bfb5-159">Remarks</span></span>

<span data-ttu-id="2bfb5-160">La fonction **OpenTnefStreamEx** est le remplacement recommandé pour [OpenTnefStream](opentnefstream.md), le point d'entrée d'origine de l'accès TNEF.</span><span class="sxs-lookup"><span data-stu-id="2bfb5-160">The **OpenTnefStreamEx** function is the recommended replacement for [OpenTnefStream](opentnefstream.md), the original entry point for TNEF access.</span></span> 
  
<span data-ttu-id="2bfb5-161">Un objet TNEF créé par la fonction **OpenTnefStreamEx** appelle ensuite la méthode OLE **IUnknown:: AddRef** pour ajouter des références pour l'objet de prise en charge, l'objet Stream et l'objet message.</span><span class="sxs-lookup"><span data-stu-id="2bfb5-161">A TNEF object created by the **OpenTnefStreamEx** function later calls the OLE method **IUnknown::AddRef** to add references for the support object, the stream object, and the message object.</span></span> <span data-ttu-id="2bfb5-162">Le fournisseur de transport peut libérer les références pour les trois objets avec un seul appel à la méthode OLE **IUnknown:: Release** sur l'objet TNEF.</span><span class="sxs-lookup"><span data-stu-id="2bfb5-162">The transport provider can release the references for all three objects with a single call to the OLE method **IUnknown::Release** on the TNEF object.</span></span> 
  
<span data-ttu-id="2bfb5-163">**OpenTnefStreamEx** alloue et initialise un objet TNEF que le fournisseur doit utiliser pour coder un message MAPI en un message de flux TNEF.</span><span class="sxs-lookup"><span data-stu-id="2bfb5-163">**OpenTnefStreamEx** allocates and initializes a TNEF object for the provider to use in encoding a MAPI message into a TNEF stream message.</span></span> <span data-ttu-id="2bfb5-164">Cette fonction peut également configurer l'objet pour le fournisseur à utiliser dans les appels ultérieurs à [ITnef:: ExtractProps](itnef-extractprops.md) pour décoder un message TNEF en flux TNEF dans un message MAPI.</span><span class="sxs-lookup"><span data-stu-id="2bfb5-164">Alternatively, this function can set up the object for the provider to use in subsequent calls to [ITnef::ExtractProps](itnef-extractprops.md) to decode a TNEF stream message into a MAPI message.</span></span> <span data-ttu-id="2bfb5-165">Pour libérer l'objet TNEF et fermer la session, le fournisseur de transport doit appeler la méthode **IUnknown:: Release** héritée sur l'objet.</span><span class="sxs-lookup"><span data-stu-id="2bfb5-165">To free the TNEF object and close the session, the transport provider must call the inherited **IUnknown::Release** method on the object.</span></span> 
  
<span data-ttu-id="2bfb5-166">La valeur de base pour le paramètre _wKeyVal_ doit être différente de zéro et ne doit pas être identique pour chaque appel à **OpenTnefStreamEx**.</span><span class="sxs-lookup"><span data-stu-id="2bfb5-166">The base value for the  _wKeyVal_ parameter must not be zero and should not be the same for every call to **OpenTnefStreamEx**.</span></span> <span data-ttu-id="2bfb5-167">À la place, utilisez des nombres aléatoires basés sur l'heure système du générateur de nombres aléatoires de la bibliothèque Runtime.</span><span class="sxs-lookup"><span data-stu-id="2bfb5-167">Instead, use random numbers based on the system time from the run-time library's random number generator.</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="2bfb5-168">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="2bfb5-168">MFCMAPI reference</span></span>

<span data-ttu-id="2bfb5-169">Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="2bfb5-169">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="2bfb5-170">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="2bfb5-170">**File**</span></span>|<span data-ttu-id="2bfb5-171">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="2bfb5-171">**Function**</span></span>|<span data-ttu-id="2bfb5-172">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="2bfb5-172">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="2bfb5-173">File. cpp</span><span class="sxs-lookup"><span data-stu-id="2bfb5-173">File.cpp</span></span>  <br/> |<span data-ttu-id="2bfb5-174">LoadFromTNEF</span><span class="sxs-lookup"><span data-stu-id="2bfb5-174">LoadFromTNEF</span></span>  <br/> |<span data-ttu-id="2bfb5-175">MFCMAPI utilise la méthode **OpenTnefStreamEx** pour ouvrir un flux sur le fichier TNEF afin que les propriétés puissent être extraites.</span><span class="sxs-lookup"><span data-stu-id="2bfb5-175">MFCMAPI uses the **OpenTnefStreamEx** method to open a stream on the TNEF file so properties may be extracted.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="2bfb5-176">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2bfb5-176">See also</span></span>

- [<span data-ttu-id="2bfb5-177">IMAPISupport : IUnknown</span><span class="sxs-lookup"><span data-stu-id="2bfb5-177">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)
- [<span data-ttu-id="2bfb5-178">IXPProvider::TransportLogon</span><span class="sxs-lookup"><span data-stu-id="2bfb5-178">IXPProvider::TransportLogon</span></span>](ixpprovider-transportlogon.md)
- [<span data-ttu-id="2bfb5-179">MFCMAPI comme un exemple de Code</span><span class="sxs-lookup"><span data-stu-id="2bfb5-179">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

