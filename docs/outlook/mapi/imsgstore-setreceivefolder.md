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
ms.openlocfilehash: c30c38e1dbc944fd3016badf2621aef5de1e08f4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784273"
---
# <a name="imsgstoresetreceivefolder"></a><span data-ttu-id="36741-103">IMsgStore::SetReceiveFolder</span><span class="sxs-lookup"><span data-stu-id="36741-103">IMsgStore::SetReceiveFolder</span></span>

  
  
<span data-ttu-id="36741-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="36741-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="36741-105">Établissement d’un dossier comme destination pour les messages entrants d’une classe de message particulier.</span><span class="sxs-lookup"><span data-stu-id="36741-105">Establishes a folder as the destination for incoming messages of a particular message class.</span></span>
  
```cpp
HRESULT SetReceiveFolder(
  LPSTR lpszMessageClass,
  ULONG ulFlags,
  ULONG cbEntryID,
  LPENTRYID lpEntryID
);
```

## <a name="parameters"></a><span data-ttu-id="36741-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="36741-106">Parameters</span></span>

 <span data-ttu-id="36741-107">_lpszMessageClass_</span><span class="sxs-lookup"><span data-stu-id="36741-107">_lpszMessageClass_</span></span>
  
> <span data-ttu-id="36741-108">[in] Un pointeur vers la classe de message qui sera associé au nouveau dossier de réception.</span><span class="sxs-lookup"><span data-stu-id="36741-108">[in] A pointer to the message class that is to be associated with the new receive folder.</span></span> <span data-ttu-id="36741-109">Si le paramètre _lpszMessageClass_ est défini sur NULL ou une chaîne vide, **SetReceiveFolder** définit la valeur par défaut recevoir de dossier pour la banque de messages.</span><span class="sxs-lookup"><span data-stu-id="36741-109">If the  _lpszMessageClass_ parameter is set to NULL or an empty string, **SetReceiveFolder** sets the default receive folder for the message store.</span></span> 
    
 <span data-ttu-id="36741-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="36741-110">_ulFlags_</span></span>
  
> <span data-ttu-id="36741-111">[in] Masque de bits d’indicateurs qui contrôle le type du texte dans les chaînes dans le passé.</span><span class="sxs-lookup"><span data-stu-id="36741-111">[in] A bitmask of flags that controls the type of the text in the passed-in strings.</span></span> <span data-ttu-id="36741-112">Vous pouvez définir l’indicateur suivant :</span><span class="sxs-lookup"><span data-stu-id="36741-112">The following flag can be set:</span></span>
    
<span data-ttu-id="36741-113">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="36741-113">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="36741-114">La chaîne de classe de message est au format Unicode.</span><span class="sxs-lookup"><span data-stu-id="36741-114">The message class string is in Unicode format.</span></span> <span data-ttu-id="36741-115">Si l’indicateur MAPI_UNICODE n’est pas définie, la chaîne de classe de message est au format ANSI.</span><span class="sxs-lookup"><span data-stu-id="36741-115">If the MAPI_UNICODE flag is not set, the message class string is in ANSI format.</span></span>
    
 <span data-ttu-id="36741-116">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="36741-116">_cbEntryID_</span></span>
  
> <span data-ttu-id="36741-117">[in] Le nombre d’octets dans l’identificateur d’entrée indiqué par le paramètre _lpEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="36741-117">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="36741-118">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="36741-118">_lpEntryID_</span></span>
  
> <span data-ttu-id="36741-119">[in] Pointeur vers l’identificateur d’entrée du dossier à établir en tant que le dossier de réception.</span><span class="sxs-lookup"><span data-stu-id="36741-119">[in] A pointer to the entry identifier of the folder to establish as the receive folder.</span></span> <span data-ttu-id="36741-120">Si le paramètre _lpEntryID_ est défini sur NULL, **SetReceiveFolder** remplace actuel recevoir de dossier par défaut de la banque de messages.</span><span class="sxs-lookup"><span data-stu-id="36741-120">If the  _lpEntryID_ parameter is set to NULL, **SetReceiveFolder** replaces the current receive folder with the message store's default.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="36741-121">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="36741-121">Return value</span></span>

<span data-ttu-id="36741-122">S_OK</span><span class="sxs-lookup"><span data-stu-id="36741-122">S_OK</span></span> 
  
