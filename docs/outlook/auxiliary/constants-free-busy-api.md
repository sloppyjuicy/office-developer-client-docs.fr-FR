---
title: Constantes (API de disponibilité)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: ff756bf1-9395-5e50-4f55-1eb0365a84ed
description: Cette rubrique contient des définitions de constantes, des identificateurs de classe et des identificateurs d'interface pour l'API de disponibilité.
ms.openlocfilehash: 13578617eaab45e7194d7a0d4d6995ef925e7f20
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317716"
---
# <a name="constants-freebusy-api"></a><span data-ttu-id="5fc73-103">Constantes (API de disponibilité)</span><span class="sxs-lookup"><span data-stu-id="5fc73-103">Constants (Free/busy API)</span></span>

<span data-ttu-id="5fc73-104">Cette rubrique contient des définitions de constantes, des identificateurs de classe et des identificateurs d'interface pour l'API de disponibilité.</span><span class="sxs-lookup"><span data-stu-id="5fc73-104">This topic contains constant definitions, class identifiers, and interface identifiers for the Free/Busy API.</span></span>
  
## <a name="constants"></a><span data-ttu-id="5fc73-105">Constantes</span><span class="sxs-lookup"><span data-stu-id="5fc73-105">Constants</span></span>

|<span data-ttu-id="5fc73-106">**Constante**</span><span class="sxs-lookup"><span data-stu-id="5fc73-106">**Constant**</span></span>|<span data-ttu-id="5fc73-107">**Définition**</span><span class="sxs-lookup"><span data-stu-id="5fc73-107">**Definition**</span></span>|
|:-----|:-----|
|<span data-ttu-id="5fc73-108">E_NOTIMPL</span><span class="sxs-lookup"><span data-stu-id="5fc73-108">E_NOTIMPL</span></span>  <br/> | <span data-ttu-id="5fc73-109">*Tel que défini dans le fichier d'en-tête du kit de développement logiciel (SDK) de Microsoft Windows winerror. h.*</span><span class="sxs-lookup"><span data-stu-id="5fc73-109">*As defined in the Microsoft Windows Software Development Kit (SDK) header file winerror.h.*</span></span>  <br/> |
|<span data-ttu-id="5fc73-110">STANDARD</span><span class="sxs-lookup"><span data-stu-id="5fc73-110">E_OUTOFMEMORY</span></span>  <br/> | <span data-ttu-id="5fc73-111">*Comme défini dans le fichier d'en-tête winerror. h du kit de développement logiciel (SDK) Windows.*</span><span class="sxs-lookup"><span data-stu-id="5fc73-111">*As defined in the Windows SDK header file winerror.h.*</span></span>  <br/> |
|<span data-ttu-id="5fc73-112">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="5fc73-112">S_FALSE</span></span>  <br/> | <span data-ttu-id="5fc73-113">*Comme défini dans le fichier d'en-tête winerror. h du kit de développement logiciel (SDK) Windows.*</span><span class="sxs-lookup"><span data-stu-id="5fc73-113">*As defined in the Windows SDK header file winerror.h.*</span></span>  <br/> |
|<span data-ttu-id="5fc73-114">S_OK</span><span class="sxs-lookup"><span data-stu-id="5fc73-114">S_OK</span></span>  <br/> | <span data-ttu-id="5fc73-115">*Comme défini dans le fichier d'en-tête winerror. h du kit de développement logiciel (SDK) Windows.*</span><span class="sxs-lookup"><span data-stu-id="5fc73-115">*As defined in the Windows SDK header file winerror.h.*</span></span>  <br/> |
   
## <a name="interface-identifiers"></a><span data-ttu-id="5fc73-116">Identificateurs d’interface</span><span class="sxs-lookup"><span data-stu-id="5fc73-116">Interface identifiers</span></span>

<span data-ttu-id="5fc73-117">Pour les identificateurs d'interface suivants, supposons que la macro DEFINE_GUID définie dans le fichier d'en-tête du kit de développement logiciel (SDK) Windows guiddef. h associe le nom symbolique du GUID à sa valeur.</span><span class="sxs-lookup"><span data-stu-id="5fc73-117">For the following interface identifiers, assume the DEFINE_GUID macro defined in the Windows SDK header file guiddef.h to associate the GUID symbolic name with its value.</span></span>
  
<span data-ttu-id="5fc73-118">{00067064-0000-0000-C000-000000000046}</span><span class="sxs-lookup"><span data-stu-id="5fc73-118">//{00067064-0000-0000-C000-000000000046}</span></span>
  
<span data-ttu-id="5fc73-119">DEFINE_GUID (IID_IEnumFBBlock, 0x00067064, 0x0, 0x0, 0xC0, 0x0, 0x0, 0x0, 0x0, 0x0, 0x0, 0x46);</span><span class="sxs-lookup"><span data-stu-id="5fc73-119">DEFINE_GUID(IID_IEnumFBBlock, 0x00067064, 0x0, 0x0, 0xc0, 0x0, 0x0, 0x0, 0x0, 0x0, 0x0, 0x46);</span></span>
  
<span data-ttu-id="5fc73-120">{00067066-0000-0000-C000-000000000046}</span><span class="sxs-lookup"><span data-stu-id="5fc73-120">//{00067066-0000-0000-C000-000000000046}</span></span>
  
<span data-ttu-id="5fc73-121">DEFINE_GUID (IID_IFreeBusyData, 0x00067066, 0x0, 0x0, 0xC0, 0x0, 0x0, 0x0, 0x0, 0x0, 0x0, 0x46);</span><span class="sxs-lookup"><span data-stu-id="5fc73-121">DEFINE_GUID(IID_IFreeBusyData, 0x00067066, 0x0, 0x0, 0xc0, 0x0, 0x0, 0x0, 0x0, 0x0, 0x0, 0x46);</span></span>
  
<span data-ttu-id="5fc73-122">{00067067-0000-0000-C000-000000000046}</span><span class="sxs-lookup"><span data-stu-id="5fc73-122">//{00067067-0000-0000-C000-000000000046}</span></span>
  
<span data-ttu-id="5fc73-123">DEFINE_GUID (IID_IFreeBusySupport, 0x00067067, 0x0, 0x0, 0xC0, 0x0, 0x0, 0x0, 0x0, 0x0, 0x0, 0x46);</span><span class="sxs-lookup"><span data-stu-id="5fc73-123">DEFINE_GUID(IID_IFreeBusySupport, 0x00067067, 0x0, 0x0, 0xc0, 0x0, 0x0, 0x0, 0x0, 0x0, 0x0, 0x46);</span></span>
  

