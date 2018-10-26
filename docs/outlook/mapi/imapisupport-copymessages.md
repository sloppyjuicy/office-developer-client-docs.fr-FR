---
title: IMAPISupportCopyMessages
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.CopyMessages
api_type:
- COM
ms.assetid: 70f67614-af0d-43f6-99f6-391a2f5673cb
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 0d3f540a14c833e0ee0ed212f6f3b3b709d72ec0
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22591036"
---
# <a name="imapisupportcopymessages"></a><span data-ttu-id="f60de-103">IMAPISupport::CopyMessages</span><span class="sxs-lookup"><span data-stu-id="f60de-103">IMAPISupport::CopyMessages</span></span>

  
  
<span data-ttu-id="f60de-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f60de-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f60de-105">Copie ou déplace les messages d’un dossier dans un autre dossier.</span><span class="sxs-lookup"><span data-stu-id="f60de-105">Copies or moves messages from one folder to another folder.</span></span>
  
```cpp
HRESULT CopyMessages(
  LPCIID lpSrcInterface,
  LPVOID lpSrcFolder,
  LPENTRYLIST lpMsgList,
  LPCIID lpDestInterface,
  LPVOID lpDestFolder,
  ULONG_PTR ulUIParam,
  LPMAPIPROGRESS lpProgress,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="f60de-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f60de-106">Parameters</span></span>

 <span data-ttu-id="f60de-107">_lpSrcInterface_</span><span class="sxs-lookup"><span data-stu-id="f60de-107">_lpSrcInterface_</span></span>
  
> <span data-ttu-id="f60de-108">[in] Pointeur vers l’identificateur d’interface (IID) qui représente l’interface à utiliser pour accéder au dossier qui contient les messages à déplacer ou copier.</span><span class="sxs-lookup"><span data-stu-id="f60de-108">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the folder that contains the messages to be copied or moved.</span></span>
    
 <span data-ttu-id="f60de-109">_lpSrcFolder_</span><span class="sxs-lookup"><span data-stu-id="f60de-109">_lpSrcFolder_</span></span>
  
> <span data-ttu-id="f60de-110">[in] Pointeur vers le dossier qui contient les messages à déplacer ou copier.</span><span class="sxs-lookup"><span data-stu-id="f60de-110">[in] A pointer to the folder that contains the messages to be copied or moved.</span></span>
    
 <span data-ttu-id="f60de-111">_lpMsgList_</span><span class="sxs-lookup"><span data-stu-id="f60de-111">_lpMsgList_</span></span>
  
> <span data-ttu-id="f60de-112">[in] Pointeur vers un tableau d’identificateurs d’entrée qui identifient les messages à déplacer ou copier.</span><span class="sxs-lookup"><span data-stu-id="f60de-112">[in] A pointer to an array of entry identifiers that identify the messages to be copied or moved.</span></span> 
    
 <span data-ttu-id="f60de-113">_lpDestInterface_</span><span class="sxs-lookup"><span data-stu-id="f60de-113">_lpDestInterface_</span></span>
  
> <span data-ttu-id="f60de-114">[in] Pointeur vers l’identificateur d’interface (IID) qui représente l’interface à utiliser pour accéder au dossier de destination pour les messages copiés ou déplacées.</span><span class="sxs-lookup"><span data-stu-id="f60de-114">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the destination folder for the copied or moved messages.</span></span>
    
 <span data-ttu-id="f60de-115">_lpDestFolder_</span><span class="sxs-lookup"><span data-stu-id="f60de-115">_lpDestFolder_</span></span>
  
> <span data-ttu-id="f60de-116">[in] Pointeur vers le dossier de destination pour les messages copiés ou déplacées.</span><span class="sxs-lookup"><span data-stu-id="f60de-116">[in] A pointer to the destination folder for the copied or moved messages.</span></span> <span data-ttu-id="f60de-117">Ce dossier doit être ouvert.</span><span class="sxs-lookup"><span data-stu-id="f60de-117">This folder must be open.</span></span>
    
 <span data-ttu-id="f60de-118">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="f60de-118">_ulUIParam_</span></span>
  
> <span data-ttu-id="f60de-119">[in] Pointeur vers un objet de progression qui affiche un indicateur de progression.</span><span class="sxs-lookup"><span data-stu-id="f60de-119">[in] A pointer to a progress object that displays a progress indicator.</span></span> <span data-ttu-id="f60de-120">Si NULL est indiqué dans _lpProgress_, le fournisseur de banque de message affiche un indicateur de progression à l’aide de l’implémentation d’objet de progression MAPI.</span><span class="sxs-lookup"><span data-stu-id="f60de-120">If NULL is passed in  _lpProgress_, the message store provider displays a progress indicator by using the MAPI progress object implementation.</span></span> <span data-ttu-id="f60de-121">Le paramètre _lpProgress_ est ignoré à moins que l’indicateur MESSAGE_DIALOG est défini dans _ulFlags_.</span><span class="sxs-lookup"><span data-stu-id="f60de-121">The  _lpProgress_ parameter is ignored unless the MESSAGE_DIALOG flag is set in  _ulFlags_.</span></span>
    
 <span data-ttu-id="f60de-122">_lpProgress_</span><span class="sxs-lookup"><span data-stu-id="f60de-122">_lpProgress_</span></span>
  
> <span data-ttu-id="f60de-123">[in] Pointeur vers un objet de progression qui affiche un indicateur de progression.</span><span class="sxs-lookup"><span data-stu-id="f60de-123">[in] A pointer to a progress object that displays a progress indicator.</span></span> <span data-ttu-id="f60de-124">Si NULL est indiqué dans _lpProgress_, le fournisseur de banque de message affiche un indicateur de progression à l’aide de l’implémentation d’objet de progression MAPI.</span><span class="sxs-lookup"><span data-stu-id="f60de-124">If NULL is passed in  _lpProgress_, the message store provider displays a progress indicator by using the MAPI progress object implementation.</span></span> <span data-ttu-id="f60de-125">Le paramètre _lpProgress_ est ignoré à moins que l’indicateur MESSAGE_DIALOG est défini dans _ulFlags_.</span><span class="sxs-lookup"><span data-stu-id="f60de-125">The  _lpProgress_ parameter is ignored unless the MESSAGE_DIALOG flag is set in  _ulFlags_.</span></span>
    
 <span data-ttu-id="f60de-126">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="f60de-126">_ulFlags_</span></span>
  
> <span data-ttu-id="f60de-127">[in] Masque de bits d’indicateurs qui contrôle la manière dont l’opération de copie ou de déplacement est effectuée.</span><span class="sxs-lookup"><span data-stu-id="f60de-127">[in] A bitmask of flags that controls how the copy or move operation is accomplished.</span></span> <span data-ttu-id="f60de-128">Les indicateurs suivants peuvent être définis :</span><span class="sxs-lookup"><span data-stu-id="f60de-128">The following flags can be set:</span></span>
    
<span data-ttu-id="f60de-129">MESSAGE_DIALOG</span><span class="sxs-lookup"><span data-stu-id="f60de-129">MESSAGE_DIALOG</span></span> 
  
> <span data-ttu-id="f60de-130">Demande l’affichage d’un indicateur de progression.</span><span class="sxs-lookup"><span data-stu-id="f60de-130">Requests the display of a progress indicator.</span></span>
    
<span data-ttu-id="f60de-131">MESSAGE_MOVE</span><span class="sxs-lookup"><span data-stu-id="f60de-131">MESSAGE_MOVE</span></span> 
  
> <span data-ttu-id="f60de-132">Les messages doivent être déplacés, au lieu de copier.</span><span class="sxs-lookup"><span data-stu-id="f60de-132">The messages should be moved, instead of copied.</span></span> <span data-ttu-id="f60de-133">Si MESSAGE_MOVE n’est pas définie, les messages sont copiés.</span><span class="sxs-lookup"><span data-stu-id="f60de-133">If MESSAGE_MOVE is not set, the messages are copied.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="f60de-134">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="f60de-134">Return value</span></span>

<span data-ttu-id="f60de-135">S_OK</span><span class="sxs-lookup"><span data-stu-id="f60de-135">S_OK</span></span> 
  
> <span data-ttu-id="f60de-136">L’opération de copie ou de déplacement a réussi.</span><span class="sxs-lookup"><span data-stu-id="f60de-136">The copy or move operation was successful.</span></span>
    
<span data-ttu-id="f60de-137">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="f60de-137">MAPI_E_USER_CANCEL</span></span> 
  
> <span data-ttu-id="f60de-138">L’utilisateur a annulé l’opération de généralement en cliquant sur le bouton **Annuler** dans une boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="f60de-138">The user canceled the operation, typically by clicking the **Cancel** button in a dialog box.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="f60de-139">Remarques</span><span class="sxs-lookup"><span data-stu-id="f60de-139">Remarks</span></span>

<span data-ttu-id="f60de-140">La méthode **IMAPISupport::CopyMessages** est implémentée pour les objets de prise en charge de fournisseur de magasin de message.</span><span class="sxs-lookup"><span data-stu-id="f60de-140">The **IMAPISupport::CopyMessages** method is implemented for message store provider support objects.</span></span> <span data-ttu-id="f60de-141">Fournisseurs de magasins de message peuvent appeler **IMAPISupport::CopyMessages** dans leur implémentation [IMAPIFolder::CopyMessages](imapifolder-copymessages.md) pour copier ou déplacer un ou plusieurs messages d’un dossier à un autre.</span><span class="sxs-lookup"><span data-stu-id="f60de-141">Message store providers can call **IMAPISupport::CopyMessages** in their implementation of [IMAPIFolder::CopyMessages](imapifolder-copymessages.md) to copy or move one or more messages from one folder to another.</span></span> <span data-ttu-id="f60de-142">Dans le cadre de l’appel **IMAPISupport::CopyMessages** , le fournisseur de banque de messages permettre spécifier que MAPI doit afficher un indicateur de progression.</span><span class="sxs-lookup"><span data-stu-id="f60de-142">As part of the **IMAPISupport::CopyMessages** call, the message store provider can specify that MAPI should display a progress indicator.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="f60de-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f60de-143">See also</span></span>



[<span data-ttu-id="f60de-144">IMAPIFolder::CopyMessages</span><span class="sxs-lookup"><span data-stu-id="f60de-144">IMAPIFolder::CopyMessages</span></span>](imapifolder-copymessages.md)
  
[<span data-ttu-id="f60de-145">IMAPISupport : IUnknown</span><span class="sxs-lookup"><span data-stu-id="f60de-145">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

