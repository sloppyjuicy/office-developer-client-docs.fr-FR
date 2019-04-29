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
# <a name="imsgstoregetreceivefolder"></a><span data-ttu-id="46985-103">IMsgStore::GetReceiveFolder</span><span class="sxs-lookup"><span data-stu-id="46985-103">IMsgStore::GetReceiveFolder</span></span>

  
  
<span data-ttu-id="46985-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="46985-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="46985-105">Obtient le dossier qui a été établi comme destination pour les messages entrants d'une classe de message spécifiée ou comme dossier de réception par défaut pour la Banque de messages.</span><span class="sxs-lookup"><span data-stu-id="46985-105">Obtains the folder that was established as the destination for incoming messages of a specified message class or as the default receive folder for the message store.</span></span>
  
```cpp
HRESULT GetReceiveFolder(
  LPSTR lpszMessageClass,
  ULONG ulFlags,
  ULONG FAR * lpcbEntryID,
  LPENTRYID FAR * lppEntryID,
  LPSTR FAR * lppszExplicitClass
);
```

## <a name="parameters"></a><span data-ttu-id="46985-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="46985-106">Parameters</span></span>

 <span data-ttu-id="46985-107">_lpszMessageClass_</span><span class="sxs-lookup"><span data-stu-id="46985-107">_lpszMessageClass_</span></span>
  
> <span data-ttu-id="46985-108">dans Pointeur vers une classe de message qui est associée à un dossier de réception.</span><span class="sxs-lookup"><span data-stu-id="46985-108">[in] A pointer to a message class that is associated with a receive folder.</span></span> <span data-ttu-id="46985-109">Si le paramètre _lpszMessageClass_ est défini sur null ou sur une chaîne vide, **GetReceiveFolder** renvoie le dossier de réception par défaut pour la Banque de messages.</span><span class="sxs-lookup"><span data-stu-id="46985-109">If the  _lpszMessageClass_ parameter is set to NULL or an empty string, **GetReceiveFolder** returns the default receive folder for the message store.</span></span> 
    
 <span data-ttu-id="46985-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="46985-110">_ulFlags_</span></span>
  
> <span data-ttu-id="46985-111">dans Masque de bits des indicateurs qui contrôle le type des chaînes transmises et renvoyées.</span><span class="sxs-lookup"><span data-stu-id="46985-111">[in] A bitmask of flags that controls the type of the passed-in and returned strings.</span></span> <span data-ttu-id="46985-112">L'indicateur suivant peut être défini:</span><span class="sxs-lookup"><span data-stu-id="46985-112">The following flag can be set:</span></span>
    
<span data-ttu-id="46985-113">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="46985-113">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="46985-114">La chaîne de la classe de message est au format Unicode.</span><span class="sxs-lookup"><span data-stu-id="46985-114">The message class string is in Unicode format.</span></span> <span data-ttu-id="46985-115">Si l'indicateur MAPI_UNICODE n'est pas défini, la chaîne de la classe de message est au format ANSI.</span><span class="sxs-lookup"><span data-stu-id="46985-115">If the MAPI_UNICODE flag is not set, the message class string is in ANSI format.</span></span>
    
 <span data-ttu-id="46985-116">_lpcbEntryID_</span><span class="sxs-lookup"><span data-stu-id="46985-116">_lpcbEntryID_</span></span>
  
> <span data-ttu-id="46985-117">remarquer Pointeur vers le nombre d'octets dans l'identificateur d'entrée pointé par le paramètre _lppEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="46985-117">[out] A pointer to the byte count in the entry identifier pointed to by the  _lppEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="46985-118">_lppEntryID_</span><span class="sxs-lookup"><span data-stu-id="46985-118">_lppEntryID_</span></span>
  
> <span data-ttu-id="46985-119">remarquer Pointeur vers un pointeur vers l'identificateur d'entrée pour le dossier de réception demandé.</span><span class="sxs-lookup"><span data-stu-id="46985-119">[out] A pointer to a pointer to the entry identifier for the requested receive folder.</span></span>
    
 <span data-ttu-id="46985-120">_lppszExplicitClass_</span><span class="sxs-lookup"><span data-stu-id="46985-120">_lppszExplicitClass_</span></span>
  
