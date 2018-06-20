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
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 219c15fc00490983e970e4533f927cf4d91916b6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784035"
---
# <a name="imapisupportregisterpreprocessor"></a><span data-ttu-id="acc50-103">IMAPISupport::RegisterPreprocessor</span><span class="sxs-lookup"><span data-stu-id="acc50-103">IMAPISupport::RegisterPreprocessor</span></span>

  
  
<span data-ttu-id="acc50-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="acc50-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="acc50-105">Enregistre la fonction préprocesseur d’un fournisseur de transport (une fonction qui est conforme au prototype [PreprocessMessage](preprocessmessage.md) ).</span><span class="sxs-lookup"><span data-stu-id="acc50-105">Registers a transport provider's preprocessor function (a function that conforms to the [PreprocessMessage](preprocessmessage.md) prototype).</span></span> 
  
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

## <a name="parameters"></a><span data-ttu-id="acc50-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="acc50-106">Parameters</span></span>

 <span data-ttu-id="acc50-107">_lpMuid_</span><span class="sxs-lookup"><span data-stu-id="acc50-107">_lpMuid_</span></span>
  
> <span data-ttu-id="acc50-108">[in] Pointeur vers la structure [MAPIUID](mapiuid.md) qui contient l’identificateur qui gère la fonction préprocesseur.</span><span class="sxs-lookup"><span data-stu-id="acc50-108">[in] A pointer to the [MAPIUID](mapiuid.md) structure that contains the identifier that the preprocessor function handles.</span></span> <span data-ttu-id="acc50-109">Le paramètre _lpMuid_ peut être NULL.</span><span class="sxs-lookup"><span data-stu-id="acc50-109">The  _lpMuid_ parameter can be NULL.</span></span> 
    
 <span data-ttu-id="acc50-110">_lpszAdrType_</span><span class="sxs-lookup"><span data-stu-id="acc50-110">_lpszAdrType_</span></span>
  
> <span data-ttu-id="acc50-111">[in] Un pointeur vers le type d’adresse pour les messages de la fonction fonctionne, telles que télécopie, SMTP ou X500.</span><span class="sxs-lookup"><span data-stu-id="acc50-111">[in] A pointer to the address type for the messages the function operates on, such as FAX, SMTP, or X500.</span></span> <span data-ttu-id="acc50-112">Le paramètre _lpszAdrType_ peut être NULL.</span><span class="sxs-lookup"><span data-stu-id="acc50-112">The  _lpszAdrType_ parameter can be NULL.</span></span> 
    
 <span data-ttu-id="acc50-113">_lpszDLLName_</span><span class="sxs-lookup"><span data-stu-id="acc50-113">_lpszDLLName_</span></span>
  
> <span data-ttu-id="acc50-114">[in] Pointeur vers le nom de la bibliothèque de liens dynamiques (DLL) qui contient le point d’entrée de la fonction préprocesseur.</span><span class="sxs-lookup"><span data-stu-id="acc50-114">[in] A pointer to the name of the dynamic-link library (DLL) that contains the entry point for the preprocessor function.</span></span>
    
 <span data-ttu-id="acc50-115">_lpszPreprocess_</span><span class="sxs-lookup"><span data-stu-id="acc50-115">_lpszPreprocess_</span></span>
  
> <span data-ttu-id="acc50-116">[in] Pointeur vers le nom de la fonction préprocesseur.</span><span class="sxs-lookup"><span data-stu-id="acc50-116">[in] A pointer to the name of the preprocessor function.</span></span> <span data-ttu-id="acc50-117">Le paramètre _lpszPreprocess_ peut être NULL.</span><span class="sxs-lookup"><span data-stu-id="acc50-117">The  _lpszPreprocess_ parameter can be NULL.</span></span> 
    
 <span data-ttu-id="acc50-118">_lpszRemovePreprocessInfo_</span><span class="sxs-lookup"><span data-stu-id="acc50-118">_lpszRemovePreprocessInfo_</span></span>
  
> <span data-ttu-id="acc50-119">[in] Pointeur vers le nom de la fonction qui supprime les informations du préprocesseur (une fonction qui est conforme au prototype [RemovePreprocessInfo](removepreprocessinfo.md) ).</span><span class="sxs-lookup"><span data-stu-id="acc50-119">[in] A pointer to the name of the function that removes preprocessor information (a function that conforms to the [RemovePreprocessInfo](removepreprocessinfo.md) prototype).</span></span> <span data-ttu-id="acc50-120">Le paramètre _lpszRemovePreprocessInfo_ peut être NULL.</span><span class="sxs-lookup"><span data-stu-id="acc50-120">The  _lpszRemovePreprocessInfo_ parameter can be NULL.</span></span> 
    
 <span data-ttu-id="acc50-121">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="acc50-121">_ulFlags_</span></span>
  
> <span data-ttu-id="acc50-122">Réservé ; doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="acc50-122">Reserved; must be zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="acc50-123">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="acc50-123">Return value</span></span>

<span data-ttu-id="acc50-124">S_OK</span><span class="sxs-lookup"><span data-stu-id="acc50-124">S_OK</span></span> 
  
> <span data-ttu-id="acc50-125">La fonction préprocesseur a été enregistrée avec succès.</span><span class="sxs-lookup"><span data-stu-id="acc50-125">The preprocessor function was successfully registered.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="acc50-126">Remarques</span><span class="sxs-lookup"><span data-stu-id="acc50-126">Remarks</span></span>

