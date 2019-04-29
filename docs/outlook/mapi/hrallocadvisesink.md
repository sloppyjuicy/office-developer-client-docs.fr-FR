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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 7f9873fe8e1825c68d4540cc1d093171e9f95727
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428899"
---
# <a name="hrallocadvisesink"></a><span data-ttu-id="0399a-103">HrAllocAdviseSink</span><span class="sxs-lookup"><span data-stu-id="0399a-103">HrAllocAdviseSink</span></span>

  
  
<span data-ttu-id="0399a-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0399a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0399a-105">Crée un objet de récepteur de notifications, en fonction d'un contexte spécifié par l'implémentation de l'appel et d'une fonction de rappel à déclencher par une notification d'événement.</span><span class="sxs-lookup"><span data-stu-id="0399a-105">Creates an advise sink object, given a context specified by the calling implementation and a callback function to be triggered by an event notification.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="0399a-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="0399a-106">Header file:</span></span>  <br/> |<span data-ttu-id="0399a-107">Mapiutil. h</span><span class="sxs-lookup"><span data-stu-id="0399a-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="0399a-108">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="0399a-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="0399a-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="0399a-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="0399a-110">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="0399a-110">Called by:</span></span>  <br/> |<span data-ttu-id="0399a-111">Applications clientes et fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="0399a-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
STDAPI HrAllocAdviseSink(
  LPNOTIFCALLBACK lpfnCallback,
  LPVOID lpvContext,
  LPMAPIADVISESINK FAR * lppAdviseSink
);
```

## <a name="parameters"></a><span data-ttu-id="0399a-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0399a-112">Parameters</span></span>

 <span data-ttu-id="0399a-113">_lpfnCallback_</span><span class="sxs-lookup"><span data-stu-id="0399a-113">_lpfnCallback_</span></span>
  
> <span data-ttu-id="0399a-114">dans Pointeur vers une fonction de rappel basée sur le prototype [NOTIFCALLBACK](notifcallback.md) que MAPI doit appeler lorsqu'un événement de notification se produit pour le récepteur de notifications nouvellement créé.</span><span class="sxs-lookup"><span data-stu-id="0399a-114">[in] Pointer to a callback function based on the [NOTIFCALLBACK](notifcallback.md) prototype that MAPI is to call when a notification event occurs for the newly created advise sink.</span></span> 
    
 <span data-ttu-id="0399a-115">_lpvContext_</span><span class="sxs-lookup"><span data-stu-id="0399a-115">_lpvContext_</span></span>
  
> <span data-ttu-id="0399a-116">dans Pointeur vers les données d'appelant transmises à la fonction de rappel lorsque MAPI les appelle.</span><span class="sxs-lookup"><span data-stu-id="0399a-116">[in] Pointer to caller data passed to the callback function when MAPI calls it.</span></span> <span data-ttu-id="0399a-117">Les données de l'appelant peuvent représenter une adresse de signification pour le client ou le fournisseur.</span><span class="sxs-lookup"><span data-stu-id="0399a-117">The caller data can represent an address of significance to the client or provider.</span></span> <span data-ttu-id="0399a-118">En règle générale, pour le code C++, le paramètre _lpvContext_ représente un pointeur vers l'adresse d'un objet.</span><span class="sxs-lookup"><span data-stu-id="0399a-118">Typically, for C++ code, the  _lpvContext_ parameter represents a pointer to the address of an object.</span></span> 
    
 <span data-ttu-id="0399a-119">_lppAdviseSink_</span><span class="sxs-lookup"><span data-stu-id="0399a-119">_lppAdviseSink_</span></span>
  
> <span data-ttu-id="0399a-120">remarquer Pointeur vers un pointeur vers un objet de récepteur de notifications.</span><span class="sxs-lookup"><span data-stu-id="0399a-120">[out] Pointer to a pointer to an advise sink object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="0399a-121">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="0399a-121">Return value</span></span>

<span data-ttu-id="0399a-122">Aucun.</span><span class="sxs-lookup"><span data-stu-id="0399a-122">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="0399a-123">Remarques</span><span class="sxs-lookup"><span data-stu-id="0399a-123">Remarks</span></span>

<span data-ttu-id="0399a-124">Pour utiliser la fonction **HrAllocAdviseSink** , une application cliente ou un fournisseur de services crée un objet pour recevoir des notifications, crée une fonction de rappel de notification basée sur le prototype de fonction [NOTIFCALLBACK](notifcallback.md) qui suit cet objet, et transmet un pointeur vers l'objet dans la fonction **HrAllocAdviseSink** en tant que valeur _lpvContext_ .</span><span class="sxs-lookup"><span data-stu-id="0399a-124">To use the **HrAllocAdviseSink** function, a client application or service provider creates an object to receive notifications, creates a notification callback function based on the [NOTIFCALLBACK](notifcallback.md) function prototype that goes with that object, and passes a pointer to the object in the **HrAllocAdviseSink** function as the  _lpvContext_ value.</span></span> <span data-ttu-id="0399a-125">Cette opération effectue une notification; dans le cadre du processus de notification, MAPI appelle la fonction de rappel avec le pointeur d'objet comme contexte.</span><span class="sxs-lookup"><span data-stu-id="0399a-125">Doing so performs a notification; and as part of the notification process, MAPI calls the callback function with the object pointer as the context.</span></span> 
  
<span data-ttu-id="0399a-126">MAPI implémente le moteur de notification de manière asynchrone.</span><span class="sxs-lookup"><span data-stu-id="0399a-126">MAPI implements its notification engine asynchronously.</span></span> <span data-ttu-id="0399a-127">En C++, le rappel de notification peut être une méthode d'objet.</span><span class="sxs-lookup"><span data-stu-id="0399a-127">In C++, the notification callback can be an object method.</span></span> <span data-ttu-id="0399a-128">Si l'objet qui génère la notification n'est pas présent, le client ou le fournisseur qui demande la notification doit conserver un nombre de référence distinct pour cet objet pour le récepteur de notification de l'objet.</span><span class="sxs-lookup"><span data-stu-id="0399a-128">If the object generating the notification is not present, the client or provider requesting notification must keep a separate reference count for that object for the object's advise sink.</span></span> 
  
> [!CAUTION]
> <span data-ttu-id="0399a-129">**HrAllocAdviseSink** doit être utilisé avec modération; Il est plus sûr pour les clients de créer leurs propres récepteurs de notification.</span><span class="sxs-lookup"><span data-stu-id="0399a-129">**HrAllocAdviseSink** should be used sparingly; it is safer for clients to create their own advise sinks.</span></span> 
  

