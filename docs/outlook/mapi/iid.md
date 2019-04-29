---
title: IID
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.IID
api_type:
- COM
ms.assetid: fa5498ab-2f8a-42f8-ba9d-1d555768594f
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 5605de7dbcc18197748713bcf909839690d7259f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411595"
---
# <a name="iid"></a><span data-ttu-id="e5fa5-103">IID</span><span class="sxs-lookup"><span data-stu-id="e5fa5-103">IID</span></span>

  
  
<span data-ttu-id="e5fa5-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e5fa5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e5fa5-105">Décrit une structure [GUID](guid.md) utilisée pour décrire un identificateur pour une interface MAPI.</span><span class="sxs-lookup"><span data-stu-id="e5fa5-105">Describes a [GUID](guid.md) structure used to describe an identifier for a MAPI interface.</span></span> 
  
```cpp
typedef struct _GUID
{
  unsigned long Data1;
  unsigned short Data2;
  unsigned short Data3;
  unsigned char Data4[8];
} GUID;

```

## <a name="members"></a><span data-ttu-id="e5fa5-106">Members</span><span class="sxs-lookup"><span data-stu-id="e5fa5-106">Members</span></span>

<span data-ttu-id="e5fa5-107">Voir la structure du **GUID** .</span><span class="sxs-lookup"><span data-stu-id="e5fa5-107">See the **GUID** structure.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="e5fa5-108">Remarques</span><span class="sxs-lookup"><span data-stu-id="e5fa5-108">Remarks</span></span>

<span data-ttu-id="e5fa5-109">Une structure d' **IID** est utilisée pour identifier une interface MAPI de manière unique et associer une interface particulière à un objet.</span><span class="sxs-lookup"><span data-stu-id="e5fa5-109">An **IID** structure is used to uniquely identify a MAPI interface and to associate a particular interface with an object.</span></span> <span data-ttu-id="e5fa5-110">Par exemple, lorsqu'un client appelle [IMAPISession:: OpenEntry](imapisession-openentry.md) pour ouvrir un dossier, le client définit le paramètre _lpInterface_ de sorte qu'il pointe vers un **IID** représentant l'interface [IMAPIFolder](imapifolderimapicontainer.md) .</span><span class="sxs-lookup"><span data-stu-id="e5fa5-110">For example, when a client calls [IMAPISession::OpenEntry](imapisession-openentry.md) to open a folder, the client sets the  _lpInterface_ parameter to point to an **IID** representing the [IMAPIFolder](imapifolderimapicontainer.md) interface.</span></span> <span data-ttu-id="e5fa5-111">MAPI définit le **IMAPIFolderIID** à IID_IMAPIFolder.</span><span class="sxs-lookup"><span data-stu-id="e5fa5-111">MAPI defines the **IMAPIFolderIID** to be IID_IMAPIFolder.</span></span> <span data-ttu-id="e5fa5-112">Les structures **IID** sont également utilisées pour identifier les interfaces OLE de manière unique.</span><span class="sxs-lookup"><span data-stu-id="e5fa5-112">**IID** structures are also used to uniquely identify OLE interfaces.</span></span> 
  
<span data-ttu-id="e5fa5-113">Toutes les structures d' **IID** spécifiques pour les interfaces MAPI sont définies dans le fichier d'en-tête Mapiguid. h.</span><span class="sxs-lookup"><span data-stu-id="e5fa5-113">All of the specific **IID** structures for the MAPI interfaces are defined in the Mapiguid.h header file.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="e5fa5-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e5fa5-114">See also</span></span>



[<span data-ttu-id="e5fa5-115">GUID</span><span class="sxs-lookup"><span data-stu-id="e5fa5-115">GUID</span></span>](guid.md)


[<span data-ttu-id="e5fa5-116">Structures MAPI</span><span class="sxs-lookup"><span data-stu-id="e5fa5-116">MAPI Structures</span></span>](mapi-structures.md)

