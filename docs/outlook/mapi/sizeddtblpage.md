---
title: SizedDtblPage
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SizedDtblPage
api_type:
- COM
ms.assetid: 47b2a69d-e902-429f-8b31-166b51aeaf7f
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: f14b8d7a9a73997f797f9cfa26a2e574222e839e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32282656"
---
# <a name="sizeddtblpage"></a><span data-ttu-id="6213b-103">SizedDtblPage</span><span class="sxs-lookup"><span data-stu-id="6213b-103">SizedDtblPage</span></span>

<span data-ttu-id="6213b-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6213b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6213b-105">Crée une structure nommée qui inclut une structure [DTBLPAGE](dtblpage.md) pour la description d'un contrôle de page à onglets, une étiquette d'une longueur spécifiée et une entrée de fichier d'aide d'une longueur spécifiée.</span><span class="sxs-lookup"><span data-stu-id="6213b-105">Creates a named structure that includes a [DTBLPAGE](dtblpage.md) structure for describing a tabbed page control, a label of a specified length, and a Help file entry of a specified length.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="6213b-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="6213b-106">Header file:</span></span>  <br/> |<span data-ttu-id="6213b-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="6213b-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="6213b-108">Structure associée:</span><span class="sxs-lookup"><span data-stu-id="6213b-108">Related structure:</span></span>  <br/> |<span data-ttu-id="6213b-109">**DTBLPAGE**</span><span class="sxs-lookup"><span data-stu-id="6213b-109">**DTBLPAGE**</span></span> <br/> |
   
```cpp
SizedDtblPage (n, n1, u)
```

## <a name="parameters"></a><span data-ttu-id="6213b-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6213b-110">Parameters</span></span>

<span data-ttu-id="6213b-111">_n_</span><span class="sxs-lookup"><span data-stu-id="6213b-111">_n_</span></span>
  
> <span data-ttu-id="6213b-112">Longueur de l'étiquette de l'onglet de page.</span><span class="sxs-lookup"><span data-stu-id="6213b-112">Length of the label for the page tab.</span></span>
    
<span data-ttu-id="6213b-113">_N1_</span><span class="sxs-lookup"><span data-stu-id="6213b-113">_n1_</span></span>
  
> <span data-ttu-id="6213b-114">Longueur de l'entrée apparaissant dans le fichier MAPISVC. inf identifiant le fichier d'aide qui sera utilisé avec le contrôle de page à onglets.</span><span class="sxs-lookup"><span data-stu-id="6213b-114">Length of the entry appearing in the Mapisvc.inf file identifying the Help file that will be used with the tabbed page control.</span></span>
    
<span data-ttu-id="6213b-115">_u_</span><span class="sxs-lookup"><span data-stu-id="6213b-115">_u_</span></span>
  
> <span data-ttu-id="6213b-116">Nom de la nouvelle structure.</span><span class="sxs-lookup"><span data-stu-id="6213b-116">Name for the new structure.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="6213b-117">Remarques</span><span class="sxs-lookup"><span data-stu-id="6213b-117">Remarks</span></span>

<span data-ttu-id="6213b-118">La macro **SizedDtblPage** vous permet de définir un contrôle de page à onglets lorsque le nombre de caractères dans l'étiquette associée et l'entrée de fichier d'aide est connu.</span><span class="sxs-lookup"><span data-stu-id="6213b-118">The **SizedDtblPage** macro lets you define a tabbed page control when the number of characters in the associated label and Help file entry is known.</span></span> <span data-ttu-id="6213b-119">La nouvelle structure est créée avec les membres suivants:</span><span class="sxs-lookup"><span data-stu-id="6213b-119">The new structure is created with the following members:</span></span> 
  
```cpp
DTBLPAGE dtblpage;
TCHAR lpszLabel[n];
TCHAR lpszComponent[n1];
```

<span data-ttu-id="6213b-120">Pour utiliser un pointeur vers la structure obtenue à partir de la macro **SizedDtblPage** en tant que pointeur de structure **DTBLPAGE** , effectuez la conversion suivante:</span><span class="sxs-lookup"><span data-stu-id="6213b-120">To use a pointer to the resulting structure from the **SizedDtblPage** macro as a **DTBLPAGE** structure pointer, perform the following cast:</span></span> 
  
```cpp
lpDtblPage = (LPDTBLPAGE) &SizedDtblPage;
```

## <a name="see-also"></a><span data-ttu-id="6213b-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6213b-121">See also</span></span>

- [<span data-ttu-id="6213b-122">DTBLPAGE</span><span class="sxs-lookup"><span data-stu-id="6213b-122">DTBLPAGE</span></span>](dtblpage.md)
- [<span data-ttu-id="6213b-123">Macros liées aux structures</span><span class="sxs-lookup"><span data-stu-id="6213b-123">Macros Related to Structures</span></span>](macros-related-to-structures.md)

