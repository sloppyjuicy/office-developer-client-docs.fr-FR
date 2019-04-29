---
title: IMSCapabilitiesGetCapabilities
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMSCapabilities.GetCapabilities
api_type:
- COM
ms.assetid: c77a8ef1-0730-d458-b35f-451d3f450fac
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: b76c55fd9ddc3aa7698f75aa6ce965544b2c9aae
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409257"
---
# <a name="imscapabilitiesgetcapabilities"></a><span data-ttu-id="a8165-103">IMSCapabilities::GetCapabilities</span><span class="sxs-lookup"><span data-stu-id="a8165-103">IMSCapabilities::GetCapabilities</span></span>

  
  
<span data-ttu-id="a8165-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a8165-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a8165-105">Obtient des informations sur ce qu'une banque peut prendre en charge en fonction du sélecteur spécifié.</span><span class="sxs-lookup"><span data-stu-id="a8165-105">Gets information about what a store can support based on the specified selector.</span></span>
  
```cpp
ULONG GetCapabilities( 
MSCAP_SELECTOR mscapSelector 
);
```

## <a name="parameters"></a><span data-ttu-id="a8165-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a8165-106">Parameters</span></span>

 <span data-ttu-id="a8165-107">*mscapSelector*</span><span class="sxs-lookup"><span data-stu-id="a8165-107">*mscapSelector*</span></span> 
  
> <span data-ttu-id="a8165-108">dans Sélecteur indiquant les fonctionnalités à renvoyer.</span><span class="sxs-lookup"><span data-stu-id="a8165-108">[in] Selector indicating which capabilities to return.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="a8165-109">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="a8165-109">Return value</span></span>

<span data-ttu-id="a8165-110">MSCAP_SECURE_FOLDER_HOMEPAGES</span><span class="sxs-lookup"><span data-stu-id="a8165-110">MSCAP_SECURE_FOLDER_HOMEPAGES</span></span>
  
> <span data-ttu-id="a8165-111">Prise en charge des page d'accueil de dossier dans une banque non définie par défaut.</span><span class="sxs-lookup"><span data-stu-id="a8165-111">Support for folder homepages in a non-default store.</span></span> <span data-ttu-id="a8165-112">Cela peut être renvoyé si **MSCAP_SEL_FOLDER** est spécifié dans *mscapSelector* .</span><span class="sxs-lookup"><span data-stu-id="a8165-112">This can be returned if **MSCAP_SEL_FOLDER** is specified in  *mscapSelector*  .</span></span> 
    
<span data-ttu-id="a8165-113">MSCAP_RES_ANNOTATION</span><span class="sxs-lookup"><span data-stu-id="a8165-113">MSCAP_RES_ANNOTATION</span></span>
  
> <span data-ttu-id="a8165-114">Si une restriction contient des arguments non valides, tels que des propriétés non valides, la Banque ignore les arguments non valides et traite uniquement les arguments valides.</span><span class="sxs-lookup"><span data-stu-id="a8165-114">If a restriction contains any invalid arguments such as invalid properties, the store ignores the invalid arguments and processes only the valid arguments.</span></span> <span data-ttu-id="a8165-115">Cela peut être renvoyé si **MSCAP_SEL_RESTRICTION** est spécifié dans *mscapSelector* .</span><span class="sxs-lookup"><span data-stu-id="a8165-115">This can be returned if **MSCAP_SEL_RESTRICTION** is specified in  *mscapSelector*  .</span></span> 
    
<span data-ttu-id="a8165-116">VALEURS</span><span class="sxs-lookup"><span data-stu-id="a8165-116">NULL</span></span>
  
> <span data-ttu-id="a8165-117">La Banque ne prend en charge aucune fonctionnalité basée sur le sélecteur donné.</span><span class="sxs-lookup"><span data-stu-id="a8165-117">The store does not support any capability based on the given selector.</span></span>
    

