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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 52fd844954f41d5d09b5e78f7c23ff6f7469bb43
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784950"
---
# <a name="opentnefstreamex"></a><span data-ttu-id="e891f-103">OpenTnefStreamEx</span><span class="sxs-lookup"><span data-stu-id="e891f-103">OpenTnefStreamEx</span></span>

<span data-ttu-id="e891f-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="e891f-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="e891f-105">Crée un objet de Transport-Neutral Encapsulation Format (TNEF) qui peut servir à coder ou décoder un objet de message dans un flux de données TNEF pour une utilisation par les transports ou des passerelles et des banques de messages.</span><span class="sxs-lookup"><span data-stu-id="e891f-105">Creates a Transport-Neutral Encapsulation Format (TNEF) object that can be used to encode or decode a message object into a TNEF data stream for use by transports or gateways and message stores.</span></span> <span data-ttu-id="e891f-106">Il s’agit du point d’entrée pour l’accès TNEF.</span><span class="sxs-lookup"><span data-stu-id="e891f-106">This is the entry point for TNEF access.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e891f-107">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="e891f-107">Header file:</span></span>  <br/> |<span data-ttu-id="e891f-108">TNEF.h</span><span class="sxs-lookup"><span data-stu-id="e891f-108">Tnef.h</span></span>  <br/> |
|<span data-ttu-id="e891f-109">Implémentée par :</span><span class="sxs-lookup"><span data-stu-id="e891f-109">Implemented by:</span></span>  <br/> |<span data-ttu-id="e891f-110">MAPI</span><span class="sxs-lookup"><span data-stu-id="e891f-110">MAPI</span></span>  <br/> |
|<span data-ttu-id="e891f-111">Appelée par :</span><span class="sxs-lookup"><span data-stu-id="e891f-111">Called by:</span></span>  <br/> |<span data-ttu-id="e891f-112">Fournisseurs de transport</span><span class="sxs-lookup"><span data-stu-id="e891f-112">Transport providers</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="e891f-113">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e891f-113">Parameters</span></span>

<span data-ttu-id="e891f-114">_lpvSupport_</span><span class="sxs-lookup"><span data-stu-id="e891f-114">_lpvSupport_</span></span>
  
> <span data-ttu-id="e891f-115">[in] Transmet un objet de prise en charge, ou passe NULL.</span><span class="sxs-lookup"><span data-stu-id="e891f-115">[in] Passes a support object, or passes in NULL.</span></span> <span data-ttu-id="e891f-116">Si la valeur NULL, le paramètre _lpAddressBook_ doit être non null.</span><span class="sxs-lookup"><span data-stu-id="e891f-116">If NULL, the  _lpAddressBook_ parameter should be non-null.</span></span> 
    
<span data-ttu-id="e891f-117">_lpStream_</span><span class="sxs-lookup"><span data-stu-id="e891f-117">_lpStream_</span></span>
  
> <span data-ttu-id="e891f-118">[in] Pointeur vers un objet stream de stockage, par exemple une interface OLE **IStream** , fournissant une source ou destination d’un message de flux TNEF.</span><span class="sxs-lookup"><span data-stu-id="e891f-118">[in] Pointer to a storage stream object, such as an OLE **IStream** interface, providing a source or destination for a TNEF stream message.</span></span> 
    
<span data-ttu-id="e891f-119">_lpszStreamName_</span><span class="sxs-lookup"><span data-stu-id="e891f-119">_lpszStreamName_</span></span>
  
> <span data-ttu-id="e891f-120">[in] Pointeur vers le nom du flux de données qui utilise l’objet TNEF.</span><span class="sxs-lookup"><span data-stu-id="e891f-120">[in] Pointer to the name of the data stream that the TNEF object uses.</span></span> <span data-ttu-id="e891f-121">Si l’appelant a défini l’indicateur TNEF_ENCODE (paramètre _ulFlags_ ) l’appel vers **OpenTnefStream**, le paramètre de _caractère_ doit spécifier un pointeur non null à une chaîne non nulle constituée de caractères validités pour un fichier d’attribution de noms.</span><span class="sxs-lookup"><span data-stu-id="e891f-121">If the caller has set the TNEF_ENCODE flag ( _ulFlags_ parameter) in its call to **OpenTnefStream**, the  _lpszName_ parameter must specify a non-null pointer to a non-null string consisting of any characters considered valid for naming a file.</span></span> <span data-ttu-id="e891f-122">MAPI n’autorise pas les noms de chaîne, y compris les caractères « [ », «] », ou « : », même si le système de fichiers permet de leur utilisation.</span><span class="sxs-lookup"><span data-stu-id="e891f-122">MAPI does not allow string names including the characters "[", "]", or ":", even if the file system permits their use.</span></span> <span data-ttu-id="e891f-123">La taille de la chaîne transmise au paramètre _le caractère_ ne doit pas dépasser la valeur de MAX_PATH, la longueur maximale d’une chaîne qui contient un nom de chemin d’accès.</span><span class="sxs-lookup"><span data-stu-id="e891f-123">The size of the string passed for the  _lpszName_ parameter must not exceed the value of MAX_PATH, the maximum length of a string that contains a path name.</span></span> 
    
