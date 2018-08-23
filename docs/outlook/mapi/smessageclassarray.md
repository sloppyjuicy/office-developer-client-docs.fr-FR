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
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: b2caa70600bd32234e38420f274bcd5c46ffb070
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578156"
---
# <a name="smessageclassarray"></a><span data-ttu-id="e6bca-103">SMessageClassArray</span><span class="sxs-lookup"><span data-stu-id="e6bca-103">SMessageClassArray</span></span>

  
  
<span data-ttu-id="e6bca-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e6bca-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e6bca-105">Contient un tableau de pointeurs vers des chaînes de classe de message.</span><span class="sxs-lookup"><span data-stu-id="e6bca-105">Contains an array of pointers to message class strings.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e6bca-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="e6bca-106">Header file:</span></span>  <br/> |<span data-ttu-id="e6bca-107">MAPIForm.h</span><span class="sxs-lookup"><span data-stu-id="e6bca-107">Mapiform.h</span></span>  <br/> |
|<span data-ttu-id="e6bca-108">Macro connexe :</span><span class="sxs-lookup"><span data-stu-id="e6bca-108">Related macro:</span></span>  <br/> |[<span data-ttu-id="e6bca-109">CbMessageClassArray</span><span class="sxs-lookup"><span data-stu-id="e6bca-109">CbMessageClassArray</span></span>](cbmessageclassarray.md) <br/> |
   
```cpp
typedef struct 
{
  ULONG cValues;
  LPCSTR aMessageClass[MAPI_DIM];
} SMessageClassArray, FAR * LPSMESSAGECLASSARRAY;

```

## <a name="members"></a><span data-ttu-id="e6bca-110">Members</span><span class="sxs-lookup"><span data-stu-id="e6bca-110">Members</span></span>

 <span data-ttu-id="e6bca-111">**cValues**</span><span class="sxs-lookup"><span data-stu-id="e6bca-111">**cValues**</span></span>
  
> <span data-ttu-id="e6bca-112">Nombre de pointeurs de chaîne de classe de message dans le tableau.</span><span class="sxs-lookup"><span data-stu-id="e6bca-112">Count of message class string pointers in the array.</span></span>
    
 <span data-ttu-id="e6bca-113">**aMessageClass**</span><span class="sxs-lookup"><span data-stu-id="e6bca-113">**aMessageClass**</span></span>
  
> <span data-ttu-id="e6bca-114">Tableau de pointeurs vers des chaînes de classe de message.</span><span class="sxs-lookup"><span data-stu-id="e6bca-114">Array of pointers to message class strings.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="e6bca-115">Remarques</span><span class="sxs-lookup"><span data-stu-id="e6bca-115">Remarks</span></span>

<span data-ttu-id="e6bca-116">La structure **SMessageClassArray** est transmise en tant que paramètre dans les méthodes suivantes :</span><span class="sxs-lookup"><span data-stu-id="e6bca-116">The **SMessageClassArray** structure is passed as a parameter in the following methods:</span></span> 
  
- [<span data-ttu-id="e6bca-117">IMAPIFormContainer::ResolveMultipleMessageClasses</span><span class="sxs-lookup"><span data-stu-id="e6bca-117">IMAPIFormContainer::ResolveMultipleMessageClasses</span></span>](imapiformcontainer-resolvemultiplemessageclasses.md)
    
- [<span data-ttu-id="e6bca-118">IMAPIFormMgr::ResolveMultipleMessageClasses</span><span class="sxs-lookup"><span data-stu-id="e6bca-118">IMAPIFormMgr::ResolveMultipleMessageClasses</span></span>](imapiformmgr-resolvemultiplemessageclasses.md)
    
## <a name="see-also"></a><span data-ttu-id="e6bca-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e6bca-119">See also</span></span>



[<span data-ttu-id="e6bca-120">Structures MAPI</span><span class="sxs-lookup"><span data-stu-id="e6bca-120">MAPI Structures</span></span>](mapi-structures.md)

