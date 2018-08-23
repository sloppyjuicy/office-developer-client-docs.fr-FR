---
title: Utilisation des macros pour la gestion des erreurs
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 351405ca-b72b-4e9e-bc8e-947344588970
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 715cd001c5eab89f40c31200a12deaf6981b9a61
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22567124"
---
# <a name="using-macros-for-error-handling"></a><span data-ttu-id="666ae-103">Utilisation des macros pour la gestion des erreurs</span><span class="sxs-lookup"><span data-stu-id="666ae-103">Using Macros for Error Handling</span></span>

  
  
<span data-ttu-id="666ae-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="666ae-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="666ae-105">Il existe plusieurs macros pour rendre plus facile d’utiliser des valeurs HRESULT.</span><span class="sxs-lookup"><span data-stu-id="666ae-105">There are several macros for making it easier to work with HRESULT values.</span></span>
  
<span data-ttu-id="666ae-106">Il existe deux jeux de macros de l’échec ou la réussite de test : HR_SUCCEEDED et HR_FAILED et a réussi et a échoué.</span><span class="sxs-lookup"><span data-stu-id="666ae-106">There are two sets of macros that test for failure or success: HR_SUCCEEDED and HR_FAILED and SUCCEEDED and FAILED.</span></span> <span data-ttu-id="666ae-107">A réussi est qu'identique à HR_SUCCEEDED et l’échec est identique à HR_FAILED.</span><span class="sxs-lookup"><span data-stu-id="666ae-107">SUCCEEDED is the same as HR_SUCCEEDED and FAILED is the same as HR_FAILED.</span></span>
  
<span data-ttu-id="666ae-108">Dans ce cas, utilisez la macro **ResultFromScode** pour définir la variable HRESULT à la valeur HRESULT de S_OK.</span><span class="sxs-lookup"><span data-stu-id="666ae-108">In this case, use the **ResultFromScode** macro to set the HRESULT variable to the corresponding HRESULT value for S_OK.</span></span> 
  
<span data-ttu-id="666ae-109">Macros couramment utilisés sont décrites brièvement dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="666ae-109">Commonly used macros are briefly described in the following table.</span></span>
  
|<span data-ttu-id="666ae-110">**Macro**</span><span class="sxs-lookup"><span data-stu-id="666ae-110">**Macro**</span></span>|<span data-ttu-id="666ae-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="666ae-111">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="666ae-112">**MAKE_HRESULT**</span><span class="sxs-lookup"><span data-stu-id="666ae-112">**MAKE_HRESULT**</span></span> <br/> |<span data-ttu-id="666ae-113">Construit une valeur HRESULT de ses composants.</span><span class="sxs-lookup"><span data-stu-id="666ae-113">Constructs an HRESULT from its components.</span></span>  <br/> |
|<span data-ttu-id="666ae-114">**HR_SUCCEEDED**</span><span class="sxs-lookup"><span data-stu-id="666ae-114">**HR_SUCCEEDED**</span></span> <br/> |<span data-ttu-id="666ae-115">Teste une valeur HRESULT pour un succès ou un avertissement.</span><span class="sxs-lookup"><span data-stu-id="666ae-115">Tests an HRESULT for a success or warning condition.</span></span>  <br/> |
|<span data-ttu-id="666ae-116">**HR_FAILED**</span><span class="sxs-lookup"><span data-stu-id="666ae-116">**HR_FAILED**</span></span> <br/> |<span data-ttu-id="666ae-117">Teste une valeur HRESULT pour une condition d’erreur.</span><span class="sxs-lookup"><span data-stu-id="666ae-117">Tests an HRESULT for an error condition.</span></span>  <br/> |
|<span data-ttu-id="666ae-118">**HRESULT_CODE**</span><span class="sxs-lookup"><span data-stu-id="666ae-118">**HRESULT_CODE**</span></span> <br/> |<span data-ttu-id="666ae-119">Extrait la partie de code d’erreur de HRESULT.</span><span class="sxs-lookup"><span data-stu-id="666ae-119">Extracts the error code part of the HRESULT.</span></span>  <br/> |
|<span data-ttu-id="666ae-120">**HRESULT_FACILITY**</span><span class="sxs-lookup"><span data-stu-id="666ae-120">**HRESULT_FACILITY**</span></span> <br/> |<span data-ttu-id="666ae-121">Extrait la facilité de HRESULT.</span><span class="sxs-lookup"><span data-stu-id="666ae-121">Extracts the facility from the HRESULT.</span></span>  <br/> |
|<span data-ttu-id="666ae-122">**HRESULT_SEVERITY**</span><span class="sxs-lookup"><span data-stu-id="666ae-122">**HRESULT_SEVERITY**</span></span> <br/> |<span data-ttu-id="666ae-123">Extrait le bit gravité la gravité.</span><span class="sxs-lookup"><span data-stu-id="666ae-123">Extracts the severity bit from the SEVERITY.</span></span>  <br/> |
|<span data-ttu-id="666ae-124">**A RÉUSSI**</span><span class="sxs-lookup"><span data-stu-id="666ae-124">**SUCCEEDED**</span></span> <br/> |<span data-ttu-id="666ae-125">Teste une valeur HRESULT pour un succès ou un avertissement.</span><span class="sxs-lookup"><span data-stu-id="666ae-125">Tests an HRESULT for a success or warning condition.</span></span>  <br/> |
|<span data-ttu-id="666ae-126">**A ÉCHOUÉ**</span><span class="sxs-lookup"><span data-stu-id="666ae-126">**FAILED**</span></span> <br/> |<span data-ttu-id="666ae-127">Teste une valeur HRESULT pour une condition d’erreur.</span><span class="sxs-lookup"><span data-stu-id="666ae-127">Tests an HRESULT for an error condition.</span></span>  <br/> |
   

