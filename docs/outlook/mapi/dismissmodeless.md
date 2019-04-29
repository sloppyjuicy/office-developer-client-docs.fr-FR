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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: dd962515a85cb6a4b8661a0fd5294cea55cd6e96
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428185"
---
# <a name="dismissmodeless"></a><span data-ttu-id="b5cc5-103">DISMISSMODELESS</span><span class="sxs-lookup"><span data-stu-id="b5cc5-103">DISMISSMODELESS</span></span>

  
  
<span data-ttu-id="b5cc5-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b5cc5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b5cc5-105">Définit une fonction de rappel que MAPI appelle lorsqu'il a ignoré une boîte de dialogue Carnet d'adresses non modale.</span><span class="sxs-lookup"><span data-stu-id="b5cc5-105">Defines a callback function that MAPI calls when it has dismissed a modeless address book dialog box.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b5cc5-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="b5cc5-106">Header file:</span></span>  <br/> |<span data-ttu-id="b5cc5-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="b5cc5-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="b5cc5-108">Fonction définie implémentée par:</span><span class="sxs-lookup"><span data-stu-id="b5cc5-108">Defined function implemented by:</span></span>  <br/> |<span data-ttu-id="b5cc5-109">Applications clientes</span><span class="sxs-lookup"><span data-stu-id="b5cc5-109">Client applications</span></span>  <br/> |
|<span data-ttu-id="b5cc5-110">Fonction définie appelée par:</span><span class="sxs-lookup"><span data-stu-id="b5cc5-110">Defined function called by:</span></span>  <br/> |<span data-ttu-id="b5cc5-111">MAPI</span><span class="sxs-lookup"><span data-stu-id="b5cc5-111">MAPI</span></span>  <br/> |
   
```cpp
void (STDMETHODCALLTYPE DISMISSMODELESS)(
  ULONG_PTR ulUIParam,
  LPVOID lpvContext
);
```

## <a name="parameters"></a><span data-ttu-id="b5cc5-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b5cc5-112">Parameters</span></span>

 <span data-ttu-id="b5cc5-113">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="b5cc5-113">_ulUIParam_</span></span>
  
> <span data-ttu-id="b5cc5-114">dans Une valeur propre à l'implémentation généralement utilisée pour passer des informations d'interface utilisateur à une fonction.</span><span class="sxs-lookup"><span data-stu-id="b5cc5-114">[in] An implementation-specific value typically used for passing user interface information to a function.</span></span> <span data-ttu-id="b5cc5-115">Par exemple, dans Microsoft Windows, ce paramètre est le descripteur de fenêtre parent de la boîte de dialogue et est de type HWND, casté en **ULONG_PTR**.</span><span class="sxs-lookup"><span data-stu-id="b5cc5-115">For example, in Microsoft Windows this parameter is the parent window handle for the dialog box and is of type HWND, cast to a **ULONG_PTR**.</span></span> <span data-ttu-id="b5cc5-116">La valeur zéro indique qu'il n'y a aucune fenêtre parent.</span><span class="sxs-lookup"><span data-stu-id="b5cc5-116">A value of zero indicates there is no parent window.</span></span> 
    
 <span data-ttu-id="b5cc5-117">_lpvContext_</span><span class="sxs-lookup"><span data-stu-id="b5cc5-117">_lpvContext_</span></span>
  
> <span data-ttu-id="b5cc5-118">dans Pointeur vers une valeur arbitraire passée à la fonction de rappel lorsque MAPI l'appelle.</span><span class="sxs-lookup"><span data-stu-id="b5cc5-118">[in] Pointer to an arbitrary value passed to the callback function when MAPI calls it.</span></span> <span data-ttu-id="b5cc5-119">Cette valeur peut représenter une adresse de l'importance de l'application cliente.</span><span class="sxs-lookup"><span data-stu-id="b5cc5-119">This value can represent an address of significance to the client application.</span></span> <span data-ttu-id="b5cc5-120">En règle générale, pour le code C++, _lpvContext_ est un pointeur vers l'adresse d'une instance d'objet C++.</span><span class="sxs-lookup"><span data-stu-id="b5cc5-120">Typically, for C++ code,  _lpvContext_ is a pointer to the address of a C++ object instance.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="b5cc5-121">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="b5cc5-121">Return value</span></span>

<span data-ttu-id="b5cc5-122">Aucun</span><span class="sxs-lookup"><span data-stu-id="b5cc5-122">None</span></span>
  
## <a name="remarks"></a><span data-ttu-id="b5cc5-123">Remarques</span><span class="sxs-lookup"><span data-stu-id="b5cc5-123">Remarks</span></span>

<span data-ttu-id="b5cc5-124">Lorsque l'application cliente appelle une boîte de dialogue Carnet d'adresses non modale, elle inclut dans sa boucle de messages Windows un appel à une fonction basée sur le prototype [ACCELERATEABSDI](accelerateabsdi.md) , qui vérifie et traite les touches d'accès rapide.</span><span class="sxs-lookup"><span data-stu-id="b5cc5-124">When the client application invokes a modeless address book dialog box, it includes in its Windows message loop a call to a function based on the [ACCELERATEABSDI](accelerateabsdi.md) prototype, which checks for and processes accelerator keys.</span></span> <span data-ttu-id="b5cc5-125">Lorsque la boîte de dialogue est fermée, MAPI appelle la fonction basée sur **DISMISSMODELESS** afin que l'application cliente arrête d'appeler la fonction **ACCELERATEABSDI** .</span><span class="sxs-lookup"><span data-stu-id="b5cc5-125">When the dialog box is closed, MAPI calls the **DISMISSMODELESS** based function so that the client application will stop calling the **ACCELERATEABSDI** based function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="b5cc5-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b5cc5-126">See also</span></span>



[<span data-ttu-id="b5cc5-127">ADRPARM</span><span class="sxs-lookup"><span data-stu-id="b5cc5-127">ADRPARM</span></span>](adrparm.md)

