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
ms.openlocfilehash: 1cd87b92a9d289f06e466f4e44ce757c93074336
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410202"
---
# <a name="deleting-a-profile"></a><span data-ttu-id="3706c-103">Suppression d’un profil</span><span class="sxs-lookup"><span data-stu-id="3706c-103">Deleting a Profile</span></span>

  
  
<span data-ttu-id="3706c-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3706c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="3706c-105">**Pour supprimer un profil**</span><span class="sxs-lookup"><span data-stu-id="3706c-105">**To delete a profile**</span></span>
  
- <span data-ttu-id="3706c-106">Appelez [IProfAdmin::D eleteProfile](iprofadmin-deleteprofile.md).</span><span class="sxs-lookup"><span data-stu-id="3706c-106">Call [IProfAdmin::DeleteProfile](iprofadmin-deleteprofile.md).</span></span>
    
 <span data-ttu-id="3706c-107">**DeleteProfile marque** le profil à supprimer s’il est en cours d’utilisation, en attendant qu’il ne soit plus actif pour le supprimer.</span><span class="sxs-lookup"><span data-stu-id="3706c-107">**DeleteProfile** marks the profile for deletion if it is currently being used, waiting until it is no longer active to remove it.</span></span> <span data-ttu-id="3706c-108">Le profil ne disparaît pas tant que chaque client avec une session active n’a pas été déconnecté.</span><span class="sxs-lookup"><span data-stu-id="3706c-108">The profile does not actually disappear until every client with an active session has disconnected.</span></span> 
  
 <span data-ttu-id="3706c-109">**DeleteProfile appelle la** fonction de point d’entrée de chaque service de message dans le profil avec le paramètre  _ulContext_ paramétré sur MSG_SERVICE_DELETE.</span><span class="sxs-lookup"><span data-stu-id="3706c-109">**DeleteProfile** calls the entry point function of every message service in the profile with the  _ulContext_ parameter set to MSG_SERVICE_DELETE.</span></span> <span data-ttu-id="3706c-110">Les appels aux fonctions de point d’entrée se produisent avant la suppression physique des services du profil.</span><span class="sxs-lookup"><span data-stu-id="3706c-110">The calls to the entry point functions occur before the services are physically removed from the profile.</span></span> 
  