<span data-ttu-id="acc50-127">La méthode **IMAPISupport::RegisterPreprocessor** est implémentée pour les objets de prise en charge des fournisseur de transport uniquement.</span><span class="sxs-lookup"><span data-stu-id="acc50-127">The **IMAPISupport::RegisterPreprocessor** method is implemented for transport provider support objects only.</span></span> <span data-ttu-id="acc50-128">Fournisseurs de transport appellent **RegisterPreprocessor** pour enregistrer une fonction préprocesseur (une fonction qui est conforme au prototype [PreprocessMessage](preprocessmessage.md) ).</span><span class="sxs-lookup"><span data-stu-id="acc50-128">Transport providers call **RegisterPreprocessor** to register a preprocessor function (a function that conforms to the [PreprocessMessage](preprocessmessage.md) prototype).</span></span> <span data-ttu-id="acc50-129">Une fonction préprocesseur doit être enregistrée avant le spouleur MAPI permettre appeler.</span><span class="sxs-lookup"><span data-stu-id="acc50-129">A preprocessor function must be registered before the MAPI spooler can call it.</span></span> 
  
<span data-ttu-id="acc50-130">Les paramètres _lpszPreprocess_, _lpszRemovePreprocessInfo_et _lpszDLLName_ doivent tous pointer les chaînes qui peuvent être utilisées conjointement avec les appels à la fonction Win32 **GetProcAddress** , ce qui permet DLL du préprocesseur point d’entrée appelé correctement.</span><span class="sxs-lookup"><span data-stu-id="acc50-130">The  _lpszPreprocess_,  _lpszRemovePreprocessInfo_, and  _lpszDLLName_ parameters should all point to strings that can be used in conjunction with calls to the Win32 **GetProcAddress** function, allowing the preprocessor's DLL entry point to be called correctly.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="acc50-131">Notes aux appelants</span><span class="sxs-lookup"><span data-stu-id="acc50-131">Notes to callers</span></span>

<span data-ttu-id="acc50-132">Les appels vers Préprocesseurs sont spécifiques à l’ordre des fournisseurs de transport.</span><span class="sxs-lookup"><span data-stu-id="acc50-132">Calls to preprocessors are specific to transport provider order.</span></span> <span data-ttu-id="acc50-133">Cela signifie que si un autre fournisseur de transport à votre fournisseur est en mesure de gérer un message, votre fonction préprocesseur ne sera pas appelée pour ce message.</span><span class="sxs-lookup"><span data-stu-id="acc50-133">This means that if another transport provider ahead of your provider is able to handle a message, your preprocessor function will not be called for that message.</span></span> <span data-ttu-id="acc50-134">Votre fonction préprocesseur être appelée uniquement pour les messages que vous allez gérer.</span><span class="sxs-lookup"><span data-stu-id="acc50-134">Your preprocessor function will be called only for messages that you will handle.</span></span>
  
<span data-ttu-id="acc50-135">Vous pouvez écrire des fonctions préprocesseur pour gérer un identificateur spécifique que stocké dans une structure [MAPIUID](mapiuid.md) ou un type d’adresse.</span><span class="sxs-lookup"><span data-stu-id="acc50-135">You can write preprocessor functions to handle either a specific identifier stored in a [MAPIUID](mapiuid.md) structure or a type of address.</span></span> <span data-ttu-id="acc50-136">Si vous spécifiez à la fois une structure **MAPIUID** dans le paramètre _lpMuid_ et un type d’adresse dans le paramètre _lpszAdrType_ , votre fonction sera appelée pour les destinataires du message qui correspondent à la **MAPIUID** ou le type d’adresse.</span><span class="sxs-lookup"><span data-stu-id="acc50-136">If you specify both a **MAPIUID** structure in the  _lpMuid_ parameter and an address type in the  _lpszAdrType_ parameter, your function will be called for message recipients that match either the **MAPIUID** or the address type.</span></span> <span data-ttu-id="acc50-137">Si _lpMuid_ a la valeur NULL et _lpszAdrType_ n’est pas NULL, votre fonction sera appelée uniquement pour les destinataires auxquels une adresse qui correspond au type désigné par _lpszAdrType_.</span><span class="sxs-lookup"><span data-stu-id="acc50-137">If  _lpMuid_ is NULL and  _lpszAdrType_ is non-NULL, your function will be called only for recipients that have an address that matches the type pointed to by  _lpszAdrType_.</span></span> <span data-ttu-id="acc50-138">Si _lpMuid_ n’est pas NULL et _lpszAdrType_ est NULL, votre fonction sera appelée pour des destinataires qui correspondent à **MAPIUID**, quel que soit leur type d’adresse.</span><span class="sxs-lookup"><span data-stu-id="acc50-138">If  _lpMuid_ is non-NULL and  _lpszAdrType_ is NULL, your function will be called for recipients that match **MAPIUID**, regardless of their address type.</span></span> <span data-ttu-id="acc50-139">Si les deux sont NULL, la fonction est appelée pour tous les destinataires du message.</span><span class="sxs-lookup"><span data-stu-id="acc50-139">If both are NULL, your function is called for all recipients of the message.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="acc50-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="acc50-140">See also</span></span>



[<span data-ttu-id="acc50-141">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="acc50-141">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="acc50-142">PreprocessMessage</span><span class="sxs-lookup"><span data-stu-id="acc50-142">PreprocessMessage</span></span>](preprocessmessage.md)
  
[<span data-ttu-id="acc50-143">RemovePreprocessInfo</span><span class="sxs-lookup"><span data-stu-id="acc50-143">RemovePreprocessInfo</span></span>](removepreprocessinfo.md)
  
[<span data-ttu-id="acc50-144">IMAPISupport : IUnknown</span><span class="sxs-lookup"><span data-stu-id="acc50-144">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

