---
title: ACCELERATEABSDI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ACCELERATEABSDI
api_type:
- HeaderDef
ms.assetid: da67dcf4-1411-4fc9-992c-115485019bd3
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: b7d4d758f7031c55aa3a23b662ec8727ea1e0719
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782870"
---
# <a name="accelerateabsdi"></a><span data-ttu-id="3eb34-103">ACCELERATEABSDI</span><span class="sxs-lookup"><span data-stu-id="3eb34-103">ACCELERATEABSDI</span></span>
 
<span data-ttu-id="3eb34-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="3eb34-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="3eb34-105">Définit une fonction de rappel de processus raccourcis dans une boîte de dialogue non modale adresse téléchargeable.</span><span class="sxs-lookup"><span data-stu-id="3eb34-105">Defines a callback function to process accelerator keys in a modeless address book dialog box.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="3eb34-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="3eb34-106">Header file:</span></span>  <br/> |<span data-ttu-id="3eb34-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="3eb34-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="3eb34-108">Fonction implémentée par :</span><span class="sxs-lookup"><span data-stu-id="3eb34-108">Defined function implemented by:</span></span>  <br/> |<span data-ttu-id="3eb34-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="3eb34-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="3eb34-110">Fonction appelée par :</span><span class="sxs-lookup"><span data-stu-id="3eb34-110">Defined function called by:</span></span>  <br/> |<span data-ttu-id="3eb34-111">Applications clientes</span><span class="sxs-lookup"><span data-stu-id="3eb34-111">Client applications</span></span>  <br/> |
   
```cpp
BOOL (STDMETHODCALLTYPE ACCELERATEABSDI)( 
  ULONG_PTR ulUIParam,
  LPVOID lpvmsg
);
```

## <a name="parameters"></a><span data-ttu-id="3eb34-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3eb34-112">Parameters</span></span>

 <span data-ttu-id="3eb34-113">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="3eb34-113">_ulUIParam_</span></span>
  
> <span data-ttu-id="3eb34-114">[in] Une valeur spécifique à l’implémentation utilisée pour transmettre des informations d’interface utilisateur à une fonction.</span><span class="sxs-lookup"><span data-stu-id="3eb34-114">[in] An implementation-specific value used for passing user interface information to a function.</span></span> <span data-ttu-id="3eb34-115">Dans les applications s’exécutant sur Microsoft Windows, _ulUIParam_ est le handle de fenêtre parent pour une boîte de dialogue et de type HWND, d’une **ULONG_PTR entière**.</span><span class="sxs-lookup"><span data-stu-id="3eb34-115">In applications running on Microsoft Windows,  _ulUIParam_ is the parent window handle for a dialog box and is of type HWND, cast to a **ULONG_PTR**.</span></span> <span data-ttu-id="3eb34-116">La valeur zéro indique aucune fenêtre parent est.</span><span class="sxs-lookup"><span data-stu-id="3eb34-116">A value of zero indicates there is no parent window.</span></span> 
    
 <span data-ttu-id="3eb34-117">_lpvmsg_</span><span class="sxs-lookup"><span data-stu-id="3eb34-117">_lpvmsg_</span></span>
  
> <span data-ttu-id="3eb34-118">[in] Pointeur vers un message Windows.</span><span class="sxs-lookup"><span data-stu-id="3eb34-118">[in] Pointer to a Windows message.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="3eb34-119">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="3eb34-119">Return value</span></span>

<span data-ttu-id="3eb34-120">Une fonction avec le prototype **ACCELERATEABSDI** renvoie la valeur TRUE si elle gère le message.</span><span class="sxs-lookup"><span data-stu-id="3eb34-120">A function with the **ACCELERATEABSDI** prototype returns TRUE if it handles the message.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="3eb34-121">Remarques</span><span class="sxs-lookup"><span data-stu-id="3eb34-121">Remarks</span></span>

<span data-ttu-id="3eb34-122">Une fonction basée sur le prototype **ACCELERATEABSDI** est utilisée uniquement avec une boîte de dialogue non modale, c'est-à-dire, uniquement si l’application cliente a défini l’indicateur DIALOG_SDI dans le membre _ulFlags_ de la structure [ADRPARM](adrparm.md) .</span><span class="sxs-lookup"><span data-stu-id="3eb34-122">A function based on the **ACCELERATEABSDI** prototype is used only with a modeless dialog, that is, only if the client application has set the DIALOG_SDI flag in the  _ulFlags_ member of the [ADRPARM](adrparm.md) structure.</span></span> 
  
<span data-ttu-id="3eb34-123">Une boîte de dialogue non modale partage boucle de message de l’application cliente Windows, au lieu d’avoir sa propre boucle.</span><span class="sxs-lookup"><span data-stu-id="3eb34-123">A modeless dialog shares the client application's Windows message loop, instead of having its own loop.</span></span> <span data-ttu-id="3eb34-124">L’application, qui contrôle la boucle de messages, ne sait pas les touches accélérateur les utilisations de boîte de dialogue, elle appelle une **ACCELERATEABSDI** fondé sur fonction pour tester et modifier les touches accélérateur par exemple CTRL + P pour l’impression.</span><span class="sxs-lookup"><span data-stu-id="3eb34-124">The application, which controls the message loop, does not know what accelerator keys the dialog uses, so it calls an **ACCELERATEABSDI** based function to test for and act upon accelerator keys such as CTRL+P for printing.</span></span> 
  
<span data-ttu-id="3eb34-125">Appels de boucle de message d’un client l' **ACCELERATEABSDI** en fonction de fonction lorsque le client appelle une boîte de dialogue non modale adresse livre avec la méthode [IAddrBook::Address](iaddrbook-address.md) .</span><span class="sxs-lookup"><span data-stu-id="3eb34-125">A client's message loop calls the **ACCELERATEABSDI** based function when the client invokes a modeless address book dialog box with the [IAddrBook::Address](iaddrbook-address.md) method.</span></span> <span data-ttu-id="3eb34-126">Cet appel est terminé lorsque MAPI appelle une fonction basée sur le prototype de fonction [DISMISSMODELESS](dismissmodeless.md) .</span><span class="sxs-lookup"><span data-stu-id="3eb34-126">This call is terminated when MAPI calls a function based on the [DISMISSMODELESS](dismissmodeless.md) function prototype.</span></span> 
  

