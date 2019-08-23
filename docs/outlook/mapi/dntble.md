---
title: DNTBLE
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 10fb1650-6c3e-f467-91cd-48e5ddd82827
description: 'Dernière modification : 05 juillet 2012'
ms.openlocfilehash: 41a61bd05bd511888aeab756166016813f4dceb8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32337113"
---
# <a name="dntble"></a><span data-ttu-id="429fd-103">DNTBLE</span><span class="sxs-lookup"><span data-stu-id="429fd-103">DNTBLE</span></span>

  
  
<span data-ttu-id="429fd-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="429fd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="429fd-105">Informations relatives au téléchargement du contenu d’un dossier à partir du serveur pendant le [téléchargement de l’état de la table](download-table-state.md).</span><span class="sxs-lookup"><span data-stu-id="429fd-105">Information for downloading the contents of a folder from the server during the [download table state](download-table-state.md).</span></span> <span data-ttu-id="429fd-106">Ce processus de téléchargement utilise une méthode de synchronisation des modifications incrémentielle (ICS) de Microsoft Exchange.</span><span class="sxs-lookup"><span data-stu-id="429fd-106">This downloading process uses Microsoft Exchange Incremental Change Synchronization (ICS).</span></span> <span data-ttu-id="429fd-107">Pour plus d’informations sur ICS, reportez-vous à [Critères d’évaluation ICS](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="429fd-107">For more information on ICS, see [ICS Evaluation Criteria](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="429fd-108">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="429fd-108">Quick info</span></span>

```cpp
struct DNTBLE 
{ 
    UINT cEntNew; 
    UINT cEntMod; 
    UINT cEntRead; 
    UINT cEntDel; 
};
```

## <a name="members"></a><span data-ttu-id="429fd-109">Membres</span><span class="sxs-lookup"><span data-stu-id="429fd-109">Members</span></span>

 <span data-ttu-id="429fd-110">_cEntNew_</span><span class="sxs-lookup"><span data-stu-id="429fd-110">_cEntNew_</span></span>
  
> <span data-ttu-id="429fd-111">[sortant] Nombre d’éléments ajoutés à la banque locale.</span><span class="sxs-lookup"><span data-stu-id="429fd-111">[out] Number of items added to the local store.</span></span> <span data-ttu-id="429fd-112">Outlook renseigne cette valeur pendant le téléchargement lors de l’utilisation d’ICS.</span><span class="sxs-lookup"><span data-stu-id="429fd-112">Outlook populates this value during the downloading when using ICS.</span></span>
    
 <span data-ttu-id="429fd-113">_cEntMod_</span><span class="sxs-lookup"><span data-stu-id="429fd-113">_cEntMod_</span></span>
  
> <span data-ttu-id="429fd-114">[sortant] Nombre d’éléments modifiés dans la banque locale.</span><span class="sxs-lookup"><span data-stu-id="429fd-114">[out] Number of items modified on the local store.</span></span> <span data-ttu-id="429fd-115">Outlook renseigne cette valeur pendant le téléchargement lors de l’utilisation d’ICS.</span><span class="sxs-lookup"><span data-stu-id="429fd-115">Outlook populates this value during the downloading when using ICS.</span></span>
    
 <span data-ttu-id="429fd-116">_cEntRead_</span><span class="sxs-lookup"><span data-stu-id="429fd-116">_cEntRead_</span></span>
  
> <span data-ttu-id="429fd-117">[sortant] Nombre d’éléments lus ou marqués comme non lus dans la banque locale.</span><span class="sxs-lookup"><span data-stu-id="429fd-117">[out] Number of items read or marked unread on the local store.</span></span> <span data-ttu-id="429fd-118">Outlook renseigne cette valeur pendant le téléchargement lors de l’utilisation d’ICS.</span><span class="sxs-lookup"><span data-stu-id="429fd-118">Outlook populates this value during the downloading when using ICS.</span></span>
    
 <span data-ttu-id="429fd-119">_cEntDel_</span><span class="sxs-lookup"><span data-stu-id="429fd-119">_cEntDel_</span></span>
  
> <span data-ttu-id="429fd-120">[sortant] Nombre d’éléments supprimés de la banque locale.</span><span class="sxs-lookup"><span data-stu-id="429fd-120">[out] Number of items deleted on the local store.</span></span> <span data-ttu-id="429fd-121">Outlook renseigne cette valeur pendant le téléchargement lors de l’utilisation d’ICS.</span><span class="sxs-lookup"><span data-stu-id="429fd-121">Outlook populates this value during the downloading when using ICS.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="429fd-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="429fd-122">See also</span></span>



[<span data-ttu-id="429fd-123">À propos de la machine à états de réplication</span><span class="sxs-lookup"><span data-stu-id="429fd-123">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="429fd-124">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="429fd-124">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="429fd-125">DNTBL</span><span class="sxs-lookup"><span data-stu-id="429fd-125">DNTBL</span></span>](dntbl.md)

