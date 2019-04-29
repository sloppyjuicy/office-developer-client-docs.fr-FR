---
title: MSCAP_SELECTOR
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f28ac144-f5ac-fd83-2b72-8d6e5fd74b6e
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 9c5d8ab5bbac91250f3b8c552ad891c62134526e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417202"
---
# <a name="mscapselector"></a><span data-ttu-id="02dcd-103">MSCAP_SELECTOR</span><span class="sxs-lookup"><span data-stu-id="02dcd-103">MSCAP_SELECTOR</span></span>

  
  
<span data-ttu-id="02dcd-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="02dcd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="02dcd-105">Spécifie les fonctionnalités à renvoyer pour un magasin.</span><span class="sxs-lookup"><span data-stu-id="02dcd-105">Specifies the capabilities to return for a store.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="02dcd-106">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="02dcd-106">Quick info</span></span>

```cpp
typedef enum 
{ 
    MSCAP_SEL_RESERVED1 = 0, 
    MSCAP_SEL_RESERVED2, 
    MSCAP_SEL_FOLDER, 
    MSCAP_SEL_RESERVED3, 
    MSCAP_SEL_RESTRICTION, 
} MSCAP_SELECTOR;
```

## <a name="members"></a><span data-ttu-id="02dcd-107">Membres</span><span class="sxs-lookup"><span data-stu-id="02dcd-107">Members</span></span>

 <span data-ttu-id="02dcd-108">*MSCAP_SEL_RESERVED1*</span><span class="sxs-lookup"><span data-stu-id="02dcd-108">*MSCAP_SEL_RESERVED1*</span></span> 
  
> <span data-ttu-id="02dcd-109">Ce membre est réservé à l'usage interne d'Outlook et n'est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="02dcd-109">This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
 <span data-ttu-id="02dcd-110">*MSCAP_SEL_RESERVED2*</span><span class="sxs-lookup"><span data-stu-id="02dcd-110">*MSCAP_SEL_RESERVED2*</span></span> 
  
> <span data-ttu-id="02dcd-111">Ce membre est réservé à l'usage interne d'Outlook et n'est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="02dcd-111">This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
 <span data-ttu-id="02dcd-112">*MSCAP_SEL_FOLDER*</span><span class="sxs-lookup"><span data-stu-id="02dcd-112">*MSCAP_SEL_FOLDER*</span></span> 
  
> <span data-ttu-id="02dcd-113">Fonctionnalités de prise en charge des dossiers sur une banque.</span><span class="sxs-lookup"><span data-stu-id="02dcd-113">Capabilities about supporting folders on a store.</span></span>
    
 <span data-ttu-id="02dcd-114">*MSCAP_SEL_RESERVED3*</span><span class="sxs-lookup"><span data-stu-id="02dcd-114">*MSCAP_SEL_RESERVED3*</span></span> 
  
> <span data-ttu-id="02dcd-115">Ce membre est réservé à l'usage interne d'Outlook et n'est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="02dcd-115">This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
 <span data-ttu-id="02dcd-116">*MSCAP_SEL_RESTRICTION*</span><span class="sxs-lookup"><span data-stu-id="02dcd-116">*MSCAP_SEL_RESTRICTION*</span></span> 
  
> <span data-ttu-id="02dcd-117">Fonctionnalités de prise en charge des restrictions sur une banque.</span><span class="sxs-lookup"><span data-stu-id="02dcd-117">Capabilities about supporting restrictions on a store.</span></span>
    

