---
title: IMAPIFormInfoCalcFormPropSet
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormInfo.CalcFormPropSet
api_type:
- COM
ms.assetid: cc3ffb8d-9cc4-47d3-9aa9-02c3a5b7775c
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 7d0c044caf430c944d8912d050e4dbaba659c8b5
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22582496"
---
# <a name="imapiforminfocalcformpropset"></a><span data-ttu-id="3efc2-103">IMAPIFormInfo::CalcFormPropSet</span><span class="sxs-lookup"><span data-stu-id="3efc2-103">IMAPIFormInfo::CalcFormPropSet</span></span>

  
  
<span data-ttu-id="3efc2-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3efc2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3efc2-105">Retourne un pointeur vers l’ensemble complet des propriétés qui utilise un formulaire.</span><span class="sxs-lookup"><span data-stu-id="3efc2-105">Returns a pointer to the complete set of properties that a form uses.</span></span>
  
```cpp
HRESULT CalcFormPropSet(
  ULONG ulFlags,
  LPMAPIFORMPROPARRAY FAR * ppFormPropArray
);
```

## <a name="parameters"></a><span data-ttu-id="3efc2-106">Param�tres</span><span class="sxs-lookup"><span data-stu-id="3efc2-106">Parameters</span></span>

 <span data-ttu-id="3efc2-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="3efc2-107">_ulFlags_</span></span>
  
> <span data-ttu-id="3efc2-108">[in] Masque de bits d’indicateurs qui contrôle le type de chaînes renvoyées.</span><span class="sxs-lookup"><span data-stu-id="3efc2-108">[in] A bitmask of flags that controls the type of strings returned.</span></span> <span data-ttu-id="3efc2-109">Vous pouvez définir l’indicateur suivant :</span><span class="sxs-lookup"><span data-stu-id="3efc2-109">The following flag can be set:</span></span>
    
<span data-ttu-id="3efc2-110">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="3efc2-110">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="3efc2-111">Les chaînes retournées sont au format Unicode.</span><span class="sxs-lookup"><span data-stu-id="3efc2-111">The returned strings are in Unicode format.</span></span> <span data-ttu-id="3efc2-112">Si l’indicateur MAPI_UNICODE n’est pas définie, les chaînes sont au format ANSI.</span><span class="sxs-lookup"><span data-stu-id="3efc2-112">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="3efc2-113">_ppFormPropArray_</span><span class="sxs-lookup"><span data-stu-id="3efc2-113">_ppFormPropArray_</span></span>
  
> <span data-ttu-id="3efc2-114">[out] Pointeur vers un pointeur vers la structure [SMAPIFormPropArray](smapiformproparray.md) retournée.</span><span class="sxs-lookup"><span data-stu-id="3efc2-114">[out] A pointer to a pointer to the returned [SMAPIFormPropArray](smapiformproparray.md) structure.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="3efc2-115">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="3efc2-115">Return value</span></span>

<span data-ttu-id="3efc2-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="3efc2-116">S_OK</span></span> 
  
> <span data-ttu-id="3efc2-117">L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.</span><span class="sxs-lookup"><span data-stu-id="3efc2-117">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="3efc2-118">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="3efc2-118">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="3efc2-119">Soit l’indicateur MAPI_UNICODE a été défini et l’implémentation ne prend pas en charge Unicode, ou MAPI_UNICODE n’a pas été défini et l’implémentation prend en charge Unicode uniquement.</span><span class="sxs-lookup"><span data-stu-id="3efc2-119">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation supports only Unicode.</span></span>
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="3efc2-120">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="3efc2-120">MFCMAPI reference</span></span>

<span data-ttu-id="3efc2-121">Pour des exemples de code MFCMAPI, voir le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="3efc2-121">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="3efc2-122">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="3efc2-122">**File**</span></span>|<span data-ttu-id="3efc2-123">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="3efc2-123">**Function**</span></span>|<span data-ttu-id="3efc2-124">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="3efc2-124">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="3efc2-125">MFCOutput.cpp</span><span class="sxs-lookup"><span data-stu-id="3efc2-125">MFCOutput.cpp</span></span>  <br/> |<span data-ttu-id="3efc2-126">_OutputFormInfo</span><span class="sxs-lookup"><span data-stu-id="3efc2-126">_OutputFormInfo</span></span>  <br/> |<span data-ttu-id="3efc2-127">MFCMAPI utilise la méthode **IMAPIFormInfo::CalcFormPropSet** lors de l’écriture de sortie de débogage pour les objets d’informations de formulaire.</span><span class="sxs-lookup"><span data-stu-id="3efc2-127">MFCMAPI uses the **IMAPIFormInfo::CalcFormPropSet** method when writing debug output for form information objects.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="3efc2-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3efc2-128">See also</span></span>



[<span data-ttu-id="3efc2-129">SMAPIFormPropArray</span><span class="sxs-lookup"><span data-stu-id="3efc2-129">SMAPIFormPropArray</span></span>](smapiformproparray.md)
  
[<span data-ttu-id="3efc2-130">IMAPIFormInfo : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="3efc2-130">IMAPIFormInfo : IMAPIProp</span></span>](imapiforminfoimapiprop.md)


[<span data-ttu-id="3efc2-131">MFCMAPI comme un exemple de Code</span><span class="sxs-lookup"><span data-stu-id="3efc2-131">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

