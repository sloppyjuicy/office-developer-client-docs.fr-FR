---
title: FLATENTRY
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FLATENTRY
api_type:
- COM
ms.assetid: 03e53e08-9113-4101-84c9-ccf6d43127f6
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: cf84c7d94e67da0ce7453829042e7be0d4e313f1
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22585548"
---
# <a name="flatentry"></a><span data-ttu-id="95f01-103">FLATENTRY</span><span class="sxs-lookup"><span data-stu-id="95f01-103">FLATENTRY</span></span>

  
  
<span data-ttu-id="95f01-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="95f01-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="95f01-105">Une structure [ENTRYID](entryid.md) plus un nombre d’octets qui spécifie la taille de la structure de la **propriété ENTRYID** .</span><span class="sxs-lookup"><span data-stu-id="95f01-105">An [ENTRYID](entryid.md) structure plus a byte count that specifies the size of the **ENTRYID** structure.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="95f01-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="95f01-106">Header file:</span></span>  <br/> |<span data-ttu-id="95f01-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="95f01-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="95f01-108">Macros connexes :</span><span class="sxs-lookup"><span data-stu-id="95f01-108">Related macros:</span></span>  <br/> |<span data-ttu-id="95f01-109">[cbFLATENTRY](cbflatentry.md), [CbNewFLATENTRY](cbnewflatentry.md)</span><span class="sxs-lookup"><span data-stu-id="95f01-109">[cbFLATENTRY](cbflatentry.md), [CbNewFLATENTRY](cbnewflatentry.md)</span></span> <br/> |
   
```cpp
typedef struct
{
  ULONG cb;
  BYTE abEntry[MAPI_DIM];
} FLATENTRY, FAR *LPFLATENTRY;

```

## <a name="members"></a><span data-ttu-id="95f01-110">Members</span><span class="sxs-lookup"><span data-stu-id="95f01-110">Members</span></span>

 <span data-ttu-id="95f01-111">**cb**</span><span class="sxs-lookup"><span data-stu-id="95f01-111">**cb**</span></span>
  
> <span data-ttu-id="95f01-112">Nombre d’octets dans le membre **abEntry** .</span><span class="sxs-lookup"><span data-stu-id="95f01-112">Count of bytes in the **abEntry** member.</span></span> 
    
 <span data-ttu-id="95f01-113">**abEntry**</span><span class="sxs-lookup"><span data-stu-id="95f01-113">**abEntry**</span></span>
  
> <span data-ttu-id="95f01-114">L’identificateur d’entrée complet qui inclut le tableau des indicateurs et des données binaires.</span><span class="sxs-lookup"><span data-stu-id="95f01-114">The complete entry identifier that includes the array of flags and binary data.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="95f01-115">Remarques</span><span class="sxs-lookup"><span data-stu-id="95f01-115">Remarks</span></span>

<span data-ttu-id="95f01-116">Une structure **FLATENTRY** ressemble à une structure [ENTRYID](entryid.md) .</span><span class="sxs-lookup"><span data-stu-id="95f01-116">A **FLATENTRY** structure resembles an [ENTRYID](entryid.md) structure.</span></span> <span data-ttu-id="95f01-117">Toutefois, il existe quelques différences :</span><span class="sxs-lookup"><span data-stu-id="95f01-117">However, there are some differences:</span></span> 
  
- <span data-ttu-id="95f01-118">Une structure **FLATENTRY** stocke la taille de l’identificateur d’entrée. **Propriété ENTRYID** n’est pas.</span><span class="sxs-lookup"><span data-stu-id="95f01-118">A **FLATENTRY** structure stores the size of the entry identifier; **ENTRYID** does not.</span></span> 
    
- <span data-ttu-id="95f01-119">Une structure **FLATENTRY** stocke les données d’indicateur avec le reste de l’identificateur d’entrée. **Propriété ENTRYID** les stocke séparément.</span><span class="sxs-lookup"><span data-stu-id="95f01-119">A **FLATENTRY** structure stores the flag data together with the rest of the entry identifier; **ENTRYID** stores them separately.</span></span> 
    
- <span data-ttu-id="95f01-120">Structure **FLATENTRY** est utilisée pour stocker un identificateur d’entrée dans un fichier ou passez-la dans un flux d’octets, tandis que d’une structure **ENTRYID** est utilisée par les méthodes d’interface [IMAPIProp](imapipropiunknown.md) et par les méthodes **OpenEntry** suivantes : [IABLogon : : OpenEntry](iablogon-openentry.md), [IAddrBook::OpenEntry](iaddrbook-openentry.md), [IMAPIContainer::OpenEntry](imapicontainer-openentry.md), [IMAPISession::OpenEntry](imapisession-openentry.md), [IMAPISupport::OpenEntry](imapisupport-openentry.md), [IMsgStore::OpenEntry](imsgstore-openentry.md), [IMSLogon::OpenEntry](imslogon-openentry.md)</span><span class="sxs-lookup"><span data-stu-id="95f01-120">A **FLATENTRY** structure is used to store an entry identifier in a file or pass it in a stream of bytes whereas an **ENTRYID** structure is used by the [IMAPIProp](imapipropiunknown.md) interface methods and by the following **OpenEntry** methods: [IABLogon::OpenEntry](iablogon-openentry.md), [IAddrBook::OpenEntry](iaddrbook-openentry.md), [IMAPIContainer::OpenEntry](imapicontainer-openentry.md), [IMAPISession::OpenEntry](imapisession-openentry.md), [IMAPISupport::OpenEntry](imapisupport-openentry.md), [IMsgStore::OpenEntry](imsgstore-openentry.md), [IMSLogon::OpenEntry](imslogon-openentry.md)</span></span>
    
- <span data-ttu-id="95f01-121">Une structure **FLATENTRY** sert à stocker un identificateur d’entrée dans un fichier ou passez-la dans un flux d’octets.</span><span class="sxs-lookup"><span data-stu-id="95f01-121">A **FLATENTRY** structure is used to store an entry identifier in a file or pass it in a stream of bytes.</span></span> <span data-ttu-id="95f01-122">Une structure **ENTRYID** est utilisée pour stocker un identificateur d’entrée sur le disque.</span><span class="sxs-lookup"><span data-stu-id="95f01-122">An **ENTRYID** structure is used to store an entry identifier on disk.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="95f01-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="95f01-123">See also</span></span>



[<span data-ttu-id="95f01-124">ENTRYID</span><span class="sxs-lookup"><span data-stu-id="95f01-124">ENTRYID</span></span>](entryid.md)


[<span data-ttu-id="95f01-125">Structures MAPI</span><span class="sxs-lookup"><span data-stu-id="95f01-125">MAPI Structures</span></span>](mapi-structures.md)

