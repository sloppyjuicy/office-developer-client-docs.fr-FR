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
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: d6621e2bcd7831016efd7ac43f93ef83aaf41c29
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784084"
---
# <a name="imapitablefreebookmark"></a><span data-ttu-id="1d077-103">IMAPITable::FreeBookmark</span><span class="sxs-lookup"><span data-stu-id="1d077-103">IMAPITable::FreeBookmark</span></span>

  
  
<span data-ttu-id="1d077-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="1d077-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="1d077-105">Libère la mémoire associée à un signet.</span><span class="sxs-lookup"><span data-stu-id="1d077-105">Releases the memory associated with a bookmark.</span></span>
  
```cpp
HRESULT FreeBookmark(
BOOKMARK bkPosition
);
```

## <a name="parameters"></a><span data-ttu-id="1d077-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1d077-106">Parameters</span></span>

 <span data-ttu-id="1d077-107">_bkPosition_</span><span class="sxs-lookup"><span data-stu-id="1d077-107">_bkPosition_</span></span>
  
> <span data-ttu-id="1d077-108">[in] Le signet afin d’être libérée, créé en appelant la méthode [IMAPITable::CreateBookmark](imapitable-createbookmark.md) .</span><span class="sxs-lookup"><span data-stu-id="1d077-108">[in] The bookmark to be freed, created by calling the [IMAPITable::CreateBookmark](imapitable-createbookmark.md) method.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="1d077-109">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="1d077-109">Return value</span></span>

<span data-ttu-id="1d077-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="1d077-110">S_OK</span></span> 
  
> <span data-ttu-id="1d077-111">Le signet a été libéré avec succès.</span><span class="sxs-lookup"><span data-stu-id="1d077-111">The bookmark was successfully freed.</span></span>
    
<span data-ttu-id="1d077-112">MAPI_E_INVALID_BOOKMARK</span><span class="sxs-lookup"><span data-stu-id="1d077-112">MAPI_E_INVALID_BOOKMARK</span></span> 
  
> <span data-ttu-id="1d077-113">Le signet spécifié n’existe pas.</span><span class="sxs-lookup"><span data-stu-id="1d077-113">The specified bookmark does not exist.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="1d077-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="1d077-114">Remarks</span></span>

<span data-ttu-id="1d077-115">La méthode **IMAPITable::FreeBookmark** libère un signet qui n’est plus nécessaire.</span><span class="sxs-lookup"><span data-stu-id="1d077-115">The **IMAPITable::FreeBookmark** method releases a bookmark that is no longer needed.</span></span> <span data-ttu-id="1d077-116">Le signet n’est plus valide après cet appel.</span><span class="sxs-lookup"><span data-stu-id="1d077-116">The bookmark is no longer valid after this call.</span></span> <span data-ttu-id="1d077-117">Chaque fois qu’une table est libérée de la mémoire, tous ses signets associés sont également libérées.</span><span class="sxs-lookup"><span data-stu-id="1d077-117">Whenever a table is released from memory, all of its associated bookmarks are also released.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="1d077-118">Remarques destinées aux responsables de l’implémentation</span><span class="sxs-lookup"><span data-stu-id="1d077-118">Notes to implementers</span></span>

<span data-ttu-id="1d077-119">Si l’appelant transmet une des trois signets prédéfinis dans le paramètre _bkPosition_ , ignorer la demande et qu’elles retournent S_OK.</span><span class="sxs-lookup"><span data-stu-id="1d077-119">If the caller passes one of the three predefined bookmarks in the  _bkPosition_ parameter, ignore the request and return S_OK.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="1d077-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1d077-120">See also</span></span>



[<span data-ttu-id="1d077-121">IMAPITable::CreateBookmark</span><span class="sxs-lookup"><span data-stu-id="1d077-121">IMAPITable::CreateBookmark</span></span>](imapitable-createbookmark.md)
  
[<span data-ttu-id="1d077-122">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="1d077-122">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)

