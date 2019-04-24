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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: e53c0cbd9946ff04516594a7ce99fdc2daf4ff4d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355741"
---
# <a name="imapiformcontainerremoveform"></a><span data-ttu-id="16a6f-103">IMAPIFormContainer::RemoveForm</span><span class="sxs-lookup"><span data-stu-id="16a6f-103">IMAPIFormContainer::RemoveForm</span></span>

  
  
<span data-ttu-id="16a6f-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="16a6f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="16a6f-105">Supprime un formulaire particulier d'un conteneur de formulaires.</span><span class="sxs-lookup"><span data-stu-id="16a6f-105">Removes a particular form from a form container.</span></span>
  
```cpp
HRESULT RemoveForm(
  LPCSTR szMessageClass
);
```

## <a name="parameters"></a><span data-ttu-id="16a6f-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="16a6f-106">Parameters</span></span>

 <span data-ttu-id="16a6f-107">_szMessageClass_</span><span class="sxs-lookup"><span data-stu-id="16a6f-107">_szMessageClass_</span></span>
  
> <span data-ttu-id="16a6f-108">dans Chaîne qui nomme la classe de message du formulaire à supprimer du conteneur de formulaire.</span><span class="sxs-lookup"><span data-stu-id="16a6f-108">[in] A string that names the message class of the form to be removed from the form container.</span></span> <span data-ttu-id="16a6f-109">Les noms de classe de message sont toujours des chaînes ANSI, jamais Unicode.</span><span class="sxs-lookup"><span data-stu-id="16a6f-109">Message class names are always ANSI strings, never Unicode.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="16a6f-110">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="16a6f-110">Return value</span></span>

<span data-ttu-id="16a6f-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="16a6f-111">S_OK</span></span> 
  
> <span data-ttu-id="16a6f-112">L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.</span><span class="sxs-lookup"><span data-stu-id="16a6f-112">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="16a6f-113">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="16a6f-113">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="16a6f-114">La classe de message passée dans le paramètre _szMessageClass_ ne correspond pas à la classe de message d'un formulaire dans le conteneur de formulaire.</span><span class="sxs-lookup"><span data-stu-id="16a6f-114">The message class passed in the  _szMessageClass_ parameter does not match the message class of any form in the form container.</span></span> 
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="16a6f-115">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="16a6f-115">MFCMAPI reference</span></span>

<span data-ttu-id="16a6f-116">Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="16a6f-116">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="16a6f-117">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="16a6f-117">**File**</span></span>|<span data-ttu-id="16a6f-118">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="16a6f-118">**Function**</span></span>|<span data-ttu-id="16a6f-119">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="16a6f-119">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="16a6f-120">FormContainerDlg. cpp</span><span class="sxs-lookup"><span data-stu-id="16a6f-120">FormContainerDlg.cpp</span></span>  <br/> |<span data-ttu-id="16a6f-121">CFormContainerDlg:: OnDeleteSelectedItem</span><span class="sxs-lookup"><span data-stu-id="16a6f-121">CFormContainerDlg::OnDeleteSelectedItem</span></span>  <br/> |<span data-ttu-id="16a6f-122">MFCMAPI utilise la méthode **IMAPIFormContainer:: RemoveForm** pour supprimer un formulaire d'un conteneur de formulaire.</span><span class="sxs-lookup"><span data-stu-id="16a6f-122">MFCMAPI uses the **IMAPIFormContainer::RemoveForm** method to delete a form from a form container.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="16a6f-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="16a6f-123">See also</span></span>



[<span data-ttu-id="16a6f-124">IMAPIFormContainer : IUnknown</span><span class="sxs-lookup"><span data-stu-id="16a6f-124">IMAPIFormContainer : IUnknown</span></span>](imapiformcontaineriunknown.md)


[<span data-ttu-id="16a6f-125">MFCMAPI comme un exemple de Code</span><span class="sxs-lookup"><span data-stu-id="16a6f-125">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

