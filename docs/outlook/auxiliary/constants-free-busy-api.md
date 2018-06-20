---
title: Constantes (disponibilité API)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: ff756bf1-9395-5e50-4f55-1eb0365a84ed
description: Cette rubrique contient des définitions de constantes, les identificateurs de classe et les identificateurs d’interface pour l’API de disponibilité.
ms.openlocfilehash: ec909d449dc9075959fc9c047457577efd52ec3a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782555"
---
# <a name="constants-freebusy-api"></a><span data-ttu-id="d4b46-103">Constantes (disponibilité API)</span><span class="sxs-lookup"><span data-stu-id="d4b46-103">Constants (Free/busy API)</span></span>

<span data-ttu-id="d4b46-104">Cette rubrique contient des définitions de constantes, les identificateurs de classe et les identificateurs d’interface pour l’API de disponibilité.</span><span class="sxs-lookup"><span data-stu-id="d4b46-104">This topic contains constant definitions, class identifiers, and interface identifiers for the Free/Busy API.</span></span>
  
## <a name="constants"></a><span data-ttu-id="d4b46-105">Constants</span><span class="sxs-lookup"><span data-stu-id="d4b46-105">Constants</span></span>

|<span data-ttu-id="d4b46-106">**Constante**</span><span class="sxs-lookup"><span data-stu-id="d4b46-106">**Constant**</span></span>|<span data-ttu-id="d4b46-107">**Définition**</span><span class="sxs-lookup"><span data-stu-id="d4b46-107">**Definition**</span></span>|
|:-----|:-----|
|<span data-ttu-id="d4b46-108">E_NOTIMPL</span><span class="sxs-lookup"><span data-stu-id="d4b46-108">E_NOTIMPL</span></span>  <br/> | <span data-ttu-id="d4b46-109">*Comme défini dans le fichier d’en-tête winerror.h Kit de développement logiciel (SDK) de Microsoft Windows.*</span><span class="sxs-lookup"><span data-stu-id="d4b46-109">*As defined in the Microsoft Windows Software Development Kit (SDK) header file winerror.h.*</span></span>  <br/> |
|<span data-ttu-id="d4b46-110">E_OUTOFMEMORY</span><span class="sxs-lookup"><span data-stu-id="d4b46-110">E_OUTOFMEMORY</span></span>  <br/> | <span data-ttu-id="d4b46-111">*Comme défini dans le fichier d’en-tête winerror.h SDK de Windows.*</span><span class="sxs-lookup"><span data-stu-id="d4b46-111">*As defined in the Windows SDK header file winerror.h.*</span></span>  <br/> |
|<span data-ttu-id="d4b46-112">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="d4b46-112">S_FALSE</span></span>  <br/> | <span data-ttu-id="d4b46-113">*Comme défini dans le fichier d’en-tête winerror.h SDK de Windows.*</span><span class="sxs-lookup"><span data-stu-id="d4b46-113">*As defined in the Windows SDK header file winerror.h.*</span></span>  <br/> |
|<span data-ttu-id="d4b46-114">S_OK</span><span class="sxs-lookup"><span data-stu-id="d4b46-114">S_OK</span></span>  <br/> | <span data-ttu-id="d4b46-115">*Comme défini dans le fichier d’en-tête winerror.h SDK de Windows.*</span><span class="sxs-lookup"><span data-stu-id="d4b46-115">*As defined in the Windows SDK header file winerror.h.*</span></span>  <br/> |
   
## <a name="interface-identifiers"></a><span data-ttu-id="d4b46-116">Identificateurs d’interface</span><span class="sxs-lookup"><span data-stu-id="d4b46-116">Interface identifiers</span></span>

<span data-ttu-id="d4b46-117">Pour les identificateurs d’interface suivant, supposons que la macro DEFINE_GUID définie dans le guiddef.h de fichier d’en-tête SDK Windows pour associer le nom symbolique GUID à sa valeur.</span><span class="sxs-lookup"><span data-stu-id="d4b46-117">For the following interface identifiers, assume the DEFINE_GUID macro defined in the Windows SDK header file guiddef.h to associate the GUID symbolic name with its value.</span></span>
  
<span data-ttu-id="d4b46-118">{00067064-0000-0000-C000-000000000046}</span><span class="sxs-lookup"><span data-stu-id="d4b46-118">//{00067064-0000-0000-C000-000000000046}</span></span>
  
<span data-ttu-id="d4b46-119">DEFINE_GUID (IID_IEnumFBBlock, 0x00067064, 0 x 0, 0 x 0, 0xc0, 0 x 0, 0 x 0, 0 x 0, 0 x 0, 0 x 0, 0 x 0, 0 x 46) ;</span><span class="sxs-lookup"><span data-stu-id="d4b46-119">DEFINE_GUID(IID_IEnumFBBlock, 0x00067064, 0x0, 0x0, 0xc0, 0x0, 0x0, 0x0, 0x0, 0x0, 0x0, 0x46);</span></span>
  
<span data-ttu-id="d4b46-120">{00067066-0000-0000-C000-000000000046}</span><span class="sxs-lookup"><span data-stu-id="d4b46-120">//{00067066-0000-0000-C000-000000000046}</span></span>
  
<span data-ttu-id="d4b46-121">DEFINE_GUID (IID_IFreeBusyData, 0x00067066, 0 x 0, 0 x 0, 0xc0, 0 x 0, 0 x 0, 0 x 0, 0 x 0, 0 x 0, 0 x 0, 0 x 46) ;</span><span class="sxs-lookup"><span data-stu-id="d4b46-121">DEFINE_GUID(IID_IFreeBusyData, 0x00067066, 0x0, 0x0, 0xc0, 0x0, 0x0, 0x0, 0x0, 0x0, 0x0, 0x46);</span></span>
  
<span data-ttu-id="d4b46-122">{00067067-0000-0000-C000-000000000046}</span><span class="sxs-lookup"><span data-stu-id="d4b46-122">//{00067067-0000-0000-C000-000000000046}</span></span>
  
<span data-ttu-id="d4b46-123">DEFINE_GUID (IID_IFreeBusySupport, 0x00067067, 0 x 0, 0 x 0, 0xc0, 0 x 0, 0 x 0, 0 x 0, 0 x 0, 0 x 0, 0 x 0, 0 x 46) ;</span><span class="sxs-lookup"><span data-stu-id="d4b46-123">DEFINE_GUID(IID_IFreeBusySupport, 0x00067067, 0x0, 0x0, 0xc0, 0x0, 0x0, 0x0, 0x0, 0x0, 0x0, 0x46);</span></span>
  