<span data-ttu-id="e891f-124">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="e891f-124">_ulFlags_</span></span>
  
> <span data-ttu-id="e891f-125">[in] Masque de bits d’indicateurs utilisés pour indiquer le mode de la fonction.</span><span class="sxs-lookup"><span data-stu-id="e891f-125">[in] Bitmask of flags used to indicate the mode of the function.</span></span> <span data-ttu-id="e891f-126">Les indicateurs suivants peuvent être définis :</span><span class="sxs-lookup"><span data-stu-id="e891f-126">The following flags can be set:</span></span>
    
<span data-ttu-id="e891f-127">TNEF_BEST_DATA</span><span class="sxs-lookup"><span data-stu-id="e891f-127">TNEF_BEST_DATA</span></span> 
  
> <span data-ttu-id="e891f-128">Toutes les propriétés possibles sont mappées dans leurs attributs de bas niveau, mais lorsqu’il existe une perte de données possible en raison de la conversion à un attribut de bas niveau, la propriété est également codée dans l’encapsule.</span><span class="sxs-lookup"><span data-stu-id="e891f-128">All possible properties are mapped into their down-level attributes, but when there is a possible data loss due to the conversion to a down-level attribute, the property is also encoded in the encapsulations.</span></span> <span data-ttu-id="e891f-129">Notez que cette opération entraîne la duplication des informations sur le flux TNEF.</span><span class="sxs-lookup"><span data-stu-id="e891f-129">Note that this will cause the duplication of information in the TNEF stream.</span></span> <span data-ttu-id="e891f-130">TNEF_BEST_DATA est la valeur par défaut si aucun autre mode n’est spécifiés.</span><span class="sxs-lookup"><span data-stu-id="e891f-130">TNEF_BEST_DATA is the default if no other modes are specified.</span></span> 
    
<span data-ttu-id="e891f-131">TNEF_COMPATIBILITY</span><span class="sxs-lookup"><span data-stu-id="e891f-131">TNEF_COMPATIBILITY</span></span> 
  
> <span data-ttu-id="e891f-132">Fournit une compatibilité descendante avec les applications clientes antérieures.</span><span class="sxs-lookup"><span data-stu-id="e891f-132">Provides backward compatibility with older client applications.</span></span> <span data-ttu-id="e891f-133">Flux TNEF codés avec cet indicateur mappe toutes les propriétés possibles dans leur attribut de bas niveau correspondant.</span><span class="sxs-lookup"><span data-stu-id="e891f-133">TNEF streams encoded with this flag will map all possible properties into their corresponding down-level attribute.</span></span> <span data-ttu-id="e891f-134">Ce mode entraîne également l’utilisation par défaut de certaines propriétés requises par les clients de bas niveau.</span><span class="sxs-lookup"><span data-stu-id="e891f-134">This mode also causes the defaulting of some properties that are required by down-level clients.</span></span> 
    
  > [!CAUTION]
  > <span data-ttu-id="e891f-135">Cet indicateur est obsolète et ne doit pas être utilisé.</span><span class="sxs-lookup"><span data-stu-id="e891f-135">This flag is obsolete and should not be used.</span></span> 
  
<span data-ttu-id="e891f-136">TNEF_DECODE</span><span class="sxs-lookup"><span data-stu-id="e891f-136">TNEF_DECODE</span></span> 
  
> <span data-ttu-id="e891f-137">L’objet TNEF sur le flux indiqué est ouvert avec accès en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="e891f-137">The TNEF object on the indicated stream is opened with read-only access.</span></span> <span data-ttu-id="e891f-138">Le fournisseur de transport doit définir cet indicateur si la fonction est d’initialiser l’objet de décodage suivantes.</span><span class="sxs-lookup"><span data-stu-id="e891f-138">The transport provider must set this flag if the function is to initialize the object for subsequent decoding.</span></span>
    
<span data-ttu-id="e891f-139">TNEF_ENCODE</span><span class="sxs-lookup"><span data-stu-id="e891f-139">TNEF_ENCODE</span></span> 
  
> <span data-ttu-id="e891f-140">Ouverture de l’objet TNEF sur le flux indiqué pour l’autorisation en lecture-écriture.</span><span class="sxs-lookup"><span data-stu-id="e891f-140">The TNEF object on the indicated stream is opened for read/write permission.</span></span> <span data-ttu-id="e891f-141">Le fournisseur de transport doit définir cet indicateur si la fonction est d’initialiser l’objet de codage suivantes.</span><span class="sxs-lookup"><span data-stu-id="e891f-141">The transport provider must set this flag if the function is to initialize the object for subsequent encoding.</span></span>
    