> <span data-ttu-id="46985-121">remarquer Pointeur vers un pointeur vers la classe de message qui définit explicitement comme dossier de réception le dossier vers lequel pointe _lppEntryID_.</span><span class="sxs-lookup"><span data-stu-id="46985-121">[out] A pointer to a pointer to the message class that explicitly sets as its receive folder the folder pointed to by  _lppEntryID_.</span></span> <span data-ttu-id="46985-122">Cette classe de message doit être la même que la classe dans le paramètre _lpszMessageClass_ , ou une classe de base de cette classe.</span><span class="sxs-lookup"><span data-stu-id="46985-122">This message class should either be the same as the class in the  _lpszMessageClass_ parameter, or a base class of that class.</span></span> <span data-ttu-id="46985-123">La transmission de la valeur NULL indique que le dossier désigné par _lppEntryID_ est le dossier de réception par défaut pour la Banque de messages.</span><span class="sxs-lookup"><span data-stu-id="46985-123">Passing NULL indicates that the folder pointed to by  _lppEntryID_ is the default receive folder for the message store.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="46985-124">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="46985-124">Return value</span></span>

<span data-ttu-id="46985-125">S_OK</span><span class="sxs-lookup"><span data-stu-id="46985-125">S_OK</span></span> 
  
> <span data-ttu-id="46985-126">Le dossier de réception a été correctement renvoyé.</span><span class="sxs-lookup"><span data-stu-id="46985-126">The receive folder was successfully returned.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="46985-127">Remarques</span><span class="sxs-lookup"><span data-stu-id="46985-127">Remarks</span></span>

<span data-ttu-id="46985-128">La méthode **IMsgStore:: GetReceiveFolder** obtient l'identificateur d'entrée d'un dossier de réception, un dossier destiné à recevoir les messages entrants d'une classe de message particulière.</span><span class="sxs-lookup"><span data-stu-id="46985-128">The **IMsgStore::GetReceiveFolder** method obtains the entry identifier of a receive folder, a folder designated to receive incoming messages of a particular message class.</span></span> <span data-ttu-id="46985-129">Les appelants peuvent spécifier une classe de message ou une valeur NULL dans le paramètre _lpszMessageClass_ .</span><span class="sxs-lookup"><span data-stu-id="46985-129">Callers can specify a message class or NULL in the  _lpszMessageClass_ parameter.</span></span> <span data-ttu-id="46985-130">Si _lpszMessageClass_ a la valeur null, **GetReceiveFolder** renvoie les valeurs suivantes:</span><span class="sxs-lookup"><span data-stu-id="46985-130">If  _lpszMessageClass_ is NULL, **GetReceiveFolder** returns the following values:</span></span> 
  
- <span data-ttu-id="46985-131">Dans _lppszExplicitClass_, le nom de la première classe de base de la classe de message désignée par _lpszMessageClass_ , qui définit explicitement un dossier de réception.</span><span class="sxs-lookup"><span data-stu-id="46985-131">In  _lppszExplicitClass_, the name of the first base class of the message class pointed to by  _lpszMessageClass_ that does explicitly set a receive folder.</span></span> 
    
- <span data-ttu-id="46985-132">Dans _lppEntryID_, l'identificateur d'entrée du dossier de réception de la classe de base vers laquelle pointe le paramètre _lppszExplicitClass_ .</span><span class="sxs-lookup"><span data-stu-id="46985-132">In  _lppEntryID_, the entry identifier of the receive folder for the base class pointed to by the  _lppszExplicitClass_ parameter.</span></span> 
    
<span data-ttu-id="46985-133">Par exemple, supposons que le dossier de réception de la classe de message **IPM. Note** a été défini sur l'identificateur d'entrée de la boîte de réception et **GetReceiveFolder** est appelé avec le contenu de _lpszMessageClass_ défini sur **IPM. Note. Phone**.</span><span class="sxs-lookup"><span data-stu-id="46985-133">For example, suppose the receive folder of the message class **IPM.Note** has been set to the entry identifier of the Inbox and **GetReceiveFolder** is called with the contents of  _lpszMessageClass_ set to **IPM.Note.Phone**.</span></span> <span data-ttu-id="46985-134">Si **IPM. Note. Phone** ne dispose pas d'un jeu de dossiers de réception explicite, **GetReceiveFolder** renvoie l'identificateur d'entrée de la boîte de réception dans _lppEntryID_ et **IPM. Remarque** dans _lppszExplicitClass_.</span><span class="sxs-lookup"><span data-stu-id="46985-134">If **IPM.Note.Phone** does not have an explicit receive folder set, **GetReceiveFolder** returns the entry identifier of the Inbox in  _lppEntryID_ and **IPM.Note** in  _lppszExplicitClass_.</span></span>
  
