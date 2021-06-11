---
title: IMAPIProgress IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProgress
api_type:
- COM
ms.assetid: 7a872296-0378-456f-b4d6-cb4d96b09d6e
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 3a3d54ac9485cc3915d3606bb84b4f3191d1ca5b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419645"
---
# <a name="imapiprogress--iunknown"></a><span data-ttu-id="a2f2e-103">IMAPIProgress : IUnknown</span><span class="sxs-lookup"><span data-stu-id="a2f2e-103">IMAPIProgress : IUnknown</span></span>

  
  
<span data-ttu-id="a2f2e-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a2f2e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a2f2e-105">Implémente un objet de progression qui fournit aux applications clientes un indicateur de progression.</span><span class="sxs-lookup"><span data-stu-id="a2f2e-105">Implements a progress object that provides client applications with a progress indicator.</span></span> <span data-ttu-id="a2f2e-106">Un indicateur de progression est un affichage de l’interface utilisateur qui indique le pourcentage d’achèvement d’une opération, tel que la copie de dossiers entre les magasins de messages.</span><span class="sxs-lookup"><span data-stu-id="a2f2e-106">A progress indicator is a user-interface display that shows the percentage of completion of an operation, such as copying folders between message stores.</span></span> <span data-ttu-id="a2f2e-107">MapI et les applications clientes implémentent des objets de progression et les fournisseurs de services les utilisent.</span><span class="sxs-lookup"><span data-stu-id="a2f2e-107">MAPI and client applications implement progress objects and service providers use them.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a2f2e-108">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="a2f2e-108">Header file:</span></span>  <br/> |<span data-ttu-id="a2f2e-109">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a2f2e-109">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="a2f2e-110">Exposé par :</span><span class="sxs-lookup"><span data-stu-id="a2f2e-110">Exposed by:</span></span>  <br/> |<span data-ttu-id="a2f2e-111">Objets de progression</span><span class="sxs-lookup"><span data-stu-id="a2f2e-111">Progress objects</span></span>  <br/> |
|<span data-ttu-id="a2f2e-112">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="a2f2e-112">Implemented by:</span></span>  <br/> |<span data-ttu-id="a2f2e-113">MAPI et applications clientes</span><span class="sxs-lookup"><span data-stu-id="a2f2e-113">MAPI and client applications</span></span>  <br/> |
|<span data-ttu-id="a2f2e-114">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="a2f2e-114">Called by:</span></span>  <br/> |<span data-ttu-id="a2f2e-115">Fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="a2f2e-115">Service providers</span></span>  <br/> |
|<span data-ttu-id="a2f2e-116">Identificateur d’interface :</span><span class="sxs-lookup"><span data-stu-id="a2f2e-116">Interface identifier:</span></span>  <br/> |<span data-ttu-id="a2f2e-117">IID_IMAPIProgress</span><span class="sxs-lookup"><span data-stu-id="a2f2e-117">IID_IMAPIProgress</span></span>  <br/> |
|<span data-ttu-id="a2f2e-118">Type de pointeur :</span><span class="sxs-lookup"><span data-stu-id="a2f2e-118">Pointer type:</span></span>  <br/> |<span data-ttu-id="a2f2e-119">LPMAPIPROGRESS</span><span class="sxs-lookup"><span data-stu-id="a2f2e-119">LPMAPIPROGRESS</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="a2f2e-120">Ordre des vtables</span><span class="sxs-lookup"><span data-stu-id="a2f2e-120">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="a2f2e-121">Progress</span><span class="sxs-lookup"><span data-stu-id="a2f2e-121">Progress</span></span>](imapiprogress-progress.md) <br/> |<span data-ttu-id="a2f2e-122">Met à jour l’indicateur de progression avec un affichage de la progression à mesure qu’il est effectué vers la fin de l’opération.</span><span class="sxs-lookup"><span data-stu-id="a2f2e-122">Updates the progress indicator with a display of the progress as it is made toward completion of the operation.</span></span>  <br/> |
|[<span data-ttu-id="a2f2e-123">GetFlags</span><span class="sxs-lookup"><span data-stu-id="a2f2e-123">GetFlags</span></span>](imapiprogress-getflags.md) <br/> |<span data-ttu-id="a2f2e-124">Renvoie les paramètres d’indicateur de l’objet de progression pour le niveau d’opération sur lequel les informations de progression sont calculées.</span><span class="sxs-lookup"><span data-stu-id="a2f2e-124">Returns flag settings from the progress object for the level of operation on which progress information is calculated.</span></span>  <br/> |
|[<span data-ttu-id="a2f2e-125">GetMax</span><span class="sxs-lookup"><span data-stu-id="a2f2e-125">GetMax</span></span>](imapiprogress-getmax.md) <br/> |<span data-ttu-id="a2f2e-126">Renvoie le nombre maximal d’éléments dans l’opération pour lesquels les informations de progression sont affichées.</span><span class="sxs-lookup"><span data-stu-id="a2f2e-126">Returns the maximum number of items in the operation for which progress information is displayed.</span></span>  <br/> |
|[<span data-ttu-id="a2f2e-127">GetMin</span><span class="sxs-lookup"><span data-stu-id="a2f2e-127">GetMin</span></span>](imapiprogress-getmin.md) <br/> |<span data-ttu-id="a2f2e-128">Renvoie la valeur minimale dans la [méthode SetLimits](imapiprogress-setlimits.md) pour laquelle les informations de progression sont affichées.</span><span class="sxs-lookup"><span data-stu-id="a2f2e-128">Returns the minimum value in the [SetLimits](imapiprogress-setlimits.md) method for which progress information is displayed.</span></span>  <br/> |
|[<span data-ttu-id="a2f2e-129">SetLimits</span><span class="sxs-lookup"><span data-stu-id="a2f2e-129">SetLimits</span></span>](imapiprogress-setlimits.md) <br/> |<span data-ttu-id="a2f2e-130">Définit les limites inférieure et supérieure du nombre d’éléments dans l’opération, ainsi que les indicateurs qui contrôlent la façon dont les informations de progression sont calculées pour l’opération.</span><span class="sxs-lookup"><span data-stu-id="a2f2e-130">Sets the lower and upper limits for the number of items in the operation, and the flags that control how progress information is calculated for the operation.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a2f2e-131">Remarques</span><span class="sxs-lookup"><span data-stu-id="a2f2e-131">Remarks</span></span>

