---
title: IMAPIFormContainerResolveMultipleMessageClasses
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormContainer.ResolveMultipleMessageCla
api_type:
- COM
ms.assetid: f18c2dd1-366f-48b4-b335-ebbc0651f467
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 0730da9c3877985853e2cd0a55420e64fbd98e0c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342181"
---
# <a name="imapiformcontainerresolvemultiplemessageclasses"></a><span data-ttu-id="81c1f-103">IMAPIFormContainer::ResolveMultipleMessageClasses</span><span class="sxs-lookup"><span data-stu-id="81c1f-103">IMAPIFormContainer::ResolveMultipleMessageClasses</span></span>

  
  
<span data-ttu-id="81c1f-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="81c1f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="81c1f-105">Résout un groupe de classes de message dans leurs formulaires dans un conteneur de formulaire et renvoie un tableau d'objets d'informations de formulaire pour ces formulaires.</span><span class="sxs-lookup"><span data-stu-id="81c1f-105">Resolves a group of message classes to their forms in a form container and returns an array of form information objects for those forms.</span></span>
  
```cpp
HRESULT ResolveMultipleMessageClasses(
  LPSMESSAGECLASSARRAY pMsgClassArray,
  ULONG ulFlags,
  LPSMAPIFORMINFOARRAY FAR * ppfrminfoarray
);
```

## <a name="parameters"></a><span data-ttu-id="81c1f-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="81c1f-106">Parameters</span></span>

 <span data-ttu-id="81c1f-107">_pMsgClassArray_</span><span class="sxs-lookup"><span data-stu-id="81c1f-107">_pMsgClassArray_</span></span>
  
> <span data-ttu-id="81c1f-108">dans Pointeur vers un tableau qui contient les noms des classes de message à résoudre.</span><span class="sxs-lookup"><span data-stu-id="81c1f-108">[in] A pointer to an array that contains the names of the message classes to resolve.</span></span> <span data-ttu-id="81c1f-109">Les noms de classe de message sont toujours des chaînes ANSI, jamais Unicode.</span><span class="sxs-lookup"><span data-stu-id="81c1f-109">Message class names are always ANSI strings, never Unicode.</span></span>
    
 <span data-ttu-id="81c1f-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="81c1f-110">_ulFlags_</span></span>
  
> <span data-ttu-id="81c1f-111">dans Masque de des indicateurs qui contrôle la manière dont les classes de message sont résolues.</span><span class="sxs-lookup"><span data-stu-id="81c1f-111">[in] A bitmask of flags that controls how the message classes are resolved.</span></span> <span data-ttu-id="81c1f-112">L'indicateur suivant peut être défini:</span><span class="sxs-lookup"><span data-stu-id="81c1f-112">The following flag can be set:</span></span>
    
<span data-ttu-id="81c1f-113">MAPIFORM_EXACTMATCH</span><span class="sxs-lookup"><span data-stu-id="81c1f-113">MAPIFORM_EXACTMATCH</span></span> 
  
> <span data-ttu-id="81c1f-114">Seules les chaînes de classe de message correspondant à une correspondance exacte doivent être résolues.</span><span class="sxs-lookup"><span data-stu-id="81c1f-114">Only message class strings that are an exact match should be resolved.</span></span>
    
 <span data-ttu-id="81c1f-115">_ppfrminfoarray_</span><span class="sxs-lookup"><span data-stu-id="81c1f-115">_ppfrminfoarray_</span></span>
  
> <span data-ttu-id="81c1f-116">remarquer Pointeur vers un pointeur vers un tableau d'objets d'informations de formulaire.</span><span class="sxs-lookup"><span data-stu-id="81c1f-116">[out] A pointer to a pointer to an array of form information objects.</span></span> <span data-ttu-id="81c1f-117">Si une application cliente transmet NULL dans le paramètre _pMsgClassArray_ , le paramètre _ppfrminfoarray_ contient les objets d'informations de formulaire pour tous les formulaires dans le conteneur.</span><span class="sxs-lookup"><span data-stu-id="81c1f-117">If a client application passes NULL in the  _pMsgClassArray_ parameter, the  _ppfrminfoarray_ parameter contains form information objects for all forms in the container.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="81c1f-118">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="81c1f-118">Return value</span></span>

<span data-ttu-id="81c1f-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="81c1f-119">S_OK</span></span> 
  
> <span data-ttu-id="81c1f-120">L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.</span><span class="sxs-lookup"><span data-stu-id="81c1f-120">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="81c1f-121">Remarques</span><span class="sxs-lookup"><span data-stu-id="81c1f-121">Remarks</span></span>

