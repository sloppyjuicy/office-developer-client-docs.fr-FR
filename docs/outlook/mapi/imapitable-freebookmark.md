---
title: IMAPITableFreeBookmark
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.FreeBookmark
api_type:
- COM
ms.assetid: 797833f7-8295-41bc-8980-977e5f5e05e8
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: a1ad209ff127a34d7da5ca8dbe1f4a6656d32876
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409453"
---
# <a name="imapitablefreebookmark"></a><span data-ttu-id="63197-103">IMAPITable::FreeBookmark</span><span class="sxs-lookup"><span data-stu-id="63197-103">IMAPITable::FreeBookmark</span></span>

  
  
<span data-ttu-id="63197-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="63197-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="63197-105">Libère la mémoire associée à un signet.</span><span class="sxs-lookup"><span data-stu-id="63197-105">Releases the memory associated with a bookmark.</span></span>
  
```cpp
HRESULT FreeBookmark(
BOOKMARK bkPosition
);
```

## <a name="parameters"></a><span data-ttu-id="63197-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="63197-106">Parameters</span></span>

 <span data-ttu-id="63197-107">_bkPosition_</span><span class="sxs-lookup"><span data-stu-id="63197-107">_bkPosition_</span></span>
  
> <span data-ttu-id="63197-108">dans Signet à libérer, créé en appelant la méthode [IMAPITable:: CreateBookmark](imapitable-createbookmark.md) .</span><span class="sxs-lookup"><span data-stu-id="63197-108">[in] The bookmark to be freed, created by calling the [IMAPITable::CreateBookmark](imapitable-createbookmark.md) method.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="63197-109">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="63197-109">Return value</span></span>

<span data-ttu-id="63197-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="63197-110">S_OK</span></span> 
  
> <span data-ttu-id="63197-111">Le signet a été libéré avec succès.</span><span class="sxs-lookup"><span data-stu-id="63197-111">The bookmark was successfully freed.</span></span>
    
<span data-ttu-id="63197-112">MAPI_E_INVALID_BOOKMARK</span><span class="sxs-lookup"><span data-stu-id="63197-112">MAPI_E_INVALID_BOOKMARK</span></span> 
  
> <span data-ttu-id="63197-113">Le signet spécifié n'existe pas.</span><span class="sxs-lookup"><span data-stu-id="63197-113">The specified bookmark does not exist.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="63197-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="63197-114">Remarks</span></span>

<span data-ttu-id="63197-115">La méthode **IMAPITable:: FreeBookmark** libère un signet qui n'est plus nécessaire.</span><span class="sxs-lookup"><span data-stu-id="63197-115">The **IMAPITable::FreeBookmark** method releases a bookmark that is no longer needed.</span></span> <span data-ttu-id="63197-116">Le signet n'est plus valide après cet appel.</span><span class="sxs-lookup"><span data-stu-id="63197-116">The bookmark is no longer valid after this call.</span></span> <span data-ttu-id="63197-117">Chaque fois qu'un tableau est libéré de la mémoire, tous ses signets associés sont également publiés.</span><span class="sxs-lookup"><span data-stu-id="63197-117">Whenever a table is released from memory, all of its associated bookmarks are also released.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="63197-118">Remarques pour les responsables de l’implémentation</span><span class="sxs-lookup"><span data-stu-id="63197-118">Notes to implementers</span></span>

<span data-ttu-id="63197-119">Si l'appelant transmet l'un des trois signets prédéfinis dans le paramètre _bkPosition_ , ignorez la demande et renvoyez S_OK.</span><span class="sxs-lookup"><span data-stu-id="63197-119">If the caller passes one of the three predefined bookmarks in the  _bkPosition_ parameter, ignore the request and return S_OK.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="63197-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="63197-120">See also</span></span>



[<span data-ttu-id="63197-121">IMAPITable::CreateBookmark</span><span class="sxs-lookup"><span data-stu-id="63197-121">IMAPITable::CreateBookmark</span></span>](imapitable-createbookmark.md)
  
[<span data-ttu-id="63197-122">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="63197-122">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)

