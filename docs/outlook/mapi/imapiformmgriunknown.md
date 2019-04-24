---
title: IMAPIFormMgr IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormMgr
api_type:
- COM
ms.assetid: 8cbd1a42-7de6-43e0-8c77-7711773843d5
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: fbe6dc9364ee953661d574b70bcd225abcfe7a81
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321650"
---
# <a name="imapiformmgr--iunknown"></a><span data-ttu-id="0ce8a-103">IMAPIFormMgr : IUnknown</span><span class="sxs-lookup"><span data-stu-id="0ce8a-103">IMAPIFormMgr : IUnknown</span></span>

  
  
<span data-ttu-id="0ce8a-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0ce8a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0ce8a-105">Permet aux visionneuses de formulaires d'obtenir des informations sur les serveurs de formulaires et de les activer.</span><span class="sxs-lookup"><span data-stu-id="0ce8a-105">Enables form viewers to obtain information about and activate form servers.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="0ce8a-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="0ce8a-106">Header file:</span></span>  <br/> |<span data-ttu-id="0ce8a-107">MAPIForm. h</span><span class="sxs-lookup"><span data-stu-id="0ce8a-107">Mapiform.h</span></span>  <br/> |
|<span data-ttu-id="0ce8a-108">Exposé par:</span><span class="sxs-lookup"><span data-stu-id="0ce8a-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="0ce8a-109">Objets du gestionnaire de formulaires</span><span class="sxs-lookup"><span data-stu-id="0ce8a-109">Form manager objects</span></span>  <br/> |
|<span data-ttu-id="0ce8a-110">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="0ce8a-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="0ce8a-111">Fournisseurs de bibliothèques de formulaires</span><span class="sxs-lookup"><span data-stu-id="0ce8a-111">Form library providers</span></span>  <br/> |
|<span data-ttu-id="0ce8a-112">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="0ce8a-112">Called by:</span></span>  <br/> |<span data-ttu-id="0ce8a-113">Visionneuses de formulaires</span><span class="sxs-lookup"><span data-stu-id="0ce8a-113">Form viewers</span></span>  <br/> |
|<span data-ttu-id="0ce8a-114">Identificateur de l'interface:</span><span class="sxs-lookup"><span data-stu-id="0ce8a-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="0ce8a-115">IID_IMAPIFormMgr</span><span class="sxs-lookup"><span data-stu-id="0ce8a-115">IID_IMAPIFormMgr</span></span>  <br/> |
|<span data-ttu-id="0ce8a-116">Type de pointeur:</span><span class="sxs-lookup"><span data-stu-id="0ce8a-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="0ce8a-117">LPMAPIFORMMGR</span><span class="sxs-lookup"><span data-stu-id="0ce8a-117">LPMAPIFORMMGR</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="0ce8a-118">Ordre vtable</span><span class="sxs-lookup"><span data-stu-id="0ce8a-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="0ce8a-119">LoadForm</span><span class="sxs-lookup"><span data-stu-id="0ce8a-119">LoadForm</span></span>](imapiformmgr-loadform.md) <br/> |<span data-ttu-id="0ce8a-120">Ouvre un formulaire pour ouvrir un message existant.</span><span class="sxs-lookup"><span data-stu-id="0ce8a-120">Starts a form to open an existing message.</span></span>  <br/> |
|[<span data-ttu-id="0ce8a-121">ResolveMessageClass</span><span class="sxs-lookup"><span data-stu-id="0ce8a-121">ResolveMessageClass</span></span>](imapiformmgr-resolvemessageclass.md) <br/> |<span data-ttu-id="0ce8a-122">Résout une classe de message sous sa forme dans un conteneur de formulaire et renvoie un objet d'informations de formulaire pour ce formulaire.</span><span class="sxs-lookup"><span data-stu-id="0ce8a-122">Resolves a message class to its form within a form container, and returns a form information object for that form.</span></span>  <br/> |
|[<span data-ttu-id="0ce8a-123">ResolveMultipleMessageClasses</span><span class="sxs-lookup"><span data-stu-id="0ce8a-123">ResolveMultipleMessageClasses</span></span>](imapiformmgr-resolvemultiplemessageclasses.md) <br/> |<span data-ttu-id="0ce8a-124">Résout un groupe de classes de message à leurs formulaires dans un conteneur de formulaires et renvoie un tableau d'objets d'informations de formulaire pour ces formulaires.</span><span class="sxs-lookup"><span data-stu-id="0ce8a-124">Resolves a group of message classes to their forms within a form container, and returns an array of form information objects for those forms.</span></span>  <br/> |
|[<span data-ttu-id="0ce8a-125">CalcFormPropSet</span><span class="sxs-lookup"><span data-stu-id="0ce8a-125">CalcFormPropSet</span></span>](imapiformmgr-calcformpropset.md) <br/> |<span data-ttu-id="0ce8a-126">Renvoie un tableau des propriétés utilisées par un groupe de formulaires.</span><span class="sxs-lookup"><span data-stu-id="0ce8a-126">Returns an array of the properties that a group of forms uses.</span></span>  <br/> |
|[<span data-ttu-id="0ce8a-127">CreateForm</span><span class="sxs-lookup"><span data-stu-id="0ce8a-127">CreateForm</span></span>](imapiformmgr-createform.md) <br/> |<span data-ttu-id="0ce8a-128">Lance un formulaire permettant de créer un nouveau message basé sur la classe de message du formulaire.</span><span class="sxs-lookup"><span data-stu-id="0ce8a-128">Launches a form to create a new message based on the form's message class.</span></span>  <br/> |
|[<span data-ttu-id="0ce8a-129">SelectForm</span><span class="sxs-lookup"><span data-stu-id="0ce8a-129">SelectForm</span></span>](imapiformmgr-selectform.md) <br/> |<span data-ttu-id="0ce8a-130">Affiche une boîte de dialogue qui permet à l'utilisateur de sélectionner un formulaire et renvoie un objet d'informations de formulaire qui décrit ce formulaire.</span><span class="sxs-lookup"><span data-stu-id="0ce8a-130">Presents a dialog box that enables the user to select a form, and returns a form information object that describes that form.</span></span>  <br/> |
|[<span data-ttu-id="0ce8a-131">SelectMultipleForms</span><span class="sxs-lookup"><span data-stu-id="0ce8a-131">SelectMultipleForms</span></span>](imapiformmgr-selectmultipleforms.md) <br/> |<span data-ttu-id="0ce8a-132">Affiche une boîte de dialogue qui permet à l'utilisateur de sélectionner plusieurs formulaires et renvoie un tableau d'objets d'informations de formulaire qui décrivent ces formulaires.</span><span class="sxs-lookup"><span data-stu-id="0ce8a-132">Presents a dialog box that enables the user to select multiple forms, and returns an array of form information objects that describe those forms.</span></span>  <br/> |
|[<span data-ttu-id="0ce8a-133">SelectFormContainer</span><span class="sxs-lookup"><span data-stu-id="0ce8a-133">SelectFormContainer</span></span>](imapiformmgr-selectformcontainer.md) <br/> |<span data-ttu-id="0ce8a-134">Affiche une boîte de dialogue qui permet à l'utilisateur de sélectionner un conteneur de formulaires et renvoie une interface pour l'objet conteneur sélectionné par l'utilisateur.</span><span class="sxs-lookup"><span data-stu-id="0ce8a-134">Presents a dialog box that enables the user to select a form container, and returns an interface for the container object the user selected.</span></span>  <br/> |
|[<span data-ttu-id="0ce8a-135">OpenFormContainer</span><span class="sxs-lookup"><span data-stu-id="0ce8a-135">OpenFormContainer</span></span>](imapiformmgr-openformcontainer.md) <br/> |<span data-ttu-id="0ce8a-136">Ouvre une interface [IMAPIFormContainer](imapiformcontaineriunknown.md) pour un conteneur de formulaire spécifique.</span><span class="sxs-lookup"><span data-stu-id="0ce8a-136">Opens an [IMAPIFormContainer](imapiformcontaineriunknown.md) interface for a specific form container.</span></span>  <br/> |
|[<span data-ttu-id="0ce8a-137">PrepareForm</span><span class="sxs-lookup"><span data-stu-id="0ce8a-137">PrepareForm</span></span>](imapiformmgr-prepareform.md) <br/> |<span data-ttu-id="0ce8a-138">Télécharge un formulaire à ouvrir.</span><span class="sxs-lookup"><span data-stu-id="0ce8a-138">Downloads a form for opening.</span></span>  <br/> |
|[<span data-ttu-id="0ce8a-139">IsInConflict</span><span class="sxs-lookup"><span data-stu-id="0ce8a-139">IsInConflict</span></span>](imapiformmgr-isinconflict.md) <br/> |<span data-ttu-id="0ce8a-140">Détermine si un formulaire peut gérer ses propres conflits de messages.</span><span class="sxs-lookup"><span data-stu-id="0ce8a-140">Determines whether a form can handle its own message conflicts.</span></span>  <br/> |
|[<span data-ttu-id="0ce8a-141">Généré</span><span class="sxs-lookup"><span data-stu-id="0ce8a-141">GetLastError</span></span>](imapiformmgr-getlasterror.md) <br/> |<span data-ttu-id="0ce8a-142">Renvoie une structure [MAPIERROR](mapierror.md) qui contient des informations sur l'erreur précédente qui s'est produite dans l'objet gestionnaire de formulaires.</span><span class="sxs-lookup"><span data-stu-id="0ce8a-142">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous error occurring to the form manager object.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="0ce8a-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0ce8a-143">See also</span></span>



[<span data-ttu-id="0ce8a-144">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="0ce8a-144">MAPI Interfaces</span></span>](mapi-interfaces.md)