<span data-ttu-id="e891f-142">TNEF_PURE</span><span class="sxs-lookup"><span data-stu-id="e891f-142">TNEF_PURE</span></span> 
  
> <span data-ttu-id="e891f-143">Code toutes les propriétés dans les blocs d’encapsulation MAPI.</span><span class="sxs-lookup"><span data-stu-id="e891f-143">Encodes all properties into the MAPI encapsulation blocks.</span></span> <span data-ttu-id="e891f-144">Par conséquent, un fichier TNEF « pur » est constitué, au plus, les attributs attMAPIProps, attAttachment, attRenddata et attRecipTable.</span><span class="sxs-lookup"><span data-stu-id="e891f-144">Therefore, a "pure" TNEF file will consist of, at most, the attributes attMAPIProps, attAttachment, attRenddata, and attRecipTable.</span></span> <span data-ttu-id="e891f-145">Ce mode est idéal pour une utilisation lorsque aucune compatibilité descendante n’est nécessaire.</span><span class="sxs-lookup"><span data-stu-id="e891f-145">This mode is ideal for use when no backward compatibility is required.</span></span>
    
<span data-ttu-id="e891f-146">_lpMessage_</span><span class="sxs-lookup"><span data-stu-id="e891f-146">_lpMessage_</span></span>
  
> <span data-ttu-id="e891f-147">[in] Pointeur vers un objet de message comme une destination d’un message décodée avec les pièces jointes ou d’une source d’un message codé avec les pièces jointes.</span><span class="sxs-lookup"><span data-stu-id="e891f-147">[in] Pointer to a message object as a destination for a decoded message with attachments or a source for an encoded message with attachments.</span></span> <span data-ttu-id="e891f-148">Toutes les propriétés d’un message de destination peuvent être remplacées par les propriétés d’un message codé.</span><span class="sxs-lookup"><span data-stu-id="e891f-148">Any properties of a destination message can be overwritten by the properties of an encoded message.</span></span>
    
<span data-ttu-id="e891f-149">_wKeyVal_</span><span class="sxs-lookup"><span data-stu-id="e891f-149">_wKeyVal_</span></span>
  
> <span data-ttu-id="e891f-150">[in] Une clé de recherche que l’objet TNEF utilise pour la correspondance de pièces jointes sur les balises de texte insérés dans le texte du message.</span><span class="sxs-lookup"><span data-stu-id="e891f-150">[in] A search key that the TNEF object uses to match attachments to the text tags inserted in the message text.</span></span> <span data-ttu-id="e891f-151">Cette valeur doit être relativement unique sur les messages.</span><span class="sxs-lookup"><span data-stu-id="e891f-151">This value should be relatively unique across messages.</span></span> 
    
<span data-ttu-id="e891f-152">_lpAddressBook_</span><span class="sxs-lookup"><span data-stu-id="e891f-152">_lpAddressBook_</span></span>
  
> <span data-ttu-id="e891f-153">[in] Pointeur vers un objet de carnet d’adresses utilisé pour obtenir des informations d’adressage des identificateurs d’entrée.</span><span class="sxs-lookup"><span data-stu-id="e891f-153">[in] Pointer to an address book object used to get addressing information for entry identifiers.</span></span> 
    
<span data-ttu-id="e891f-154">_lppTNEF_</span><span class="sxs-lookup"><span data-stu-id="e891f-154">_lppTNEF_</span></span>
  
> <span data-ttu-id="e891f-155">[out] Pointeur vers le nouvel objet TNEF.</span><span class="sxs-lookup"><span data-stu-id="e891f-155">[out] Pointer to the new TNEF object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="e891f-156">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="e891f-156">Return value</span></span>

<span data-ttu-id="e891f-157">S_OK</span><span class="sxs-lookup"><span data-stu-id="e891f-157">S_OK</span></span> 
  
> <span data-ttu-id="e891f-158">L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.</span><span class="sxs-lookup"><span data-stu-id="e891f-158">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="e891f-159">Remarques</span><span class="sxs-lookup"><span data-stu-id="e891f-159">Remarks</span></span>

<span data-ttu-id="e891f-160">La fonction **OpenTnefStreamEx** est le remplacement recommandé pour [OpenTnefStream](opentnefstream.md), le point d’entrée d’origine pour l’accès TNEF.</span><span class="sxs-lookup"><span data-stu-id="e891f-160">The **OpenTnefStreamEx** function is the recommended replacement for [OpenTnefStream](opentnefstream.md), the original entry point for TNEF access.</span></span> 
  
