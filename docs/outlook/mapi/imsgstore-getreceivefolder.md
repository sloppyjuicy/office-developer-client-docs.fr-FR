---
title: IMsgStoreGetReceiveFolder
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgStore.GetReceiveFolder
api_type:
- COM
ms.assetid: ccd9d623-a3cb-4e66-9649-78c3887cb726
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: ab21dcfb9011b675e3db4e4df29cb6ecafa6e7c6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435347"
---
# <a name="imsgstoregetreceivefolder"></a><span data-ttu-id="4215b-103">IMsgStore::GetReceiveFolder</span><span class="sxs-lookup"><span data-stu-id="4215b-103">IMsgStore::GetReceiveFolder</span></span>

  
  
<span data-ttu-id="4215b-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4215b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4215b-105">Obtient le dossier qui a été établi comme destination pour les messages entrants d’une classe de message spécifiée ou comme dossier de réception par défaut pour la magasin de messages.</span><span class="sxs-lookup"><span data-stu-id="4215b-105">Obtains the folder that was established as the destination for incoming messages of a specified message class or as the default receive folder for the message store.</span></span>
  
```cpp
HRESULT GetReceiveFolder(
  LPSTR lpszMessageClass,
  ULONG ulFlags,
  ULONG FAR * lpcbEntryID,
  LPENTRYID FAR * lppEntryID,
  LPSTR FAR * lppszExplicitClass
);
```

## <a name="parameters"></a><span data-ttu-id="4215b-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4215b-106">Parameters</span></span>

 <span data-ttu-id="4215b-107">_lpszMessageClass_</span><span class="sxs-lookup"><span data-stu-id="4215b-107">_lpszMessageClass_</span></span>
  
> <span data-ttu-id="4215b-108">[in] Pointeur vers une classe de message associée à un dossier de réception.</span><span class="sxs-lookup"><span data-stu-id="4215b-108">[in] A pointer to a message class that is associated with a receive folder.</span></span> <span data-ttu-id="4215b-109">Si le  _paramètre lpszMessageClass_ a la valeur NULL ou une chaîne vide, **GetReceiveFolder** renvoie le dossier de réception par défaut pour la magasin de messages.</span><span class="sxs-lookup"><span data-stu-id="4215b-109">If the  _lpszMessageClass_ parameter is set to NULL or an empty string, **GetReceiveFolder** returns the default receive folder for the message store.</span></span> 
    
 <span data-ttu-id="4215b-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="4215b-110">_ulFlags_</span></span>
  
> <span data-ttu-id="4215b-111">[in] Masque de bits d’indicateurs qui contrôle le type des chaînes transmises et renvoyées.</span><span class="sxs-lookup"><span data-stu-id="4215b-111">[in] A bitmask of flags that controls the type of the passed-in and returned strings.</span></span> <span data-ttu-id="4215b-112">L’indicateur suivant peut être définie :</span><span class="sxs-lookup"><span data-stu-id="4215b-112">The following flag can be set:</span></span>
    
<span data-ttu-id="4215b-113">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="4215b-113">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="4215b-114">La chaîne de classe de message est au format Unicode.</span><span class="sxs-lookup"><span data-stu-id="4215b-114">The message class string is in Unicode format.</span></span> <span data-ttu-id="4215b-115">Si l’MAPI_UNICODE n’est pas définie, la chaîne de classe de message est au format ANSI.</span><span class="sxs-lookup"><span data-stu-id="4215b-115">If the MAPI_UNICODE flag is not set, the message class string is in ANSI format.</span></span>
    
 <span data-ttu-id="4215b-116">_lpcbEntryID_</span><span class="sxs-lookup"><span data-stu-id="4215b-116">_lpcbEntryID_</span></span>
  
> <span data-ttu-id="4215b-117">[out] Pointeur vers le nombre d’byte dans l’identificateur d’entrée pointé par _le paramètre lppEntryID._</span><span class="sxs-lookup"><span data-stu-id="4215b-117">[out] A pointer to the byte count in the entry identifier pointed to by the  _lppEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="4215b-118">_lppEntryID_</span><span class="sxs-lookup"><span data-stu-id="4215b-118">_lppEntryID_</span></span>
  
