---
title: CheckParms
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.CheckParms
api_type:
- COM
ms.assetid: 328f12f0-e4e7-407f-8eb8-0d4bf543962d
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: e7a4fde57515f0b8a41b9acf4adb01dd177a7a19
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783037"
---
# <a name="checkparms"></a><span data-ttu-id="8fa07-103">CheckParms</span><span class="sxs-lookup"><span data-stu-id="8fa07-103">CheckParms</span></span>

  
  
<span data-ttu-id="8fa07-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="8fa07-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="8fa07-105">Appelle une fonction interne pour valider les paramètres de débogage sur les méthodes de fournisseur de service appelées par MAPI.</span><span class="sxs-lookup"><span data-stu-id="8fa07-105">Calls an internal function to validate debugging parameters on service provider methods called by MAPI.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="8fa07-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="8fa07-106">Header file:</span></span>  <br/> |<span data-ttu-id="8fa07-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="8fa07-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="8fa07-108">Implémentée par :</span><span class="sxs-lookup"><span data-stu-id="8fa07-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="8fa07-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="8fa07-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="8fa07-110">Appelée par :</span><span class="sxs-lookup"><span data-stu-id="8fa07-110">Called by:</span></span>  <br/> |<span data-ttu-id="8fa07-111">Fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="8fa07-111">Service providers</span></span>  <br/> |
   
```cpp
HRESULT CheckParms(
  METHODS eMethod,
  LPVOID First
);
```

## <a name="parameters"></a><span data-ttu-id="8fa07-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8fa07-112">Parameters</span></span>

 <span data-ttu-id="8fa07-113">_eMethod_</span><span class="sxs-lookup"><span data-stu-id="8fa07-113">_eMethod_</span></span>
  
> <span data-ttu-id="8fa07-114">[in] Spécifie, par l’énumération, la méthode à valider.</span><span class="sxs-lookup"><span data-stu-id="8fa07-114">[in] Specifies, by enumeration, the method to validate.</span></span> 
    
 <span data-ttu-id="8fa07-115">_Premier_</span><span class="sxs-lookup"><span data-stu-id="8fa07-115">_First_</span></span>
  
> <span data-ttu-id="8fa07-116">[in] Pointeur vers le premier argument dans la pile.</span><span class="sxs-lookup"><span data-stu-id="8fa07-116">[in] Pointer to the first argument on the stack.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="8fa07-117">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="8fa07-117">Return value</span></span>

<span data-ttu-id="8fa07-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="8fa07-118">S_OK</span></span> 
  
> <span data-ttu-id="8fa07-119">L'appel a réussi.</span><span class="sxs-lookup"><span data-stu-id="8fa07-119">The call succeeded.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="8fa07-120">Remarques</span><span class="sxs-lookup"><span data-stu-id="8fa07-120">Remarks</span></span>

<span data-ttu-id="8fa07-121">Contrairement aux [ValidateParms](validateparms.md) et [UlValidateParms](ulvalidateparms.md) des macros, la macro **CheckParms** n’effectue pas une validation de paramètre complet.</span><span class="sxs-lookup"><span data-stu-id="8fa07-121">In contrast to the [ValidateParms](validateparms.md) and [UlValidateParms](ulvalidateparms.md) macros, the **CheckParms** macro does not perform a full parameter validation.</span></span> <span data-ttu-id="8fa07-122">Paramètres passés entre MAPI et service fournisseurs sont supposés soit correct **CheckParms** effectue une validation de débogage uniquement.</span><span class="sxs-lookup"><span data-stu-id="8fa07-122">Parameters passed between MAPI and service providers are assumed to be correct, so **CheckParms** performs a debug validation only.</span></span> 
  

