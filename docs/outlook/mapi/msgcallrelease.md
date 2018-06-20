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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: aaa1adaa170349c3df3a2256802a502cb2512b20
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784893"
---
# <a name="msgcallrelease"></a><span data-ttu-id="e6249-103">MSGCALLRELEASE</span><span class="sxs-lookup"><span data-stu-id="e6249-103">MSGCALLRELEASE</span></span>

  
  
<span data-ttu-id="e6249-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="e6249-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="e6249-105">Définit une fonction de rappel que vous pouvez libérer une interface **IStorage** après la version finale d’un objet **IMessage** greffée il avec la fonction [OpenIMsgOnIStg](openimsgonistg.md) .</span><span class="sxs-lookup"><span data-stu-id="e6249-105">Defines a callback function that can free an **IStorage** interface after the final release of an **IMessage** object built on top of it with the [OpenIMsgOnIStg](openimsgonistg.md) function.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e6249-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="e6249-106">Header file:</span></span>  <br/> |<span data-ttu-id="e6249-107">IMessage.h</span><span class="sxs-lookup"><span data-stu-id="e6249-107">Imessage.h</span></span>  <br/> |
|<span data-ttu-id="e6249-108">Fonction implémentée par :</span><span class="sxs-lookup"><span data-stu-id="e6249-108">Defined function implemented by:</span></span>  <br/> |<span data-ttu-id="e6249-109">Les applications clientes et des fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="e6249-109">Client applications and service providers</span></span>  <br/> |
|<span data-ttu-id="e6249-110">Fonction appelée par :</span><span class="sxs-lookup"><span data-stu-id="e6249-110">Defined function called by:</span></span>  <br/> |<span data-ttu-id="e6249-111">MAPI</span><span class="sxs-lookup"><span data-stu-id="e6249-111">MAPI</span></span>  <br/> |
   
```cpp
typedef void (STDAPICALLTYPE MSGCALLRELEASE)(
  ULONG  ulCallerData,
  LPMESSAGE  lpMessage );
```

## <a name="parameters"></a><span data-ttu-id="e6249-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e6249-112">Parameters</span></span>

 <span data-ttu-id="e6249-113">_ulCallerData_</span><span class="sxs-lookup"><span data-stu-id="e6249-113">_ulCallerData_</span></span>
  
> <span data-ttu-id="e6249-114">[in] Contient des informations d’application appelant sur l’interface **IMessage** .</span><span class="sxs-lookup"><span data-stu-id="e6249-114">[in] Contains calling application information about the **IMessage** interface.</span></span> 
    
 <span data-ttu-id="e6249-115">_lpMessage_</span><span class="sxs-lookup"><span data-stu-id="e6249-115">_lpMessage_</span></span>
  
> <span data-ttu-id="e6249-116">[in] Pointeur vers le message de niveau supérieur et les pièces jointes qui ont été publiées.</span><span class="sxs-lookup"><span data-stu-id="e6249-116">[in] Pointer to the top-level message and attachments that have been released.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="e6249-117">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="e6249-117">Return value</span></span>

<span data-ttu-id="e6249-118">Aucun.</span><span class="sxs-lookup"><span data-stu-id="e6249-118">None.</span></span>
  

