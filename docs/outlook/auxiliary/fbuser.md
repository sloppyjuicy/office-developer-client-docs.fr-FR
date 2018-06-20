---
title: FBUser
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal649b5400-8dc5-cc5c-3455-f462e2d31689
ms.assetid: ''
description: Identifie un utilisateur qui peut ou non posséder des informations de disponibilité des données disponibles.
ms.openlocfilehash: e83689e28f5fb6e1eae28d760bb57f5ad3796f8e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782553"
---
# <a name="fbuser"></a><span data-ttu-id="e9918-103">FBUser</span><span class="sxs-lookup"><span data-stu-id="e9918-103">FBUser</span></span>

<span data-ttu-id="e9918-104">Identifie un utilisateur qui peut ou non posséder des informations de disponibilité des données disponibles.</span><span class="sxs-lookup"><span data-stu-id="e9918-104">Identifies a user who may or may not have free/busy data available.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="e9918-105">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="e9918-105">Quick info</span></span>

```cpp
typedef struct tagFBUser 
{ 
   ULONG m_cbEid; 
   LPENTRYID m_lpEid; 
   ULONG m_ulReserved; 
   LPWSTR m_pwszReserved; 
} FBUser;

```

## <a name="members"></a><span data-ttu-id="e9918-106">Membres</span><span class="sxs-lookup"><span data-stu-id="e9918-106">Members</span></span>

<span data-ttu-id="e9918-107">_m_cbEid_</span><span class="sxs-lookup"><span data-stu-id="e9918-107">_m_cbEid_</span></span>
  
> <span data-ttu-id="e9918-108">La longueur de l’identificateur d’entrée de l’utilisateur de messagerie, tel que représenté par l’interface [IMailUser](http://msdn.microsoft.com/library/wab._wab_IMailUser%28Office.15%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="e9918-108">The length of the entry ID of the mail user as represented by the [IMailUser](http://msdn.microsoft.com/library/wab._wab_IMailUser%28Office.15%29.aspx) interface.</span></span> 
    
<span data-ttu-id="e9918-109">_m_lpEid_</span><span class="sxs-lookup"><span data-stu-id="e9918-109">_m_lpEid_</span></span>
  
> <span data-ttu-id="e9918-110">L’identificateur d’entrée de l’utilisateur de messagerie, tel que représenté par l’interface **IMailUser** .</span><span class="sxs-lookup"><span data-stu-id="e9918-110">The entry ID of the mail user as represented by the **IMailUser** interface.</span></span> 
    
<span data-ttu-id="e9918-111">_m_ulReserved_</span><span class="sxs-lookup"><span data-stu-id="e9918-111">_m_ulReserved_</span></span>
  
> <span data-ttu-id="e9918-112">Ce paramètre est réservé à un usage interne Outlook et n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="e9918-112">This parameter is reserved for Outlook internal use and is not supported.</span></span>
    
<span data-ttu-id="e9918-113">_m_pwszReserved_</span><span class="sxs-lookup"><span data-stu-id="e9918-113">_m_pwszReserved_</span></span>
  
> <span data-ttu-id="e9918-114">Ce paramètre est réservé à un usage interne Outlook et n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="e9918-114">This parameter is reserved for Outlook internal use and is not supported.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e9918-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e9918-115">See also</span></span>

- [<span data-ttu-id="e9918-116">À propos de l'API de type disponible/occupé</span><span class="sxs-lookup"><span data-stu-id="e9918-116">About the Free/Busy API</span></span>](about-the-free-busy-api.md)  
- [<span data-ttu-id="e9918-117">IFreeBusySupport</span><span class="sxs-lookup"><span data-stu-id="e9918-117">IFreeBusySupport</span></span>](ifreebusysupport.md)

