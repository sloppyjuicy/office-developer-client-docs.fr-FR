---
title: Utilisation de Macros pour la gestion des erreurs
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 351405ca-b72b-4e9e-bc8e-947344588970
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: c4e216f2204f4ee97d9eeac81f77ce6a82fff3f0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787445"
---
# <a name="using-macros-for-error-handling"></a><span data-ttu-id="7f423-103">Utilisation de Macros pour la gestion des erreurs</span><span class="sxs-lookup"><span data-stu-id="7f423-103">Using Macros for Error Handling</span></span>

  
  
<span data-ttu-id="7f423-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="7f423-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="7f423-105">Il existe plusieurs macros pour rendre plus facile d’utiliser des valeurs HRESULT.</span><span class="sxs-lookup"><span data-stu-id="7f423-105">There are several macros for making it easier to work with HRESULT values.</span></span>
  
<span data-ttu-id="7f423-106">Il existe deux jeux de macros de l’échec ou la réussite de test : HR_SUCCEEDED et HR_FAILED et a réussi et a échoué.</span><span class="sxs-lookup"><span data-stu-id="7f423-106">There are two sets of macros that test for failure or success: HR_SUCCEEDED and HR_FAILED and SUCCEEDED and FAILED.</span></span> <span data-ttu-id="7f423-107">A réussi est qu'identique à HR_SUCCEEDED et l’échec est identique à HR_FAILED.</span><span class="sxs-lookup"><span data-stu-id="7f423-107">SUCCEEDED is the same as HR_SUCCEEDED and FAILED is the same as HR_FAILED.</span></span>
  
<span data-ttu-id="7f423-108">Dans ce cas, utilisez la macro **ResultFromScode** pour définir la variable HRESULT à la valeur HRESULT de S_OK.</span><span class="sxs-lookup"><span data-stu-id="7f423-108">In this case, use the **ResultFromScode** macro to set the HRESULT variable to the corresponding HRESULT value for S_OK.</span></span> 
  
<span data-ttu-id="7f423-109">Macros couramment utilisés sont décrites brièvement dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="7f423-109">Commonly used macros are briefly described in the following table.</span></span>
  
|<span data-ttu-id="7f423-110">**Macro**</span><span class="sxs-lookup"><span data-stu-id="7f423-110">**Macro**</span></span>|<span data-ttu-id="7f423-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="7f423-111">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="7f423-112">**MAKE_HRESULT**</span><span class="sxs-lookup"><span data-stu-id="7f423-112">**MAKE_HRESULT**</span></span> <br/> |<span data-ttu-id="7f423-113">Construit une valeur HRESULT de ses composants.</span><span class="sxs-lookup"><span data-stu-id="7f423-113">Constructs an HRESULT from its components.</span></span>  <br/> |
|<span data-ttu-id="7f423-114">**HR_SUCCEEDED**</span><span class="sxs-lookup"><span data-stu-id="7f423-114">**HR_SUCCEEDED**</span></span> <br/> |<span data-ttu-id="7f423-115">Teste une valeur HRESULT pour un succès ou un avertissement.</span><span class="sxs-lookup"><span data-stu-id="7f423-115">Tests an HRESULT for a success or warning condition.</span></span>  <br/> |
|<span data-ttu-id="7f423-116">**HR_FAILED**</span><span class="sxs-lookup"><span data-stu-id="7f423-116">**HR_FAILED**</span></span> <br/> |<span data-ttu-id="7f423-117">Teste une valeur HRESULT pour une condition d’erreur.</span><span class="sxs-lookup"><span data-stu-id="7f423-117">Tests an HRESULT for an error condition.</span></span>  <br/> |
|<span data-ttu-id="7f423-118">**HRESULT_CODE**</span><span class="sxs-lookup"><span data-stu-id="7f423-118">**HRESULT_CODE**</span></span> <br/> |<span data-ttu-id="7f423-119">Extrait la partie de code d’erreur de HRESULT.</span><span class="sxs-lookup"><span data-stu-id="7f423-119">Extracts the error code part of the HRESULT.</span></span>  <br/> |
|<span data-ttu-id="7f423-120">**HRESULT_FACILITY**</span><span class="sxs-lookup"><span data-stu-id="7f423-120">**HRESULT_FACILITY**</span></span> <br/> |<span data-ttu-id="7f423-121">Extrait la facilité de HRESULT.</span><span class="sxs-lookup"><span data-stu-id="7f423-121">Extracts the facility from the HRESULT.</span></span>  <br/> |
|<span data-ttu-id="7f423-122">**HRESULT_SEVERITY**</span><span class="sxs-lookup"><span data-stu-id="7f423-122">**HRESULT_SEVERITY**</span></span> <br/> |<span data-ttu-id="7f423-123">Extrait le bit gravité la gravité.</span><span class="sxs-lookup"><span data-stu-id="7f423-123">Extracts the severity bit from the SEVERITY.</span></span>  <br/> |
|<span data-ttu-id="7f423-124">**A RÉUSSI**</span><span class="sxs-lookup"><span data-stu-id="7f423-124">**SUCCEEDED**</span></span> <br/> |<span data-ttu-id="7f423-125">Teste une valeur HRESULT pour un succès ou un avertissement.</span><span class="sxs-lookup"><span data-stu-id="7f423-125">Tests an HRESULT for a success or warning condition.</span></span>  <br/> |
|<span data-ttu-id="7f423-126">**A ÉCHOUÉ**</span><span class="sxs-lookup"><span data-stu-id="7f423-126">**FAILED**</span></span> <br/> |<span data-ttu-id="7f423-127">Teste une valeur HRESULT pour une condition d’erreur.</span><span class="sxs-lookup"><span data-stu-id="7f423-127">Tests an HRESULT for an error condition.</span></span>  <br/> |
   

