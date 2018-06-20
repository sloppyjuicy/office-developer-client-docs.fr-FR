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
ms.openlocfilehash: 4fdd50a1108a6546445516664b01fb0f994fbfdb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783820"
---
# <a name="imapiformmgr--iunknown"></a><span data-ttu-id="48221-103">IMAPIFormMgr : IUnknown</span><span class="sxs-lookup"><span data-stu-id="48221-103">IMAPIFormMgr : IUnknown</span></span>

  
  
<span data-ttu-id="48221-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="48221-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="48221-105">Permet les visionneuses de formulaire obtenir des informations sur et activer des serveurs de formulaire.</span><span class="sxs-lookup"><span data-stu-id="48221-105">Enables form viewers to obtain information about and activate form servers.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="48221-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="48221-106">Header file:</span></span>  <br/> |<span data-ttu-id="48221-107">MAPIForm.h</span><span class="sxs-lookup"><span data-stu-id="48221-107">Mapiform.h</span></span>  <br/> |
|<span data-ttu-id="48221-108">Exposés par :</span><span class="sxs-lookup"><span data-stu-id="48221-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="48221-109">Objets Gestionnaire de formulaire</span><span class="sxs-lookup"><span data-stu-id="48221-109">Form manager objects</span></span>  <br/> |
|<span data-ttu-id="48221-110">Implémentée par :</span><span class="sxs-lookup"><span data-stu-id="48221-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="48221-111">Fournisseurs de bibliothèques de formulaires</span><span class="sxs-lookup"><span data-stu-id="48221-111">Form library providers</span></span>  <br/> |
|<span data-ttu-id="48221-112">Appelée par :</span><span class="sxs-lookup"><span data-stu-id="48221-112">Called by:</span></span>  <br/> |<span data-ttu-id="48221-113">Visionneuses de formulaire</span><span class="sxs-lookup"><span data-stu-id="48221-113">Form viewers</span></span>  <br/> |
|<span data-ttu-id="48221-114">Identificateur de l’interface :</span><span class="sxs-lookup"><span data-stu-id="48221-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="48221-115">IID_IMAPIFormMgr</span><span class="sxs-lookup"><span data-stu-id="48221-115">IID_IMAPIFormMgr</span></span>  <br/> |
|<span data-ttu-id="48221-116">Type de pointeur :</span><span class="sxs-lookup"><span data-stu-id="48221-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="48221-117">LPMAPIFORMMGR</span><span class="sxs-lookup"><span data-stu-id="48221-117">LPMAPIFORMMGR</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="48221-118">Ordre vtable</span><span class="sxs-lookup"><span data-stu-id="48221-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="48221-119">LoadForm</span><span class="sxs-lookup"><span data-stu-id="48221-119">LoadForm</span></span>](imapiformmgr-loadform.md) <br/> |<span data-ttu-id="48221-120">Démarre un formulaire pour ouvrir un message existant.</span><span class="sxs-lookup"><span data-stu-id="48221-120">Starts a form to open an existing message.</span></span>  <br/> |
|[<span data-ttu-id="48221-121">ResolveMessageClass</span><span class="sxs-lookup"><span data-stu-id="48221-121">ResolveMessageClass</span></span>](imapiformmgr-resolvemessageclass.md) <br/> |<span data-ttu-id="48221-122">Associe une classe de message à sa forme au sein d’un conteneur de formulaire et renvoie un objet d’informations de formulaire pour ce formulaire.</span><span class="sxs-lookup"><span data-stu-id="48221-122">Resolves a message class to its form within a form container, and returns a form information object for that form.</span></span>  <br/> |
|[<span data-ttu-id="48221-123">ResolveMultipleMessageClasses</span><span class="sxs-lookup"><span data-stu-id="48221-123">ResolveMultipleMessageClasses</span></span>](imapiformmgr-resolvemultiplemessageclasses.md) <br/> |<span data-ttu-id="48221-124">Résout un groupe de classes de message à leurs formulaires dans un conteneur de formulaire et renvoie un tableau de formulaire objets des informations pour les formulaires.</span><span class="sxs-lookup"><span data-stu-id="48221-124">Resolves a group of message classes to their forms within a form container, and returns an array of form information objects for those forms.</span></span>  <br/> |
|[<span data-ttu-id="48221-125">CalcFormPropSet</span><span class="sxs-lookup"><span data-stu-id="48221-125">CalcFormPropSet</span></span>](imapiformmgr-calcformpropset.md) <br/> |<span data-ttu-id="48221-126">Renvoie un tableau des propriétés qui utilise un groupe de formulaires.</span><span class="sxs-lookup"><span data-stu-id="48221-126">Returns an array of the properties that a group of forms uses.</span></span>  <br/> |
|[<span data-ttu-id="48221-127">CreateForm</span><span class="sxs-lookup"><span data-stu-id="48221-127">CreateForm</span></span>](imapiformmgr-createform.md) <br/> |<span data-ttu-id="48221-128">Ouvre un formulaire pour créer un nouveau message en fonction de la classe de message du formulaire.</span><span class="sxs-lookup"><span data-stu-id="48221-128">Launches a form to create a new message based on the form's message class.</span></span>  <br/> |
|[<span data-ttu-id="48221-129">SelectForm</span><span class="sxs-lookup"><span data-stu-id="48221-129">SelectForm</span></span>](imapiformmgr-selectform.md) <br/> |<span data-ttu-id="48221-130">Affiche une boîte de dialogue qui permet à l’utilisateur de sélectionner un formulaire et renvoie un objet d’informations de formulaire qui décrit ce formulaire.</span><span class="sxs-lookup"><span data-stu-id="48221-130">Presents a dialog box that enables the user to select a form, and returns a form information object that describes that form.</span></span>  <br/> |
|[<span data-ttu-id="48221-131">SelectMultipleForms</span><span class="sxs-lookup"><span data-stu-id="48221-131">SelectMultipleForms</span></span>](imapiformmgr-selectmultipleforms.md) <br/> |<span data-ttu-id="48221-132">Affiche une boîte de dialogue qui permet à l’utilisateur de sélectionner plusieurs formulaires et renvoie un tableau de formulaire objets informations décrivant les formulaires.</span><span class="sxs-lookup"><span data-stu-id="48221-132">Presents a dialog box that enables the user to select multiple forms, and returns an array of form information objects that describe those forms.</span></span>  <br/> |
|[<span data-ttu-id="48221-133">SelectFormContainer</span><span class="sxs-lookup"><span data-stu-id="48221-133">SelectFormContainer</span></span>](imapiformmgr-selectformcontainer.md) <br/> |<span data-ttu-id="48221-134">Présente une boîte de dialogue qui permet à l’utilisateur sélectionner un conteneur de formulaire et renvoie une interface pour l’objet conteneur de l’utilisateur sélectionné.</span><span class="sxs-lookup"><span data-stu-id="48221-134">Presents a dialog box that enables the user to select a form container, and returns an interface for the container object the user selected.</span></span>  <br/> |
|[<span data-ttu-id="48221-135">OpenFormContainer</span><span class="sxs-lookup"><span data-stu-id="48221-135">OpenFormContainer</span></span>](imapiformmgr-openformcontainer.md) <br/> |<span data-ttu-id="48221-136">Ouvre une interface [IMAPIFormContainer](imapiformcontaineriunknown.md) pour un conteneur de formulaire spécifique.</span><span class="sxs-lookup"><span data-stu-id="48221-136">Opens an [IMAPIFormContainer](imapiformcontaineriunknown.md) interface for a specific form container.</span></span>  <br/> |
|[<span data-ttu-id="48221-137">PrepareForm</span><span class="sxs-lookup"><span data-stu-id="48221-137">PrepareForm</span></span>](imapiformmgr-prepareform.md) <br/> |<span data-ttu-id="48221-138">Télécharge un formulaire d’ouverture.</span><span class="sxs-lookup"><span data-stu-id="48221-138">Downloads a form for opening.</span></span>  <br/> |
|[<span data-ttu-id="48221-139">IsInConflict</span><span class="sxs-lookup"><span data-stu-id="48221-139">IsInConflict</span></span>](imapiformmgr-isinconflict.md) <br/> |<span data-ttu-id="48221-140">Détermine si un formulaire peut gérer son propre conflits de message.</span><span class="sxs-lookup"><span data-stu-id="48221-140">Determines whether a form can handle its own message conflicts.</span></span>  <br/> |
|[<span data-ttu-id="48221-141">GetLastError</span><span class="sxs-lookup"><span data-stu-id="48221-141">GetLastError</span></span>](imapiformmgr-getlasterror.md) <br/> |<span data-ttu-id="48221-142">Retourne une structure [MAPIERROR](mapierror.md) qui contient des informations sur l’erreur précédente à l’objet de gestionnaire de formulaire.</span><span class="sxs-lookup"><span data-stu-id="48221-142">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous error occurring to the form manager object.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="48221-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="48221-143">See also</span></span>



[<span data-ttu-id="48221-144">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="48221-144">MAPI Interfaces</span></span>](mapi-interfaces.md)

