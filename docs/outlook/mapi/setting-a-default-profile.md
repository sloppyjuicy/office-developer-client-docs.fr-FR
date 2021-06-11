---
title: Définition d’un profil par défaut
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 1d1e862d-ba49-48a1-bb51-0af861323b7b
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: f6bf8f88fa3e87ae619fa32d759fc182290998ad
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439813"
---
# <a name="setting-a-default-profile"></a><span data-ttu-id="0ed25-103">Définition d’un profil par défaut</span><span class="sxs-lookup"><span data-stu-id="0ed25-103">Setting a Default Profile</span></span>

  
  
<span data-ttu-id="0ed25-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0ed25-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0ed25-105">Le profil par défaut est le profil utilisé si vous n’en spécifiez pas explicitement un dans l’appel à [MAPILogonEx](mapilogonex.md), en spécifiant à la place l’indicateur MAPI_USE_DEFAULT.</span><span class="sxs-lookup"><span data-stu-id="0ed25-105">The default profile is the profile that is used if you do not explicitly specify one in the call to [MAPILogonEx](mapilogonex.md), setting instead the MAPI_USE_DEFAULT flag.</span></span>
  
 <span data-ttu-id="0ed25-106">**Pour établir un profil par défaut**</span><span class="sxs-lookup"><span data-stu-id="0ed25-106">**To establish a default profile**</span></span>
  
1. <span data-ttu-id="0ed25-107">Appelez la [fonction MAPIAdminProfiles pour](mapiadminprofiles.md) récupérer un pointeur d’interface **IProfAdmin.**</span><span class="sxs-lookup"><span data-stu-id="0ed25-107">Call the [MAPIAdminProfiles](mapiadminprofiles.md) function to retrieve an **IProfAdmin** interface pointer.</span></span> 
    
2. <span data-ttu-id="0ed25-108">Appelez [IProfAdmin::SetDefaultProfile](iprofadmin-setdefaultprofile.md).</span><span class="sxs-lookup"><span data-stu-id="0ed25-108">Call [IProfAdmin::SetDefaultProfile](iprofadmin-setdefaultprofile.md).</span></span> <span data-ttu-id="0ed25-109">**SetDefaultProfile** définit la propriété **PR_DEFAULT_PROFILE** ([PidTagDefaultProfile](pidtagdefaultprofile-canonical-property.md)) pour le nouveau profil par défaut et supprime le paramètre du profil par défaut précédent.</span><span class="sxs-lookup"><span data-stu-id="0ed25-109">**SetDefaultProfile** sets the **PR_DEFAULT_PROFILE** ([PidTagDefaultProfile](pidtagdefaultprofile-canonical-property.md)) property for the new default profile and removes the setting for the previous default profile.</span></span>
    

