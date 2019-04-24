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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: efa5d60098fd5f16328669249a8445a124d9878b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317338"
---
# <a name="imsgstoresetreceivefolder"></a><span data-ttu-id="d6854-103">IMsgStore::SetReceiveFolder</span><span class="sxs-lookup"><span data-stu-id="d6854-103">IMsgStore::SetReceiveFolder</span></span>

  
  
<span data-ttu-id="d6854-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d6854-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d6854-105">Établit un dossier comme destination pour les messages entrants d'une classe de message particulière.</span><span class="sxs-lookup"><span data-stu-id="d6854-105">Establishes a folder as the destination for incoming messages of a particular message class.</span></span>
  
```cpp
HRESULT SetReceiveFolder(
  LPSTR lpszMessageClass,
  ULONG ulFlags,
  ULONG cbEntryID,
  LPENTRYID lpEntryID
);
```

## <a name="parameters"></a><span data-ttu-id="d6854-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d6854-106">Parameters</span></span>

 <span data-ttu-id="d6854-107">_lpszMessageClass_</span><span class="sxs-lookup"><span data-stu-id="d6854-107">_lpszMessageClass_</span></span>
  
> <span data-ttu-id="d6854-108">dans Pointeur vers la classe de message qui doit être associée au nouveau dossier de réception.</span><span class="sxs-lookup"><span data-stu-id="d6854-108">[in] A pointer to the message class that is to be associated with the new receive folder.</span></span> <span data-ttu-id="d6854-109">Si le paramètre _lpszMessageClass_ est défini sur null ou sur une chaîne vide, **SetReceiveFolder** définit le dossier de réception par défaut pour la Banque de messages.</span><span class="sxs-lookup"><span data-stu-id="d6854-109">If the  _lpszMessageClass_ parameter is set to NULL or an empty string, **SetReceiveFolder** sets the default receive folder for the message store.</span></span> 
    
 <span data-ttu-id="d6854-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="d6854-110">_ulFlags_</span></span>
  
> <span data-ttu-id="d6854-111">dans Masque de bits des indicateurs qui contrôle le type du texte dans les chaînes transmises.</span><span class="sxs-lookup"><span data-stu-id="d6854-111">[in] A bitmask of flags that controls the type of the text in the passed-in strings.</span></span> <span data-ttu-id="d6854-112">L'indicateur suivant peut être défini:</span><span class="sxs-lookup"><span data-stu-id="d6854-112">The following flag can be set:</span></span>
    
<span data-ttu-id="d6854-113">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="d6854-113">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="d6854-114">La chaîne de la classe de message est au format Unicode.</span><span class="sxs-lookup"><span data-stu-id="d6854-114">The message class string is in Unicode format.</span></span> <span data-ttu-id="d6854-115">Si l'indicateur MAPI_UNICODE n'est pas défini, la chaîne de la classe de message est au format ANSI.</span><span class="sxs-lookup"><span data-stu-id="d6854-115">If the MAPI_UNICODE flag is not set, the message class string is in ANSI format.</span></span>
    
 <span data-ttu-id="d6854-116">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="d6854-116">_cbEntryID_</span></span>
  
> <span data-ttu-id="d6854-117">dans Nombre d'octets dans l'identificateur d'entrée pointé par le paramètre _lpEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="d6854-117">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="d6854-118">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="d6854-118">_lpEntryID_</span></span>
  
> <span data-ttu-id="d6854-119">dans Pointeur vers l'identificateur d'entrée du dossier à établir en tant que dossier de réception.</span><span class="sxs-lookup"><span data-stu-id="d6854-119">[in] A pointer to the entry identifier of the folder to establish as the receive folder.</span></span> <span data-ttu-id="d6854-120">Si le paramètre _lpEntryID_ est défini sur null, **SetReceiveFolder** remplace le dossier de réception actuel par la valeur par défaut de la Banque de messages.</span><span class="sxs-lookup"><span data-stu-id="d6854-120">If the  _lpEntryID_ parameter is set to NULL, **SetReceiveFolder** replaces the current receive folder with the message store's default.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="d6854-121">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="d6854-121">Return value</span></span>

<span data-ttu-id="d6854-122">S_OK</span><span class="sxs-lookup"><span data-stu-id="d6854-122">S_OK</span></span> 
  
