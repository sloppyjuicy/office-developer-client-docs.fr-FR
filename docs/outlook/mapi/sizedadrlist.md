---
title: SizedADRLIST
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SizedADRLIST
api_type:
- COM
ms.assetid: 5c64d74a-83a7-4122-b1d1-fcca0f4a6cdb
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 62911e0dec15002f39fff81e8c517c1cb11d0183
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22574740"
---
# <a name="sizedadrlist"></a><span data-ttu-id="57d61-103">SizedADRLIST</span><span class="sxs-lookup"><span data-stu-id="57d61-103">SizedADRLIST</span></span>

<span data-ttu-id="57d61-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="57d61-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="57d61-105">Définit une structure [ADRLIST](adrlist.md) avec le nom spécifié qui contient un nombre spécifié de structures [ADRENTRY](adrentry.md) .</span><span class="sxs-lookup"><span data-stu-id="57d61-105">Defines an [ADRLIST](adrlist.md) structure with the specified name that contains a specified number of [ADRENTRY](adrentry.md) structures.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="57d61-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="57d61-106">Header file:</span></span>  <br/> |<span data-ttu-id="57d61-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="57d61-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="57d61-108">Structure connexe :</span><span class="sxs-lookup"><span data-stu-id="57d61-108">Related structure:</span></span>  <br/> |<span data-ttu-id="57d61-109">**ADRLIST**</span><span class="sxs-lookup"><span data-stu-id="57d61-109">**ADRLIST**</span></span> <br/> |
   
```cpp
SizedADRLIST (_centries,_name)
```

## <a name="parameters"></a><span data-ttu-id="57d61-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="57d61-110">Parameters</span></span>

<span data-ttu-id="57d61-111">__centries_</span><span class="sxs-lookup"><span data-stu-id="57d61-111">__centries_</span></span>
  
> <span data-ttu-id="57d61-112">Nombre de structures **ADRENTRY** à inclure dans la nouvelle structure **ADRLIST** .</span><span class="sxs-lookup"><span data-stu-id="57d61-112">Count of **ADRENTRY** structures to be included in the new **ADRLIST** structure.</span></span> 
    
<span data-ttu-id="57d61-113">__nom_</span><span class="sxs-lookup"><span data-stu-id="57d61-113">__name_</span></span>
  
> <span data-ttu-id="57d61-114">Nom de la nouvelle structure **ADRLIST** .</span><span class="sxs-lookup"><span data-stu-id="57d61-114">Name for the new **ADRLIST** structure.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="57d61-115">Remarques</span><span class="sxs-lookup"><span data-stu-id="57d61-115">Remarks</span></span>

<span data-ttu-id="57d61-116">La macro **SizedADRLIST** vous permet de définir une liste de destinataires qui a des limites explicites lorsque les besoins en matière de longueur de tableau.</span><span class="sxs-lookup"><span data-stu-id="57d61-116">The **SizedADRLIST** macro lets you define a recipient list that has explicit bounds when array length requirements are known.</span></span> <span data-ttu-id="57d61-117">Le code suivant montre comment convertir le résultat de la macro **SizedADRLIST** vers un pointeur de structure **ADRLIST** :</span><span class="sxs-lookup"><span data-stu-id="57d61-117">The following code shows how to cast the result of the **SizedADRLIST** macro to an **ADRLIST** structure pointer:</span></span> 
  
```cpp
lpADRList = (LPADRLIST) &SizedADRList;
```

## <a name="see-also"></a><span data-ttu-id="57d61-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="57d61-118">See also</span></span>

- [<span data-ttu-id="57d61-119">ADRLIST</span><span class="sxs-lookup"><span data-stu-id="57d61-119">ADRLIST</span></span>](adrlist.md)
- [<span data-ttu-id="57d61-120">ADRENTRY</span><span class="sxs-lookup"><span data-stu-id="57d61-120">ADRENTRY</span></span>](adrentry.md)
- [<span data-ttu-id="57d61-121">Macros liées aux structures</span><span class="sxs-lookup"><span data-stu-id="57d61-121">Macros Related to Structures</span></span>](macros-related-to-structures.md)

