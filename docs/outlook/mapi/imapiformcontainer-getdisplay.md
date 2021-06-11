---
title: IMAPIFormContainerGetDisplay
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormContainer.GetDisplay
api_type:
- COM
ms.assetid: 6829e273-4a75-4278-b58a-ae7543e075ac
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 994041d050df56fd3fa3c0e599542e05a202ad65
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416131"
---
# <a name="imapiformcontainergetdisplay"></a><span data-ttu-id="9a7ba-103">IMAPIFormContainer::GetDisplay</span><span class="sxs-lookup"><span data-stu-id="9a7ba-103">IMAPIFormContainer::GetDisplay</span></span>

  
  
<span data-ttu-id="9a7ba-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9a7ba-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9a7ba-105">Renvoie le nom complet d’un conteneur de formulaire.</span><span class="sxs-lookup"><span data-stu-id="9a7ba-105">Returns the display name of a form container.</span></span>
  
```cpp
HRESULT GetDisplay(
  ULONG ulFlags,
  LPSTR FAR * pszDisplayName
);
```

## <a name="parameters"></a><span data-ttu-id="9a7ba-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="9a7ba-106">Parameters</span></span>

 <span data-ttu-id="9a7ba-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="9a7ba-107">_ulFlags_</span></span>
  
> <span data-ttu-id="9a7ba-108">[in] Masque de bits d’indicateurs qui contrôle le type de la chaîne renvoyée.</span><span class="sxs-lookup"><span data-stu-id="9a7ba-108">[in] A bitmask of flags that controls the type of the returned string.</span></span> <span data-ttu-id="9a7ba-109">L’indicateur suivant peut être définie :</span><span class="sxs-lookup"><span data-stu-id="9a7ba-109">The following flag can be set:</span></span>
    
<span data-ttu-id="9a7ba-110">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="9a7ba-110">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="9a7ba-111">La chaîne renvoyée est au format Unicode.</span><span class="sxs-lookup"><span data-stu-id="9a7ba-111">The returned string is in Unicode format.</span></span> <span data-ttu-id="9a7ba-112">Si l MAPI_UNICODE n’est pas définie, la chaîne est au format ANSI.</span><span class="sxs-lookup"><span data-stu-id="9a7ba-112">If the MAPI_UNICODE flag is not set, the string is in ANSI format.</span></span>
    
 <span data-ttu-id="9a7ba-113">_pszDisplayName_</span><span class="sxs-lookup"><span data-stu-id="9a7ba-113">_pszDisplayName_</span></span>
  
> <span data-ttu-id="9a7ba-114">[out] Pointeur vers une chaîne qui contient le nom complet du conteneur de formulaires.</span><span class="sxs-lookup"><span data-stu-id="9a7ba-114">[out] A pointer to a string that contains the display name of the form container.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="9a7ba-115">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="9a7ba-115">Return value</span></span>

<span data-ttu-id="9a7ba-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="9a7ba-116">S_OK</span></span> 
  
> <span data-ttu-id="9a7ba-117">L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.</span><span class="sxs-lookup"><span data-stu-id="9a7ba-117">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="9a7ba-118">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="9a7ba-118">MFCMAPI reference</span></span>

<span data-ttu-id="9a7ba-119">Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="9a7ba-119">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="9a7ba-120">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="9a7ba-120">**File**</span></span>|<span data-ttu-id="9a7ba-121">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="9a7ba-121">**Function**</span></span>|<span data-ttu-id="9a7ba-122">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="9a7ba-122">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="9a7ba-123">FormContainerDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="9a7ba-123">FormContainerDlg.cpp</span></span>  <br/> |<span data-ttu-id="9a7ba-124">CFormContainerDlg::CFormContainerDlg</span><span class="sxs-lookup"><span data-stu-id="9a7ba-124">CFormContainerDlg::CFormContainerDlg</span></span>  <br/> |<span data-ttu-id="9a7ba-125">MFCMAPI utilise la méthode **IMAPIFormContainer::GetDisplay** pour obtenir le nom du conteneur de formulaires lors du rendu de CFormContainerDlg.</span><span class="sxs-lookup"><span data-stu-id="9a7ba-125">MFCMAPI uses the **IMAPIFormContainer::GetDisplay** method to get the name of the form container when it renders CFormContainerDlg.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="9a7ba-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9a7ba-126">See also</span></span>



[<span data-ttu-id="9a7ba-127">IMAPIFormContainer : IUnknown</span><span class="sxs-lookup"><span data-stu-id="9a7ba-127">IMAPIFormContainer : IUnknown</span></span>](imapiformcontaineriunknown.md)


[<span data-ttu-id="9a7ba-128">MFCMAPI comme un exemple de Code</span><span class="sxs-lookup"><span data-stu-id="9a7ba-128">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

