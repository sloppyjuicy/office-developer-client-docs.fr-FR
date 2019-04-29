---
title: IMAPIMessageSiteCopyMessage
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIMessageSite.CopyMessage
api_type:
- COM
ms.assetid: d4e18483-409a-4d81-91dc-f4aec29a82bb
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: aeb8b090997bd0c4f51f872b36d6520547846f7f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429999"
---
# <a name="imapimessagesitecopymessage"></a><span data-ttu-id="a80aa-103">IMAPIMessageSite::CopyMessage</span><span class="sxs-lookup"><span data-stu-id="a80aa-103">IMAPIMessageSite::CopyMessage</span></span>

  
  
<span data-ttu-id="a80aa-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a80aa-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a80aa-105">Copie le message actif dans un dossier.</span><span class="sxs-lookup"><span data-stu-id="a80aa-105">Copies the current message to a folder.</span></span>
  
```cpp
HRESULT CopyMessage(
  LPMAPIFOLDER pFolderDestination
);
```

## <a name="parameters"></a><span data-ttu-id="a80aa-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a80aa-106">Parameters</span></span>

 <span data-ttu-id="a80aa-107">_pFolderDestination_</span><span class="sxs-lookup"><span data-stu-id="a80aa-107">_pFolderDestination_</span></span>
  
> <span data-ttu-id="a80aa-108">dans Pointeur vers le dossier dans lequel le message doit être copié.</span><span class="sxs-lookup"><span data-stu-id="a80aa-108">[in] A pointer to the folder where the message is to be copied.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="a80aa-109">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="a80aa-109">Return value</span></span>

<span data-ttu-id="a80aa-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="a80aa-110">S_OK</span></span> 
  
> <span data-ttu-id="a80aa-111">L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.</span><span class="sxs-lookup"><span data-stu-id="a80aa-111">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="a80aa-112">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="a80aa-112">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="a80aa-113">L'opération n'est pas prise en charge par ce site de messages.</span><span class="sxs-lookup"><span data-stu-id="a80aa-113">The operation is not supported by this message site.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="a80aa-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="a80aa-114">Remarks</span></span>

<span data-ttu-id="a80aa-115">Les objets de formulaire appellent la méthode **IMAPIMessageSite:: CopyMessage** pour copier le message actif dans un nouveau dossier.</span><span class="sxs-lookup"><span data-stu-id="a80aa-115">Form objects call the **IMAPIMessageSite::CopyMessage** method to copy the current message to a new folder.</span></span> <span data-ttu-id="a80aa-116">**CopyMessage** ne change pas le message actuellement affiché à l'utilisateur, et aucune interface n'est renvoyée au formulaire pour le message nouvellement créé.</span><span class="sxs-lookup"><span data-stu-id="a80aa-116">**CopyMessage** does not change the message currently being displayed to the user, and no interface for the newly created message is returned to the form.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="a80aa-117">Remarques pour les responsables de l’implémentation</span><span class="sxs-lookup"><span data-stu-id="a80aa-117">Notes to implementers</span></span>

<span data-ttu-id="a80aa-118">Une implémentation type de la méthode **CopyMessage** effectue les tâches suivantes:</span><span class="sxs-lookup"><span data-stu-id="a80aa-118">A typical implementation of the **CopyMessage** method performs the following tasks:</span></span> 
  
1. <span data-ttu-id="a80aa-119">Crée un nouveau message pour le message en cours à copier.</span><span class="sxs-lookup"><span data-stu-id="a80aa-119">Creates a new message for the current message to be copied to.</span></span>
    
2. <span data-ttu-id="a80aa-120">Appelle la méthode [IPersistMessage:: Save](ipersistmessage-save.md) avec un pointeur vers le nouveau message dans le paramètre _pMessage_ et false dans le paramètre _fSameAsLoad_ .</span><span class="sxs-lookup"><span data-stu-id="a80aa-120">Calls the [IPersistMessage::Save](ipersistmessage-save.md) method with a pointer to the new message in the  _pMessage_ parameter and FALSE in the  _fSameAsLoad_ parameter.</span></span> 
    
3. <span data-ttu-id="a80aa-121">Appelle la méthode [IPersistMessage:: SaveCompleted](ipersistmessage-savecompleted.md) , en transmettant la valeur null dans le paramètre _pMessage_ .</span><span class="sxs-lookup"><span data-stu-id="a80aa-121">Calls the [IPersistMessage::SaveCompleted](ipersistmessage-savecompleted.md) method, passing NULL in the  _pMessage_ parameter.</span></span> 
    
4. <span data-ttu-id="a80aa-122">Appelle la méthode [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) sur le nouveau message.</span><span class="sxs-lookup"><span data-stu-id="a80aa-122">Calls the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method on the new message.</span></span> 
    
<span data-ttu-id="a80aa-123">Pour obtenir la liste des interfaces liées aux serveurs de formulaires, voir [MAPI Form interfaces](mapi-form-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="a80aa-123">For a list of interfaces that are related to form servers, see [MAPI Form Interfaces](mapi-form-interfaces.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="a80aa-124">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="a80aa-124">MFCMAPI reference</span></span>

<span data-ttu-id="a80aa-125">Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="a80aa-125">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="a80aa-126">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="a80aa-126">**File**</span></span>|<span data-ttu-id="a80aa-127">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="a80aa-127">**Function**</span></span>|<span data-ttu-id="a80aa-128">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="a80aa-128">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="a80aa-129">MyMAPIFormViewer. cpp</span><span class="sxs-lookup"><span data-stu-id="a80aa-129">MyMAPIFormViewer.cpp</span></span>  <br/> |<span data-ttu-id="a80aa-130">CMyMAPIFormViewer:: CopyMessage</span><span class="sxs-lookup"><span data-stu-id="a80aa-130">CMyMAPIFormViewer::CopyMessage</span></span>  <br/> |<span data-ttu-id="a80aa-131">Non implémenté.</span><span class="sxs-lookup"><span data-stu-id="a80aa-131">Not implemented.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a80aa-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a80aa-132">See also</span></span>



[<span data-ttu-id="a80aa-133">IMAPIProp::SaveChanges</span><span class="sxs-lookup"><span data-stu-id="a80aa-133">IMAPIProp::SaveChanges</span></span>](imapiprop-savechanges.md)
  
[<span data-ttu-id="a80aa-134">IPersistMessage::Save</span><span class="sxs-lookup"><span data-stu-id="a80aa-134">IPersistMessage::Save</span></span>](ipersistmessage-save.md)
  
[<span data-ttu-id="a80aa-135">IPersistMessage::SaveCompleted</span><span class="sxs-lookup"><span data-stu-id="a80aa-135">IPersistMessage::SaveCompleted</span></span>](ipersistmessage-savecompleted.md)
  
[<span data-ttu-id="a80aa-136">IMAPIMessageSite : IUnknown</span><span class="sxs-lookup"><span data-stu-id="a80aa-136">IMAPIMessageSite : IUnknown</span></span>](imapimessagesiteiunknown.md)


[<span data-ttu-id="a80aa-137">MFCMAPI comme un exemple de Code</span><span class="sxs-lookup"><span data-stu-id="a80aa-137">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="a80aa-138">Interfaces de formulaire MAPI</span><span class="sxs-lookup"><span data-stu-id="a80aa-138">MAPI Form Interfaces</span></span>](mapi-form-interfaces.md)

