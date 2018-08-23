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
ms.openlocfilehash: 00c7560427ece58026030ce6895d60aec7cc5a2e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22570939"
---
# <a name="iid"></a><span data-ttu-id="eb454-103">IID</span><span class="sxs-lookup"><span data-stu-id="eb454-103">IID</span></span>

  
  
<span data-ttu-id="eb454-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="eb454-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="eb454-105">Décrit une structure [GUID](guid.md) utilisée pour décrire un identificateur pour l’interface MAPI.</span><span class="sxs-lookup"><span data-stu-id="eb454-105">Describes a [GUID](guid.md) structure used to describe an identifier for a MAPI interface.</span></span> 
  
```cpp
typedef struct _GUID
{
  unsigned long Data1;
  unsigned short Data2;
  unsigned short Data3;
  unsigned char Data4[8];
} GUID;

```

## <a name="members"></a><span data-ttu-id="eb454-106">Members</span><span class="sxs-lookup"><span data-stu-id="eb454-106">Members</span></span>

<span data-ttu-id="eb454-107">Voir la structure **GUID** .</span><span class="sxs-lookup"><span data-stu-id="eb454-107">See the **GUID** structure.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="eb454-108">Remarques</span><span class="sxs-lookup"><span data-stu-id="eb454-108">Remarks</span></span>

<span data-ttu-id="eb454-109">Une structure **IID** est utilisée pour identifier de manière unique une interface MAPI et pour associer une interface donnée à un objet.</span><span class="sxs-lookup"><span data-stu-id="eb454-109">An **IID** structure is used to uniquely identify a MAPI interface and to associate a particular interface with an object.</span></span> <span data-ttu-id="eb454-110">Par exemple, lorsqu’un client appelle [IMAPISession::OpenEntry](imapisession-openentry.md) pour ouvrir un dossier, le client définit le paramètre _lpInterface_ pour pointer vers un **IID** qui représente l’interface [IMAPIFolder](imapifolderimapicontainer.md) .</span><span class="sxs-lookup"><span data-stu-id="eb454-110">For example, when a client calls [IMAPISession::OpenEntry](imapisession-openentry.md) to open a folder, the client sets the  _lpInterface_ parameter to point to an **IID** representing the [IMAPIFolder](imapifolderimapicontainer.md) interface.</span></span> <span data-ttu-id="eb454-111">MAPI définit **IMAPIFolderIID** à IID_IMAPIFolder.</span><span class="sxs-lookup"><span data-stu-id="eb454-111">MAPI defines the **IMAPIFolderIID** to be IID_IMAPIFolder.</span></span> <span data-ttu-id="eb454-112">Structures **IID** sont également utilisés pour identifier de manière unique les interfaces OLE.</span><span class="sxs-lookup"><span data-stu-id="eb454-112">**IID** structures are also used to uniquely identify OLE interfaces.</span></span> 
  
<span data-ttu-id="eb454-113">Toutes les structures **IID** spécifiques pour les interfaces MAPI sont définies dans le fichier d’en-tête Mapiguid.h.</span><span class="sxs-lookup"><span data-stu-id="eb454-113">All of the specific **IID** structures for the MAPI interfaces are defined in the Mapiguid.h header file.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="eb454-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="eb454-114">See also</span></span>



[<span data-ttu-id="eb454-115">GUID</span><span class="sxs-lookup"><span data-stu-id="eb454-115">GUID</span></span>](guid.md)


[<span data-ttu-id="eb454-116">Structures MAPI</span><span class="sxs-lookup"><span data-stu-id="eb454-116">MAPI Structures</span></span>](mapi-structures.md)

