---
title: OpenIMsgOnIStg
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- OpenIMsgOnIStg
api_type:
- HeaderDef
ms.assetid: a98b0b26-9b19-44ca-9b4e-0ad4d1c54325
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 56e663ced33da933b4276911b609f2fae1c5d78e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22563963"
---
# <a name="openimsgonistg"></a><span data-ttu-id="1eb6b-103">OpenIMsgOnIStg</span><span class="sxs-lookup"><span data-stu-id="1eb6b-103">OpenIMsgOnIStg</span></span>

<span data-ttu-id="1eb6b-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1eb6b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1eb6b-105">Crée un nouvel objet [IMessage](imessageimapiprop.md) par-dessus un objet OLE **IStorage** existant, à l’intérieur d’une session de messagerie.</span><span class="sxs-lookup"><span data-stu-id="1eb6b-105">Builds a new [IMessage](imessageimapiprop.md) object on top of an existing OLE **IStorage** object, to be used within a message session.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="1eb6b-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="1eb6b-106">Header file:</span></span>  <br/> |<span data-ttu-id="1eb6b-107">IMessage.h</span><span class="sxs-lookup"><span data-stu-id="1eb6b-107">Imessage.h</span></span>  <br/> |
|<span data-ttu-id="1eb6b-108">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="1eb6b-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="1eb6b-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="1eb6b-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="1eb6b-110">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="1eb6b-110">Called by:</span></span>  <br/> |<span data-ttu-id="1eb6b-111">Les applications clientes et des fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="1eb6b-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE OpenIMsgOnIStg(
  LPMSGSESS lpMsgSess,
  LPALLOCATEBUFFER lpAllocateBuffer,
  LPALLOCATEMORE lpAllocateMore,
  LPFREEBUFFER lpFreeBuffer,
  LPMALLOC lpmalloc,
  LPVOID lpMapiSup,
  LPSTORAGE lpStg,
  MSGCALLRELEASE FAR * lpfMsgCallRelease,
  ULONG ulCallerData,
  ULONG ulFlags,
  LPMESSAGE FAR * lppMsg
);
```

## <a name="parameters"></a><span data-ttu-id="1eb6b-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1eb6b-112">Parameters</span></span>

<span data-ttu-id="1eb6b-113">_lpMsgSess_</span><span class="sxs-lookup"><span data-stu-id="1eb6b-113">_lpMsgSess_</span></span>
  
> <span data-ttu-id="1eb6b-114">[in] Pointeur vers un objet de la session message dans laquelle nouvelle **IMessage**- sur - objet **IStorage** doit être créé.</span><span class="sxs-lookup"><span data-stu-id="1eb6b-114">[in] Pointer to a message session object within which the new **IMessage**-on- **IStorage** object is to be created.</span></span> 
    
<span data-ttu-id="1eb6b-115">_lpAllocateBuffer_</span><span class="sxs-lookup"><span data-stu-id="1eb6b-115">_lpAllocateBuffer_</span></span>
  
> <span data-ttu-id="1eb6b-116">[in] Pointeur vers la fonction [MAPIAllocateBuffer](mapiallocatebuffer.md) , à utiliser pour allouer de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="1eb6b-116">[in] Pointer to the [MAPIAllocateBuffer](mapiallocatebuffer.md) function, to be used to allocate memory.</span></span> 
    
<span data-ttu-id="1eb6b-117">_lpAllocateMore_</span><span class="sxs-lookup"><span data-stu-id="1eb6b-117">_lpAllocateMore_</span></span>
  
> <span data-ttu-id="1eb6b-118">[in] Pointeur vers la fonction [MAPIAllocateMore](mapiallocatemore.md) , à utiliser pour allouer plus de mémoire.</span><span class="sxs-lookup"><span data-stu-id="1eb6b-118">[in] Pointer to the [MAPIAllocateMore](mapiallocatemore.md) function, to be used to allocate additional memory.</span></span> 
    
<span data-ttu-id="1eb6b-119">_lpFreeBuffer_</span><span class="sxs-lookup"><span data-stu-id="1eb6b-119">_lpFreeBuffer_</span></span>
  
> <span data-ttu-id="1eb6b-120">[in] Pointeur vers la fonction [MAPIFreeBuffer](mapifreebuffer.md) , à utiliser pour libérer de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="1eb6b-120">[in] Pointer to the [MAPIFreeBuffer](mapifreebuffer.md) function, to be used to free memory.</span></span> 
    
<span data-ttu-id="1eb6b-121">_lpMalloc_</span><span class="sxs-lookup"><span data-stu-id="1eb6b-121">_lpMalloc_</span></span>
  
> <span data-ttu-id="1eb6b-122">[in] Pointeur vers un objet d’allocation mémoire exposant l’interface OLE **IMalloc** .</span><span class="sxs-lookup"><span data-stu-id="1eb6b-122">[in] Pointer to a memory allocator object exposing the OLE **IMalloc** interface.</span></span> <span data-ttu-id="1eb6b-123">L’interface **IMessage** doit utiliser cette méthode de répartition lorsque vous travaillez avec des interfaces telles que **IStorage** et **IStream**.</span><span class="sxs-lookup"><span data-stu-id="1eb6b-123">The **IMessage** interface needs to use this allocation method when working with interfaces such as **IStorage** and **IStream**.</span></span> 
    
<span data-ttu-id="1eb6b-124">_lpMapiSup_</span><span class="sxs-lookup"><span data-stu-id="1eb6b-124">_lpMapiSup_</span></span>
  
> <span data-ttu-id="1eb6b-125">[in] Facultatif pointeur vers un objet de prise en charge MAPI un fournisseur de services peut utiliser pour appeler les méthodes de le [IMAPISupport : IUnknown](imapisupportiunknown.md) interface.</span><span class="sxs-lookup"><span data-stu-id="1eb6b-125">[in] Optional pointer to a MAPI support object that a service provider can use to call the methods of the [IMAPISupport : IUnknown](imapisupportiunknown.md) interface.</span></span> 
    
<span data-ttu-id="1eb6b-126">_lpStg_</span><span class="sxs-lookup"><span data-stu-id="1eb6b-126">_lpStg_</span></span>
  
> <span data-ttu-id="1eb6b-127">[entrée, sortie] Pointeur vers un objet OLE **IStorage** qui est ouvert et est en lecture seule ou autorisation en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="1eb6b-127">[in, out] Pointer to an OLE **IStorage** object that is open and has read-only or read/write permission.</span></span> <span data-ttu-id="1eb6b-128">Étant donné que **IMessage** ne prend pas en charge l’accès en écriture uniquement, **OpenIMsgOnIStg** n’accepte pas un objet de stockage ouvert en mode écriture seule.</span><span class="sxs-lookup"><span data-stu-id="1eb6b-128">Because **IMessage** does not support write-only access, **OpenIMsgOnIStg** does not accept a storage object opened in write-only mode.</span></span> 
    
<span data-ttu-id="1eb6b-129">_lpfMsgCallRelease_</span><span class="sxs-lookup"><span data-stu-id="1eb6b-129">_lpfMsgCallRelease_</span></span>
  
> <span data-ttu-id="1eb6b-130">[in] Pointeur facultatif à une fonction de rappel selon le prototype [MSGCALLRELEASE](msgcallrelease.md) MAPI, vous pouvez appeler après la dernière version de l' objet **IStorage** - sur - **IMessage**.</span><span class="sxs-lookup"><span data-stu-id="1eb6b-130">[in] Optional pointer to a callback function based on the [MSGCALLRELEASE](msgcallrelease.md) prototype that MAPI is to call following the last release on the **IMessage**-on- **IStorage** object.</span></span> 
    
<span data-ttu-id="1eb6b-131">_ulCallerData_</span><span class="sxs-lookup"><span data-stu-id="1eb6b-131">_ulCallerData_</span></span>
  
> <span data-ttu-id="1eb6b-132">[in] Données de l’appelant enregistré par MAPI avec l’objet **IStorage** **IMessage**- sur - et transmises à la **MSGCALLRELEASE** en fonction de fonction de rappel.</span><span class="sxs-lookup"><span data-stu-id="1eb6b-132">[in] Caller data saved by MAPI with the **IMessage**-on- **IStorage** object and passed to the **MSGCALLRELEASE** based callback function.</span></span> <span data-ttu-id="1eb6b-133">Les données fournissent le contexte sur l’objet **IMessage** libérée et l’objet **IStorage** sur lequel il a été généré.</span><span class="sxs-lookup"><span data-stu-id="1eb6b-133">The data provides context about the **IMessage** object being released and the **IStorage** object on top of which it was built.</span></span> 
    
<span data-ttu-id="1eb6b-134">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="1eb6b-134">_ulFlags_</span></span>
  
> <span data-ttu-id="1eb6b-135">[in] Masque de bits d’indicateurs permet de contrôler si la méthode OLE **IStorage::Commit** est appelée lorsque l’application cliente ou un fournisseur de services appelle la méthode **IMessage::SaveChanges** .</span><span class="sxs-lookup"><span data-stu-id="1eb6b-135">[in] Bitmask of flags used to control whether the OLE **IStorage::Commit** method is called when the client application or service provider calls the **IMessage::SaveChanges** method.</span></span> <span data-ttu-id="1eb6b-136">Les indicateurs suivants peuvent être définis :</span><span class="sxs-lookup"><span data-stu-id="1eb6b-136">The following flags can be set:</span></span> 
    
<span data-ttu-id="1eb6b-137">IMSG_NO_ISTG_COMMIT</span><span class="sxs-lookup"><span data-stu-id="1eb6b-137">IMSG_NO_ISTG_COMMIT</span></span> 
  
> <span data-ttu-id="1eb6b-138">La méthode OLE **IStorage::Commit** ne pas doit être appelée lorsque le client ou le fournisseur appelle [SaveChanges](imapiprop-savechanges.md).</span><span class="sxs-lookup"><span data-stu-id="1eb6b-138">The OLE method **IStorage::Commit** is not to be called when the client or provider calls [SaveChanges](imapiprop-savechanges.md).</span></span> 
    
<span data-ttu-id="1eb6b-139">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="1eb6b-139">MAPI_UNICODE</span></span>
  
> <span data-ttu-id="1eb6b-140">Permet la création de fichiers de .msg Unicode.</span><span class="sxs-lookup"><span data-stu-id="1eb6b-140">Enables creation of Unicode .msg files.</span></span> <span data-ttu-id="1eb6b-141">Le fichier [IMessage](imessageimapiprop.md) affiche STORE_UNICODE_OK dans son [PR_STORE_SUPPORT_MASK](pidtagstoresupportmask-canonical-property.md) et prend en charge les propriétés Unicode.</span><span class="sxs-lookup"><span data-stu-id="1eb6b-141">The resulting [IMessage](imessageimapiprop.md) file shows STORE_UNICODE_OK in its [PR_STORE_SUPPORT_MASK](pidtagstoresupportmask-canonical-property.md) and supports Unicode properties.</span></span> 
    
  > [!NOTE]
  > <span data-ttu-id="1eb6b-142">L’indicateur MAPI_UNICODE est uniquement pris en charge dans cette fonction sur Outlook 2003 ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="1eb6b-142">The MAPI_UNICODE flag is only supported in this function on Outlook 2003 or higher.</span></span> 
  
<span data-ttu-id="1eb6b-143">_lppMsg_</span><span class="sxs-lookup"><span data-stu-id="1eb6b-143">_lppMsg_</span></span>
  
> <span data-ttu-id="1eb6b-144">[out] Pointeur vers un pointeur vers l’objet **IMessage** ouvert.</span><span class="sxs-lookup"><span data-stu-id="1eb6b-144">[out] Pointer to a pointer to the opened **IMessage** object.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="1eb6b-145">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="1eb6b-145">Return value</span></span>

<span data-ttu-id="1eb6b-146">S_OK</span><span class="sxs-lookup"><span data-stu-id="1eb6b-146">S_OK</span></span> 
  
> <span data-ttu-id="1eb6b-147">L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.</span><span class="sxs-lookup"><span data-stu-id="1eb6b-147">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="1eb6b-148">Remarques</span><span class="sxs-lookup"><span data-stu-id="1eb6b-148">Remarks</span></span>

<span data-ttu-id="1eb6b-149">Attributs de la propriété est accessible uniquement sur propriété objets, autrement dit, l’implémentation de la [IMAPIProp : IUnknown](imapipropiunknown.md) interface.</span><span class="sxs-lookup"><span data-stu-id="1eb6b-149">Property attributes can only be accessed on property objects, that is, objects implementing the [IMAPIProp : IUnknown](imapipropiunknown.md) interface.</span></span> <span data-ttu-id="1eb6b-150">Pour rendre les propriétés MAPI disponible sur un objet de stockage structuré OLE, **OpenIMsgOnIStg** génère une [IMessage : IMAPIProp](imessageimapiprop.md) objet en haut de l’objet OLE **IStorage** .</span><span class="sxs-lookup"><span data-stu-id="1eb6b-150">To make MAPI properties available on an OLE structured storage object, **OpenIMsgOnIStg** builds an [IMessage : IMAPIProp](imessageimapiprop.md) object on top of the OLE **IStorage** object.</span></span> <span data-ttu-id="1eb6b-151">Les attributs de propriété sur de tels objets peuvent définir ou a été modifiés avec [SetAttribIMsgOnIStg](setattribimsgonistg.md) et récupérés par [GetAttribIMsgOnIStg](getattribimsgonistg.md).</span><span class="sxs-lookup"><span data-stu-id="1eb6b-151">The property attributes on such objects can be set or altered with [SetAttribIMsgOnIStg](setattribimsgonistg.md) and retrieved with [GetAttribIMsgOnIStg](getattribimsgonistg.md).</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="1eb6b-152">Notes aux appelants</span><span class="sxs-lookup"><span data-stu-id="1eb6b-152">Notes to callers</span></span>

<span data-ttu-id="1eb6b-153">Une session de messagerie doit être ouvert avec [OpenIMsgSession](openimsgsession.md) avant l’appel de **OpenIMsgOnIStg** .</span><span class="sxs-lookup"><span data-stu-id="1eb6b-153">A message session should be opened with [OpenIMsgSession](openimsgsession.md) before **OpenIMsgOnIStg** is called.</span></span> <span data-ttu-id="1eb6b-154">Fournissant un paramètre valide _lpMsgSess_ se sures que le nouveau message est créé au sein d’une session de messagerie afin qu’il est fermé lorsque la session est fermée.</span><span class="sxs-lookup"><span data-stu-id="1eb6b-154">Supplying a valid  _lpMsgSess_ parameter make sures that the new message is created within a message session so that it is closed when the session is closed.</span></span> <span data-ttu-id="1eb6b-155">Si _lpMsgSess_ est NULL, le message est créé indépendamment de toute session de messagerie.</span><span class="sxs-lookup"><span data-stu-id="1eb6b-155">If  _lpMsgSess_ is NULL, the message is created independently of any message session.</span></span> <span data-ttu-id="1eb6b-156">Si l’application cliente ou un fournisseur de services qui a créé le message ne pas version il, ainsi que ses pièces jointes et ouvrir des tables, mémoire fuite et peut provoquer l’arrêt de l’application.</span><span class="sxs-lookup"><span data-stu-id="1eb6b-156">If the client application or service provider that created the message does not release it, as well as all its attachments and open tables, memory is leaked and may cause the application to terminate.</span></span> 
  
<span data-ttu-id="1eb6b-157">MAPI utilise les fonctions désignées par _lpAllocateBuffer_, _lpAllocateMore_et _lpFreeBuffer_ pour la plupart de l’allocation de mémoire et de désaffectation, en particulier pour allouer de la mémoire pour une utilisation par les applications clientes lors de l’appel des interfaces de l’objet par exemple [IMAPIProp::GetProps](imapiprop-getprops.md) et [IMAPITable::QueryRows](imapitable-queryrows.md).</span><span class="sxs-lookup"><span data-stu-id="1eb6b-157">MAPI uses the functions pointed to by  _lpAllocateBuffer_,  _lpAllocateMore_, and  _lpFreeBuffer_ for most memory allocation and deallocation, in particular to allocate memory for use by client applications when calling object interfaces such as [IMAPIProp::GetProps](imapiprop-getprops.md) and [IMAPITable::QueryRows](imapitable-queryrows.md).</span></span> <span data-ttu-id="1eb6b-158">Les pointeurs _lpAllocateBuffer_, _lpAllocateMore_et _lpFreeBuffer_ sont facultatifs lorsque la fonction **OpenIMsgOnIStg** est appelée avec un paramètre valide _lpMapiSup_ .</span><span class="sxs-lookup"><span data-stu-id="1eb6b-158">The  _lpAllocateBuffer_,  _lpAllocateMore_, and  _lpFreeBuffer_ pointers are optional when the **OpenIMsgOnIStg** function is called with a valid  _lpMapiSup_ parameter.</span></span> 
  
<span data-ttu-id="1eb6b-159">Car elle porte sur un objet OLE sous-jacent, MAPI doit également utiliser l’allocation de mémoire OLE.</span><span class="sxs-lookup"><span data-stu-id="1eb6b-159">Because it is dealing with an underlying OLE object, MAPI also needs to use OLE memory allocation.</span></span> <span data-ttu-id="1eb6b-160">Pour plus d’informations sur les objets de stockage structuré OLE et l’allocation de mémoire OLE, consultez la _référence du programmeur OLE_.</span><span class="sxs-lookup"><span data-stu-id="1eb6b-160">For more information about OLE structured storage objects and OLE memory allocation, see the  _OLE Programmer's Reference_.</span></span> 
  
<span data-ttu-id="1eb6b-161">Si une valeur valide est fournie pour _lpMapiSup_, **IMessage** prend en charge les indicateurs MAPI_DIALOG et ATTACH_DIALOG en appelant la méthode [IMAPISupport::DoProgressDialog](imapisupport-doprogressdialog.md) pour fournir une interface utilisateur d’avancement de [IMAPIProp::CopyTo](imapiprop-copyto.md) et les méthodes [IMessage::DeleteAttach](imessage-deleteattach.md) .</span><span class="sxs-lookup"><span data-stu-id="1eb6b-161">If a valid value is supplied for  _lpMapiSup_, **IMessage** supports the MAPI_DIALOG and ATTACH_DIALOG flags by calling the [IMAPISupport::DoProgressDialog](imapisupport-doprogressdialog.md) method to supply a progress user interface for the [IMAPIProp::CopyTo](imapiprop-copyto.md) and [IMessage::DeleteAttach](imessage-deleteattach.md) methods.</span></span> <span data-ttu-id="1eb6b-162">En outre, la méthode [IMessage::ModifyRecipients](imessage-modifyrecipients.md) tente de convertir les identificateurs d’entrée à court terme pour les identificateurs d’entrée à long terme en appelant la méthode [IMAPISupport::OpenAddressBook](imapisupport-openaddressbook.md) et effectuer des appels sur l’objet de carnet d’adresses qui en résulte.</span><span class="sxs-lookup"><span data-stu-id="1eb6b-162">Also, the [IMessage::ModifyRecipients](imessage-modifyrecipients.md) method attempts to convert short-term entry identifiers to long-term entry identifiers by calling the [IMAPISupport::OpenAddressBook](imapisupport-openaddressbook.md) method and making calls on the resulting address book object.</span></span> <span data-ttu-id="1eb6b-163">Si la valeur NULL est passée pour _lpMapiSup_, **IMessage** ignore MAPI_DIALOG et ATTACH_DIALOG et stocke les identificateurs d’entrée à court terme sans conversion.</span><span class="sxs-lookup"><span data-stu-id="1eb6b-163">If NULL is passed for  _lpMapiSup_, **IMessage** ignores MAPI_DIALOG and ATTACH_DIALOG and stores short-term entry identifiers without conversion.</span></span> 
  
<span data-ttu-id="1eb6b-164">L’objet **IStorage** désigné par le paramètre _lpStg_ doit être ouvert en mode STGM_READWRITE ou STGM_READ.</span><span class="sxs-lookup"><span data-stu-id="1eb6b-164">The **IStorage** object pointed to by the  _lpStg_ parameter must be opened in either the STGM_READ or STGM_READWRITE mode.</span></span> <span data-ttu-id="1eb6b-165">Si le mode STGM_READWRITE est utilisé, le mode STGM_TRANSACTED doit également être défini.</span><span class="sxs-lookup"><span data-stu-id="1eb6b-165">If the STGM_READWRITE mode is used, the STGM_TRANSACTED mode must also be set.</span></span> 
  
<span data-ttu-id="1eb6b-166">La fonction de rappel vers laquelle pointée le paramètre _lpfMsgCallRelease_ est facultative ; s’il est fourni, il doit être basé sur le prototype de fonction [MSGCALLRELEASE](msgcallrelease.md) .</span><span class="sxs-lookup"><span data-stu-id="1eb6b-166">The callback function pointed to by the  _lpfMsgCallRelease_ parameter is optional; if provided, it should be based on the [MSGCALLRELEASE](msgcallrelease.md) function prototype.</span></span> <span data-ttu-id="1eb6b-167">L’interface **IMessage** appelle lorsque le décompte de références de l’objet **IStorage** **IMessage**- sur - a la valeur zéro par le dernier appel à la méthode **Release** .</span><span class="sxs-lookup"><span data-stu-id="1eb6b-167">The **IMessage** interface calls it when the reference count of the **IMessage**-on- **IStorage** object is set to zero by the last call to its **Release** method.</span></span> <span data-ttu-id="1eb6b-168">La fonction de rappel est fréquemment utilisée pour libérer de l’interface **IStorage** sous-jacent.</span><span class="sxs-lookup"><span data-stu-id="1eb6b-168">The callback function is commonly used to free the underlying **IStorage** interface.</span></span> <span data-ttu-id="1eb6b-169">**IMessage** ne tente pas accéder à l’objet **IStorage** désigné par le paramètre _lpStg_ après avoir effectué le rappel.</span><span class="sxs-lookup"><span data-stu-id="1eb6b-169">**IMessage** will not attempt to access the **IStorage** object pointed to by the  _lpStg_ parameter after making the callback.</span></span> 
  
<span data-ttu-id="1eb6b-170">Certains clients ou des fournisseurs peuvent écrire des données supplémentaires à l’objet **IStorage** au-delà quel **IMessage** lui-même écrit lorsque la méthode [SaveChanges](imapiprop-savechanges.md) est appelée.</span><span class="sxs-lookup"><span data-stu-id="1eb6b-170">Some clients or providers might write additional data to the **IStorage** object beyond what **IMessage** itself writes when its [SaveChanges](imapiprop-savechanges.md) method is called.</span></span> <span data-ttu-id="1eb6b-171">Le client ou le fournisseur peut utiliser l’indicateur IMSG_NO_ISTG_COMMIT pour empêcher l’appel à la méthode OLE **IStorage::Commit** lors du traitement d’un appel de **SaveChanges** ; **IMessage** Dans ce cas le client ou le fournisseur doit lui-même valider l’objet **IStorage** lors de l’écriture de données supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="1eb6b-171">The client or provider can use the IMSG_NO_ISTG_COMMIT flag to prevent **IMessage** from calling the OLE **IStorage::Commit** method while processing a **SaveChanges** call; in this case the client or provider must itself commit the **IStorage** object when the additional data is written.</span></span> <span data-ttu-id="1eb6b-172">Pour faciliter cela, l’implémentation **IMessage** garantit nommer tous les substorages qu’il crée dans l’objet **IStorage** commençant par la chaîne « __ », autrement dit, avec deux traits de soulignement.</span><span class="sxs-lookup"><span data-stu-id="1eb6b-172">To aid in this, the **IMessage** implementation guarantees to name all substorages it creates in the **IStorage** object starting with the string "__", that is, with two underscores.</span></span> <span data-ttu-id="1eb6b-173">Le client ou le fournisseur pour éviter les collisions de noms, en conservant les noms sous-stockage en dehors de cet espace de noms.</span><span class="sxs-lookup"><span data-stu-id="1eb6b-173">The client or provider can avoid name collisions by keeping its substorage names out of this namespace.</span></span> 
  
<span data-ttu-id="1eb6b-174">MAPI ne définit pas le comportement de plusieurs opérations d’ouverture exécutée sur un sous-objet d’un message, comme une pièce jointe, un flux de données ou un message incorporé.</span><span class="sxs-lookup"><span data-stu-id="1eb6b-174">MAPI does not define the behavior of multiple open operations performed on a subobject of a message, such as an attachment, a stream, or an embedded message.</span></span> <span data-ttu-id="1eb6b-175">MAPI permet actuellement un sous-objet qui est déjà ouvert à ouvrir une fois encore, mais MAPI effectue l’opération d’ouverture en incrémentant le décompte de références pour l’objet ouvert existant avant des retourner au client ou au fournisseur qui a appelé la [IMessage::OpenAttach ](imessage-openattach.md)ou la méthode [IMAPIProp::OpenProperty](imapiprop-openproperty.md) .</span><span class="sxs-lookup"><span data-stu-id="1eb6b-175">MAPI currently allows a subobject that is already open to be opened once more, but MAPI performs the open operation by incrementing the reference count for the existing open object and returning it to the client or provider that called the [IMessage::OpenAttach](imessage-openattach.md) or [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method.</span></span> <span data-ttu-id="1eb6b-176">Cela signifie que l’accès demandé pour la première opération open sur un sous-objet est l’accès fourni pour toutes les opérations open suivantes, quel que soit l’accès demandé par les opérations.</span><span class="sxs-lookup"><span data-stu-id="1eb6b-176">This means the access requested for the first open operation on a subobject is the access provided for all subsequent open operations, regardless of the access requested by the operations.</span></span> 
  
<span data-ttu-id="1eb6b-177">La procédure correcte pour placer un message dans une pièce jointe est d’appeler la méthode [IMAPIProp::OpenProperty](imapiprop-openproperty.md) avec un identificateur d’interface de IID_IMessage.</span><span class="sxs-lookup"><span data-stu-id="1eb6b-177">The correct procedure for placing a message into an attachment is to call the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method with an interface identifier of IID_IMessage.</span></span> <span data-ttu-id="1eb6b-178">**OpenProperty** actuellement prend également en charge la création de pièces jointes des messages disponibles directement sur l’interface OLE **IStorage** , autrement dit, à l’aide de l’identificateur d’interface IID_IStorage.</span><span class="sxs-lookup"><span data-stu-id="1eb6b-178">**OpenProperty** currently also supports creation of message attachments available directly on the OLE **IStorage** interface, that is, using the IID_IStorage interface identifier.</span></span> <span data-ttu-id="1eb6b-179">**IStorage** access est pris en charge pour autoriser un moyen facile placer un document Microsoft Word en pièce jointe sans le convertir vers ou à partir de l’interface OLE **IStream** .</span><span class="sxs-lookup"><span data-stu-id="1eb6b-179">**IStorage** access is supported to allow an easy way to put a Microsoft Word document into an attachment without converting it to or from the OLE **IStream** interface.</span></span> <span data-ttu-id="1eb6b-180">Toutefois, **IMessage** peut se comporter prévisible si **OpenIMsgOnIStg** est passé un pointeur **IStorage** pour les données de pièce jointe et les objets sont distribuées dans le bon ordre.</span><span class="sxs-lookup"><span data-stu-id="1eb6b-180">However, **IMessage** may not behave predictably if **OpenIMsgOnIStg** is passed an **IStorage** pointer to the attachment data and then the objects are released in the wrong order.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="1eb6b-181">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="1eb6b-181">MFCMAPI reference</span></span>

<span data-ttu-id="1eb6b-182">Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="1eb6b-182">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="1eb6b-183">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="1eb6b-183">**File**</span></span>|<span data-ttu-id="1eb6b-184">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="1eb6b-184">**Function**</span></span>|<span data-ttu-id="1eb6b-185">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="1eb6b-185">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="1eb6b-186">File.cpp</span><span class="sxs-lookup"><span data-stu-id="1eb6b-186">File.cpp</span></span>  <br/> |<span data-ttu-id="1eb6b-187">LoadMSGToMessage</span><span class="sxs-lookup"><span data-stu-id="1eb6b-187">LoadMSGToMessage</span></span>  <br/> |<span data-ttu-id="1eb6b-188">MFCMAPI utilise la méthode **OpenIMsgOnIStg** pour ouvrir une interface IMessage au-dessus de la. MSG fichier afin que le fichier peut être manipulé avec l’interface MAPI.</span><span class="sxs-lookup"><span data-stu-id="1eb6b-188">MFCMAPI uses the **OpenIMsgOnIStg** method to open an IMessage interface on top of the .MSG file so that the file may be manipulated with MAPI.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="1eb6b-189">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1eb6b-189">See also</span></span>

- [<span data-ttu-id="1eb6b-190">MFCMAPI comme un exemple de Code</span><span class="sxs-lookup"><span data-stu-id="1eb6b-190">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

