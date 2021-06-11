---
title: IMsgStoreSetReceiveFolder
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgStore.SetReceiveFolder
api_type:
- COM
ms.assetid: 469f0412-1343-47ce-b6e8-e0d5e56c29bb
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: efa5d60098fd5f16328669249a8445a124d9878b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434087"
---
# <a name="imsgstoresetreceivefolder"></a><span data-ttu-id="8d9ab-103">IMsgStore::SetReceiveFolder</span><span class="sxs-lookup"><span data-stu-id="8d9ab-103">IMsgStore::SetReceiveFolder</span></span>

  
  
<span data-ttu-id="8d9ab-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8d9ab-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8d9ab-105">Établit un dossier comme destination pour les messages entrants d’une classe de message particulière.</span><span class="sxs-lookup"><span data-stu-id="8d9ab-105">Establishes a folder as the destination for incoming messages of a particular message class.</span></span>
  
```cpp
HRESULT SetReceiveFolder(
  LPSTR lpszMessageClass,
  ULONG ulFlags,
  ULONG cbEntryID,
  LPENTRYID lpEntryID
);
```

## <a name="parameters"></a><span data-ttu-id="8d9ab-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="8d9ab-106">Parameters</span></span>

 <span data-ttu-id="8d9ab-107">_lpszMessageClass_</span><span class="sxs-lookup"><span data-stu-id="8d9ab-107">_lpszMessageClass_</span></span>
  
> <span data-ttu-id="8d9ab-108">[in] Pointeur vers la classe de message à associer au nouveau dossier de réception.</span><span class="sxs-lookup"><span data-stu-id="8d9ab-108">[in] A pointer to the message class that is to be associated with the new receive folder.</span></span> <span data-ttu-id="8d9ab-109">Si le  _paramètre lpszMessageClass_ a la valeur NULL ou une chaîne vide, **SetReceiveFolder** définit le dossier de réception par défaut pour la magasin de messages.</span><span class="sxs-lookup"><span data-stu-id="8d9ab-109">If the  _lpszMessageClass_ parameter is set to NULL or an empty string, **SetReceiveFolder** sets the default receive folder for the message store.</span></span> 
    
 <span data-ttu-id="8d9ab-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="8d9ab-110">_ulFlags_</span></span>
  
> <span data-ttu-id="8d9ab-111">[in] Masque de bits d’indicateurs qui contrôle le type du texte dans les chaînes transmises.</span><span class="sxs-lookup"><span data-stu-id="8d9ab-111">[in] A bitmask of flags that controls the type of the text in the passed-in strings.</span></span> <span data-ttu-id="8d9ab-112">L’indicateur suivant peut être définie :</span><span class="sxs-lookup"><span data-stu-id="8d9ab-112">The following flag can be set:</span></span>
    
<span data-ttu-id="8d9ab-113">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="8d9ab-113">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="8d9ab-114">La chaîne de classe de message est au format Unicode.</span><span class="sxs-lookup"><span data-stu-id="8d9ab-114">The message class string is in Unicode format.</span></span> <span data-ttu-id="8d9ab-115">Si l’MAPI_UNICODE n’est pas définie, la chaîne de classe de message est au format ANSI.</span><span class="sxs-lookup"><span data-stu-id="8d9ab-115">If the MAPI_UNICODE flag is not set, the message class string is in ANSI format.</span></span>
    
 <span data-ttu-id="8d9ab-116">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="8d9ab-116">_cbEntryID_</span></span>
  
> <span data-ttu-id="8d9ab-117">[in] Nombre d’bytes dans l’identificateur d’entrée pointé par _le paramètre lpEntryID._</span><span class="sxs-lookup"><span data-stu-id="8d9ab-117">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="8d9ab-118">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="8d9ab-118">_lpEntryID_</span></span>
  
> <span data-ttu-id="8d9ab-119">[in] Pointeur vers l’identificateur d’entrée du dossier à établir en tant que dossier de réception.</span><span class="sxs-lookup"><span data-stu-id="8d9ab-119">[in] A pointer to the entry identifier of the folder to establish as the receive folder.</span></span> <span data-ttu-id="8d9ab-120">Si le  _paramètre lpEntryID_ est définie sur NULL, **SetReceiveFolder** remplace le dossier de réception actuel par la valeur par défaut de la boutique de messages.</span><span class="sxs-lookup"><span data-stu-id="8d9ab-120">If the  _lpEntryID_ parameter is set to NULL, **SetReceiveFolder** replaces the current receive folder with the message store's default.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="8d9ab-121">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="8d9ab-121">Return value</span></span>

