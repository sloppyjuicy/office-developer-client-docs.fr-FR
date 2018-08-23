---
title: HrAllocAdviseSink
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- HrAllocAdviseSink
api_type:
- HeaderDef
ms.assetid: 1dd460e6-ce95-4fef-bb5e-8d778c9716d5
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: d5cb43bfa3acd912e397644657223c177d6afb30
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589321"
---
# <a name="hrallocadvisesink"></a><span data-ttu-id="f17cf-103">HrAllocAdviseSink</span><span class="sxs-lookup"><span data-stu-id="f17cf-103">HrAllocAdviseSink</span></span>

  
  
<span data-ttu-id="f17cf-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f17cf-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f17cf-105">Crée un objet récepteur advise, étant donné un contexte spécifié par l’implémentation d’appel et une fonction de rappel pour être déclenché par une notification d’événement.</span><span class="sxs-lookup"><span data-stu-id="f17cf-105">Creates an advise sink object, given a context specified by the calling implementation and a callback function to be triggered by an event notification.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f17cf-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="f17cf-106">Header file:</span></span>  <br/> |<span data-ttu-id="f17cf-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="f17cf-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="f17cf-108">Implémentée par :</span><span class="sxs-lookup"><span data-stu-id="f17cf-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="f17cf-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="f17cf-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="f17cf-110">Appelée par :</span><span class="sxs-lookup"><span data-stu-id="f17cf-110">Called by:</span></span>  <br/> |<span data-ttu-id="f17cf-111">Les applications clientes et des fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="f17cf-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
STDAPI HrAllocAdviseSink(
  LPNOTIFCALLBACK lpfnCallback,
  LPVOID lpvContext,
  LPMAPIADVISESINK FAR * lppAdviseSink
);
```

## <a name="parameters"></a><span data-ttu-id="f17cf-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f17cf-112">Parameters</span></span>

 <span data-ttu-id="f17cf-113">_lpfnCallback_</span><span class="sxs-lookup"><span data-stu-id="f17cf-113">_lpfnCallback_</span></span>
  
> <span data-ttu-id="f17cf-114">[in] Pointeur vers une fonction de rappel selon le prototype [NOTIFCALLBACK](notifcallback.md) MAPI consiste à appeler lorsque cet événement se produit un événement de notification pour le récepteur de notification nouvellement créé.</span><span class="sxs-lookup"><span data-stu-id="f17cf-114">[in] Pointer to a callback function based on the [NOTIFCALLBACK](notifcallback.md) prototype that MAPI is to call when a notification event occurs for the newly created advise sink.</span></span> 
    
 <span data-ttu-id="f17cf-115">_lpvContext_</span><span class="sxs-lookup"><span data-stu-id="f17cf-115">_lpvContext_</span></span>
  
> <span data-ttu-id="f17cf-116">[in] Pointeur vers les données de l’appelant transmis à la fonction de rappel lorsque MAPI il l’appelle.</span><span class="sxs-lookup"><span data-stu-id="f17cf-116">[in] Pointer to caller data passed to the callback function when MAPI calls it.</span></span> <span data-ttu-id="f17cf-117">Les données de l’appelant peuvent représenter une adresse de l’argument précision pour le client ou le fournisseur.</span><span class="sxs-lookup"><span data-stu-id="f17cf-117">The caller data can represent an address of significance to the client or provider.</span></span> <span data-ttu-id="f17cf-118">En règle générale, pour le code C++, le paramètre _lpvContext_ représente un pointeur vers l’adresse d’un objet.</span><span class="sxs-lookup"><span data-stu-id="f17cf-118">Typically, for C++ code, the  _lpvContext_ parameter represents a pointer to the address of an object.</span></span> 
    
 <span data-ttu-id="f17cf-119">_lppAdviseSink_</span><span class="sxs-lookup"><span data-stu-id="f17cf-119">_lppAdviseSink_</span></span>
  
> <span data-ttu-id="f17cf-120">[out] Pointeur vers un pointeur vers un objet de réception de notifications.</span><span class="sxs-lookup"><span data-stu-id="f17cf-120">[out] Pointer to a pointer to an advise sink object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="f17cf-121">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="f17cf-121">Return value</span></span>

<span data-ttu-id="f17cf-122">Aucun.</span><span class="sxs-lookup"><span data-stu-id="f17cf-122">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="f17cf-123">Remarques</span><span class="sxs-lookup"><span data-stu-id="f17cf-123">Remarks</span></span>

<span data-ttu-id="f17cf-124">Pour utiliser la fonction **HrAllocAdviseSink** , une application cliente ou un fournisseur de services crée un objet pour recevoir des notifications, crée une fonction de rappel de notification basée sur le prototype de fonction [NOTIFCALLBACK](notifcallback.md) qui accompagne cet objet, et passe un pointeur vers l’objet dans la fonction **HrAllocAdviseSink** en tant que la valeur _lpvContext_ .</span><span class="sxs-lookup"><span data-stu-id="f17cf-124">To use the **HrAllocAdviseSink** function, a client application or service provider creates an object to receive notifications, creates a notification callback function based on the [NOTIFCALLBACK](notifcallback.md) function prototype that goes with that object, and passes a pointer to the object in the **HrAllocAdviseSink** function as the  _lpvContext_ value.</span></span> <span data-ttu-id="f17cf-125">Cela effectue une notification ; et, dans le cadre du processus de notification, les appels MAPI avec le pointeur de l’objet en tant que le contexte de la fonction de rappel.</span><span class="sxs-lookup"><span data-stu-id="f17cf-125">Doing so performs a notification; and as part of the notification process, MAPI calls the callback function with the object pointer as the context.</span></span> 
  
<span data-ttu-id="f17cf-126">MAPI implémente le moteur de notification asynchrone.</span><span class="sxs-lookup"><span data-stu-id="f17cf-126">MAPI implements its notification engine asynchronously.</span></span> <span data-ttu-id="f17cf-127">En C++, le rappel de notification peut être une méthode d’objet.</span><span class="sxs-lookup"><span data-stu-id="f17cf-127">In C++, the notification callback can be an object method.</span></span> <span data-ttu-id="f17cf-128">Si l’objet de génération de la notification n’est pas présent, le client ou le fournisseur demande de notification doit conserver un décompte de références distincte pour cet objet de l’objet récepteur de notification.</span><span class="sxs-lookup"><span data-stu-id="f17cf-128">If the object generating the notification is not present, the client or provider requesting notification must keep a separate reference count for that object for the object's advise sink.</span></span> 
  
> [!CAUTION]
> <span data-ttu-id="f17cf-129">**HrAllocAdviseSink** doit être utilisé avec modération ; Il est recommandé pour les clients créer leurs propres récepteurs advise.</span><span class="sxs-lookup"><span data-stu-id="f17cf-129">**HrAllocAdviseSink** should be used sparingly; it is safer for clients to create their own advise sinks.</span></span> 
  

