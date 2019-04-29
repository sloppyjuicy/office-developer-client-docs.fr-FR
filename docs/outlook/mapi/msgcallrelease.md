---
title: MSGCALLRELEASE
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.MSGCALLRELEASE
api_type:
- COM
ms.assetid: 23c08597-41f0-4f48-a63e-79962fa812bc
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 9ffaab1e9cc381be2abfb389f4b72067dca2438b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405911"
---
# <a name="msgcallrelease"></a><span data-ttu-id="ea467-103">MSGCALLRELEASE</span><span class="sxs-lookup"><span data-stu-id="ea467-103">MSGCALLRELEASE</span></span>

  
  
<span data-ttu-id="ea467-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ea467-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ea467-105">Définit une fonction de rappel qui peut libérer une interface **IStorage** après la publication de la version finale d'un objet **IMessage** basée dessus avec la fonction [OpenIMsgOnIStg](openimsgonistg.md) .</span><span class="sxs-lookup"><span data-stu-id="ea467-105">Defines a callback function that can free an **IStorage** interface after the final release of an **IMessage** object built on top of it with the [OpenIMsgOnIStg](openimsgonistg.md) function.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ea467-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="ea467-106">Header file:</span></span>  <br/> |<span data-ttu-id="ea467-107">IMessage. h</span><span class="sxs-lookup"><span data-stu-id="ea467-107">Imessage.h</span></span>  <br/> |
|<span data-ttu-id="ea467-108">Fonction définie implémentée par:</span><span class="sxs-lookup"><span data-stu-id="ea467-108">Defined function implemented by:</span></span>  <br/> |<span data-ttu-id="ea467-109">Applications clientes et fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="ea467-109">Client applications and service providers</span></span>  <br/> |
|<span data-ttu-id="ea467-110">Fonction définie appelée par:</span><span class="sxs-lookup"><span data-stu-id="ea467-110">Defined function called by:</span></span>  <br/> |<span data-ttu-id="ea467-111">MAPI</span><span class="sxs-lookup"><span data-stu-id="ea467-111">MAPI</span></span>  <br/> |
   
```cpp
typedef void (STDAPICALLTYPE MSGCALLRELEASE)(
  ULONG  ulCallerData,
  LPMESSAGE  lpMessage );
```

## <a name="parameters"></a><span data-ttu-id="ea467-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ea467-112">Parameters</span></span>

 <span data-ttu-id="ea467-113">_ulCallerData_</span><span class="sxs-lookup"><span data-stu-id="ea467-113">_ulCallerData_</span></span>
  
> <span data-ttu-id="ea467-114">dans Contient des informations sur l'application appelante à propos de l'interface **IMessage** .</span><span class="sxs-lookup"><span data-stu-id="ea467-114">[in] Contains calling application information about the **IMessage** interface.</span></span> 
    
 <span data-ttu-id="ea467-115">_lpMessage_</span><span class="sxs-lookup"><span data-stu-id="ea467-115">_lpMessage_</span></span>
  
> <span data-ttu-id="ea467-116">dans Pointeur vers le message de niveau supérieur et pièces jointes qui ont été publiées.</span><span class="sxs-lookup"><span data-stu-id="ea467-116">[in] Pointer to the top-level message and attachments that have been released.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="ea467-117">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="ea467-117">Return value</span></span>

<span data-ttu-id="ea467-118">Aucun.</span><span class="sxs-lookup"><span data-stu-id="ea467-118">None.</span></span>
  