<span data-ttu-id="8d9ab-122">S_OK</span><span class="sxs-lookup"><span data-stu-id="8d9ab-122">S_OK</span></span> 
  
> <span data-ttu-id="8d9ab-123">Un dossier de réception a été correctement établi.</span><span class="sxs-lookup"><span data-stu-id="8d9ab-123">A receive folder was successfully established.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="8d9ab-124">Remarques</span><span class="sxs-lookup"><span data-stu-id="8d9ab-124">Remarks</span></span>

<span data-ttu-id="8d9ab-125">La **méthode IMsgStore::SetReceiveFolder** définit ou modifie le dossier de réception d’une classe de message particulière.</span><span class="sxs-lookup"><span data-stu-id="8d9ab-125">The **IMsgStore::SetReceiveFolder** method sets or changes the receive folder for a particular message class.</span></span> <span data-ttu-id="8d9ab-126">Avec **SetReceiveFolder,** un client peut, à l’aide d’appels successifs, spécifier un dossier de réception différent pour chaque classe de message définie ou spécifier que les messages entrants pour plusieurs classes de messages sont tous placés dans le même dossier.</span><span class="sxs-lookup"><span data-stu-id="8d9ab-126">With **SetReceiveFolder**, a client can, by using successive calls, specify a different receive folder for each defined message class or specify that incoming messages for multiple message classes all go to the same folder.</span></span> <span data-ttu-id="8d9ab-127">Par exemple, un client peut avoir sa propre classe de messages arrive dans son propre dossier.</span><span class="sxs-lookup"><span data-stu-id="8d9ab-127">For example, a client can have its own class of messages arrive in its own folder.</span></span> <span data-ttu-id="8d9ab-128">Une application de télécopie peut désigner un dossier dans lequel le fournisseur de magasins place les télécopies entrantes et un autre dossier dans lequel il place les télécopies sortantes.</span><span class="sxs-lookup"><span data-stu-id="8d9ab-128">A fax application can designate one folder in which the store provider puts incoming faxes and another folder in which the provider puts outgoing faxes.</span></span>
  
<span data-ttu-id="8d9ab-129">Si une erreur se produit pendant l’appel de **SetReceiveFolder,** le paramètre du dossier de réception reste inchangé.</span><span class="sxs-lookup"><span data-stu-id="8d9ab-129">If an error occurs during the call to **SetReceiveFolder**, the receive folder setting remains unchanged.</span></span> 
  
<span data-ttu-id="8d9ab-130">Si **SetReceiveFolder** modifie le paramètre du dossier de réception avec  _lpEntryID_ définie sur NULL, indiquant que le dossier de réception par défaut doit être définie, **SetReceiveFolder** renvoie S_OK même s’il n’y avait aucun paramètre existant pour la classe de message indiquée.</span><span class="sxs-lookup"><span data-stu-id="8d9ab-130">If **SetReceiveFolder** changes the receive folder setting with  _lpEntryID_ set to NULL, indicating that the default receive folder should be set, **SetReceiveFolder** returns S_OK even if there was no existing setting for the indicated message class.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="8d9ab-131">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="8d9ab-131">MFCMAPI reference</span></span>

<span data-ttu-id="8d9ab-132">Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="8d9ab-132">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="8d9ab-133">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="8d9ab-133">**File**</span></span>|<span data-ttu-id="8d9ab-134">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="8d9ab-134">**Function**</span></span>|<span data-ttu-id="8d9ab-135">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="8d9ab-135">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="8d9ab-136">MsgStoreDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="8d9ab-136">MsgStoreDlg.cpp</span></span>  <br/> |<span data-ttu-id="8d9ab-137">CMsgStoreDlg::OnSetReceiveFolder</span><span class="sxs-lookup"><span data-stu-id="8d9ab-137">CMsgStoreDlg::OnSetReceiveFolder</span></span>  <br/> |<span data-ttu-id="8d9ab-138">MFCMAPI utilise la méthode **IMsgStore::SetReceiveFolder** pour définir un dossier comme dossier de réception pour une classe de message particulière.</span><span class="sxs-lookup"><span data-stu-id="8d9ab-138">MFCMAPI uses the **IMsgStore::SetReceiveFolder** method to set a folder as the receive folder for a particular message class.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="8d9ab-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8d9ab-139">See also</span></span>



[<span data-ttu-id="8d9ab-140">IMsgStore : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="8d9ab-140">IMsgStore : IMAPIProp</span></span>](imsgstoreimapiprop.md)


[<span data-ttu-id="8d9ab-141">MFCMAPI comme un exemple de Code</span><span class="sxs-lookup"><span data-stu-id="8d9ab-141">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

