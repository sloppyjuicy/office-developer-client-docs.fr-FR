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
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: e9a1c416cbf992c9cbcfb5de42d302ff16e7f521
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573186"
---
# <a name="msgcallrelease"></a><span data-ttu-id="34c44-103">MSGCALLRELEASE</span><span class="sxs-lookup"><span data-stu-id="34c44-103">MSGCALLRELEASE</span></span>

  
  
<span data-ttu-id="34c44-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="34c44-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="34c44-105">Définit une fonction de rappel que vous pouvez libérer une interface **IStorage** après la version finale d’un objet **IMessage** greffée il avec la fonction [OpenIMsgOnIStg](openimsgonistg.md) .</span><span class="sxs-lookup"><span data-stu-id="34c44-105">Defines a callback function that can free an **IStorage** interface after the final release of an **IMessage** object built on top of it with the [OpenIMsgOnIStg](openimsgonistg.md) function.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="34c44-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="34c44-106">Header file:</span></span>  <br/> |<span data-ttu-id="34c44-107">IMessage.h</span><span class="sxs-lookup"><span data-stu-id="34c44-107">Imessage.h</span></span>  <br/> |
|<span data-ttu-id="34c44-108">Fonction implémentée par :</span><span class="sxs-lookup"><span data-stu-id="34c44-108">Defined function implemented by:</span></span>  <br/> |<span data-ttu-id="34c44-109">Les applications clientes et des fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="34c44-109">Client applications and service providers</span></span>  <br/> |
|<span data-ttu-id="34c44-110">Fonction appelée par :</span><span class="sxs-lookup"><span data-stu-id="34c44-110">Defined function called by:</span></span>  <br/> |<span data-ttu-id="34c44-111">MAPI</span><span class="sxs-lookup"><span data-stu-id="34c44-111">MAPI</span></span>  <br/> |
   
```cpp
typedef void (STDAPICALLTYPE MSGCALLRELEASE)(
  ULONG  ulCallerData,
  LPMESSAGE  lpMessage );
```

## <a name="parameters"></a><span data-ttu-id="34c44-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="34c44-112">Parameters</span></span>

 <span data-ttu-id="34c44-113">_ulCallerData_</span><span class="sxs-lookup"><span data-stu-id="34c44-113">_ulCallerData_</span></span>
  
> <span data-ttu-id="34c44-114">[in] Contient des informations d’application appelant sur l’interface **IMessage** .</span><span class="sxs-lookup"><span data-stu-id="34c44-114">[in] Contains calling application information about the **IMessage** interface.</span></span> 
    
 <span data-ttu-id="34c44-115">_lpMessage_</span><span class="sxs-lookup"><span data-stu-id="34c44-115">_lpMessage_</span></span>
  
> <span data-ttu-id="34c44-116">[in] Pointeur vers le message de niveau supérieur et les pièces jointes qui ont été publiées.</span><span class="sxs-lookup"><span data-stu-id="34c44-116">[in] Pointer to the top-level message and attachments that have been released.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="34c44-117">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="34c44-117">Return value</span></span>

<span data-ttu-id="34c44-118">Aucun.</span><span class="sxs-lookup"><span data-stu-id="34c44-118">None.</span></span>
  

