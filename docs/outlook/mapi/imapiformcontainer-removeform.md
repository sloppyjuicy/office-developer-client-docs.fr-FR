---
title: IMAPIFormContainerRemoveForm
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormContainer.RemoveForm
api_type:
- COM
ms.assetid: 7f851ce8-bd01-4ea5-86e0-e44323cc0aab
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: e53c0cbd9946ff04516594a7ce99fdc2daf4ff4d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432197"
---
# <a name="imapiformcontainerremoveform"></a><span data-ttu-id="daf7c-103">IMAPIFormContainer::RemoveForm</span><span class="sxs-lookup"><span data-stu-id="daf7c-103">IMAPIFormContainer::RemoveForm</span></span>

  
  
<span data-ttu-id="daf7c-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="daf7c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="daf7c-105">Supprime un formulaire particulier d'un conteneur de formulaires.</span><span class="sxs-lookup"><span data-stu-id="daf7c-105">Removes a particular form from a form container.</span></span>
  
```cpp
HRESULT RemoveForm(
  LPCSTR szMessageClass
);
```

## <a name="parameters"></a><span data-ttu-id="daf7c-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="daf7c-106">Parameters</span></span>

 <span data-ttu-id="daf7c-107">_szMessageClass_</span><span class="sxs-lookup"><span data-stu-id="daf7c-107">_szMessageClass_</span></span>
  
> <span data-ttu-id="daf7c-108">dans Chaîne qui nomme la classe de message du formulaire à supprimer du conteneur de formulaire.</span><span class="sxs-lookup"><span data-stu-id="daf7c-108">[in] A string that names the message class of the form to be removed from the form container.</span></span> <span data-ttu-id="daf7c-109">Les noms de classe de message sont toujours des chaînes ANSI, jamais Unicode.</span><span class="sxs-lookup"><span data-stu-id="daf7c-109">Message class names are always ANSI strings, never Unicode.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="daf7c-110">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="daf7c-110">Return value</span></span>

<span data-ttu-id="daf7c-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="daf7c-111">S_OK</span></span> 
  
> <span data-ttu-id="daf7c-112">L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.</span><span class="sxs-lookup"><span data-stu-id="daf7c-112">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="daf7c-113">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="daf7c-113">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="daf7c-114">La classe de message passée dans le paramètre _szMessageClass_ ne correspond pas à la classe de message d'un formulaire dans le conteneur de formulaire.</span><span class="sxs-lookup"><span data-stu-id="daf7c-114">The message class passed in the  _szMessageClass_ parameter does not match the message class of any form in the form container.</span></span> 
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="daf7c-115">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="daf7c-115">MFCMAPI reference</span></span>

<span data-ttu-id="daf7c-116">Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="daf7c-116">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="daf7c-117">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="daf7c-117">**File**</span></span>|<span data-ttu-id="daf7c-118">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="daf7c-118">**Function**</span></span>|<span data-ttu-id="daf7c-119">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="daf7c-119">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="daf7c-120">FormContainerDlg. cpp</span><span class="sxs-lookup"><span data-stu-id="daf7c-120">FormContainerDlg.cpp</span></span>  <br/> |<span data-ttu-id="daf7c-121">CFormContainerDlg:: OnDeleteSelectedItem</span><span class="sxs-lookup"><span data-stu-id="daf7c-121">CFormContainerDlg::OnDeleteSelectedItem</span></span>  <br/> |<span data-ttu-id="daf7c-122">MFCMAPI utilise la méthode **IMAPIFormContainer:: RemoveForm** pour supprimer un formulaire d'un conteneur de formulaire.</span><span class="sxs-lookup"><span data-stu-id="daf7c-122">MFCMAPI uses the **IMAPIFormContainer::RemoveForm** method to delete a form from a form container.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="daf7c-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="daf7c-123">See also</span></span>



[<span data-ttu-id="daf7c-124">IMAPIFormContainer : IUnknown</span><span class="sxs-lookup"><span data-stu-id="daf7c-124">IMAPIFormContainer : IUnknown</span></span>](imapiformcontaineriunknown.md)


[<span data-ttu-id="daf7c-125">MFCMAPI comme un exemple de Code</span><span class="sxs-lookup"><span data-stu-id="daf7c-125">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