<span data-ttu-id="a2f2e-132">MAPI inclut  _un paramètre lpProgress_ dans de nombreuses méthodes qui effectuent des opérations potentiellement longues.</span><span class="sxs-lookup"><span data-stu-id="a2f2e-132">MAPI includes an  _lpProgress_ parameter in many of the methods that perform potentially lengthy operations.</span></span>  <span data-ttu-id="a2f2e-133">_LpProgress_ pointe vers une implémentation cliente d’un objet de progression.</span><span class="sxs-lookup"><span data-stu-id="a2f2e-133">_lpProgress_ points to a client implementation of a progress object.</span></span> <span data-ttu-id="a2f2e-134">Les clients qui implémentent **l’interface IMAPIProgress** définissent ce paramètre pour qu’il pointe vers leur implémentation ; les clients qui n’implémentent **pas IMAPIProgress** définissent le paramètre sur NULL.</span><span class="sxs-lookup"><span data-stu-id="a2f2e-134">Clients that implement the **IMAPIProgress** interface set this parameter to point to their implementation; clients that do not implement **IMAPIProgress** set the parameter to NULL.</span></span> <span data-ttu-id="a2f2e-135">Pour afficher un indicateur de progression pendant le traitement de l’opération, les fournisseurs de services utilisent l’objet de progression fourni par le client, s’il est disponible, ou une implémentation MAPI (indiquée lorsque  _lpProgress_ est définie sur NULL).</span><span class="sxs-lookup"><span data-stu-id="a2f2e-135">To display a progress indicator during processing of the operation, service providers use the progress object supplied by the client, if available, or a MAPI implementation (indicated when  _lpProgress_ is set to NULL).</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="a2f2e-136">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="a2f2e-136">MFCMAPI reference</span></span>

<span data-ttu-id="a2f2e-137">Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="a2f2e-137">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="a2f2e-138">**Files**</span><span class="sxs-lookup"><span data-stu-id="a2f2e-138">**Files**</span></span>|<span data-ttu-id="a2f2e-139">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="a2f2e-139">**Function**</span></span>|<span data-ttu-id="a2f2e-140">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="a2f2e-140">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="a2f2e-141">MapiProgress.h et MapiProgress.cpp</span><span class="sxs-lookup"><span data-stu-id="a2f2e-141">MapiProgress.h and MapiProgress.cpp</span></span>  <br/> |<span data-ttu-id="a2f2e-142">Non applicable</span><span class="sxs-lookup"><span data-stu-id="a2f2e-142">Not applicable</span></span>  <br/> |<span data-ttu-id="a2f2e-143">Si le paramètre IMAPIProgress est activé, MFCMAPI passe une implémentation **IMAPIProgress** à toutes les fonctions que MFCMAPI appelle et qui acceptent une implémentation.</span><span class="sxs-lookup"><span data-stu-id="a2f2e-143">If the IMAPIProgress setting is enabled, MFCMAPI will pass an **IMAPIProgress** implementation to all functions that MFCMAPI invokes that accept an implementation.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a2f2e-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a2f2e-144">See also</span></span>



[<span data-ttu-id="a2f2e-145">MFCMAPI comme un exemple de Code</span><span class="sxs-lookup"><span data-stu-id="a2f2e-145">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="a2f2e-146">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="a2f2e-146">MAPI Interfaces</span></span>](mapi-interfaces.md)

