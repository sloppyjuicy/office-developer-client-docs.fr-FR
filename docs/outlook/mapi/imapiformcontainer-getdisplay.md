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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 0f9826dab72968055604c5bb9f8f537facc5618e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783783"
---
# <a name="imapiformcontainergetdisplay"></a><span data-ttu-id="232fd-103">IMAPIFormContainer::GetDisplay</span><span class="sxs-lookup"><span data-stu-id="232fd-103">IMAPIFormContainer::GetDisplay</span></span>

  
  
<span data-ttu-id="232fd-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="232fd-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="232fd-105">Renvoie le nom complet d’un conteneur de formulaire.</span><span class="sxs-lookup"><span data-stu-id="232fd-105">Returns the display name of a form container.</span></span>
  
```cpp
HRESULT GetDisplay(
  ULONG ulFlags,
  LPSTR FAR * pszDisplayName
);
```

## <a name="parameters"></a><span data-ttu-id="232fd-106">Param�tres</span><span class="sxs-lookup"><span data-stu-id="232fd-106">Parameters</span></span>

 <span data-ttu-id="232fd-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="232fd-107">_ulFlags_</span></span>
  
> <span data-ttu-id="232fd-108">[in] Masque de bits d’indicateurs qui contrôle le type de la chaîne retournée.</span><span class="sxs-lookup"><span data-stu-id="232fd-108">[in] A bitmask of flags that controls the type of the returned string.</span></span> <span data-ttu-id="232fd-109">Vous pouvez définir l’indicateur suivant :</span><span class="sxs-lookup"><span data-stu-id="232fd-109">The following flag can be set:</span></span>
    
<span data-ttu-id="232fd-110">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="232fd-110">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="232fd-111">La chaîne retournée est au format Unicode.</span><span class="sxs-lookup"><span data-stu-id="232fd-111">The returned string is in Unicode format.</span></span> <span data-ttu-id="232fd-112">Si l’indicateur MAPI_UNICODE n’est pas définie, la chaîne est au format ANSI.</span><span class="sxs-lookup"><span data-stu-id="232fd-112">If the MAPI_UNICODE flag is not set, the string is in ANSI format.</span></span>
    
 <span data-ttu-id="232fd-113">_pszDisplayName_</span><span class="sxs-lookup"><span data-stu-id="232fd-113">_pszDisplayName_</span></span>
  
> <span data-ttu-id="232fd-114">[out] Pointeur vers une chaîne qui contient le nom complet du conteneur de formulaire.</span><span class="sxs-lookup"><span data-stu-id="232fd-114">[out] A pointer to a string that contains the display name of the form container.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="232fd-115">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="232fd-115">Return value</span></span>

<span data-ttu-id="232fd-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="232fd-116">S_OK</span></span> 
  
> <span data-ttu-id="232fd-117">L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.</span><span class="sxs-lookup"><span data-stu-id="232fd-117">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="232fd-118">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="232fd-118">MFCMAPI reference</span></span>

<span data-ttu-id="232fd-119">Pour des exemples de code MFCMAPI, voir le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="232fd-119">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="232fd-120">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="232fd-120">**File**</span></span>|<span data-ttu-id="232fd-121">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="232fd-121">**Function**</span></span>|<span data-ttu-id="232fd-122">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="232fd-122">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="232fd-123">FormContainerDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="232fd-123">FormContainerDlg.cpp</span></span>  <br/> |<span data-ttu-id="232fd-124">CFormContainerDlg::CFormContainerDlg</span><span class="sxs-lookup"><span data-stu-id="232fd-124">CFormContainerDlg::CFormContainerDlg</span></span>  <br/> |<span data-ttu-id="232fd-125">MFCMAPI utilise la méthode **IMAPIFormContainer::GetDisplay** pour obtenir le nom du formulaire conteneur lors du rendu CFormContainerDlg.</span><span class="sxs-lookup"><span data-stu-id="232fd-125">MFCMAPI uses the **IMAPIFormContainer::GetDisplay** method to get the name of the form container when it renders CFormContainerDlg.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="232fd-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="232fd-126">See also</span></span>



[<span data-ttu-id="232fd-127">IMAPIFormContainer : IUnknown</span><span class="sxs-lookup"><span data-stu-id="232fd-127">IMAPIFormContainer : IUnknown</span></span>](imapiformcontaineriunknown.md)


[<span data-ttu-id="232fd-128">MFCMAPI comme un exemple de Code</span><span class="sxs-lookup"><span data-stu-id="232fd-128">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

