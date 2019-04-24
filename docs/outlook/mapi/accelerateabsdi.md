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
ms.openlocfilehash: 46e87caa68a45a188272340db408c52546f02a57
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322126"
---
# <a name="accelerateabsdi"></a><span data-ttu-id="a5cc0-103">ACCELERATEABSDI</span><span class="sxs-lookup"><span data-stu-id="a5cc0-103">ACCELERATEABSDI</span></span>
 
<span data-ttu-id="a5cc0-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a5cc0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a5cc0-105">Définit une fonction de rappel pour traiter les touches d'accès rapide dans une boîte de dialogue Carnet d'adresses non modal.</span><span class="sxs-lookup"><span data-stu-id="a5cc0-105">Defines a callback function to process accelerator keys in a modeless address book dialog box.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a5cc0-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="a5cc0-106">Header file:</span></span>  <br/> |<span data-ttu-id="a5cc0-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="a5cc0-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="a5cc0-108">Fonction définie implémentée par:</span><span class="sxs-lookup"><span data-stu-id="a5cc0-108">Defined function implemented by:</span></span>  <br/> |<span data-ttu-id="a5cc0-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="a5cc0-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="a5cc0-110">Fonction définie appelée par:</span><span class="sxs-lookup"><span data-stu-id="a5cc0-110">Defined function called by:</span></span>  <br/> |<span data-ttu-id="a5cc0-111">Applications clientes</span><span class="sxs-lookup"><span data-stu-id="a5cc0-111">Client applications</span></span>  <br/> |
   
```cpp
BOOL (STDMETHODCALLTYPE ACCELERATEABSDI)( 
  ULONG_PTR ulUIParam,
  LPVOID lpvmsg
);
```

## <a name="parameters"></a><span data-ttu-id="a5cc0-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a5cc0-112">Parameters</span></span>

 <span data-ttu-id="a5cc0-113">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="a5cc0-113">_ulUIParam_</span></span>
  
> <span data-ttu-id="a5cc0-114">dans Valeur propre à l'implémentation utilisée pour passer des informations d'interface utilisateur à une fonction.</span><span class="sxs-lookup"><span data-stu-id="a5cc0-114">[in] An implementation-specific value used for passing user interface information to a function.</span></span> <span data-ttu-id="a5cc0-115">Dans les applications qui s'exécutent sur Microsoft Windows, _ulUIParam_ est le descripteur de fenêtre parente pour une boîte de dialogue et type HWND, casté en **ULONG_PTR**.</span><span class="sxs-lookup"><span data-stu-id="a5cc0-115">In applications running on Microsoft Windows,  _ulUIParam_ is the parent window handle for a dialog box and is of type HWND, cast to a **ULONG_PTR**.</span></span> <span data-ttu-id="a5cc0-116">La valeur zéro indique qu'il n'y a aucune fenêtre parent.</span><span class="sxs-lookup"><span data-stu-id="a5cc0-116">A value of zero indicates there is no parent window.</span></span> 
    
 <span data-ttu-id="a5cc0-117">_lpvmsg_</span><span class="sxs-lookup"><span data-stu-id="a5cc0-117">_lpvmsg_</span></span>
  
> <span data-ttu-id="a5cc0-118">dans Pointeur vers un message Windows.</span><span class="sxs-lookup"><span data-stu-id="a5cc0-118">[in] Pointer to a Windows message.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="a5cc0-119">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="a5cc0-119">Return value</span></span>

<span data-ttu-id="a5cc0-120">Une fonction avec le prototype **ACCELERATEABSDI** renvoie la valeur true si elle gère le message.</span><span class="sxs-lookup"><span data-stu-id="a5cc0-120">A function with the **ACCELERATEABSDI** prototype returns TRUE if it handles the message.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="a5cc0-121">Remarques</span><span class="sxs-lookup"><span data-stu-id="a5cc0-121">Remarks</span></span>

<span data-ttu-id="a5cc0-122">Une fonction basée sur le prototype **ACCELERATEABSDI** est utilisée uniquement avec une boîte de dialogue non modale, c'est-à-dire, uniquement si l'application cliente a défini l'indicateur DIALOG_SDI dans le membre _ulFlags_ de la structure [ADRPARM](adrparm.md) .</span><span class="sxs-lookup"><span data-stu-id="a5cc0-122">A function based on the **ACCELERATEABSDI** prototype is used only with a modeless dialog, that is, only if the client application has set the DIALOG_SDI flag in the  _ulFlags_ member of the [ADRPARM](adrparm.md) structure.</span></span> 
  
<span data-ttu-id="a5cc0-123">Une boîte de dialogue non modale partage la boucle de messages Windows de l'application cliente, au lieu d'avoir sa propre boucle.</span><span class="sxs-lookup"><span data-stu-id="a5cc0-123">A modeless dialog shares the client application's Windows message loop, instead of having its own loop.</span></span> <span data-ttu-id="a5cc0-124">L'application, qui contrôle la boucle de messages, ne sait pas quelles clés d'accélérateur la boîte de dialogue utilise, afin qu'elle appelle une fonction basée sur **ACCELERATEABSDI** pour tester et agir sur des clés d'accélérateur telles que Ctrl + P pour l'impression.</span><span class="sxs-lookup"><span data-stu-id="a5cc0-124">The application, which controls the message loop, does not know what accelerator keys the dialog uses, so it calls an **ACCELERATEABSDI** based function to test for and act upon accelerator keys such as CTRL+P for printing.</span></span> 
  
<span data-ttu-id="a5cc0-125">La boucle de messages d'un client appelle la fonction basée sur **ACCELERATEABSDI** lorsque le client appelle une boîte de dialogue Carnet d'adresses sans mode avec la méthode [IAddrBook:: Address](iaddrbook-address.md) .</span><span class="sxs-lookup"><span data-stu-id="a5cc0-125">A client's message loop calls the **ACCELERATEABSDI** based function when the client invokes a modeless address book dialog box with the [IAddrBook::Address](iaddrbook-address.md) method.</span></span> <span data-ttu-id="a5cc0-126">Cet appel est terminé lorsque MAPI appelle une fonction basée sur le prototype de fonction [DISMISSMODELESS](dismissmodeless.md) .</span><span class="sxs-lookup"><span data-stu-id="a5cc0-126">This call is terminated when MAPI calls a function based on the [DISMISSMODELESS](dismissmodeless.md) function prototype.</span></span> 
  

