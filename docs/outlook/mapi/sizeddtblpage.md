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
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: ae3f84c6b219c7becb88737f0d6c9fcb9722ea34
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22584967"
---
# <a name="sizeddtblpage"></a><span data-ttu-id="fea6f-103">SizedDtblPage</span><span class="sxs-lookup"><span data-stu-id="fea6f-103">SizedDtblPage</span></span>

<span data-ttu-id="fea6f-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fea6f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fea6f-105">Crée une structure nommée qui inclut une structure [DTBLPAGE](dtblpage.md) pour la description d’un contrôle de la page à onglets, une étiquette d’une longueur spécifiée, une entrée de fichier d’aide d’une longueur spécifiée.</span><span class="sxs-lookup"><span data-stu-id="fea6f-105">Creates a named structure that includes a [DTBLPAGE](dtblpage.md) structure for describing a tabbed page control, a label of a specified length, and a Help file entry of a specified length.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="fea6f-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="fea6f-106">Header file:</span></span>  <br/> |<span data-ttu-id="fea6f-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="fea6f-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="fea6f-108">Structure connexe :</span><span class="sxs-lookup"><span data-stu-id="fea6f-108">Related structure:</span></span>  <br/> |<span data-ttu-id="fea6f-109">**DTBLPAGE**</span><span class="sxs-lookup"><span data-stu-id="fea6f-109">**DTBLPAGE**</span></span> <br/> |
   
```cpp
SizedDtblPage (n, n1, u)
```

## <a name="parameters"></a><span data-ttu-id="fea6f-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="fea6f-110">Parameters</span></span>

<span data-ttu-id="fea6f-111">_n_</span><span class="sxs-lookup"><span data-stu-id="fea6f-111">_n_</span></span>
  
> <span data-ttu-id="fea6f-112">Longueur de l’étiquette de l’onglet page.</span><span class="sxs-lookup"><span data-stu-id="fea6f-112">Length of the label for the page tab.</span></span>
    
<span data-ttu-id="fea6f-113">_N1_</span><span class="sxs-lookup"><span data-stu-id="fea6f-113">_n1_</span></span>
  
> <span data-ttu-id="fea6f-114">Longueur de l’entrée figurant dans le fichier Mapisvc.inf qui identifie le fichier d’aide qui sera utilisé avec le contrôle de la page à onglets.</span><span class="sxs-lookup"><span data-stu-id="fea6f-114">Length of the entry appearing in the Mapisvc.inf file identifying the Help file that will be used with the tabbed page control.</span></span>
    
<span data-ttu-id="fea6f-115">_u_</span><span class="sxs-lookup"><span data-stu-id="fea6f-115">_u_</span></span>
  
> <span data-ttu-id="fea6f-116">Nom de la nouvelle structure.</span><span class="sxs-lookup"><span data-stu-id="fea6f-116">Name for the new structure.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="fea6f-117">Remarques</span><span class="sxs-lookup"><span data-stu-id="fea6f-117">Remarks</span></span>

<span data-ttu-id="fea6f-118">La macro **SizedDtblPage** vous permet de définir un contrôle de la page à onglets lorsque le nombre de caractères dans l’étiquette associée et l’entrée de fichier d’aide est connu.</span><span class="sxs-lookup"><span data-stu-id="fea6f-118">The **SizedDtblPage** macro lets you define a tabbed page control when the number of characters in the associated label and Help file entry is known.</span></span> <span data-ttu-id="fea6f-119">La nouvelle structure est créée avec les membres suivants :</span><span class="sxs-lookup"><span data-stu-id="fea6f-119">The new structure is created with the following members:</span></span> 
  
```cpp
DTBLPAGE dtblpage;
TCHAR lpszLabel[n];
TCHAR lpszComponent[n1];
```

<span data-ttu-id="fea6f-120">Pour utiliser un pointeur vers la structure obtenue à partir de la macro **SizedDtblPage** comme un pointeur de structure **DTBLPAGE** , effectuer le cast suivant :</span><span class="sxs-lookup"><span data-stu-id="fea6f-120">To use a pointer to the resulting structure from the **SizedDtblPage** macro as a **DTBLPAGE** structure pointer, perform the following cast:</span></span> 
  
```cpp
lpDtblPage = (LPDTBLPAGE) &SizedDtblPage;
```

## <a name="see-also"></a><span data-ttu-id="fea6f-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fea6f-121">See also</span></span>

- [<span data-ttu-id="fea6f-122">DTBLPAGE</span><span class="sxs-lookup"><span data-stu-id="fea6f-122">DTBLPAGE</span></span>](dtblpage.md)
- [<span data-ttu-id="fea6f-123">Macros liées aux structures</span><span class="sxs-lookup"><span data-stu-id="fea6f-123">Macros Related to Structures</span></span>](macros-related-to-structures.md)