<span data-ttu-id="46985-135">Si le client appelle **GetReceiveFolder** pour une classe de message et n'a pas défini de dossier de réception pour cette classe de message, _lppszExplicitClass_ est soit une chaîne de longueur nulle, soit une chaîne au format Unicode, soit une chaîne au format ANSI selon que le le client a défini l'indicateur MAPI_UNICODE dans le paramètre _ulFlags_ .</span><span class="sxs-lookup"><span data-stu-id="46985-135">If the client calls **GetReceiveFolder** for a message class and has not set a receive folder for that message class,  _lppszExplicitClass_ is either a zero-length string, a string in Unicode format, or a string in ANSI format depending on whether the client set the MAPI_UNICODE flag in the  _ulFlags_ parameter.</span></span> 
  
<span data-ttu-id="46985-136">Un dossier de réception par défaut, obtenu en transmettant NULL dans le paramètre _lpszMessageClass_ , existe toujours pour chaque banque de messages.</span><span class="sxs-lookup"><span data-stu-id="46985-136">A default receive folder, obtained by passing NULL in the  _lpszMessageClass_ parameter, always exists for every message store.</span></span> 
  
<span data-ttu-id="46985-137">Un client doit appeler la fonction [MAPIFreeBuffer](mapifreebuffer.md) lorsqu'elle est exécutée avec l'identificateur d'entrée renvoyé dans _lppEntryID_ pour libérer la mémoire qui contient cet identificateur d'entrée.</span><span class="sxs-lookup"><span data-stu-id="46985-137">A client should call the [MAPIFreeBuffer](mapifreebuffer.md) function when it is done with the entry identifier returned in  _lppEntryID_ to free the memory that holds that entry identifier.</span></span> <span data-ttu-id="46985-138">Elle doit également appeler **MAPIFreeBuffer** lorsque vous avez fini d'utiliser la chaîne de classe de message renvoyée dans _lppszExplicitClass_ pour libérer la mémoire qui contient cette chaîne.</span><span class="sxs-lookup"><span data-stu-id="46985-138">It should also call **MAPIFreeBuffer** when it is done with the message class string returned in  _lppszExplicitClass_ to free the memory that holds that string.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="46985-139">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="46985-139">MFCMAPI reference</span></span>

<span data-ttu-id="46985-140">Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="46985-140">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="46985-141">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="46985-141">**File**</span></span>|<span data-ttu-id="46985-142">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="46985-142">**Function**</span></span>|<span data-ttu-id="46985-143">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="46985-143">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="46985-144">MAPIFunctions. cpp</span><span class="sxs-lookup"><span data-stu-id="46985-144">MAPIFunctions.cpp</span></span>  <br/> |<span data-ttu-id="46985-145">GetInbox</span><span class="sxs-lookup"><span data-stu-id="46985-145">GetInbox</span></span>  <br/> |<span data-ttu-id="46985-146">MFCMAPI utilise la méthode **IMsgStore:: GetReceiveFolder** pour localiser le dossier boîte de réception.</span><span class="sxs-lookup"><span data-stu-id="46985-146">MFCMAPI uses the **IMsgStore::GetReceiveFolder** method to locate the Inbox folder.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="46985-147">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="46985-147">See also</span></span>



[<span data-ttu-id="46985-148">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="46985-148">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="46985-149">IMsgStore : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="46985-149">IMsgStore : IMAPIProp</span></span>](imsgstoreimapiprop.md)


[<span data-ttu-id="46985-150">MFCMAPI comme un exemple de Code</span><span class="sxs-lookup"><span data-stu-id="46985-150">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