<span data-ttu-id="81c1f-122">Les applications clientes appellent la méthode **IMAPIFormContainer:: ResolveMultipleMessageClasses** pour résoudre un groupe de classes de messages en formulaires dans un conteneur de formulaire.</span><span class="sxs-lookup"><span data-stu-id="81c1f-122">Client applications call the **IMAPIFormContainer::ResolveMultipleMessageClasses** method to resolve a group of message classes to forms within a form container.</span></span> <span data-ttu-id="81c1f-123">Le tableau des objets d'informations de formulaire renvoyés dans le paramètre _ppfrminfoarray_ fournit un accès supplémentaire à chacune des propriétés des formulaires.</span><span class="sxs-lookup"><span data-stu-id="81c1f-123">The array of form information objects returned in the  _ppfrminfoarray_ parameter provides further access to each of the forms' properties.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="81c1f-124">Remarques pour les appelants</span><span class="sxs-lookup"><span data-stu-id="81c1f-124">Notes to callers</span></span>

<span data-ttu-id="81c1f-125">Pour résoudre un groupe de classes de message en formulaires, transmettez un tableau de noms de classes de message à résoudre.</span><span class="sxs-lookup"><span data-stu-id="81c1f-125">To resolve a group of message classes to forms, pass in an array of message class names to be resolved.</span></span> <span data-ttu-id="81c1f-126">Pour forcer la résolution de façon exacte (autrement dit, pour empêcher la résolution d'une classe de base de la classe de message), l'indicateur MAPIFORM_EXACTMATCH peut être passé dans le paramètre _ulFlags_ .</span><span class="sxs-lookup"><span data-stu-id="81c1f-126">To force the resolution to be exact (that is, to prevent resolution to a base class of the message class), the MAPIFORM_EXACTMATCH flag can be passed in the  _ulFlags_ parameter.</span></span> 
  
<span data-ttu-id="81c1f-127">Si une classe de message ne peut pas être résolue en un formulaire, la valeur NULL est renvoyée pour cette classe de message dans le tableau d'informations sur le formulaire.</span><span class="sxs-lookup"><span data-stu-id="81c1f-127">If a message class cannot be resolved to a form, NULL is returned for that message class in the form information array.</span></span> <span data-ttu-id="81c1f-128">Par conséquent, même si la méthode renvoie S_OK, ne partez pas du principe que toutes les classes de message ont été résolues avec succès.</span><span class="sxs-lookup"><span data-stu-id="81c1f-128">Therefore, even if the method returns S_OK, do not assume that all message classes have been successfully resolved.</span></span> <span data-ttu-id="81c1f-129">Au lieu de cela, vérifiez les valeurs du tableau renvoyé.</span><span class="sxs-lookup"><span data-stu-id="81c1f-129">Instead, check the values in the returned array.</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="81c1f-130">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="81c1f-130">MFCMAPI reference</span></span>

<span data-ttu-id="81c1f-131">Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="81c1f-131">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="81c1f-132">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="81c1f-132">**File**</span></span>|<span data-ttu-id="81c1f-133">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="81c1f-133">**Function**</span></span>|<span data-ttu-id="81c1f-134">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="81c1f-134">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="81c1f-135">FormContainerDlg. cpp</span><span class="sxs-lookup"><span data-stu-id="81c1f-135">FormContainerDlg.cpp</span></span>  <br/> |<span data-ttu-id="81c1f-136">CFormContainerDlg:: OnResolveMultipleMessageClasses</span><span class="sxs-lookup"><span data-stu-id="81c1f-136">CFormContainerDlg::OnResolveMultipleMessageClasses</span></span>  <br/> |<span data-ttu-id="81c1f-137">MFCMAPI utilise la méthode **IMAPIFormContainer:: ResolveMultipleMessageClasses** pour localiser un formulaire associé à un ensemble de classes de message.</span><span class="sxs-lookup"><span data-stu-id="81c1f-137">MFCMAPI uses the **IMAPIFormContainer::ResolveMultipleMessageClasses** method to locate a form that is associated with a set of message classes.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="81c1f-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="81c1f-138">See also</span></span>



[<span data-ttu-id="81c1f-139">IMAPIFormContainer::ResolveMessageClass</span><span class="sxs-lookup"><span data-stu-id="81c1f-139">IMAPIFormContainer::ResolveMessageClass</span></span>](imapiformcontainer-resolvemessageclass.md)
  
[<span data-ttu-id="81c1f-140">IMAPIFormContainer : IUnknown</span><span class="sxs-lookup"><span data-stu-id="81c1f-140">IMAPIFormContainer : IUnknown</span></span>](imapiformcontaineriunknown.md)


[<span data-ttu-id="81c1f-141">MFCMAPI comme un exemple de Code</span><span class="sxs-lookup"><span data-stu-id="81c1f-141">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

