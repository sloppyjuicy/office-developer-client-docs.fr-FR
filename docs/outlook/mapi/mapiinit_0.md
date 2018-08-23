---
title: MAPIINIT_0
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.MAPIINIT_0
api_type:
- COM
ms.assetid: 70739711-ff43-407d-bc8b-6baf7a476fef
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 1eb4d7ac8d0287388a1bb76185f23636eddcf809
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22591673"
---
# <a name="mapiinit0"></a><span data-ttu-id="1a35c-103">MAPIINIT_0</span><span class="sxs-lookup"><span data-stu-id="1a35c-103">MAPIINIT_0</span></span>

  
  
<span data-ttu-id="1a35c-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1a35c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1a35c-105">Présente les options de la fonction [exécuter MAPIInitialize](mapiinitialize.md) .</span><span class="sxs-lookup"><span data-stu-id="1a35c-105">Conveys options to the [MAPIInitialize](mapiinitialize.md) function.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="1a35c-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="1a35c-106">Header file:</span></span>  <br/> |<span data-ttu-id="1a35c-107">MAPIX. H</span><span class="sxs-lookup"><span data-stu-id="1a35c-107">MAPIX.H</span></span>  <br/> |
   
```cpp
typedef struct
{
  ULONG ulVersion;
  ULONG ulFlags;
} MAPIINIT_0, FAR *LPMAPIINIT_0;

```

## <a name="members"></a><span data-ttu-id="1a35c-108">Members</span><span class="sxs-lookup"><span data-stu-id="1a35c-108">Members</span></span>

 <span data-ttu-id="1a35c-109">**ulVersion**</span><span class="sxs-lookup"><span data-stu-id="1a35c-109">**ulVersion**</span></span>
  
> <span data-ttu-id="1a35c-110">Valeur entière qui représente le numéro de version de la structure **MAPIINIT_0** .</span><span class="sxs-lookup"><span data-stu-id="1a35c-110">An integer value that represents the version number of the **MAPIINIT_0** structure.</span></span> <span data-ttu-id="1a35c-111">Le membre **ulVersion** est une expansion future et ne représente pas la version de l’interface MAPI.</span><span class="sxs-lookup"><span data-stu-id="1a35c-111">The **ulVersion** member is for future expansion and does not represent the version of the MAPI interface.</span></span> <span data-ttu-id="1a35c-112">Actuellement, **ulVersion** doit être défini sur MAPI_INIT_VERSION.</span><span class="sxs-lookup"><span data-stu-id="1a35c-112">Currently, **ulVersion** must be set to MAPI_INIT_VERSION.</span></span> 
    
 <span data-ttu-id="1a35c-113">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="1a35c-113">**ulFlags**</span></span>
  
> <span data-ttu-id="1a35c-114">Masque de bits d’indicateurs utilisés pour contrôler l’initialisation de la session MAPI.</span><span class="sxs-lookup"><span data-stu-id="1a35c-114">The bitmask of flags used to control the initialization of the MAPI session.</span></span> <span data-ttu-id="1a35c-115">Les indicateurs suivants peuvent être définis :</span><span class="sxs-lookup"><span data-stu-id="1a35c-115">The following flags can be set:</span></span>
    
<span data-ttu-id="1a35c-116">MAPI_MULTITHREAD_NOTIFICATIONS</span><span class="sxs-lookup"><span data-stu-id="1a35c-116">MAPI_MULTITHREAD_NOTIFICATIONS</span></span> 
  
> <span data-ttu-id="1a35c-117">MAPI doit générer des notifications à l’aide d’un thread dédié à la gestion plutôt que le premier thread utilisé pour appeler **exécuter MAPIInitialize**de la notification.</span><span class="sxs-lookup"><span data-stu-id="1a35c-117">MAPI should generate notifications using a thread dedicated to notification handling instead of the first thread used to call **MAPIInitialize**.</span></span>
    
