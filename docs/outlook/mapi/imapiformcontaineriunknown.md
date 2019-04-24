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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 208af28307a60615ecafda0992881c5df36aa56f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342188"
---
# <a name="imapiformcontainer--iunknown"></a><span data-ttu-id="7caca-103">IMAPIFormContainer : IUnknown</span><span class="sxs-lookup"><span data-stu-id="7caca-103">IMAPIFormContainer : IUnknown</span></span>

  
  
<span data-ttu-id="7caca-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7caca-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7caca-105">Gère les formulaires dans les bibliothèques de formulaires.</span><span class="sxs-lookup"><span data-stu-id="7caca-105">Manages forms in form libraries.</span></span> <span data-ttu-id="7caca-106">Cette interface est utilisée pour créer des bibliothèques de formulaires propres à l'application.</span><span class="sxs-lookup"><span data-stu-id="7caca-106">This interface is used to create application-specific form libraries.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="7caca-107">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="7caca-107">Header file:</span></span>  <br/> |<span data-ttu-id="7caca-108">MAPIForm. h</span><span class="sxs-lookup"><span data-stu-id="7caca-108">Mapiform.h</span></span>  <br/> |
|<span data-ttu-id="7caca-109">Exposé par:</span><span class="sxs-lookup"><span data-stu-id="7caca-109">Exposed by:</span></span>  <br/> |<span data-ttu-id="7caca-110">Objets conteneur de formulaire</span><span class="sxs-lookup"><span data-stu-id="7caca-110">Form container objects</span></span>  <br/> |
|<span data-ttu-id="7caca-111">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="7caca-111">Implemented by:</span></span>  <br/> |<span data-ttu-id="7caca-112">Fournisseurs de bibliothèques de formulaires</span><span class="sxs-lookup"><span data-stu-id="7caca-112">Form library providers</span></span>  <br/> |
|<span data-ttu-id="7caca-113">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="7caca-113">Called by:</span></span>  <br/> |<span data-ttu-id="7caca-114">Applications clientes</span><span class="sxs-lookup"><span data-stu-id="7caca-114">Client applications</span></span>  <br/> |
|<span data-ttu-id="7caca-115">Identificateur de l'interface:</span><span class="sxs-lookup"><span data-stu-id="7caca-115">Interface identifier:</span></span>  <br/> |<span data-ttu-id="7caca-116">IID_IMAPIFormContainer</span><span class="sxs-lookup"><span data-stu-id="7caca-116">IID_IMAPIFormContainer</span></span>  <br/> |
|<span data-ttu-id="7caca-117">Type de pointeur:</span><span class="sxs-lookup"><span data-stu-id="7caca-117">Pointer type:</span></span>  <br/> |<span data-ttu-id="7caca-118">LPMAPIFORMCONTAINER</span><span class="sxs-lookup"><span data-stu-id="7caca-118">LPMAPIFORMCONTAINER</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="7caca-119">Ordre vtable</span><span class="sxs-lookup"><span data-stu-id="7caca-119">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="7caca-120">InstallForm</span><span class="sxs-lookup"><span data-stu-id="7caca-120">InstallForm</span></span>](imapiformcontainer-installform.md) <br/> |<span data-ttu-id="7caca-121">Installe un formulaire dans un conteneur de formulaire.</span><span class="sxs-lookup"><span data-stu-id="7caca-121">Installs a form into a form container.</span></span>  <br/> |
|[<span data-ttu-id="7caca-122">RemoveForm</span><span class="sxs-lookup"><span data-stu-id="7caca-122">RemoveForm</span></span>](imapiformcontainer-removeform.md) <br/> |<span data-ttu-id="7caca-123">Supprime un formulaire particulier d'un conteneur de formulaires.</span><span class="sxs-lookup"><span data-stu-id="7caca-123">Removes a particular form from a form container.</span></span>  <br/> |
|[<span data-ttu-id="7caca-124">ResolveMessageClass</span><span class="sxs-lookup"><span data-stu-id="7caca-124">ResolveMessageClass</span></span>](imapiformcontainer-resolvemessageclass.md) <br/> |<span data-ttu-id="7caca-125">Résout une classe de message en son formulaire dans un conteneur de formulaire et renvoie un objet d'informations de formulaire pour ce formulaire.</span><span class="sxs-lookup"><span data-stu-id="7caca-125">Resolves a message class to its form in a form container and returns a form information object for that form.</span></span>  <br/> |
|[<span data-ttu-id="7caca-126">ResolveMultipleMessageClasses</span><span class="sxs-lookup"><span data-stu-id="7caca-126">ResolveMultipleMessageClasses</span></span>](imapiformcontainer-resolvemultiplemessageclasses.md) <br/> |<span data-ttu-id="7caca-127">Résout un groupe de classes de message dans leurs formulaires dans un conteneur de formulaire et renvoie un tableau d'objets d'informations de formulaire pour ces formulaires.</span><span class="sxs-lookup"><span data-stu-id="7caca-127">Resolves a group of message classes to their forms in a form container and returns an array of form information objects for those forms.</span></span>  <br/> |
|[<span data-ttu-id="7caca-128">CalcFormPropSet</span><span class="sxs-lookup"><span data-stu-id="7caca-128">CalcFormPropSet</span></span>](imapiformcontainer-calcformpropset.md) <br/> |<span data-ttu-id="7caca-129">Renvoie un tableau des propriétés utilisées par tous les formulaires installés dans un conteneur de formulaire.</span><span class="sxs-lookup"><span data-stu-id="7caca-129">Returns an array of the properties used by all forms installed in a form container.</span></span>  <br/> |
|[<span data-ttu-id="7caca-130">GetDisplay</span><span class="sxs-lookup"><span data-stu-id="7caca-130">GetDisplay</span></span>](imapiformcontainer-getdisplay.md) <br/> |<span data-ttu-id="7caca-131">Renvoie le nom d'affichage d'un conteneur de formulaire.</span><span class="sxs-lookup"><span data-stu-id="7caca-131">Returns the display name of a form container.</span></span>  <br/> |
|[<span data-ttu-id="7caca-132">Généré</span><span class="sxs-lookup"><span data-stu-id="7caca-132">GetLastError</span></span>](imapiformcontainer-getlasterror.md) <br/> |<span data-ttu-id="7caca-133">Renvoie une structure [MAPIERROR](mapierror.md) contenant des informations sur l'erreur précédente qui s'est produite dans l'objet conteneur de formulaire.</span><span class="sxs-lookup"><span data-stu-id="7caca-133">Returns a [MAPIERROR](mapierror.md) structure containing information about the previous error occurring to the form container object.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="7caca-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7caca-134">See also</span></span>



[<span data-ttu-id="7caca-135">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="7caca-135">MAPI Interfaces</span></span>](mapi-interfaces.md)

