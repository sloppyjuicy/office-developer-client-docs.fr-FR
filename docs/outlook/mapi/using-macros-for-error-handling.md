---
title: Utilisation de macros pour la gestion des erreurs
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 351405ca-b72b-4e9e-bc8e-947344588970
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 9e6901d6583e7a7924a4a7c19c0a262bcef74bd3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435564"
---
# <a name="using-macros-for-error-handling"></a><span data-ttu-id="66291-103">Utilisation de macros pour la gestion des erreurs</span><span class="sxs-lookup"><span data-stu-id="66291-103">Using Macros for Error Handling</span></span>

  
  
<span data-ttu-id="66291-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="66291-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="66291-105">Il existe plusieurs macros qui facilitent l’emploi des valeurs HRESULT.</span><span class="sxs-lookup"><span data-stu-id="66291-105">There are several macros for making it easier to work with HRESULT values.</span></span>
  
<span data-ttu-id="66291-106">Il existe deux ensembles de macros qui testent l’échec ou la réussite : HR_SUCCEEDED et HR_FAILED et SUCCEEDED et FAILED.</span><span class="sxs-lookup"><span data-stu-id="66291-106">There are two sets of macros that test for failure or success: HR_SUCCEEDED and HR_FAILED and SUCCEEDED and FAILED.</span></span> <span data-ttu-id="66291-107">SUCCEEDED est identique à HR_SUCCEEDED et FAILED est identique à HR_FAILED.</span><span class="sxs-lookup"><span data-stu-id="66291-107">SUCCEEDED is the same as HR_SUCCEEDED and FAILED is the same as HR_FAILED.</span></span>
  
<span data-ttu-id="66291-108">Dans ce cas, utilisez la macro **ResultFromScode** pour définir la variable HRESULT sur la valeur HRESULT correspondante pour S_OK.</span><span class="sxs-lookup"><span data-stu-id="66291-108">In this case, use the **ResultFromScode** macro to set the HRESULT variable to the corresponding HRESULT value for S_OK.</span></span> 
  
<span data-ttu-id="66291-109">Les macros couramment utilisées sont brièvement décrites dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="66291-109">Commonly used macros are briefly described in the following table.</span></span>
  
|<span data-ttu-id="66291-110">**Macro**</span><span class="sxs-lookup"><span data-stu-id="66291-110">**Macro**</span></span>|<span data-ttu-id="66291-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="66291-111">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="66291-112">**MAKE_HRESULT**</span><span class="sxs-lookup"><span data-stu-id="66291-112">**MAKE_HRESULT**</span></span> <br/> |<span data-ttu-id="66291-113">Construit un HRESULT à partir de ses composants.</span><span class="sxs-lookup"><span data-stu-id="66291-113">Constructs an HRESULT from its components.</span></span>  <br/> |
|<span data-ttu-id="66291-114">**HR_SUCCEEDED**</span><span class="sxs-lookup"><span data-stu-id="66291-114">**HR_SUCCEEDED**</span></span> <br/> |<span data-ttu-id="66291-115">Teste un HRESULT pour une condition de réussite ou d’avertissement.</span><span class="sxs-lookup"><span data-stu-id="66291-115">Tests an HRESULT for a success or warning condition.</span></span>  <br/> |
|<span data-ttu-id="66291-116">**HR_FAILED**</span><span class="sxs-lookup"><span data-stu-id="66291-116">**HR_FAILED**</span></span> <br/> |<span data-ttu-id="66291-117">Teste une condition d’erreur HRESULT.</span><span class="sxs-lookup"><span data-stu-id="66291-117">Tests an HRESULT for an error condition.</span></span>  <br/> |
|<span data-ttu-id="66291-118">**HRESULT_CODE**</span><span class="sxs-lookup"><span data-stu-id="66291-118">**HRESULT_CODE**</span></span> <br/> |<span data-ttu-id="66291-119">Extrait la partie code d’erreur du HRESULT.</span><span class="sxs-lookup"><span data-stu-id="66291-119">Extracts the error code part of the HRESULT.</span></span>  <br/> |
|<span data-ttu-id="66291-120">**HRESULT_FACILITY**</span><span class="sxs-lookup"><span data-stu-id="66291-120">**HRESULT_FACILITY**</span></span> <br/> |<span data-ttu-id="66291-121">Extrait la fonction du HRESULT.</span><span class="sxs-lookup"><span data-stu-id="66291-121">Extracts the facility from the HRESULT.</span></span>  <br/> |
|<span data-ttu-id="66291-122">**HRESULT_SEVERITY**</span><span class="sxs-lookup"><span data-stu-id="66291-122">**HRESULT_SEVERITY**</span></span> <br/> |<span data-ttu-id="66291-123">Extrait le bit de gravité de la GRAVITÉ.</span><span class="sxs-lookup"><span data-stu-id="66291-123">Extracts the severity bit from the SEVERITY.</span></span>  <br/> |
|<span data-ttu-id="66291-124">**SUCCEEDED**</span><span class="sxs-lookup"><span data-stu-id="66291-124">**SUCCEEDED**</span></span> <br/> |<span data-ttu-id="66291-125">Teste un HRESULT pour une condition de réussite ou d’avertissement.</span><span class="sxs-lookup"><span data-stu-id="66291-125">Tests an HRESULT for a success or warning condition.</span></span>  <br/> |
|<span data-ttu-id="66291-126">**FAILED**</span><span class="sxs-lookup"><span data-stu-id="66291-126">**FAILED**</span></span> <br/> |<span data-ttu-id="66291-127">Teste une condition d’erreur HRESULT.</span><span class="sxs-lookup"><span data-stu-id="66291-127">Tests an HRESULT for an error condition.</span></span>  <br/> |
   

