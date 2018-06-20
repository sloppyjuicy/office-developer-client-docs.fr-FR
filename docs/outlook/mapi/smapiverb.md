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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 4d060d62deb685b4691846c2b8e48a82ae3195ea
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787222"
---
# <a name="smapiverb"></a><span data-ttu-id="e30ca-103">SMAPIVerb</span><span class="sxs-lookup"><span data-stu-id="e30ca-103">SMAPIVerb</span></span>

  
  
<span data-ttu-id="e30ca-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="e30ca-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="e30ca-105">Décrit un verbe MAPI.</span><span class="sxs-lookup"><span data-stu-id="e30ca-105">Describes a MAPI verb.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e30ca-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="e30ca-106">Header file:</span></span>  <br/> |<span data-ttu-id="e30ca-107">MAPIForm.h</span><span class="sxs-lookup"><span data-stu-id="e30ca-107">Mapiform.h</span></span>  <br/> |
   
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

## <a name="members"></a><span data-ttu-id="e30ca-108">Membres</span><span class="sxs-lookup"><span data-stu-id="e30ca-108">Members</span></span>

 <span data-ttu-id="e30ca-109">**lVerb**</span><span class="sxs-lookup"><span data-stu-id="e30ca-109">**lVerb**</span></span>
  
> <span data-ttu-id="e30ca-110">Code représentant le verbe qui est transmis à [IMAPIForm::DoVerb](imapiform-doverb.md).</span><span class="sxs-lookup"><span data-stu-id="e30ca-110">Code representing the verb that is passed to [IMAPIForm::DoVerb](imapiform-doverb.md).</span></span> <span data-ttu-id="e30ca-111">Les verbes standard sont définies dans le fichier d’en-tête Exchform.h.</span><span class="sxs-lookup"><span data-stu-id="e30ca-111">Standard verbs are defined in the header file Exchform.h.</span></span>
    
 <span data-ttu-id="e30ca-112">**szVerbname**</span><span class="sxs-lookup"><span data-stu-id="e30ca-112">**szVerbname**</span></span>
  
> <span data-ttu-id="e30ca-113">Nom complet du verbe telle qu’elle apparaît dans le menu formulaire.</span><span class="sxs-lookup"><span data-stu-id="e30ca-113">Display name of the verb as it appears on the form menu.</span></span>
    
 <span data-ttu-id="e30ca-114">**fuFlags**</span><span class="sxs-lookup"><span data-stu-id="e30ca-114">**fuFlags**</span></span>
  
> <span data-ttu-id="e30ca-115">Indicateurs pour le verbe.</span><span class="sxs-lookup"><span data-stu-id="e30ca-115">Flags for the verb.</span></span>
    
 <span data-ttu-id="e30ca-116">**grfAttribs**</span><span class="sxs-lookup"><span data-stu-id="e30ca-116">**grfAttribs**</span></span>
  
> <span data-ttu-id="e30ca-117">Attributs du verbe.</span><span class="sxs-lookup"><span data-stu-id="e30ca-117">Attributes of the verb.</span></span> 
    
 <span data-ttu-id="e30ca-118">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="e30ca-118">**ulFlags**</span></span>
  
> <span data-ttu-id="e30ca-119">Indicateur indiquant le format du nom d’affichage du verbe.</span><span class="sxs-lookup"><span data-stu-id="e30ca-119">Flag indicating the format of the verb's display name.</span></span> <span data-ttu-id="e30ca-120">Vous pouvez définir l’indicateur suivant :</span><span class="sxs-lookup"><span data-stu-id="e30ca-120">The following flag can be set:</span></span>
    
<span data-ttu-id="e30ca-121">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="e30ca-121">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="e30ca-122">Le nom complet est au format Unicode.</span><span class="sxs-lookup"><span data-stu-id="e30ca-122">The display name is in Unicode format.</span></span> <span data-ttu-id="e30ca-123">Si l’indicateur MAPI_UNICODE n’est pas définie, le nom complet est au format ANSI.</span><span class="sxs-lookup"><span data-stu-id="e30ca-123">If the MAPI_UNICODE flag is not set, the display name is in ANSI format.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="e30ca-124">Remarques</span><span class="sxs-lookup"><span data-stu-id="e30ca-124">Remarks</span></span>

<span data-ttu-id="e30ca-125">La structure **SMAPIVerb** est transmise en tant que paramètre dans les méthodes suivantes :</span><span class="sxs-lookup"><span data-stu-id="e30ca-125">The **SMAPIVerb** structure is passed as a parameter in the following methods:</span></span> 
  
- [<span data-ttu-id="e30ca-126">IMAPIFormContainer::ResolveMultipleMessageClasses</span><span class="sxs-lookup"><span data-stu-id="e30ca-126">IMAPIFormContainer::ResolveMultipleMessageClasses</span></span>](imapiformcontainer-resolvemultiplemessageclasses.md)
    
- [<span data-ttu-id="e30ca-127">IMAPIFormMgr::ResolveMultipleMessageClasses</span><span class="sxs-lookup"><span data-stu-id="e30ca-127">IMAPIFormMgr::ResolveMultipleMessageClasses</span></span>](imapiformmgr-resolvemultiplemessageclasses.md)
    
## <a name="see-also"></a><span data-ttu-id="e30ca-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e30ca-128">See also</span></span>



[<span data-ttu-id="e30ca-129">CbMessageClassArray</span><span class="sxs-lookup"><span data-stu-id="e30ca-129">CbMessageClassArray</span></span>](cbmessageclassarray.md)


[<span data-ttu-id="e30ca-130">Structures MAPI</span><span class="sxs-lookup"><span data-stu-id="e30ca-130">MAPI Structures</span></span>](mapi-structures.md)

