---
title: IMAPIFormInfoCalcVerbSet
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormInfo.CalcVerbSet
api_type:
- COM
ms.assetid: 0170dc9d-dc72-48e2-a522-374f199b18ea
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: babff746af16d51ca154d049943f6be7e9fab589
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428780"
---
# <a name="imapiforminfocalcverbset"></a><span data-ttu-id="d4a15-103">IMAPIFormInfo::CalcVerbSet</span><span class="sxs-lookup"><span data-stu-id="d4a15-103">IMAPIFormInfo::CalcVerbSet</span></span>

  
  
<span data-ttu-id="d4a15-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d4a15-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d4a15-105">Renvoie un pointeur vers l’ensemble complet des verbes qu’un formulaire utilise.</span><span class="sxs-lookup"><span data-stu-id="d4a15-105">Returns a pointer to the complete set of verbs that a form uses.</span></span>
  
```cpp
HRESULT CalcVerbSet(
  ULONG ulFlags,
  LPMAPIVERBARRAY FAR * ppMAPIVerbArray
);
```

## <a name="parameters"></a><span data-ttu-id="d4a15-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d4a15-106">Parameters</span></span>

 <span data-ttu-id="d4a15-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="d4a15-107">_ulFlags_</span></span>
  
> <span data-ttu-id="d4a15-108">[in] Masque de bits d’indicateurs qui contrôle le type de chaînes renvoyées.</span><span class="sxs-lookup"><span data-stu-id="d4a15-108">[in] A bitmask of flags that controls the type of strings returned.</span></span> <span data-ttu-id="d4a15-109">L’indicateur suivant peut être définie :</span><span class="sxs-lookup"><span data-stu-id="d4a15-109">The following flag can be set:</span></span>
    
<span data-ttu-id="d4a15-110">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="d4a15-110">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="d4a15-111">Les chaînes renvoyées sont au format Unicode.</span><span class="sxs-lookup"><span data-stu-id="d4a15-111">The returned strings are in Unicode format.</span></span> <span data-ttu-id="d4a15-112">Si l’MAPI_UNICODE n’est pas définie, les chaînes sont au format ANSI.</span><span class="sxs-lookup"><span data-stu-id="d4a15-112">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="d4a15-113">_ppMAPIVerbArray_</span><span class="sxs-lookup"><span data-stu-id="d4a15-113">_ppMAPIVerbArray_</span></span>
  
> <span data-ttu-id="d4a15-114">[out] Pointeur vers un pointeur vers la structure [SMAPIVerbArray](smapiverbarray.md) renvoyée qui contient les verbes du formulaire.</span><span class="sxs-lookup"><span data-stu-id="d4a15-114">[out] A pointer to a pointer to the returned [SMAPIVerbArray](smapiverbarray.md) structure that contains the form's verbs.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="d4a15-115">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="d4a15-115">Return value</span></span>

<span data-ttu-id="d4a15-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="d4a15-116">S_OK</span></span> 
  
> <span data-ttu-id="d4a15-117">L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.</span><span class="sxs-lookup"><span data-stu-id="d4a15-117">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="d4a15-118">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="d4a15-118">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="d4a15-119">L’indicateur MAPI_UNICODE a été définie et l’implémentation ne prend pas en charge Unicode, ou MAPI_UNICODE n’a pas été définie et l’implémentation prend uniquement en charge Unicode.</span><span class="sxs-lookup"><span data-stu-id="d4a15-119">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation supports only Unicode.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="d4a15-120">Remarques</span><span class="sxs-lookup"><span data-stu-id="d4a15-120">Remarks</span></span>

<span data-ttu-id="d4a15-121">Les applications clientes appellent la méthode **IMAPIFormInfo::CalcVerbSet** pour obtenir un pointeur vers l’ensemble de verbes utilisés par un formulaire.</span><span class="sxs-lookup"><span data-stu-id="d4a15-121">Client applications call the **IMAPIFormInfo::CalcVerbSet** method to obtain a pointer to the set of verbs used by a form.</span></span> <span data-ttu-id="d4a15-122">Dans la structure **SMAPIVerbArray** renvoyée dans le paramètre _ppMAPIVerbArray,_ les verbes sont renvoyés par ordre de numéro d’index ; L’index de chaque verbe se trouve dans son **membre lVerb.**</span><span class="sxs-lookup"><span data-stu-id="d4a15-122">In the **SMAPIVerbArray** structure returned in the  _ppMAPIVerbArray_ parameter, the verbs are returned in order of index number; each verb's index is found in its **lVerb** member.</span></span> <span data-ttu-id="d4a15-123">Les applications clientes peuvent utiliser le tableau de verbes pour créer dynamiquement des menus, masquer ou afficher des boutons, etc.</span><span class="sxs-lookup"><span data-stu-id="d4a15-123">Client applications can use the verb array to dynamically build menus, hide or show buttons, and so on.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="d4a15-124">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="d4a15-124">MFCMAPI reference</span></span>

<span data-ttu-id="d4a15-125">Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="d4a15-125">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="d4a15-126">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="d4a15-126">**File**</span></span>|<span data-ttu-id="d4a15-127">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="d4a15-127">**Function**</span></span>|<span data-ttu-id="d4a15-128">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="d4a15-128">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="d4a15-129">MFCOutput.cpp</span><span class="sxs-lookup"><span data-stu-id="d4a15-129">MFCOutput.cpp</span></span>  <br/> |<span data-ttu-id="d4a15-130">_OutputFormInfo</span><span class="sxs-lookup"><span data-stu-id="d4a15-130">_OutputFormInfo</span></span>  <br/> |<span data-ttu-id="d4a15-131">MFCMAPI utilise la méthode **IMAPIFormInfo::CalcVerbSet** lors de l’écriture de la sortie de débogage pour les objets d’informations de formulaire.</span><span class="sxs-lookup"><span data-stu-id="d4a15-131">MFCMAPI uses the **IMAPIFormInfo::CalcVerbSet** method while writing debug output for form information objects.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d4a15-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d4a15-132">See also</span></span>



[<span data-ttu-id="d4a15-133">SMAPIVerbArray</span><span class="sxs-lookup"><span data-stu-id="d4a15-133">SMAPIVerbArray</span></span>](smapiverbarray.md)
  
[<span data-ttu-id="d4a15-134">IMAPIFormInfo : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="d4a15-134">IMAPIFormInfo : IMAPIProp</span></span>](imapiforminfoimapiprop.md)


[<span data-ttu-id="d4a15-135">MFCMAPI comme un exemple de Code</span><span class="sxs-lookup"><span data-stu-id="d4a15-135">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