> <span data-ttu-id="4215b-119">[out] Pointeur vers un pointeur vers l’identificateur d’entrée pour le dossier de réception demandé.</span><span class="sxs-lookup"><span data-stu-id="4215b-119">[out] A pointer to a pointer to the entry identifier for the requested receive folder.</span></span>
    
 <span data-ttu-id="4215b-120">_lppszExplicitClass_</span><span class="sxs-lookup"><span data-stu-id="4215b-120">_lppszExplicitClass_</span></span>
  
> <span data-ttu-id="4215b-121">[out] Pointeur vers un pointeur vers la classe de message qui définit explicitement comme dossier de réception le dossier pointé par  _lppEntryID_.</span><span class="sxs-lookup"><span data-stu-id="4215b-121">[out] A pointer to a pointer to the message class that explicitly sets as its receive folder the folder pointed to by  _lppEntryID_.</span></span> <span data-ttu-id="4215b-122">Cette classe de message doit être la même que la classe dans le paramètre  _lpszMessageClass_ ou une classe de base de cette classe.</span><span class="sxs-lookup"><span data-stu-id="4215b-122">This message class should either be the same as the class in the  _lpszMessageClass_ parameter, or a base class of that class.</span></span> <span data-ttu-id="4215b-123">La transmission de la valeur NULL indique que le dossier pointé par  _lppEntryID_ est le dossier de réception par défaut pour la magasin de messages.</span><span class="sxs-lookup"><span data-stu-id="4215b-123">Passing NULL indicates that the folder pointed to by  _lppEntryID_ is the default receive folder for the message store.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="4215b-124">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="4215b-124">Return value</span></span>

<span data-ttu-id="4215b-125">S_OK</span><span class="sxs-lookup"><span data-stu-id="4215b-125">S_OK</span></span> 
  
> <span data-ttu-id="4215b-126">Le dossier de réception a été renvoyé avec succès.</span><span class="sxs-lookup"><span data-stu-id="4215b-126">The receive folder was successfully returned.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="4215b-127">Remarques</span><span class="sxs-lookup"><span data-stu-id="4215b-127">Remarks</span></span>

<span data-ttu-id="4215b-128">La **méthode IMsgStore::GetReceiveFolder** obtient l’identificateur d’entrée d’un dossier de réception, un dossier désigné pour recevoir les messages entrants d’une classe de message particulière.</span><span class="sxs-lookup"><span data-stu-id="4215b-128">The **IMsgStore::GetReceiveFolder** method obtains the entry identifier of a receive folder, a folder designated to receive incoming messages of a particular message class.</span></span> <span data-ttu-id="4215b-129">Les appelants peuvent spécifier une classe de message ou null dans _le paramètre lpszMessageClass._</span><span class="sxs-lookup"><span data-stu-id="4215b-129">Callers can specify a message class or NULL in the  _lpszMessageClass_ parameter.</span></span> <span data-ttu-id="4215b-130">Si  _lpszMessageClass a_ la valeur NULL, **GetReceiveFolder** renvoie les valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="4215b-130">If  _lpszMessageClass_ is NULL, **GetReceiveFolder** returns the following values:</span></span> 
  
- <span data-ttu-id="4215b-131">Dans  _lppszExplicitClass_, le nom de la première classe de base de la classe de message pointée par  _lpszMessageClass_ qui ne définisse explicitement un dossier de réception.</span><span class="sxs-lookup"><span data-stu-id="4215b-131">In  _lppszExplicitClass_, the name of the first base class of the message class pointed to by  _lpszMessageClass_ that does explicitly set a receive folder.</span></span> 
    
- <span data-ttu-id="4215b-132">Dans _lppEntryID_, l’identificateur d’entrée du dossier de réception pour la classe de base pointée par le paramètre _lppszExplicitClass._</span><span class="sxs-lookup"><span data-stu-id="4215b-132">In  _lppEntryID_, the entry identifier of the receive folder for the base class pointed to by the  _lppszExplicitClass_ parameter.</span></span> 
    
