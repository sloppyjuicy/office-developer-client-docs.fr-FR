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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 01b42c04244d35d72dd856222b4bab543b84db45
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412694"
---
# <a name="smessageclassarray"></a><span data-ttu-id="a5d85-103">SMessageClassArray</span><span class="sxs-lookup"><span data-stu-id="a5d85-103">SMessageClassArray</span></span>

  
  
<span data-ttu-id="a5d85-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a5d85-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a5d85-105">Contient un tableau de pointeurs vers des chaînes de classe de message.</span><span class="sxs-lookup"><span data-stu-id="a5d85-105">Contains an array of pointers to message class strings.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a5d85-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="a5d85-106">Header file:</span></span>  <br/> |<span data-ttu-id="a5d85-107">Mapiform.h</span><span class="sxs-lookup"><span data-stu-id="a5d85-107">Mapiform.h</span></span>  <br/> |
|<span data-ttu-id="a5d85-108">Macro associée :</span><span class="sxs-lookup"><span data-stu-id="a5d85-108">Related macro:</span></span>  <br/> |[<span data-ttu-id="a5d85-109">CbMessageClassArray</span><span class="sxs-lookup"><span data-stu-id="a5d85-109">CbMessageClassArray</span></span>](cbmessageclassarray.md) <br/> |
   
```cpp
typedef struct 
{
  ULONG cValues;
  LPCSTR aMessageClass[MAPI_DIM];
} SMessageClassArray, FAR * LPSMESSAGECLASSARRAY;

```

## <a name="members"></a><span data-ttu-id="a5d85-110">Members</span><span class="sxs-lookup"><span data-stu-id="a5d85-110">Members</span></span>

 <span data-ttu-id="a5d85-111">**cValues**</span><span class="sxs-lookup"><span data-stu-id="a5d85-111">**cValues**</span></span>
  
> <span data-ttu-id="a5d85-112">Nombre de pointeurs de chaîne de classe de message dans le tableau.</span><span class="sxs-lookup"><span data-stu-id="a5d85-112">Count of message class string pointers in the array.</span></span>
    
 <span data-ttu-id="a5d85-113">**aMessageClass**</span><span class="sxs-lookup"><span data-stu-id="a5d85-113">**aMessageClass**</span></span>
  
> <span data-ttu-id="a5d85-114">Tableau de pointeurs vers des chaînes de classe de message.</span><span class="sxs-lookup"><span data-stu-id="a5d85-114">Array of pointers to message class strings.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="a5d85-115">Remarques</span><span class="sxs-lookup"><span data-stu-id="a5d85-115">Remarks</span></span>

<span data-ttu-id="a5d85-116">La structure **SMessageClassArray** est passée en tant que paramètre dans les méthodes suivantes :</span><span class="sxs-lookup"><span data-stu-id="a5d85-116">The **SMessageClassArray** structure is passed as a parameter in the following methods:</span></span> 
  
- [<span data-ttu-id="a5d85-117">IMAPIFormContainer::ResolveMultipleMessageClasses</span><span class="sxs-lookup"><span data-stu-id="a5d85-117">IMAPIFormContainer::ResolveMultipleMessageClasses</span></span>](imapiformcontainer-resolvemultiplemessageclasses.md)
    
- [<span data-ttu-id="a5d85-118">IMAPIFormMgr::ResolveMultipleMessageClasses</span><span class="sxs-lookup"><span data-stu-id="a5d85-118">IMAPIFormMgr::ResolveMultipleMessageClasses</span></span>](imapiformmgr-resolvemultiplemessageclasses.md)
    
## <a name="see-also"></a><span data-ttu-id="a5d85-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a5d85-119">See also</span></span>



[<span data-ttu-id="a5d85-120">Structures MAPI</span><span class="sxs-lookup"><span data-stu-id="a5d85-120">MAPI Structures</span></span>](mapi-structures.md)

