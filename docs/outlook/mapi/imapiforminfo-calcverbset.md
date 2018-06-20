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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 362afb1efeddeae72cc19256c377cb2c0f7ecba0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783786"
---
# <a name="imapiforminfocalcverbset"></a><span data-ttu-id="57952-103">IMAPIFormInfo::CalcVerbSet</span><span class="sxs-lookup"><span data-stu-id="57952-103">IMAPIFormInfo::CalcVerbSet</span></span>

  
  
<span data-ttu-id="57952-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="57952-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="57952-105">Retourne un pointeur vers l’ensemble complet des verbes qui utilise un formulaire.</span><span class="sxs-lookup"><span data-stu-id="57952-105">Returns a pointer to the complete set of verbs that a form uses.</span></span>
  
```cpp
HRESULT CalcVerbSet(
  ULONG ulFlags,
  LPMAPIVERBARRAY FAR * ppMAPIVerbArray
);
```

## <a name="parameters"></a><span data-ttu-id="57952-106">Param�tres</span><span class="sxs-lookup"><span data-stu-id="57952-106">Parameters</span></span>

 <span data-ttu-id="57952-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="57952-107">_ulFlags_</span></span>
  
> <span data-ttu-id="57952-108">[in] Masque de bits d’indicateurs qui contrôle le type de chaînes renvoyées.</span><span class="sxs-lookup"><span data-stu-id="57952-108">[in] A bitmask of flags that controls the type of strings returned.</span></span> <span data-ttu-id="57952-109">Vous pouvez définir l’indicateur suivant :</span><span class="sxs-lookup"><span data-stu-id="57952-109">The following flag can be set:</span></span>
    
<span data-ttu-id="57952-110">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="57952-110">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="57952-111">Les chaînes retournées sont au format Unicode.</span><span class="sxs-lookup"><span data-stu-id="57952-111">The returned strings are in Unicode format.</span></span> <span data-ttu-id="57952-112">Si l’indicateur MAPI_UNICODE n’est pas définie, les chaînes sont au format ANSI.</span><span class="sxs-lookup"><span data-stu-id="57952-112">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="57952-113">_ppMAPIVerbArray_</span><span class="sxs-lookup"><span data-stu-id="57952-113">_ppMAPIVerbArray_</span></span>
  
> <span data-ttu-id="57952-114">[out] Pointeur vers un pointeur vers la structure [SMAPIVerbArray](smapiverbarray.md) retournée qui contient les verbes du formulaire.</span><span class="sxs-lookup"><span data-stu-id="57952-114">[out] A pointer to a pointer to the returned [SMAPIVerbArray](smapiverbarray.md) structure that contains the form's verbs.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="57952-115">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="57952-115">Return value</span></span>

<span data-ttu-id="57952-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="57952-116">S_OK</span></span> 
  
> <span data-ttu-id="57952-117">L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.</span><span class="sxs-lookup"><span data-stu-id="57952-117">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="57952-118">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="57952-118">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="57952-119">Soit l’indicateur MAPI_UNICODE a été défini et l’implémentation ne prend pas en charge Unicode, ou MAPI_UNICODE n’a pas été défini et l’implémentation prend en charge Unicode uniquement.</span><span class="sxs-lookup"><span data-stu-id="57952-119">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation supports only Unicode.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="57952-120">Remarques</span><span class="sxs-lookup"><span data-stu-id="57952-120">Remarks</span></span>

<span data-ttu-id="57952-121">Applications clientes appellent la méthode **IMAPIFormInfo::CalcVerbSet** pour obtenir un pointeur vers l’ensemble de verbes utilisés par un formulaire.</span><span class="sxs-lookup"><span data-stu-id="57952-121">Client applications call the **IMAPIFormInfo::CalcVerbSet** method to obtain a pointer to the set of verbs used by a form.</span></span> <span data-ttu-id="57952-122">Dans la structure **SMAPIVerbArray** retournée dans le paramètre _ppMAPIVerbArray_ , les verbes sont retournés dans l’ordre de numéro d’index ; index de chaque verbe se trouve dans son membre **lVerb** .</span><span class="sxs-lookup"><span data-stu-id="57952-122">In the **SMAPIVerbArray** structure returned in the  _ppMAPIVerbArray_ parameter, the verbs are returned in order of index number; each verb's index is found in its **lVerb** member.</span></span> <span data-ttu-id="57952-123">Applications clientes permet le tableau verbe dynamiquement créer des menus, masquer ou afficher les boutons et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="57952-123">Client applications can use the verb array to dynamically build menus, hide or show buttons, and so on.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="57952-124">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="57952-124">MFCMAPI reference</span></span>

<span data-ttu-id="57952-125">Pour des exemples de code MFCMAPI, voir le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="57952-125">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="57952-126">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="57952-126">**File**</span></span>|<span data-ttu-id="57952-127">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="57952-127">**Function**</span></span>|<span data-ttu-id="57952-128">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="57952-128">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="57952-129">MFCOutput.cpp</span><span class="sxs-lookup"><span data-stu-id="57952-129">MFCOutput.cpp</span></span>  <br/> |<span data-ttu-id="57952-130">_OutputFormInfo</span><span class="sxs-lookup"><span data-stu-id="57952-130">_OutputFormInfo</span></span>  <br/> |<span data-ttu-id="57952-131">MFCMAPI utilise la méthode **IMAPIFormInfo::CalcVerbSet** lors de l’écriture de sortie de débogage pour les objets d’informations de formulaire.</span><span class="sxs-lookup"><span data-stu-id="57952-131">MFCMAPI uses the **IMAPIFormInfo::CalcVerbSet** method while writing debug output for form information objects.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="57952-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="57952-132">See also</span></span>



[<span data-ttu-id="57952-133">SMAPIVerbArray</span><span class="sxs-lookup"><span data-stu-id="57952-133">SMAPIVerbArray</span></span>](smapiverbarray.md)
  
[<span data-ttu-id="57952-134">IMAPIFormInfo : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="57952-134">IMAPIFormInfo : IMAPIProp</span></span>](imapiforminfoimapiprop.md)


[<span data-ttu-id="57952-135">MFCMAPI comme un exemple de Code</span><span class="sxs-lookup"><span data-stu-id="57952-135">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

