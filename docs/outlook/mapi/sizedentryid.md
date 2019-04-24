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
ms.openlocfilehash: 88cf91330dea82dda490b81cc8de6fea0504baf7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32282683"
---
# <a name="sizedentryid"></a><span data-ttu-id="dd764-103">SizedENTRYID</span><span class="sxs-lookup"><span data-stu-id="dd764-103">SizedENTRYID</span></span>

<span data-ttu-id="dd764-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="dd764-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="dd764-105">Crée une structure [EntryID](entryid.md) nommée qui contient un membre **AB** d'une taille spécifiée.</span><span class="sxs-lookup"><span data-stu-id="dd764-105">Creates a named [ENTRYID](entryid.md) structure that contains an **ab** member of a specified size.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="dd764-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="dd764-106">Header file:</span></span>  <br/> |<span data-ttu-id="dd764-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="dd764-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="dd764-108">Structure associée:</span><span class="sxs-lookup"><span data-stu-id="dd764-108">Related structure:</span></span>  <br/> |<span data-ttu-id="dd764-109">**ENTRÉE**</span><span class="sxs-lookup"><span data-stu-id="dd764-109">**ENTRYID**</span></span> <br/> |
   
```cpp
SizedENTRYID (_cb, _name)
```

## <a name="parameters"></a><span data-ttu-id="dd764-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="dd764-110">Parameters</span></span>

<span data-ttu-id="dd764-111">__CB_</span><span class="sxs-lookup"><span data-stu-id="dd764-111">__cb_</span></span>
  
> <span data-ttu-id="dd764-112">Nombre d'octets dans le membre **AB** de la nouvelle structure.</span><span class="sxs-lookup"><span data-stu-id="dd764-112">Count of bytes in the **ab** member of the new structure.</span></span> 
    
<span data-ttu-id="dd764-113">__nom_</span><span class="sxs-lookup"><span data-stu-id="dd764-113">__name_</span></span>
  
> <span data-ttu-id="dd764-114">Nom de la nouvelle structure.</span><span class="sxs-lookup"><span data-stu-id="dd764-114">Name for the new structure.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="dd764-115">Remarques</span><span class="sxs-lookup"><span data-stu-id="dd764-115">Remarks</span></span>

<span data-ttu-id="dd764-116">La macro **SizedENTRYID** vous permet de définir un identificateur d'entrée après des exigences de longueur de tableau connues.</span><span class="sxs-lookup"><span data-stu-id="dd764-116">The **SizedENTRYID** macro lets you define an entry identifier after array length requirements are known.</span></span> <span data-ttu-id="dd764-117">Utilisez cette macro pour créer un identificateur d'entrée avec des limites explicites.</span><span class="sxs-lookup"><span data-stu-id="dd764-117">Use this macro to create an entry identifier with explicit bounds.</span></span> 
  
<span data-ttu-id="dd764-118">Pour utiliser la nouvelle structure qui résulte de la macro **SizedENTRYID** en tant que pointeur vers une structure **EntryID** , effectuez la conversion suivante:</span><span class="sxs-lookup"><span data-stu-id="dd764-118">To use the new structure that results from the **SizedENTRYID** macro as a pointer to an **ENTRYID** structure, perform the following cast:</span></span> 
  
```cpp
lpENTRYID = (LPENTRYID) &SizedENTRYID;

```

## <a name="see-also"></a><span data-ttu-id="dd764-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dd764-119">See also</span></span>

- [<span data-ttu-id="dd764-120">ENTRÉE</span><span class="sxs-lookup"><span data-stu-id="dd764-120">ENTRYID</span></span>](entryid.md)
- [<span data-ttu-id="dd764-121">Macros liées aux structures</span><span class="sxs-lookup"><span data-stu-id="dd764-121">Macros Related to Structures</span></span>](macros-related-to-structures.md)