<span data-ttu-id="4215b-133">Par exemple, supposons que le dossier de réception de la classe de message **IPM. Note** has been set to the entry identifier of the Inbox and **GetReceiveFolder** is called with the contents of  _lpszMessageClass_ set to **IPM. Note.Phone**.</span><span class="sxs-lookup"><span data-stu-id="4215b-133">For example, suppose the receive folder of the message class **IPM.Note** has been set to the entry identifier of the Inbox and **GetReceiveFolder** is called with the contents of  _lpszMessageClass_ set to **IPM.Note.Phone**.</span></span> <span data-ttu-id="4215b-134">Si **IPM. Note.Phone** does not have an explicit receive folder set, **GetReceiveFolder** returns the entry identifier of the Inbox in  _lppEntryID_ and **IPM. Remarque** dans  _lppszExplicitClass_.</span><span class="sxs-lookup"><span data-stu-id="4215b-134">If **IPM.Note.Phone** does not have an explicit receive folder set, **GetReceiveFolder** returns the entry identifier of the Inbox in  _lppEntryID_ and **IPM.Note** in  _lppszExplicitClass_.</span></span>
  
<span data-ttu-id="4215b-135">Si le client appelle **GetReceiveFolder** pour une classe de message et n’a pas de dossier de réception pour cette classe de message, _lppszExplicitClass_ est une chaîne de longueur nulle, une chaîne au format Unicode ou une chaîne au format ANSI, selon que le client a ou non paramétré l’indicateur MAPI_UNICODE dans le paramètre _ulFlags._</span><span class="sxs-lookup"><span data-stu-id="4215b-135">If the client calls **GetReceiveFolder** for a message class and has not set a receive folder for that message class,  _lppszExplicitClass_ is either a zero-length string, a string in Unicode format, or a string in ANSI format depending on whether the client set the MAPI_UNICODE flag in the  _ulFlags_ parameter.</span></span> 
  
<span data-ttu-id="4215b-136">Un dossier de réception par défaut, obtenu en passant la valeur NULL dans le paramètre  _lpszMessageClass,_ existe toujours pour chaque magasin de messages.</span><span class="sxs-lookup"><span data-stu-id="4215b-136">A default receive folder, obtained by passing NULL in the  _lpszMessageClass_ parameter, always exists for every message store.</span></span> 
  
<span data-ttu-id="4215b-137">Un client doit appeler la [fonction MAPIFreeBuffer](mapifreebuffer.md) lorsqu’elle est effectuée avec l’identificateur d’entrée renvoyé dans  _lppEntryID_ pour libérer la mémoire qui contient cet identificateur d’entrée.</span><span class="sxs-lookup"><span data-stu-id="4215b-137">A client should call the [MAPIFreeBuffer](mapifreebuffer.md) function when it is done with the entry identifier returned in  _lppEntryID_ to free the memory that holds that entry identifier.</span></span> <span data-ttu-id="4215b-138">Il doit également appeler **MAPIFreeBuffer** lorsqu’il est terminé avec la chaîne de classe de message renvoyée dans  _lppszExplicitClass_ pour libérer la mémoire qui contient cette chaîne.</span><span class="sxs-lookup"><span data-stu-id="4215b-138">It should also call **MAPIFreeBuffer** when it is done with the message class string returned in  _lppszExplicitClass_ to free the memory that holds that string.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="4215b-139">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="4215b-139">MFCMAPI reference</span></span>

<span data-ttu-id="4215b-140">Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="4215b-140">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="4215b-141">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="4215b-141">**File**</span></span>|<span data-ttu-id="4215b-142">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="4215b-142">**Function**</span></span>|<span data-ttu-id="4215b-143">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="4215b-143">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="4215b-144">MAPIFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="4215b-144">MAPIFunctions.cpp</span></span>  <br/> |<span data-ttu-id="4215b-145">GetInbox</span><span class="sxs-lookup"><span data-stu-id="4215b-145">GetInbox</span></span>  <br/> |<span data-ttu-id="4215b-146">MFCMAPI utilise la **méthode IMsgStore::GetReceiveFolder** pour localiser le dossier Boîte de réception.</span><span class="sxs-lookup"><span data-stu-id="4215b-146">MFCMAPI uses the **IMsgStore::GetReceiveFolder** method to locate the Inbox folder.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="4215b-147">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4215b-147">See also</span></span>



[<span data-ttu-id="4215b-148">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="4215b-148">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="4215b-149">IMsgStore : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="4215b-149">IMsgStore : IMAPIProp</span></span>](imsgstoreimapiprop.md)


[<span data-ttu-id="4215b-150">MFCMAPI comme un exemple de Code</span><span class="sxs-lookup"><span data-stu-id="4215b-150">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

