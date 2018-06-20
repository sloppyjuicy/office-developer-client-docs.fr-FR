---
title: SMAPIVerbArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SMAPIVerbArray
api_type:
- COM
ms.assetid: 8736f75c-3e95-42dd-9bc1-2f0bd23c4a02
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 1767c86cb5390572b95530060f2295034ed35f43
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787218"
---
# <a name="smapiverbarray"></a><span data-ttu-id="fd521-103">SMAPIVerbArray</span><span class="sxs-lookup"><span data-stu-id="fd521-103">SMAPIVerbArray</span></span>

  
  
<span data-ttu-id="fd521-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="fd521-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="fd521-105">Contient un tableau de structures [SMAPIVerb](smapiverb.md) qui décrivent les verbes MAPI.</span><span class="sxs-lookup"><span data-stu-id="fd521-105">Contains an array of [SMAPIVerb](smapiverb.md) structures that describe MAPI verbs.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="fd521-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="fd521-106">Header file:</span></span>  <br/> |<span data-ttu-id="fd521-107">MAPIForm.h</span><span class="sxs-lookup"><span data-stu-id="fd521-107">Mapiform.h</span></span>  <br/> |
|<span data-ttu-id="fd521-108">Macro connexe :</span><span class="sxs-lookup"><span data-stu-id="fd521-108">Related macro:</span></span>  <br/> |[<span data-ttu-id="fd521-109">CbMAPIVerbArray</span><span class="sxs-lookup"><span data-stu-id="fd521-109">CbMAPIVerbArray</span></span>](cbmapiverbarray.md) <br/> |
   
```cpp
typedef struct
{
  ULONG cMAPIVerb;
  SMAPIVerb aMAPIVerb[MAPI_DIM];
} SMAPIVerbArray, FAR * LPMAPIVERBARRAY;

```

## <a name="members"></a><span data-ttu-id="fd521-110">Membres</span><span class="sxs-lookup"><span data-stu-id="fd521-110">Members</span></span>

 <span data-ttu-id="fd521-111">**cForms**</span><span class="sxs-lookup"><span data-stu-id="fd521-111">**cForms**</span></span>
  
> <span data-ttu-id="fd521-112">Nombre de verbes dans le tableau.</span><span class="sxs-lookup"><span data-stu-id="fd521-112">Count of verbs in the array.</span></span>
    
 <span data-ttu-id="fd521-113">**aFormInfo**</span><span class="sxs-lookup"><span data-stu-id="fd521-113">**aFormInfo**</span></span>
  
> <span data-ttu-id="fd521-114">Tableau des verbes MAPI.</span><span class="sxs-lookup"><span data-stu-id="fd521-114">Array of MAPI verbs.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="fd521-115">Remarques</span><span class="sxs-lookup"><span data-stu-id="fd521-115">Remarks</span></span>

<span data-ttu-id="fd521-116">La structure **SMAPIVerbArray** est transmise en tant que paramètre dans la méthode [IMAPIFormInfo::CalcVerbSet](imapiforminfo-calcverbset.md) .</span><span class="sxs-lookup"><span data-stu-id="fd521-116">The **SMAPIVerbArray** structure is passed as a parameter in the [IMAPIFormInfo::CalcVerbSet](imapiforminfo-calcverbset.md) method.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="fd521-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fd521-117">See also</span></span>



[<span data-ttu-id="fd521-118">SMAPIVerb</span><span class="sxs-lookup"><span data-stu-id="fd521-118">SMAPIVerb</span></span>](smapiverb.md)


[<span data-ttu-id="fd521-119">Structures MAPI</span><span class="sxs-lookup"><span data-stu-id="fd521-119">MAPI Structures</span></span>](mapi-structures.md)

