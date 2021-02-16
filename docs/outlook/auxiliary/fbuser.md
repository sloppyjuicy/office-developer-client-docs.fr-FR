---
title: FBUser
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal649b5400-8dc5-cc5c-3455-f462e2d31689
ms.assetid: ''
description: Identifie un utilisateur qui peut ou non avoir des données de libre/occupé disponibles.
ms.openlocfilehash: 2511a94678f9ef8f2cb6be868db4f718d92ecb6d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317660"
---
# <a name="fbuser"></a><span data-ttu-id="ee25b-103">FBUser</span><span class="sxs-lookup"><span data-stu-id="ee25b-103">FBUser</span></span>

<span data-ttu-id="ee25b-104">Identifie un utilisateur qui peut ou non avoir des données de libre/occupé disponibles.</span><span class="sxs-lookup"><span data-stu-id="ee25b-104">Identifies a user who may or may not have free/busy data available.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="ee25b-105">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="ee25b-105">Quick info</span></span>

```cpp
typedef struct tagFBUser 
{ 
   ULONG m_cbEid; 
   LPENTRYID m_lpEid; 
   ULONG m_ulReserved; 
   LPWSTR m_pwszReserved; 
} FBUser;

```

## <a name="members"></a><span data-ttu-id="ee25b-106">Membres</span><span class="sxs-lookup"><span data-stu-id="ee25b-106">Members</span></span>

<span data-ttu-id="ee25b-107">_m_cbEid_</span><span class="sxs-lookup"><span data-stu-id="ee25b-107">_m_cbEid_</span></span>
  
> <span data-ttu-id="ee25b-108">Longueur de l’ID d’entrée de l’utilisateur de messagerie tel que représenté par l’interface [IMailUser.](https://docs.microsoft.com/previous-versions/windows/desktop/wab/-wab-imailuser-deleteprops)</span><span class="sxs-lookup"><span data-stu-id="ee25b-108">The length of the entry ID of the mail user as represented by the [IMailUser](https://docs.microsoft.com/previous-versions/windows/desktop/wab/-wab-imailuser-deleteprops) interface.</span></span> 
    
<span data-ttu-id="ee25b-109">_m_lpEid_</span><span class="sxs-lookup"><span data-stu-id="ee25b-109">_m_lpEid_</span></span>
  
> <span data-ttu-id="ee25b-110">ID d’entrée de l’utilisateur de messagerie tel que représenté par l’interface **IMailUser.**</span><span class="sxs-lookup"><span data-stu-id="ee25b-110">The entry ID of the mail user as represented by the **IMailUser** interface.</span></span> 
    
<span data-ttu-id="ee25b-111">_m_ulReserved_</span><span class="sxs-lookup"><span data-stu-id="ee25b-111">_m_ulReserved_</span></span>
  
> <span data-ttu-id="ee25b-112">Ce paramètre est réservé à un usage interne à Outlook et n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="ee25b-112">This parameter is reserved for Outlook internal use and is not supported.</span></span>
    
<span data-ttu-id="ee25b-113">_m_pwszReserved_</span><span class="sxs-lookup"><span data-stu-id="ee25b-113">_m_pwszReserved_</span></span>
  
> <span data-ttu-id="ee25b-114">Ce paramètre est réservé à un usage interne à Outlook et n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="ee25b-114">This parameter is reserved for Outlook internal use and is not supported.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ee25b-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ee25b-115">See also</span></span>

- [<span data-ttu-id="ee25b-116">À propos de l’API Disponibilité</span><span class="sxs-lookup"><span data-stu-id="ee25b-116">About the Free/Busy API</span></span>](about-the-free-busy-api.md)  
- [<span data-ttu-id="ee25b-117">IFreeBusySupport</span><span class="sxs-lookup"><span data-stu-id="ee25b-117">IFreeBusySupport</span></span>](ifreebusysupport.md)

