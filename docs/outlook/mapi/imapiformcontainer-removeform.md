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
ms.openlocfilehash: 0d2c908f86ccd66ffd3a2eb2506d129ee2a14d48
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783765"
---
# <a name="imapiformcontainerremoveform"></a><span data-ttu-id="f8b42-103">IMAPIFormContainer::RemoveForm</span><span class="sxs-lookup"><span data-stu-id="f8b42-103">IMAPIFormContainer::RemoveForm</span></span>

  
  
<span data-ttu-id="f8b42-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="f8b42-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="f8b42-105">Supprime un formulaire particulier à partir d’un conteneur de formulaire.</span><span class="sxs-lookup"><span data-stu-id="f8b42-105">Removes a particular form from a form container.</span></span>
  
```cpp
HRESULT RemoveForm(
  LPCSTR szMessageClass
);
```

## <a name="parameters"></a><span data-ttu-id="f8b42-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f8b42-106">Parameters</span></span>

 <span data-ttu-id="f8b42-107">_szMessageClass_</span><span class="sxs-lookup"><span data-stu-id="f8b42-107">_szMessageClass_</span></span>
  
> <span data-ttu-id="f8b42-108">[in] Chaîne qui nomme la classe de message du formulaire à supprimer du conteneur de formulaire.</span><span class="sxs-lookup"><span data-stu-id="f8b42-108">[in] A string that names the message class of the form to be removed from the form container.</span></span> <span data-ttu-id="f8b42-109">Noms de classe de message sont toujours des chaînes ANSI, Unicode jamais.</span><span class="sxs-lookup"><span data-stu-id="f8b42-109">Message class names are always ANSI strings, never Unicode.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="f8b42-110">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="f8b42-110">Return value</span></span>

<span data-ttu-id="f8b42-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="f8b42-111">S_OK</span></span> 
  
> <span data-ttu-id="f8b42-112">L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.</span><span class="sxs-lookup"><span data-stu-id="f8b42-112">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="f8b42-113">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="f8b42-113">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="f8b42-114">La classe de message transmise dans le paramètre _szMessageClass_ ne correspond pas à la classe de message de n’importe quel formulaire dans le conteneur du formulaire.</span><span class="sxs-lookup"><span data-stu-id="f8b42-114">The message class passed in the  _szMessageClass_ parameter does not match the message class of any form in the form container.</span></span> 
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="f8b42-115">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="f8b42-115">MFCMAPI reference</span></span>

<span data-ttu-id="f8b42-116">Pour des exemples de code MFCMAPI, voir le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="f8b42-116">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="f8b42-117">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="f8b42-117">**File**</span></span>|<span data-ttu-id="f8b42-118">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="f8b42-118">**Function**</span></span>|<span data-ttu-id="f8b42-119">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="f8b42-119">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="f8b42-120">FormContainerDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="f8b42-120">FormContainerDlg.cpp</span></span>  <br/> |<span data-ttu-id="f8b42-121">CFormContainerDlg::OnDeleteSelectedItem</span><span class="sxs-lookup"><span data-stu-id="f8b42-121">CFormContainerDlg::OnDeleteSelectedItem</span></span>  <br/> |<span data-ttu-id="f8b42-122">MFCMAPI utilise la méthode **IMAPIFormContainer::RemoveForm** pour supprimer un formulaire à partir d’un conteneur de formulaire.</span><span class="sxs-lookup"><span data-stu-id="f8b42-122">MFCMAPI uses the **IMAPIFormContainer::RemoveForm** method to delete a form from a form container.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f8b42-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f8b42-123">See also</span></span>



[<span data-ttu-id="f8b42-124">IMAPIFormContainer : IUnknown</span><span class="sxs-lookup"><span data-stu-id="f8b42-124">IMAPIFormContainer : IUnknown</span></span>](imapiformcontaineriunknown.md)


[<span data-ttu-id="f8b42-125">MFCMAPI comme un exemple de Code</span><span class="sxs-lookup"><span data-stu-id="f8b42-125">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