> <span data-ttu-id="d6854-123">Un dossier de réception a été correctement établi.</span><span class="sxs-lookup"><span data-stu-id="d6854-123">A receive folder was successfully established.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="d6854-124">Remarques</span><span class="sxs-lookup"><span data-stu-id="d6854-124">Remarks</span></span>

<span data-ttu-id="d6854-125">La méthode **IMsgStore:: SetReceiveFolder** définit ou modifie le dossier de réception d'une classe de message particulière.</span><span class="sxs-lookup"><span data-stu-id="d6854-125">The **IMsgStore::SetReceiveFolder** method sets or changes the receive folder for a particular message class.</span></span> <span data-ttu-id="d6854-126">Avec **SetReceiveFolder**, un client peut, en utilisant des appels successifs, spécifier un autre dossier de réception pour chaque classe de message définie ou spécifier que les messages entrants pour plusieurs classes de message accèdent au même dossier.</span><span class="sxs-lookup"><span data-stu-id="d6854-126">With **SetReceiveFolder**, a client can, by using successive calls, specify a different receive folder for each defined message class or specify that incoming messages for multiple message classes all go to the same folder.</span></span> <span data-ttu-id="d6854-127">Par exemple, un client peut avoir sa propre classe de messages arrivant dans son propre dossier.</span><span class="sxs-lookup"><span data-stu-id="d6854-127">For example, a client can have its own class of messages arrive in its own folder.</span></span> <span data-ttu-id="d6854-128">Une application de télécopie peut désigner un dossier dans lequel le fournisseur de banque d'applications place les télécopies entrantes et un autre dossier dans lequel le fournisseur place les télécopies sortantes.</span><span class="sxs-lookup"><span data-stu-id="d6854-128">A fax application can designate one folder in which the store provider puts incoming faxes and another folder in which the provider puts outgoing faxes.</span></span>
  
<span data-ttu-id="d6854-129">Si une erreur se produit lors de l'appel à **SetReceiveFolder**, le paramètre de dossier de réception reste inchangé.</span><span class="sxs-lookup"><span data-stu-id="d6854-129">If an error occurs during the call to **SetReceiveFolder**, the receive folder setting remains unchanged.</span></span> 
  
<span data-ttu-id="d6854-130">Si **SetReceiveFolder** remplace le paramètre de dossier de réception par _lpEntryID_ par null, ce qui indique que le dossier de réception par défaut doit être défini, **SetReceiveFolder** renvoie S_OK même s'il n'existe aucun paramètre pour le spécifié classe de message.</span><span class="sxs-lookup"><span data-stu-id="d6854-130">If **SetReceiveFolder** changes the receive folder setting with  _lpEntryID_ set to NULL, indicating that the default receive folder should be set, **SetReceiveFolder** returns S_OK even if there was no existing setting for the indicated message class.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="d6854-131">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="d6854-131">MFCMAPI reference</span></span>

<span data-ttu-id="d6854-132">Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="d6854-132">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="d6854-133">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="d6854-133">**File**</span></span>|<span data-ttu-id="d6854-134">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="d6854-134">**Function**</span></span>|<span data-ttu-id="d6854-135">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="d6854-135">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="d6854-136">MsgStoreDlg. cpp</span><span class="sxs-lookup"><span data-stu-id="d6854-136">MsgStoreDlg.cpp</span></span>  <br/> |<span data-ttu-id="d6854-137">CMsgStoreDlg:: OnSetReceiveFolder</span><span class="sxs-lookup"><span data-stu-id="d6854-137">CMsgStoreDlg::OnSetReceiveFolder</span></span>  <br/> |<span data-ttu-id="d6854-138">MFCMAPI utilise la méthode **IMsgStore:: SetReceiveFolder** pour définir un dossier en tant que dossier de réception pour une classe de message particulière.</span><span class="sxs-lookup"><span data-stu-id="d6854-138">MFCMAPI uses the **IMsgStore::SetReceiveFolder** method to set a folder as the receive folder for a particular message class.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d6854-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d6854-139">See also</span></span>



[<span data-ttu-id="d6854-140">IMsgStore : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="d6854-140">IMsgStore : IMAPIProp</span></span>](imsgstoreimapiprop.md)


[<span data-ttu-id="d6854-141">MFCMAPI comme un exemple de Code</span><span class="sxs-lookup"><span data-stu-id="d6854-141">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

