---
title: IMAPISupportRegisterPreprocessor
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.RegisterPreprocessor
api_type:
- COM
ms.assetid: 9b5659ab-2b49-41ab-92ce-ca343e35d670
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 58215de6cc4e9e68386f8f017839752acc6e1753
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404896"
---
# <a name="imapisupportregisterpreprocessor"></a><span data-ttu-id="5ac61-103">IMAPISupport::RegisterPreprocessor</span><span class="sxs-lookup"><span data-stu-id="5ac61-103">IMAPISupport::RegisterPreprocessor</span></span>

  
  
<span data-ttu-id="5ac61-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5ac61-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5ac61-105">Inscrit la fonction de préprocesseur d’un fournisseur de transport (fonction conforme au prototype [PreprocessMessage).](preprocessmessage.md)</span><span class="sxs-lookup"><span data-stu-id="5ac61-105">Registers a transport provider's preprocessor function (a function that conforms to the [PreprocessMessage](preprocessmessage.md) prototype).</span></span> 
  
```cpp
HRESULT RegisterPreprocessor(
LPMAPIUID lpMuid,
LPSTR lpszAdrType,
LPSTR lpszDLLName,
LPSTR lpszPreprocess,
LPSTR lpszRemovePreprocessInfo,
ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="5ac61-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5ac61-106">Parameters</span></span>

 <span data-ttu-id="5ac61-107">_lpMuid_</span><span class="sxs-lookup"><span data-stu-id="5ac61-107">_lpMuid_</span></span>
  
> <span data-ttu-id="5ac61-108">[in] Pointeur vers la structure [MAPIUID](mapiuid.md) qui contient l’identificateur géré par la fonction de préprocesseur.</span><span class="sxs-lookup"><span data-stu-id="5ac61-108">[in] A pointer to the [MAPIUID](mapiuid.md) structure that contains the identifier that the preprocessor function handles.</span></span> <span data-ttu-id="5ac61-109">Le  _paramètre lpMuid_ peut être NULL.</span><span class="sxs-lookup"><span data-stu-id="5ac61-109">The  _lpMuid_ parameter can be NULL.</span></span> 
    
 <span data-ttu-id="5ac61-110">_lpszAdrType_</span><span class="sxs-lookup"><span data-stu-id="5ac61-110">_lpszAdrType_</span></span>
  
> <span data-ttu-id="5ac61-111">[in] Pointeur vers le type d’adresse pour les messages surés par la fonction, tels que FAX, SMTP ou X500.</span><span class="sxs-lookup"><span data-stu-id="5ac61-111">[in] A pointer to the address type for the messages the function operates on, such as FAX, SMTP, or X500.</span></span> <span data-ttu-id="5ac61-112">Le  _paramètre lpszAdrType_ peut être NULL.</span><span class="sxs-lookup"><span data-stu-id="5ac61-112">The  _lpszAdrType_ parameter can be NULL.</span></span> 
    
 <span data-ttu-id="5ac61-113">_lpszDLLName_</span><span class="sxs-lookup"><span data-stu-id="5ac61-113">_lpszDLLName_</span></span>
  
> <span data-ttu-id="5ac61-114">[in] Pointeur vers le nom de la bibliothèque de liens dynamiques (DLL) qui contient le point d’entrée de la fonction de préprocesseur.</span><span class="sxs-lookup"><span data-stu-id="5ac61-114">[in] A pointer to the name of the dynamic-link library (DLL) that contains the entry point for the preprocessor function.</span></span>
    
 <span data-ttu-id="5ac61-115">_lpszPreprocess_</span><span class="sxs-lookup"><span data-stu-id="5ac61-115">_lpszPreprocess_</span></span>
  
> <span data-ttu-id="5ac61-116">[in] Pointeur vers le nom de la fonction de préprocesseur.</span><span class="sxs-lookup"><span data-stu-id="5ac61-116">[in] A pointer to the name of the preprocessor function.</span></span> <span data-ttu-id="5ac61-117">Le  _paramètre lpszPreprocess_ peut être NULL.</span><span class="sxs-lookup"><span data-stu-id="5ac61-117">The  _lpszPreprocess_ parameter can be NULL.</span></span> 
    
 <span data-ttu-id="5ac61-118">_lpszRemovePreprocessInfo_</span><span class="sxs-lookup"><span data-stu-id="5ac61-118">_lpszRemovePreprocessInfo_</span></span>
  
> <span data-ttu-id="5ac61-119">[in] Pointeur vers le nom de la fonction qui supprime les informations de préprocesseur (fonction conforme au prototype [RemovePreprocessInfo).](removepreprocessinfo.md)</span><span class="sxs-lookup"><span data-stu-id="5ac61-119">[in] A pointer to the name of the function that removes preprocessor information (a function that conforms to the [RemovePreprocessInfo](removepreprocessinfo.md) prototype).</span></span> <span data-ttu-id="5ac61-120">Le  _paramètre lpszRemovePreprocessInfo_ peut être NULL.</span><span class="sxs-lookup"><span data-stu-id="5ac61-120">The  _lpszRemovePreprocessInfo_ parameter can be NULL.</span></span> 
    
 <span data-ttu-id="5ac61-121">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="5ac61-121">_ulFlags_</span></span>
  
> <span data-ttu-id="5ac61-122">Réservé ; doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="5ac61-122">Reserved; must be zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="5ac61-123">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="5ac61-123">Return value</span></span>

<span data-ttu-id="5ac61-124">S_OK</span><span class="sxs-lookup"><span data-stu-id="5ac61-124">S_OK</span></span> 
  
> <span data-ttu-id="5ac61-125">La fonction de préprocesseur a été enregistrée avec succès.</span><span class="sxs-lookup"><span data-stu-id="5ac61-125">The preprocessor function was successfully registered.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="5ac61-126">Remarques</span><span class="sxs-lookup"><span data-stu-id="5ac61-126">Remarks</span></span>

<span data-ttu-id="5ac61-127">La **méthode IMAPISupport::RegisterPreprocessor** est implémentée pour les objets de prise en charge du fournisseur de transport uniquement.</span><span class="sxs-lookup"><span data-stu-id="5ac61-127">The **IMAPISupport::RegisterPreprocessor** method is implemented for transport provider support objects only.</span></span> <span data-ttu-id="5ac61-128">Les fournisseurs de transport **appellent RegisterPreprocessor** pour inscrire une fonction de préprocesseur (fonction conforme au prototype [PreprocessMessage).](preprocessmessage.md)</span><span class="sxs-lookup"><span data-stu-id="5ac61-128">Transport providers call **RegisterPreprocessor** to register a preprocessor function (a function that conforms to the [PreprocessMessage](preprocessmessage.md) prototype).</span></span> <span data-ttu-id="5ac61-129">Une fonction de préprocesseur doit être enregistrée pour que lepooler MAPI puisse l’appeler.</span><span class="sxs-lookup"><span data-stu-id="5ac61-129">A preprocessor function must be registered before the MAPI spooler can call it.</span></span> 
  
<span data-ttu-id="5ac61-130">Les paramètres  _lpszPreprocess_,  _lpszRemovePreprocessInfo_ et  _lpszDLLName_ doivent tous pointer vers des chaînes qui peuvent être utilisées conjointement avec des appels à la fonction Win32 **GetProcAddress,** ce qui permet d’appeler correctement le point d’entrée DLL du préprocesseur.</span><span class="sxs-lookup"><span data-stu-id="5ac61-130">The  _lpszPreprocess_,  _lpszRemovePreprocessInfo_, and  _lpszDLLName_ parameters should all point to strings that can be used in conjunction with calls to the Win32 **GetProcAddress** function, allowing the preprocessor's DLL entry point to be called correctly.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="5ac61-131">Remarques pour les appelants</span><span class="sxs-lookup"><span data-stu-id="5ac61-131">Notes to callers</span></span>

<span data-ttu-id="5ac61-132">Les appels aux préprocesseurs sont spécifiques à l’ordre du fournisseur de transport.</span><span class="sxs-lookup"><span data-stu-id="5ac61-132">Calls to preprocessors are specific to transport provider order.</span></span> <span data-ttu-id="5ac61-133">Cela signifie que si un autre fournisseur de transport devant votre fournisseur est en mesure de gérer un message, votre fonction de préprocesseur ne sera pas appelée pour ce message.</span><span class="sxs-lookup"><span data-stu-id="5ac61-133">This means that if another transport provider ahead of your provider is able to handle a message, your preprocessor function will not be called for that message.</span></span> <span data-ttu-id="5ac61-134">Votre fonction de préprocesseur sera appelée uniquement pour les messages que vous gérerez.</span><span class="sxs-lookup"><span data-stu-id="5ac61-134">Your preprocessor function will be called only for messages that you will handle.</span></span>
  
<span data-ttu-id="5ac61-135">Vous pouvez écrire des fonctions de préprocesseur pour gérer un identificateur spécifique stocké dans une structure [MAPIUID](mapiuid.md) ou un type d’adresse.</span><span class="sxs-lookup"><span data-stu-id="5ac61-135">You can write preprocessor functions to handle either a specific identifier stored in a [MAPIUID](mapiuid.md) structure or a type of address.</span></span> <span data-ttu-id="5ac61-136">Si vous spécifiez une structure **MAPIUID** dans le paramètre  _lpMuid_ et un type d’adresse dans le paramètre  _lpszAdrType,_ votre fonction sera appelée pour les destinataires de message qui correspondent au **MAPIUID** ou au type d’adresse.</span><span class="sxs-lookup"><span data-stu-id="5ac61-136">If you specify both a **MAPIUID** structure in the  _lpMuid_ parameter and an address type in the  _lpszAdrType_ parameter, your function will be called for message recipients that match either the **MAPIUID** or the address type.</span></span> <span data-ttu-id="5ac61-137">Si  _lpMuid_ est NULL et  _lpszAdrType_ est non NULL, votre fonction est appelée uniquement pour les destinataires dont l’adresse correspond au type pointé par  _lpszAdrType_.</span><span class="sxs-lookup"><span data-stu-id="5ac61-137">If  _lpMuid_ is NULL and  _lpszAdrType_ is non-NULL, your function will be called only for recipients that have an address that matches the type pointed to by  _lpszAdrType_.</span></span> <span data-ttu-id="5ac61-138">Si  _lpMuid_ est non NULL et  _lpszAdrType_ est NULL, votre fonction est appelée pour les destinataires qui correspondent à **MAPIUID,** quel que soit leur type d’adresse.</span><span class="sxs-lookup"><span data-stu-id="5ac61-138">If  _lpMuid_ is non-NULL and  _lpszAdrType_ is NULL, your function will be called for recipients that match **MAPIUID**, regardless of their address type.</span></span> <span data-ttu-id="5ac61-139">Si les deux sont NULL, votre fonction est appelée pour tous les destinataires du message.</span><span class="sxs-lookup"><span data-stu-id="5ac61-139">If both are NULL, your function is called for all recipients of the message.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="5ac61-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5ac61-140">See also</span></span>



[<span data-ttu-id="5ac61-141">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="5ac61-141">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="5ac61-142">PreprocessMessage</span><span class="sxs-lookup"><span data-stu-id="5ac61-142">PreprocessMessage</span></span>](preprocessmessage.md)
  
[<span data-ttu-id="5ac61-143">RemovePreprocessInfo</span><span class="sxs-lookup"><span data-stu-id="5ac61-143">RemovePreprocessInfo</span></span>](removepreprocessinfo.md)
  
[<span data-ttu-id="5ac61-144">IMAPISupport : IUnknown</span><span class="sxs-lookup"><span data-stu-id="5ac61-144">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

