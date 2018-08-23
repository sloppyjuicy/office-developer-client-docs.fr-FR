---
title: Suppression d’un profil
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4d01ab2e-40fd-409d-a69d-163b7d5462ca
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: d13af3a2d0293641fd87d1065bceedfa4b62a3b4
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573242"
---
# <a name="deleting-a-profile"></a><span data-ttu-id="eb5b3-103">Suppression d’un profil</span><span class="sxs-lookup"><span data-stu-id="eb5b3-103">Deleting a Profile</span></span>

  
  
<span data-ttu-id="eb5b3-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="eb5b3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="eb5b3-105">**Pour supprimer un profil**</span><span class="sxs-lookup"><span data-stu-id="eb5b3-105">**To delete a profile**</span></span>
  
- <span data-ttu-id="eb5b3-106">Appelez [IProfAdmin::DeleteProfile](iprofadmin-deleteprofile.md).</span><span class="sxs-lookup"><span data-stu-id="eb5b3-106">Call [IProfAdmin::DeleteProfile](iprofadmin-deleteprofile.md).</span></span>
    
 <span data-ttu-id="eb5b3-107">**DeleteProfile** marque le profil de suppression si elle est actuellement utilisée, en attente jusqu'à ce qu’il n’est plus actif à supprimer.</span><span class="sxs-lookup"><span data-stu-id="eb5b3-107">**DeleteProfile** marks the profile for deletion if it is currently being used, waiting until it is no longer active to remove it.</span></span> <span data-ttu-id="eb5b3-108">Le profil ne disparaît pas réellement jusqu'à ce que tous les clients avec une session active sont déconnecté.</span><span class="sxs-lookup"><span data-stu-id="eb5b3-108">The profile does not actually disappear until every client with an active session has disconnected.</span></span> 
  
 <span data-ttu-id="eb5b3-109">**DeleteProfile** appelle la fonction de point d’entrée de chaque service de message dans le profil avec le paramètre _ulContext_ défini sur MSG_SERVICE_DELETE.</span><span class="sxs-lookup"><span data-stu-id="eb5b3-109">**DeleteProfile** calls the entry point function of every message service in the profile with the  _ulContext_ parameter set to MSG_SERVICE_DELETE.</span></span> <span data-ttu-id="eb5b3-110">Les appels aux fonctions de point d’entrée se produisent avant que les services sont physiquement retirés du profil.</span><span class="sxs-lookup"><span data-stu-id="eb5b3-110">The calls to the entry point functions occur before the services are physically removed from the profile.</span></span> 
  

