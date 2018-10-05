---
title: IPersistMessageSave
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPersistMessage.Save
api_type:
- COM
ms.assetid: 17875c13-f55b-4538-ac6f-c020281c3175
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: fa3f1d6339000fcc53e0ee22dafec4362e65ca7f
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25397155"
---
# <a name="ipersistmessagesave"></a><span data-ttu-id="31630-103">IPersistMessage::Save</span><span class="sxs-lookup"><span data-stu-id="31630-103">IPersistMessage::Save</span></span>

  
  
<span data-ttu-id="31630-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="31630-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="31630-105">Enregistre un formulaire révisé dans le message à partir de laquelle il a été chargé ou créé.</span><span class="sxs-lookup"><span data-stu-id="31630-105">Saves a revised form back to the message from which it was loaded or created.</span></span>
  
```cpp
HRESULT Save(
  LPMESSAGE pMessage,
  ULONG fSameAsLoad
);
```

## <a name="parameters"></a><span data-ttu-id="31630-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="31630-106">Parameters</span></span>

 <span data-ttu-id="31630-107">_pMessage_</span><span class="sxs-lookup"><span data-stu-id="31630-107">_pMessage_</span></span>
  
> <span data-ttu-id="31630-108">[in] Pointeur vers le message.</span><span class="sxs-lookup"><span data-stu-id="31630-108">[in] A pointer to the message.</span></span>
    
 <span data-ttu-id="31630-109">_fSameAsLoad_</span><span class="sxs-lookup"><span data-stu-id="31630-109">_fSameAsLoad_</span></span>
  
> <span data-ttu-id="31630-110">[in] TRUE pour indiquer que le message vers lequel pointe par _pMessage_ est le message à partir de laquelle le formulaire a été chargé ou créé ; Sinon, FALSE.</span><span class="sxs-lookup"><span data-stu-id="31630-110">[in] TRUE to indicate that the message pointed to by  _pMessage_ is the message from which the form was loaded or created; otherwise, FALSE.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="31630-111">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="31630-111">Return value</span></span>

<span data-ttu-id="31630-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="31630-112">S_OK</span></span> 
  
> <span data-ttu-id="31630-113">Le formulaire a été enregistré avec succès.</span><span class="sxs-lookup"><span data-stu-id="31630-113">The form was successfully saved.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="31630-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="31630-114">Remarks</span></span>

<span data-ttu-id="31630-115">Visionneuses de formulaire appeler la méthode **IPersistMessage::Save** pour enregistrer un formulaire révisé dans le message à partir de laquelle il a été chargé ou créé.</span><span class="sxs-lookup"><span data-stu-id="31630-115">Form viewers call the **IPersistMessage::Save** method to save a revised form back to the message from which it was loaded or created.</span></span> 
  
 <span data-ttu-id="31630-116">**Enregistrer** doit être appelée uniquement lorsque le formulaire est dans son état [Normal](normal-state.md) .</span><span class="sxs-lookup"><span data-stu-id="31630-116">**Save** should only be called when the form is in its [Normal](normal-state.md) state.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="31630-117">Remarques à l’attention des responsables de l’implémentation</span><span class="sxs-lookup"><span data-stu-id="31630-117">Notes to implementers</span></span>

<span data-ttu-id="31630-118">Ne vous engagez pas les modifications enregistrées ; C’est à l’appelant pour valider les modifications.</span><span class="sxs-lookup"><span data-stu-id="31630-118">Do not commit the saved changes; it is up to the caller to commit the changes.</span></span> <span data-ttu-id="31630-119">Ne jamais modifier les propriétés qui appartiennent au message du formulaire à l’exception lors de l’appel à **Enregistrer** .</span><span class="sxs-lookup"><span data-stu-id="31630-119">Never make changes to the properties that belong to the form's message except during the **Save** call.</span></span> 
  
<span data-ttu-id="31630-120">Si _fSameAsLoad_ est défini sur TRUE, vous pouvez enregistrer les modifications apportées à un message existant du formulaire.</span><span class="sxs-lookup"><span data-stu-id="31630-120">If  _fSameAsLoad_ is set to TRUE, you can save the changes to the form's existing message.</span></span> <span data-ttu-id="31630-121">Si _fSameAsLoad_ est défini sur FALSE, vous devez copier toutes les propriétés à partir du message d’origine dans le message vers lequel pointé _pMessage_ avant d’effectuer l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="31630-121">If  _fSameAsLoad_ is set to FALSE, you must copy all of the properties from the original message into the message pointed to by  _pMessage_ before performing the save.</span></span> <span data-ttu-id="31630-122">Utilisez la méthode [IMAPIProp::CopyTo](imapiprop-copyto.md) du message d’origine pour copier les propriétés.</span><span class="sxs-lookup"><span data-stu-id="31630-122">Use the original message's [IMAPIProp::CopyTo](imapiprop-copyto.md) method to copy the properties.</span></span> 
  
<span data-ttu-id="31630-123">Lorsque toutes les propriétés ont été copiés, entrez l’état [NoScribble](noscribble-state.md) .</span><span class="sxs-lookup"><span data-stu-id="31630-123">When all of the properties have been copied, enter the [NoScribble](noscribble-state.md) state.</span></span> <span data-ttu-id="31630-124">Si aucune erreur ne se produire, retournent S_OK.</span><span class="sxs-lookup"><span data-stu-id="31630-124">If no errors occur, return S_OK.</span></span> <span data-ttu-id="31630-125">Sinon, renvoie l’erreur de l’action a échoué.</span><span class="sxs-lookup"><span data-stu-id="31630-125">Otherwise, return the error from the failed action.</span></span> 
  
<span data-ttu-id="31630-126">Si vous **enregistrez** est appelée lorsque le formulaire est dans un état autre que Normal, retourner E_UNEXPECTED.</span><span class="sxs-lookup"><span data-stu-id="31630-126">If **Save** is called when the form is in any state other than Normal, return E_UNEXPECTED.</span></span> 
  
<span data-ttu-id="31630-127">Pour plus d’informations sur l’enregistrement des objets de stockage, consultez la documentation sur les méthodes [IPersistStorage](https://msdn.microsoft.com/library/1c1a20fc-c101-4cbc-a7a6-30613aa387d7%28Office.15%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="31630-127">For more information about saving storage objects, see the documentation on the [IPersistStorage](https://msdn.microsoft.com/library/1c1a20fc-c101-4cbc-a7a6-30613aa387d7%28Office.15%29.aspx) methods.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="31630-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="31630-128">See also</span></span>



[<span data-ttu-id="31630-129">IPersistMessage : IUnknown</span><span class="sxs-lookup"><span data-stu-id="31630-129">IPersistMessage : IUnknown</span></span>](ipersistmessageiunknown.md)


[<span data-ttu-id="31630-130">États de formulaire</span><span class="sxs-lookup"><span data-stu-id="31630-130">Form States</span></span>](form-states.md)

