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
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 27db5f54f6a6feba77308a4a63fe4c16448550cb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784232"
---
# <a name="imscapabilitiesgetcapabilities"></a><span data-ttu-id="0d0d3-103">IMSCapabilities::GetCapabilities</span><span class="sxs-lookup"><span data-stu-id="0d0d3-103">IMSCapabilities::GetCapabilities</span></span>

  
  
<span data-ttu-id="0d0d3-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="0d0d3-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="0d0d3-105">Obtient des informations sur qu’une banque peut prendre en charge en fonction de la sélection spécifiée.</span><span class="sxs-lookup"><span data-stu-id="0d0d3-105">Gets information about what a store can support based on the specified selector.</span></span>
  
```cpp
ULONG GetCapabilities( 
MSCAP_SELECTOR mscapSelector 
);
```

## <a name="parameters"></a><span data-ttu-id="0d0d3-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0d0d3-106">Parameters</span></span>

 <span data-ttu-id="0d0d3-107">*mscapSelector*</span><span class="sxs-lookup"><span data-stu-id="0d0d3-107">*mscapSelector*</span></span> 
  
> <span data-ttu-id="0d0d3-108">[in] Sélecteur indiquant les fonctionnalités à renvoyer.</span><span class="sxs-lookup"><span data-stu-id="0d0d3-108">[in] Selector indicating which capabilities to return.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="0d0d3-109">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="0d0d3-109">Return value</span></span>

<span data-ttu-id="0d0d3-110">MSCAP_SECURE_FOLDER_HOMEPAGES</span><span class="sxs-lookup"><span data-stu-id="0d0d3-110">MSCAP_SECURE_FOLDER_HOMEPAGES</span></span>
  
> <span data-ttu-id="0d0d3-111">Prise en charge pour les pages d’accueil de dossier dans une banque par défaut.</span><span class="sxs-lookup"><span data-stu-id="0d0d3-111">Support for folder homepages in a non-default store.</span></span> <span data-ttu-id="0d0d3-112">Cela peut être renvoyé si **MSCAP_SEL_FOLDER** est spécifié dans *mscapSelector* .</span><span class="sxs-lookup"><span data-stu-id="0d0d3-112">This can be returned if **MSCAP_SEL_FOLDER** is specified in  *mscapSelector*  .</span></span> 
    
<span data-ttu-id="0d0d3-113">MSCAP_RES_ANNOTATION</span><span class="sxs-lookup"><span data-stu-id="0d0d3-113">MSCAP_RES_ANNOTATION</span></span>
  
> <span data-ttu-id="0d0d3-114">Si une restriction contient un argument non valide tel que les propriétés non valides, la banque d’informations ignore les arguments non valides et traite uniquement les arguments valides.</span><span class="sxs-lookup"><span data-stu-id="0d0d3-114">If a restriction contains any invalid arguments such as invalid properties, the store ignores the invalid arguments and processes only the valid arguments.</span></span> <span data-ttu-id="0d0d3-115">Cela peut être renvoyé si **MSCAP_SEL_RESTRICTION** est spécifié dans *mscapSelector* .</span><span class="sxs-lookup"><span data-stu-id="0d0d3-115">This can be returned if **MSCAP_SEL_RESTRICTION** is specified in  *mscapSelector*  .</span></span> 
    
<span data-ttu-id="0d0d3-116">NULL</span><span class="sxs-lookup"><span data-stu-id="0d0d3-116">NULL</span></span>
  
> <span data-ttu-id="0d0d3-117">Le magasin ne gère pas de fonction basée sur le sélecteur de donnée.</span><span class="sxs-lookup"><span data-stu-id="0d0d3-117">The store does not support any capability based on the given selector.</span></span>
    