<span data-ttu-id="1a35c-118">MAPI_NT_SERVICE</span><span class="sxs-lookup"><span data-stu-id="1a35c-118">MAPI_NT_SERVICE</span></span> 
  
> <span data-ttu-id="1a35c-119">L’appelant est exécuté comme un service Windows.</span><span class="sxs-lookup"><span data-stu-id="1a35c-119">The caller is running as a Windows service.</span></span> <span data-ttu-id="1a35c-120">Appelants qui n’exécutent pas comme un service Windows ne doit pas définir cet indicateur ; Cet indicateur doivent être défini par les appelants qui sont en cours d’exécution en tant que service.</span><span class="sxs-lookup"><span data-stu-id="1a35c-120">Callers that are not running as a Windows service should not set this flag; callers that are running as a service must set this flag.</span></span>
    
<span data-ttu-id="1a35c-121">MAPI_NO_COINIT</span><span class="sxs-lookup"><span data-stu-id="1a35c-121">MAPI_NO_COINIT</span></span>
  
> <span data-ttu-id="1a35c-122">Définir l’indicateur MAPI_NO_COINT pour pouvoir **exécuter MAPIInitialize** n’essaie pas d’initialiser COM avec un appel à [CoInitialize](http://msdn.microsoft.com/library/0f171cf4-87b9-43a6-97f2-80ed344fe376%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="1a35c-122">Set the MAPI_NO_COINT flag so that **MAPIInitialize** does not try to initialize COM with a call to [CoInitialize](http://msdn.microsoft.com/library/0f171cf4-87b9-43a6-97f2-80ed344fe376%28Office.15%29.aspx).</span></span> <span data-ttu-id="1a35c-123">Si une structure **MAPIINIT_0** est passée à **exécuter MAPIInitialize** avec _ulFlags_ défini sur MAPI_NO_COINIT, MAPI part du principe que COM a déjà été initialisé et ignore l’appel à **CoInitialize**.</span><span class="sxs-lookup"><span data-stu-id="1a35c-123">If a **MAPIINIT_0** structure is passed into **MAPIInitialize** with  _ulFlags_ set to MAPI_NO_COINIT, MAPI will assume that COM has already been initialized and will bypass the call to **CoInitialize**.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="1a35c-124">Remarques</span><span class="sxs-lookup"><span data-stu-id="1a35c-124">Remarks</span></span>

<span data-ttu-id="1a35c-125">Clients multithreads doivent définir l’indicateur MAPI_MULTITHREAD_NOTIFICATIONS.</span><span class="sxs-lookup"><span data-stu-id="1a35c-125">Multithreaded clients should set the MAPI_MULTITHREAD_NOTIFICATIONS flag.</span></span> <span data-ttu-id="1a35c-126">Si l’indicateur n’est pas définie, les notifications sont générées sur le thread utilisé pour le premier appel à **exécuter MAPIInitialize**.</span><span class="sxs-lookup"><span data-stu-id="1a35c-126">If the flag is not set, notifications are generated on the thread used to make the first call to **MAPIInitialize**.</span></span> 
  
<span data-ttu-id="1a35c-127">Pour plus d’informations sur le moment de définir cet indicateur et comment implémenter la sécurité des threads dans un client, voir [Threading MAPI](threading-in-mapi.md).</span><span class="sxs-lookup"><span data-stu-id="1a35c-127">For more information about when to set this flag and how to implement thread safety in a client, see [Threading in MAPI](threading-in-mapi.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="1a35c-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1a35c-128">See also</span></span>



[<span data-ttu-id="1a35c-129">MAPIInitialize</span><span class="sxs-lookup"><span data-stu-id="1a35c-129">MAPIInitialize</span></span>](mapiinitialize.md)


[<span data-ttu-id="1a35c-130">Structures MAPI</span><span class="sxs-lookup"><span data-stu-id="1a35c-130">MAPI Structures</span></span>](mapi-structures.md)