<span data-ttu-id="e891f-161">Un objet TNEF créé ultérieurement par la fonction **OpenTnefStreamEx** appelle la méthode OLE **IUnknown::AddRef** pour ajouter des références pour l’objet de prise en charge, l’objet stream et l’objet du message.</span><span class="sxs-lookup"><span data-stu-id="e891f-161">A TNEF object created by the **OpenTnefStreamEx** function later calls the OLE method **IUnknown::AddRef** to add references for the support object, the stream object, and the message object.</span></span> <span data-ttu-id="e891f-162">Le fournisseur de transport permettre libérer les références pour tous les trois objets avec un seul appel à la méthode OLE **IUnknown::Release** sur l’objet TNEF.</span><span class="sxs-lookup"><span data-stu-id="e891f-162">The transport provider can release the references for all three objects with a single call to the OLE method **IUnknown::Release** on the TNEF object.</span></span> 
  
<span data-ttu-id="e891f-163">**OpenTnefStreamEx** alloue et initialise un objet TNEF pour le fournisseur à utiliser dans le codage d’un message MAPI dans un message de flux TNEF.</span><span class="sxs-lookup"><span data-stu-id="e891f-163">**OpenTnefStreamEx** allocates and initializes a TNEF object for the provider to use in encoding a MAPI message into a TNEF stream message.</span></span> <span data-ttu-id="e891f-164">Cette fonction peut également définir l’objet pour le fournisseur à utiliser dans les appels suivants à [ITnef::ExtractProps](itnef-extractprops.md) pour décoder un message de flux TNEF dans un message MAPI.</span><span class="sxs-lookup"><span data-stu-id="e891f-164">Alternatively, this function can set up the object for the provider to use in subsequent calls to [ITnef::ExtractProps](itnef-extractprops.md) to decode a TNEF stream message into a MAPI message.</span></span> <span data-ttu-id="e891f-165">Pour libérer de l’objet TNEF, fermez la session, le fournisseur de transport doit appeler la méthode **IUnknown::Release** héritée sur l’objet.</span><span class="sxs-lookup"><span data-stu-id="e891f-165">To free the TNEF object and close the session, the transport provider must call the inherited **IUnknown::Release** method on the object.</span></span> 
  
<span data-ttu-id="e891f-166">La valeur de base pour le paramètre _wKeyVal_ ne doit pas être zéro et ne doit pas être la même pour chaque appel à **OpenTnefStreamEx**.</span><span class="sxs-lookup"><span data-stu-id="e891f-166">The base value for the  _wKeyVal_ parameter must not be zero and should not be the same for every call to **OpenTnefStreamEx**.</span></span> <span data-ttu-id="e891f-167">Au lieu de cela, utilisez des nombres aléatoires en fonction de l’heure système à partir du Générateur de nombres aléatoires de la bibliothèque d’exécution.</span><span class="sxs-lookup"><span data-stu-id="e891f-167">Instead, use random numbers based on the system time from the run-time library's random number generator.</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="e891f-168">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="e891f-168">MFCMAPI reference</span></span>

<span data-ttu-id="e891f-169">Pour des exemples de code MFCMAPI, voir le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="e891f-169">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="e891f-170">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="e891f-170">**File**</span></span>|<span data-ttu-id="e891f-171">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="e891f-171">**Function**</span></span>|<span data-ttu-id="e891f-172">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="e891f-172">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="e891f-173">File.cpp</span><span class="sxs-lookup"><span data-stu-id="e891f-173">File.cpp</span></span>  <br/> |<span data-ttu-id="e891f-174">LoadFromTNEF</span><span class="sxs-lookup"><span data-stu-id="e891f-174">LoadFromTNEF</span></span>  <br/> |<span data-ttu-id="e891f-175">MFCMAPI utilise la méthode **OpenTnefStreamEx** pour ouvrir un flux de données sur le fichier TNEF afin que les propriétés peuvent être extraits.</span><span class="sxs-lookup"><span data-stu-id="e891f-175">MFCMAPI uses the **OpenTnefStreamEx** method to open a stream on the TNEF file so properties may be extracted.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e891f-176">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e891f-176">See also</span></span>

- [<span data-ttu-id="e891f-177">IMAPISupport : IUnknown</span><span class="sxs-lookup"><span data-stu-id="e891f-177">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)
- [<span data-ttu-id="e891f-178">IXPProvider::TransportLogon</span><span class="sxs-lookup"><span data-stu-id="e891f-178">IXPProvider::TransportLogon</span></span>](ixpprovider-transportlogon.md)
- [<span data-ttu-id="e891f-179">MFCMAPI comme un exemple de Code</span><span class="sxs-lookup"><span data-stu-id="e891f-179">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

