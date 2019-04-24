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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: c35a1eb54b29c04bc8eed453272b59aae0ea737e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32282774"
---
# <a name="sizedadrlist"></a><span data-ttu-id="28138-103">SizedADRLIST</span><span class="sxs-lookup"><span data-stu-id="28138-103">SizedADRLIST</span></span>

<span data-ttu-id="28138-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="28138-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="28138-105">Définit une structure [ADRLIST](adrlist.md) avec le nom spécifié qui contient un nombre spécifié de structures [ADRENTRY](adrentry.md) .</span><span class="sxs-lookup"><span data-stu-id="28138-105">Defines an [ADRLIST](adrlist.md) structure with the specified name that contains a specified number of [ADRENTRY](adrentry.md) structures.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="28138-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="28138-106">Header file:</span></span>  <br/> |<span data-ttu-id="28138-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="28138-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="28138-108">Structure associée:</span><span class="sxs-lookup"><span data-stu-id="28138-108">Related structure:</span></span>  <br/> |<span data-ttu-id="28138-109">**ADRLIST**</span><span class="sxs-lookup"><span data-stu-id="28138-109">**ADRLIST**</span></span> <br/> |
   
```cpp
SizedADRLIST (_centries,_name)
```

## <a name="parameters"></a><span data-ttu-id="28138-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="28138-110">Parameters</span></span>

<span data-ttu-id="28138-111">__centries_</span><span class="sxs-lookup"><span data-stu-id="28138-111">__centries_</span></span>
  
> <span data-ttu-id="28138-112">Nombre de structures **ADRENTRY** à inclure dans la nouvelle structure **ADRLIST** .</span><span class="sxs-lookup"><span data-stu-id="28138-112">Count of **ADRENTRY** structures to be included in the new **ADRLIST** structure.</span></span> 
    
<span data-ttu-id="28138-113">__nom_</span><span class="sxs-lookup"><span data-stu-id="28138-113">__name_</span></span>
  
> <span data-ttu-id="28138-114">Nom de la nouvelle structure **ADRLIST** .</span><span class="sxs-lookup"><span data-stu-id="28138-114">Name for the new **ADRLIST** structure.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="28138-115">Remarques</span><span class="sxs-lookup"><span data-stu-id="28138-115">Remarks</span></span>

<span data-ttu-id="28138-116">La macro **SizedADRLIST** vous permet de définir une liste de destinataires qui contient des limites explicites lorsque les exigences de longueur de tableau sont connues.</span><span class="sxs-lookup"><span data-stu-id="28138-116">The **SizedADRLIST** macro lets you define a recipient list that has explicit bounds when array length requirements are known.</span></span> <span data-ttu-id="28138-117">Le code suivant montre comment convertir le résultat de la macro **SizedADRLIST** en pointeur de structure **ADRLIST** :</span><span class="sxs-lookup"><span data-stu-id="28138-117">The following code shows how to cast the result of the **SizedADRLIST** macro to an **ADRLIST** structure pointer:</span></span> 
  
```cpp
lpADRList = (LPADRLIST) &SizedADRList;
```

## <a name="see-also"></a><span data-ttu-id="28138-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="28138-118">See also</span></span>

- [<span data-ttu-id="28138-119">ADRLIST</span><span class="sxs-lookup"><span data-stu-id="28138-119">ADRLIST</span></span>](adrlist.md)
- [<span data-ttu-id="28138-120">ADRENTRY</span><span class="sxs-lookup"><span data-stu-id="28138-120">ADRENTRY</span></span>](adrentry.md)
- [<span data-ttu-id="28138-121">Macros liées aux structures</span><span class="sxs-lookup"><span data-stu-id="28138-121">Macros Related to Structures</span></span>](macros-related-to-structures.md)

