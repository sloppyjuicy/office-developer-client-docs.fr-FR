---
title: DISMISSMODELESS
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.DISMISSMODELESS
api_type:
- COM
ms.assetid: ef93ef3d-c159-40ae-9b8d-0af8a0567565
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: dc830665f425b747d2fdb05641dc037a2e84f695
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783187"
---
# <a name="dismissmodeless"></a><span data-ttu-id="eb4c5-103">DISMISSMODELESS</span><span class="sxs-lookup"><span data-stu-id="eb4c5-103">DISMISSMODELESS</span></span>

  
  
<span data-ttu-id="eb4c5-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="eb4c5-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="eb4c5-105">Définit une fonction de rappel appels MAPI lorsqu’il a rejeté une boîte de dialogue non modale adresse téléchargeable.</span><span class="sxs-lookup"><span data-stu-id="eb4c5-105">Defines a callback function that MAPI calls when it has dismissed a modeless address book dialog box.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="eb4c5-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="eb4c5-106">Header file:</span></span>  <br/> |<span data-ttu-id="eb4c5-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="eb4c5-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="eb4c5-108">Fonction implémentée par :</span><span class="sxs-lookup"><span data-stu-id="eb4c5-108">Defined function implemented by:</span></span>  <br/> |<span data-ttu-id="eb4c5-109">Applications clientes</span><span class="sxs-lookup"><span data-stu-id="eb4c5-109">Client applications</span></span>  <br/> |
|<span data-ttu-id="eb4c5-110">Fonction appelée par :</span><span class="sxs-lookup"><span data-stu-id="eb4c5-110">Defined function called by:</span></span>  <br/> |<span data-ttu-id="eb4c5-111">MAPI</span><span class="sxs-lookup"><span data-stu-id="eb4c5-111">MAPI</span></span>  <br/> |
   
```cpp
void (STDMETHODCALLTYPE DISMISSMODELESS)(
  ULONG_PTR ulUIParam,
  LPVOID lpvContext
);
```

## <a name="parameters"></a><span data-ttu-id="eb4c5-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="eb4c5-112">Parameters</span></span>

 <span data-ttu-id="eb4c5-113">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="eb4c5-113">_ulUIParam_</span></span>
  
> <span data-ttu-id="eb4c5-114">[in] Une valeur spécifique à l’implémentation est généralement utilisée pour transmettre des informations d’interface utilisateur à une fonction.</span><span class="sxs-lookup"><span data-stu-id="eb4c5-114">[in] An implementation-specific value typically used for passing user interface information to a function.</span></span> <span data-ttu-id="eb4c5-115">Par exemple, dans Microsoft Windows ce paramètre est le handle de fenêtre parent pour la boîte de dialogue et est de type HWND, d’une **ULONG_PTR entière**.</span><span class="sxs-lookup"><span data-stu-id="eb4c5-115">For example, in Microsoft Windows this parameter is the parent window handle for the dialog box and is of type HWND, cast to a **ULONG_PTR**.</span></span> <span data-ttu-id="eb4c5-116">La valeur zéro indique aucune fenêtre parent est.</span><span class="sxs-lookup"><span data-stu-id="eb4c5-116">A value of zero indicates there is no parent window.</span></span> 
    
 <span data-ttu-id="eb4c5-117">_lpvContext_</span><span class="sxs-lookup"><span data-stu-id="eb4c5-117">_lpvContext_</span></span>
  
> <span data-ttu-id="eb4c5-118">[in] Pointeur vers une valeur arbitraire transmis à la fonction de rappel lorsque MAPI il l’appelle.</span><span class="sxs-lookup"><span data-stu-id="eb4c5-118">[in] Pointer to an arbitrary value passed to the callback function when MAPI calls it.</span></span> <span data-ttu-id="eb4c5-119">Cette valeur peut représenter une adresse de l’argument précision à l’application cliente.</span><span class="sxs-lookup"><span data-stu-id="eb4c5-119">This value can represent an address of significance to the client application.</span></span> <span data-ttu-id="eb4c5-120">En règle générale, pour le code C++, _lpvContext_ est un pointeur vers l’adresse d’une instance d’objet C++.</span><span class="sxs-lookup"><span data-stu-id="eb4c5-120">Typically, for C++ code,  _lpvContext_ is a pointer to the address of a C++ object instance.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="eb4c5-121">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="eb4c5-121">Return value</span></span>

<span data-ttu-id="eb4c5-122">Aucune</span><span class="sxs-lookup"><span data-stu-id="eb4c5-122">None</span></span>
  
## <a name="remarks"></a><span data-ttu-id="eb4c5-123">Remarques</span><span class="sxs-lookup"><span data-stu-id="eb4c5-123">Remarks</span></span>

<span data-ttu-id="eb4c5-124">Lorsque l’application cliente appelle une boîte de dialogue non modale adresse téléchargeable, il inclut dans sa boucle de message Windows un appel à une fonction basée sur le prototype [ACCELERATEABSDI](accelerateabsdi.md) , qui recherche et traite les touches de raccourci.</span><span class="sxs-lookup"><span data-stu-id="eb4c5-124">When the client application invokes a modeless address book dialog box, it includes in its Windows message loop a call to a function based on the [ACCELERATEABSDI](accelerateabsdi.md) prototype, which checks for and processes accelerator keys.</span></span> <span data-ttu-id="eb4c5-125">Lorsque la boîte de dialogue est fermée, les appels MAPI que fonction en fonction de la **DISMISSMODELESS** afin que l’application cliente s’arrête **ACCELERATEABSDI** l’appel en fonction de fonction.</span><span class="sxs-lookup"><span data-stu-id="eb4c5-125">When the dialog box is closed, MAPI calls the **DISMISSMODELESS** based function so that the client application will stop calling the **ACCELERATEABSDI** based function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="eb4c5-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="eb4c5-126">See also</span></span>



[<span data-ttu-id="eb4c5-127">ADRPARM</span><span class="sxs-lookup"><span data-stu-id="eb4c5-127">ADRPARM</span></span>](adrparm.md)

