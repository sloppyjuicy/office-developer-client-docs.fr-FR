---
title: SizedENTRYID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SizedENTRYID
api_type:
- COM
ms.assetid: 491170af-db35-4d7e-a912-44ffe8c7506b
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 814cfeab61854469f460cc38f927b0e3723f6f0d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787172"
---
# <a name="sizedentryid"></a><span data-ttu-id="ab5a1-103">SizedENTRYID</span><span class="sxs-lookup"><span data-stu-id="ab5a1-103">SizedENTRYID</span></span>

<span data-ttu-id="ab5a1-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="ab5a1-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="ab5a1-105">Crée une structure [ENTRYID](entryid.md) nommée qui contient un membre de **Carnet d’adresses** d’une taille spécifiée.</span><span class="sxs-lookup"><span data-stu-id="ab5a1-105">Creates a named [ENTRYID](entryid.md) structure that contains an **ab** member of a specified size.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ab5a1-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="ab5a1-106">Header file:</span></span>  <br/> |<span data-ttu-id="ab5a1-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="ab5a1-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="ab5a1-108">Structure connexe :</span><span class="sxs-lookup"><span data-stu-id="ab5a1-108">Related structure:</span></span>  <br/> |<span data-ttu-id="ab5a1-109">**PROPRIÉTÉ ENTRYID**</span><span class="sxs-lookup"><span data-stu-id="ab5a1-109">**ENTRYID**</span></span> <br/> |
   
```cpp
SizedENTRYID (_cb, _name)
```

## <a name="parameters"></a><span data-ttu-id="ab5a1-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ab5a1-110">Parameters</span></span>

<span data-ttu-id="ab5a1-111">__cb_</span><span class="sxs-lookup"><span data-stu-id="ab5a1-111">__cb_</span></span>
  
> <span data-ttu-id="ab5a1-112">Nombre d’octets dans le membre de **Carnet d’adresses** de la nouvelle structure.</span><span class="sxs-lookup"><span data-stu-id="ab5a1-112">Count of bytes in the **ab** member of the new structure.</span></span> 
    
<span data-ttu-id="ab5a1-113">__nom_</span><span class="sxs-lookup"><span data-stu-id="ab5a1-113">__name_</span></span>
  
> <span data-ttu-id="ab5a1-114">Nom de la nouvelle structure.</span><span class="sxs-lookup"><span data-stu-id="ab5a1-114">Name for the new structure.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="ab5a1-115">Remarques</span><span class="sxs-lookup"><span data-stu-id="ab5a1-115">Remarks</span></span>

<span data-ttu-id="ab5a1-116">La macro **SizedENTRYID** vous permet de définir un identificateur d’entrée une fois que les besoins en matière de longueur de tableau.</span><span class="sxs-lookup"><span data-stu-id="ab5a1-116">The **SizedENTRYID** macro lets you define an entry identifier after array length requirements are known.</span></span> <span data-ttu-id="ab5a1-117">Utilisez cette macro pour créer un identificateur d’entrée avec des limites explicites.</span><span class="sxs-lookup"><span data-stu-id="ab5a1-117">Use this macro to create an entry identifier with explicit bounds.</span></span> 
  
<span data-ttu-id="ab5a1-118">Pour utiliser la nouvelle structure de résultats de la macro **SizedENTRYID** comme un pointeur vers une structure **ENTRYID** , effectuer le cast suivant :</span><span class="sxs-lookup"><span data-stu-id="ab5a1-118">To use the new structure that results from the **SizedENTRYID** macro as a pointer to an **ENTRYID** structure, perform the following cast:</span></span> 
  
```cpp
lpENTRYID = (LPENTRYID) &SizedENTRYID;

```

## <a name="see-also"></a><span data-ttu-id="ab5a1-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ab5a1-119">See also</span></span>

- [<span data-ttu-id="ab5a1-120">PROPRIÉTÉ ENTRYID</span><span class="sxs-lookup"><span data-stu-id="ab5a1-120">ENTRYID</span></span>](entryid.md)
- [<span data-ttu-id="ab5a1-121">Macros relatives aux Structures</span><span class="sxs-lookup"><span data-stu-id="ab5a1-121">Macros Related to Structures</span></span>](macros-related-to-structures.md)

