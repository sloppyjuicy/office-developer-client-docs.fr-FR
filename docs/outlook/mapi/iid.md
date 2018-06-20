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
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: a0e859ac0f8bcc3bd83e336c85da21f1251efcb5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783680"
---
# <a name="iid"></a><span data-ttu-id="a58f9-103">IID</span><span class="sxs-lookup"><span data-stu-id="a58f9-103">IID</span></span>

  
  
<span data-ttu-id="a58f9-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="a58f9-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="a58f9-105">Décrit une structure [GUID](guid.md) utilisée pour décrire un identificateur pour l’interface MAPI.</span><span class="sxs-lookup"><span data-stu-id="a58f9-105">Describes a [GUID](guid.md) structure used to describe an identifier for a MAPI interface.</span></span> 
  
```cpp
typedef struct _GUID
{
  unsigned long Data1;
  unsigned short Data2;
  unsigned short Data3;
  unsigned char Data4[8];
} GUID;

```

## <a name="members"></a><span data-ttu-id="a58f9-106">Membres</span><span class="sxs-lookup"><span data-stu-id="a58f9-106">Members</span></span>

<span data-ttu-id="a58f9-107">Voir la structure **GUID** .</span><span class="sxs-lookup"><span data-stu-id="a58f9-107">See the **GUID** structure.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="a58f9-108">Remarques</span><span class="sxs-lookup"><span data-stu-id="a58f9-108">Remarks</span></span>

<span data-ttu-id="a58f9-109">Une structure **IID** est utilisée pour identifier de manière unique une interface MAPI et pour associer une interface donnée à un objet.</span><span class="sxs-lookup"><span data-stu-id="a58f9-109">An **IID** structure is used to uniquely identify a MAPI interface and to associate a particular interface with an object.</span></span> <span data-ttu-id="a58f9-110">Par exemple, lorsqu’un client appelle [IMAPISession::OpenEntry](imapisession-openentry.md) pour ouvrir un dossier, le client définit le paramètre _lpInterface_ pour pointer vers un **IID** qui représente l’interface [IMAPIFolder](imapifolderimapicontainer.md) .</span><span class="sxs-lookup"><span data-stu-id="a58f9-110">For example, when a client calls [IMAPISession::OpenEntry](imapisession-openentry.md) to open a folder, the client sets the  _lpInterface_ parameter to point to an **IID** representing the [IMAPIFolder](imapifolderimapicontainer.md) interface.</span></span> <span data-ttu-id="a58f9-111">MAPI définit **IMAPIFolderIID** à IID_IMAPIFolder.</span><span class="sxs-lookup"><span data-stu-id="a58f9-111">MAPI defines the **IMAPIFolderIID** to be IID_IMAPIFolder.</span></span> <span data-ttu-id="a58f9-112">Structures **IID** sont également utilisés pour identifier de manière unique les interfaces OLE.</span><span class="sxs-lookup"><span data-stu-id="a58f9-112">**IID** structures are also used to uniquely identify OLE interfaces.</span></span> 
  
<span data-ttu-id="a58f9-113">Toutes les structures **IID** spécifiques pour les interfaces MAPI sont définies dans le fichier d’en-tête Mapiguid.h.</span><span class="sxs-lookup"><span data-stu-id="a58f9-113">All of the specific **IID** structures for the MAPI interfaces are defined in the Mapiguid.h header file.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="a58f9-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a58f9-114">See also</span></span>



[<span data-ttu-id="a58f9-115">GUID</span><span class="sxs-lookup"><span data-stu-id="a58f9-115">GUID</span></span>](guid.md)


[<span data-ttu-id="a58f9-116">Structures MAPI</span><span class="sxs-lookup"><span data-stu-id="a58f9-116">MAPI Structures</span></span>](mapi-structures.md)

