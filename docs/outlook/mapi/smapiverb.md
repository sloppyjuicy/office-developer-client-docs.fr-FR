---
title: SMAPIVerb
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SMAPIVerb
api_type:
- COM
ms.assetid: 45066528-2447-4178-aaa3-7513ed0b3ba4
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 3ef284a2c036abb9eac10ecf33de4adbf61f3c54
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410958"
---
# <a name="smapiverb"></a><span data-ttu-id="bfe4e-103">SMAPIVerb</span><span class="sxs-lookup"><span data-stu-id="bfe4e-103">SMAPIVerb</span></span>

  
  
<span data-ttu-id="bfe4e-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bfe4e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bfe4e-105">Décrit un verbe MAPI.</span><span class="sxs-lookup"><span data-stu-id="bfe4e-105">Describes a MAPI verb.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="bfe4e-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="bfe4e-106">Header file:</span></span>  <br/> |<span data-ttu-id="bfe4e-107">Mapiform.h</span><span class="sxs-lookup"><span data-stu-id="bfe4e-107">Mapiform.h</span></span>  <br/> |
   
```cpp
typedef struct
{
  ULONG lVerb;
  LPSTR szVerbname;
  DWORD fuFlags;
  DWORD grfAttribs;
  ULONG ulFlags; /* Either 0 or MAPI_UNICODE */
} SMAPIVerb, FAR * LPMAPIVERB;

```

## <a name="members"></a><span data-ttu-id="bfe4e-108">Members</span><span class="sxs-lookup"><span data-stu-id="bfe4e-108">Members</span></span>

 <span data-ttu-id="bfe4e-109">**lVerb**</span><span class="sxs-lookup"><span data-stu-id="bfe4e-109">**lVerb**</span></span>
  
> <span data-ttu-id="bfe4e-110">Code représentant le verbe transmis à [IMAPIForm::D oVerb](imapiform-doverb.md).</span><span class="sxs-lookup"><span data-stu-id="bfe4e-110">Code representing the verb that is passed to [IMAPIForm::DoVerb](imapiform-doverb.md).</span></span> <span data-ttu-id="bfe4e-111">Les verbes standard sont définis dans le fichier d’en-tête Exchform.h.</span><span class="sxs-lookup"><span data-stu-id="bfe4e-111">Standard verbs are defined in the header file Exchform.h.</span></span>
    
 <span data-ttu-id="bfe4e-112">**szVerbname**</span><span class="sxs-lookup"><span data-stu-id="bfe4e-112">**szVerbname**</span></span>
  
> <span data-ttu-id="bfe4e-113">Nom complet du verbe tel qu’il apparaît dans le menu du formulaire.</span><span class="sxs-lookup"><span data-stu-id="bfe4e-113">Display name of the verb as it appears on the form menu.</span></span>
    
 <span data-ttu-id="bfe4e-114">**fuFlags**</span><span class="sxs-lookup"><span data-stu-id="bfe4e-114">**fuFlags**</span></span>
  
> <span data-ttu-id="bfe4e-115">Indicateurs du verbe.</span><span class="sxs-lookup"><span data-stu-id="bfe4e-115">Flags for the verb.</span></span>
    
 <span data-ttu-id="bfe4e-116">**grfAttribs**</span><span class="sxs-lookup"><span data-stu-id="bfe4e-116">**grfAttribs**</span></span>
  
> <span data-ttu-id="bfe4e-117">Attributs du verbe.</span><span class="sxs-lookup"><span data-stu-id="bfe4e-117">Attributes of the verb.</span></span> 
    
 <span data-ttu-id="bfe4e-118">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="bfe4e-118">**ulFlags**</span></span>
  
> <span data-ttu-id="bfe4e-119">Indicateur indiquant le format du nom complet du verbe.</span><span class="sxs-lookup"><span data-stu-id="bfe4e-119">Flag indicating the format of the verb's display name.</span></span> <span data-ttu-id="bfe4e-120">L’indicateur suivant peut être définie :</span><span class="sxs-lookup"><span data-stu-id="bfe4e-120">The following flag can be set:</span></span>
    
<span data-ttu-id="bfe4e-121">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="bfe4e-121">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="bfe4e-122">Le nom complet est au format Unicode.</span><span class="sxs-lookup"><span data-stu-id="bfe4e-122">The display name is in Unicode format.</span></span> <span data-ttu-id="bfe4e-123">Si l’MAPI_UNICODE n’est pas définie, le nom complet est au format ANSI.</span><span class="sxs-lookup"><span data-stu-id="bfe4e-123">If the MAPI_UNICODE flag is not set, the display name is in ANSI format.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="bfe4e-124">Remarques</span><span class="sxs-lookup"><span data-stu-id="bfe4e-124">Remarks</span></span>

<span data-ttu-id="bfe4e-125">La structure **SMAPIVerb** est transmise en tant que paramètre dans les méthodes suivantes :</span><span class="sxs-lookup"><span data-stu-id="bfe4e-125">The **SMAPIVerb** structure is passed as a parameter in the following methods:</span></span> 
  
- [<span data-ttu-id="bfe4e-126">IMAPIFormContainer::ResolveMultipleMessageClasses</span><span class="sxs-lookup"><span data-stu-id="bfe4e-126">IMAPIFormContainer::ResolveMultipleMessageClasses</span></span>](imapiformcontainer-resolvemultiplemessageclasses.md)
    
- [<span data-ttu-id="bfe4e-127">IMAPIFormMgr::ResolveMultipleMessageClasses</span><span class="sxs-lookup"><span data-stu-id="bfe4e-127">IMAPIFormMgr::ResolveMultipleMessageClasses</span></span>](imapiformmgr-resolvemultiplemessageclasses.md)
    
## <a name="see-also"></a><span data-ttu-id="bfe4e-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bfe4e-128">See also</span></span>



[<span data-ttu-id="bfe4e-129">CbMessageClassArray</span><span class="sxs-lookup"><span data-stu-id="bfe4e-129">CbMessageClassArray</span></span>](cbmessageclassarray.md)


[<span data-ttu-id="bfe4e-130">Structures MAPI</span><span class="sxs-lookup"><span data-stu-id="bfe4e-130">MAPI Structures</span></span>](mapi-structures.md)

