---
title: IMAPIFormContainer IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormContainer
api_type:
- COM
ms.assetid: 437c8a75-1121-4919-8bd4-d57c0d6f4b9a
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 3f03412c9ab639678c68016ec1a8eff937b6c1a0
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22590987"
---
# <a name="imapiformcontainer--iunknown"></a><span data-ttu-id="a5b4b-103">IMAPIFormContainer : IUnknown</span><span class="sxs-lookup"><span data-stu-id="a5b4b-103">IMAPIFormContainer : IUnknown</span></span>

  
  
<span data-ttu-id="a5b4b-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a5b4b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a5b4b-105">Gère les formulaires dans les bibliothèques de formulaires.</span><span class="sxs-lookup"><span data-stu-id="a5b4b-105">Manages forms in form libraries.</span></span> <span data-ttu-id="a5b4b-106">Cette interface est utilisée pour créer des bibliothèques de formulaires spécifique à l’application.</span><span class="sxs-lookup"><span data-stu-id="a5b4b-106">This interface is used to create application-specific form libraries.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a5b4b-107">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="a5b4b-107">Header file:</span></span>  <br/> |<span data-ttu-id="a5b4b-108">MAPIForm.h</span><span class="sxs-lookup"><span data-stu-id="a5b4b-108">Mapiform.h</span></span>  <br/> |
|<span data-ttu-id="a5b4b-109">Exposés par :</span><span class="sxs-lookup"><span data-stu-id="a5b4b-109">Exposed by:</span></span>  <br/> |<span data-ttu-id="a5b4b-110">Objets conteneurs de formulaire</span><span class="sxs-lookup"><span data-stu-id="a5b4b-110">Form container objects</span></span>  <br/> |
|<span data-ttu-id="a5b4b-111">Implémentée par :</span><span class="sxs-lookup"><span data-stu-id="a5b4b-111">Implemented by:</span></span>  <br/> |<span data-ttu-id="a5b4b-112">Fournisseurs de bibliothèques de formulaires</span><span class="sxs-lookup"><span data-stu-id="a5b4b-112">Form library providers</span></span>  <br/> |
|<span data-ttu-id="a5b4b-113">Appelée par :</span><span class="sxs-lookup"><span data-stu-id="a5b4b-113">Called by:</span></span>  <br/> |<span data-ttu-id="a5b4b-114">Applications clientes</span><span class="sxs-lookup"><span data-stu-id="a5b4b-114">Client applications</span></span>  <br/> |
|<span data-ttu-id="a5b4b-115">Identificateur de l’interface :</span><span class="sxs-lookup"><span data-stu-id="a5b4b-115">Interface identifier:</span></span>  <br/> |<span data-ttu-id="a5b4b-116">IID_IMAPIFormContainer</span><span class="sxs-lookup"><span data-stu-id="a5b4b-116">IID_IMAPIFormContainer</span></span>  <br/> |
|<span data-ttu-id="a5b4b-117">Type de pointeur :</span><span class="sxs-lookup"><span data-stu-id="a5b4b-117">Pointer type:</span></span>  <br/> |<span data-ttu-id="a5b4b-118">LPMAPIFORMCONTAINER</span><span class="sxs-lookup"><span data-stu-id="a5b4b-118">LPMAPIFORMCONTAINER</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="a5b4b-119">Ordre vtable</span><span class="sxs-lookup"><span data-stu-id="a5b4b-119">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="a5b4b-120">InstallForm</span><span class="sxs-lookup"><span data-stu-id="a5b4b-120">InstallForm</span></span>](imapiformcontainer-installform.md) <br/> |<span data-ttu-id="a5b4b-121">Installe un formulaire dans un conteneur de formulaire.</span><span class="sxs-lookup"><span data-stu-id="a5b4b-121">Installs a form into a form container.</span></span>  <br/> |
|[<span data-ttu-id="a5b4b-122">RemoveForm</span><span class="sxs-lookup"><span data-stu-id="a5b4b-122">RemoveForm</span></span>](imapiformcontainer-removeform.md) <br/> |<span data-ttu-id="a5b4b-123">Supprime un formulaire particulier à partir d’un conteneur de formulaire.</span><span class="sxs-lookup"><span data-stu-id="a5b4b-123">Removes a particular form from a form container.</span></span>  <br/> |
|[<span data-ttu-id="a5b4b-124">ResolveMessageClass</span><span class="sxs-lookup"><span data-stu-id="a5b4b-124">ResolveMessageClass</span></span>](imapiformcontainer-resolvemessageclass.md) <br/> |<span data-ttu-id="a5b4b-125">Résout une classe de message à sa forme dans un conteneur de formulaire et renvoie un objet d’informations de formulaire pour ce formulaire.</span><span class="sxs-lookup"><span data-stu-id="a5b4b-125">Resolves a message class to its form in a form container and returns a form information object for that form.</span></span>  <br/> |
|[<span data-ttu-id="a5b4b-126">ResolveMultipleMessageClasses</span><span class="sxs-lookup"><span data-stu-id="a5b4b-126">ResolveMultipleMessageClasses</span></span>](imapiformcontainer-resolvemultiplemessageclasses.md) <br/> |<span data-ttu-id="a5b4b-127">Résout un groupe de classes de message à leurs formulaires dans un conteneur de formulaire et renvoie un tableau de formulaire objets des informations pour les formulaires.</span><span class="sxs-lookup"><span data-stu-id="a5b4b-127">Resolves a group of message classes to their forms in a form container and returns an array of form information objects for those forms.</span></span>  <br/> |
|[<span data-ttu-id="a5b4b-128">CalcFormPropSet</span><span class="sxs-lookup"><span data-stu-id="a5b4b-128">CalcFormPropSet</span></span>](imapiformcontainer-calcformpropset.md) <br/> |<span data-ttu-id="a5b4b-129">Renvoie un tableau de propriétés utilisées par tous les formulaires installés dans un conteneur de formulaire.</span><span class="sxs-lookup"><span data-stu-id="a5b4b-129">Returns an array of the properties used by all forms installed in a form container.</span></span>  <br/> |
|[<span data-ttu-id="a5b4b-130">GetDisplay</span><span class="sxs-lookup"><span data-stu-id="a5b4b-130">GetDisplay</span></span>](imapiformcontainer-getdisplay.md) <br/> |<span data-ttu-id="a5b4b-131">Renvoie le nom complet d’un conteneur de formulaire.</span><span class="sxs-lookup"><span data-stu-id="a5b4b-131">Returns the display name of a form container.</span></span>  <br/> |
|[<span data-ttu-id="a5b4b-132">GetLastError</span><span class="sxs-lookup"><span data-stu-id="a5b4b-132">GetLastError</span></span>](imapiformcontainer-getlasterror.md) <br/> |<span data-ttu-id="a5b4b-133">Retourne une structure [MAPIERROR](mapierror.md) contenant des informations sur l’erreur précédente à l’objet conteneur de formulaire en cours.</span><span class="sxs-lookup"><span data-stu-id="a5b4b-133">Returns a [MAPIERROR](mapierror.md) structure containing information about the previous error occurring to the form container object.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a5b4b-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a5b4b-134">See also</span></span>



[<span data-ttu-id="a5b4b-135">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="a5b4b-135">MAPI Interfaces</span></span>](mapi-interfaces.md)

