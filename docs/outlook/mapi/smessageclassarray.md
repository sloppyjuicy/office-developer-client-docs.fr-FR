---
title: SMessageClassArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SMessageClassArray
api_type:
- COM
ms.assetid: 05f8c191-db2b-4174-8b3c-a9fdabfe6ac8
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 01b42c04244d35d72dd856222b4bab543b84db45
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339661"
---
# <a name="smessageclassarray"></a><span data-ttu-id="06975-103">SMessageClassArray</span><span class="sxs-lookup"><span data-stu-id="06975-103">SMessageClassArray</span></span>

  
  
<span data-ttu-id="06975-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="06975-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="06975-105">Contient un tableau de pointeurs vers des chaînes de classe de message.</span><span class="sxs-lookup"><span data-stu-id="06975-105">Contains an array of pointers to message class strings.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="06975-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="06975-106">Header file:</span></span>  <br/> |<span data-ttu-id="06975-107">MAPIForm. h</span><span class="sxs-lookup"><span data-stu-id="06975-107">Mapiform.h</span></span>  <br/> |
|<span data-ttu-id="06975-108">Macro connexe:</span><span class="sxs-lookup"><span data-stu-id="06975-108">Related macro:</span></span>  <br/> |[<span data-ttu-id="06975-109">CbMessageClassArray</span><span class="sxs-lookup"><span data-stu-id="06975-109">CbMessageClassArray</span></span>](cbmessageclassarray.md) <br/> |
   
```cpp
typedef struct 
{
  ULONG cValues;
  LPCSTR aMessageClass[MAPI_DIM];
} SMessageClassArray, FAR * LPSMESSAGECLASSARRAY;

```

## <a name="members"></a><span data-ttu-id="06975-110">Members</span><span class="sxs-lookup"><span data-stu-id="06975-110">Members</span></span>

 <span data-ttu-id="06975-111">**cValues**</span><span class="sxs-lookup"><span data-stu-id="06975-111">**cValues**</span></span>
  
> <span data-ttu-id="06975-112">Nombre de pointeurs de chaîne de classe de message dans le tableau.</span><span class="sxs-lookup"><span data-stu-id="06975-112">Count of message class string pointers in the array.</span></span>
    
 <span data-ttu-id="06975-113">**aMessageClass**</span><span class="sxs-lookup"><span data-stu-id="06975-113">**aMessageClass**</span></span>
  
> <span data-ttu-id="06975-114">Tableau de pointeurs vers des chaînes de classe de message.</span><span class="sxs-lookup"><span data-stu-id="06975-114">Array of pointers to message class strings.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="06975-115">Remarques</span><span class="sxs-lookup"><span data-stu-id="06975-115">Remarks</span></span>

<span data-ttu-id="06975-116">La structure **SMessageClassArray** est transmise en tant que paramètre dans les méthodes suivantes:</span><span class="sxs-lookup"><span data-stu-id="06975-116">The **SMessageClassArray** structure is passed as a parameter in the following methods:</span></span> 
  
- [<span data-ttu-id="06975-117">IMAPIFormContainer::ResolveMultipleMessageClasses</span><span class="sxs-lookup"><span data-stu-id="06975-117">IMAPIFormContainer::ResolveMultipleMessageClasses</span></span>](imapiformcontainer-resolvemultiplemessageclasses.md)
    
- [<span data-ttu-id="06975-118">IMAPIFormMgr::ResolveMultipleMessageClasses</span><span class="sxs-lookup"><span data-stu-id="06975-118">IMAPIFormMgr::ResolveMultipleMessageClasses</span></span>](imapiformmgr-resolvemultiplemessageclasses.md)
    
## <a name="see-also"></a><span data-ttu-id="06975-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="06975-119">See also</span></span>



[<span data-ttu-id="06975-120">Structures MAPI</span><span class="sxs-lookup"><span data-stu-id="06975-120">MAPI Structures</span></span>](mapi-structures.md)