> <span data-ttu-id="36741-123">Un dossier de réception a été établi.</span><span class="sxs-lookup"><span data-stu-id="36741-123">A receive folder was successfully established.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="36741-124">Remarques</span><span class="sxs-lookup"><span data-stu-id="36741-124">Remarks</span></span>

<span data-ttu-id="36741-125">La méthode **IMsgStore::SetReceiveFolder** définit ou modifie le dossier de réception pour une classe de message particulier.</span><span class="sxs-lookup"><span data-stu-id="36741-125">The **IMsgStore::SetReceiveFolder** method sets or changes the receive folder for a particular message class.</span></span> <span data-ttu-id="36741-126">Avec **SetReceiveFolder**, un client peut, à l’aide d’appels successifs, spécifiez un autre dossier pour chaque classe de message défini de réception ou spécifier que les messages entrants pour plusieurs classes de message toutes les atteindre le même dossier.</span><span class="sxs-lookup"><span data-stu-id="36741-126">With **SetReceiveFolder**, a client can, by using successive calls, specify a different receive folder for each defined message class or specify that incoming messages for multiple message classes all go to the same folder.</span></span> <span data-ttu-id="36741-127">Par exemple, un client peut avoir sa propre classe de messages arrivent dans son propre dossier.</span><span class="sxs-lookup"><span data-stu-id="36741-127">For example, a client can have its own class of messages arrive in its own folder.</span></span> <span data-ttu-id="36741-128">Une application de télécopie peut désigner un dossier dans lequel le fournisseur de banque place les télécopies entrantes et un autre dossier dans lequel le fournisseur met les télécopies sortantes.</span><span class="sxs-lookup"><span data-stu-id="36741-128">A fax application can designate one folder in which the store provider puts incoming faxes and another folder in which the provider puts outgoing faxes.</span></span>
  
<span data-ttu-id="36741-129">Si une erreur se produit pendant l’appel à **SetReceiveFolder**, le paramètre de dossier de réception reste inchangé.</span><span class="sxs-lookup"><span data-stu-id="36741-129">If an error occurs during the call to **SetReceiveFolder**, the receive folder setting remains unchanged.</span></span> 
  
<span data-ttu-id="36741-130">Si **SetReceiveFolder** modifie le paramètre de dossier de réception avec _lpEntryID_ valeur NULL, indiquant que le dossier de réception par défaut doit être défini, **SetReceiveFolder** renvoie S_OK même si aucun paramètre existant pour le texte indiqué s’est produite classe de message.</span><span class="sxs-lookup"><span data-stu-id="36741-130">If **SetReceiveFolder** changes the receive folder setting with  _lpEntryID_ set to NULL, indicating that the default receive folder should be set, **SetReceiveFolder** returns S_OK even if there was no existing setting for the indicated message class.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="36741-131">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="36741-131">MFCMAPI reference</span></span>

<span data-ttu-id="36741-132">Pour des exemples de code MFCMAPI, voir le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="36741-132">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="36741-133">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="36741-133">**File**</span></span>|<span data-ttu-id="36741-134">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="36741-134">**Function**</span></span>|<span data-ttu-id="36741-135">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="36741-135">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="36741-136">MsgStoreDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="36741-136">MsgStoreDlg.cpp</span></span>  <br/> |<span data-ttu-id="36741-137">CMsgStoreDlg::OnSetReceiveFolder</span><span class="sxs-lookup"><span data-stu-id="36741-137">CMsgStoreDlg::OnSetReceiveFolder</span></span>  <br/> |<span data-ttu-id="36741-138">MFCMAPI utilise la méthode **IMsgStore::SetReceiveFolder** pour définir un dossier sous le dossier de réception pour une classe de message particulier.</span><span class="sxs-lookup"><span data-stu-id="36741-138">MFCMAPI uses the **IMsgStore::SetReceiveFolder** method to set a folder as the receive folder for a particular message class.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="36741-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="36741-139">See also</span></span>



[<span data-ttu-id="36741-140">IMsgStore : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="36741-140">IMsgStore : IMAPIProp</span></span>](imsgstoreimapiprop.md)


[<span data-ttu-id="36741-141">MFCMAPI comme un exemple de Code</span><span class="sxs-lookup"><span data-stu-id="36741-141">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

