---
title: Recherche d’un nom de profil
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 18df25b7-16b7-44cd-a9a0-5276966c1fd4
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: b4efdd8d8238d4bc7e89a1153b9be34c7af76355
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407920"
---
# <a name="finding-a-profile-name"></a><span data-ttu-id="2e2ea-103">Recherche d’un nom de profil</span><span class="sxs-lookup"><span data-stu-id="2e2ea-103">Finding a Profile Name</span></span>

  
  
<span data-ttu-id="2e2ea-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2e2ea-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2e2ea-105">Les clients doivent parfois trouver le nom du profil actuellement utilisé pour la session, le nom du profil par défaut ou le nom d’un profil de remplacement installé sur l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="2e2ea-105">Clients sometimes need to find the name of the profile currently being used for the session, the name of the default profile, or the name of an alternate profile installed on the computer.</span></span>
  
<span data-ttu-id="2e2ea-106">Il existe plusieurs façons de récupérer le nom d’un profil au cours d’une session.</span><span class="sxs-lookup"><span data-stu-id="2e2ea-106">There are a few ways to retrieve the name of a profile during the course of a session.</span></span> <span data-ttu-id="2e2ea-107">Si vous devez trouver le nom d’un profil qui n’est pas nécessairement celui utilisé pour la session, utilisez la première procédure.</span><span class="sxs-lookup"><span data-stu-id="2e2ea-107">If you need to find the name of a profile that is not necessarily the one being used for the session, use the first procedure.</span></span> <span data-ttu-id="2e2ea-108">Si vous avez besoin de trouver le nom du profil par défaut, utilisez la deuxième procédure.</span><span class="sxs-lookup"><span data-stu-id="2e2ea-108">If you need to find the name of the default profile, use the second procedure.</span></span> <span data-ttu-id="2e2ea-109">Si vous avez besoin de trouver le nom du profil actuel pour la session, utilisez la dernière procédure.</span><span class="sxs-lookup"><span data-stu-id="2e2ea-109">If you need to find the name of the current profile for the session, use the last procedure.</span></span> 
  
 <span data-ttu-id="2e2ea-110">**Pour rechercher le nom d’un profil**</span><span class="sxs-lookup"><span data-stu-id="2e2ea-110">**To find the name of any profile**</span></span>
  
1. <span data-ttu-id="2e2ea-111">Appelez [MAPIAdminProfiles](mapiadminprofiles.md) pour récupérer un pointeur d’interface **IProfAdmin.**</span><span class="sxs-lookup"><span data-stu-id="2e2ea-111">Call [MAPIAdminProfiles](mapiadminprofiles.md) to retrieve an **IProfAdmin** interface pointer.</span></span> 
    
2. <span data-ttu-id="2e2ea-112">Appelez [IProfAdmin::GetProfileTable](iprofadmin-getprofiletable.md) pour accéder à la table de profil.</span><span class="sxs-lookup"><span data-stu-id="2e2ea-112">Call [IProfAdmin::GetProfileTable](iprofadmin-getprofiletable.md) to access the profile table.</span></span> 
    
3. <span data-ttu-id="2e2ea-113">Appelez la méthode [IMAPITable::QueryRows](imapitable-queryrows.md) de la table de profil pour récupérer toutes les lignes de la table et examinez chacune d’elles pour déterminer si elle représente votre profil cible.</span><span class="sxs-lookup"><span data-stu-id="2e2ea-113">Call the profile table's [IMAPITable::QueryRows](imapitable-queryrows.md) method to retrieve all of the rows in the table and examine each one to determine if it represents your target profile.</span></span> 
    
 <span data-ttu-id="2e2ea-114">**Pour rechercher le nom du profil par défaut**</span><span class="sxs-lookup"><span data-stu-id="2e2ea-114">**To find the name of the default profile**</span></span>
  
1. <span data-ttu-id="2e2ea-115">Appelez [MAPIAdminProfiles](mapiadminprofiles.md).</span><span class="sxs-lookup"><span data-stu-id="2e2ea-115">Call [MAPIAdminProfiles](mapiadminprofiles.md).</span></span>
    
2. <span data-ttu-id="2e2ea-116">Appelez [IProfAdmin::GetProfileTable](iprofadmin-getprofiletable.md) pour accéder à la table de profil.</span><span class="sxs-lookup"><span data-stu-id="2e2ea-116">Call [IProfAdmin::GetProfileTable](iprofadmin-getprofiletable.md) to access the profile table.</span></span> 
    
3. <span data-ttu-id="2e2ea-117">Créez une restriction de propriété avec une structure [SPropertyRestriction](spropertyrestriction.md) pour faire correspondre PR_DEFAULT_PROFILE **(** [PidTagDefaultProfile](pidtagdefaultprofile-canonical-property.md)) avec la valeur TRUE.</span><span class="sxs-lookup"><span data-stu-id="2e2ea-117">Build a property restriction with an [SPropertyRestriction](spropertyrestriction.md) structure to match **PR_DEFAULT_PROFILE** ([PidTagDefaultProfile](pidtagdefaultprofile-canonical-property.md)) with the value TRUE.</span></span>
    
4. <span data-ttu-id="2e2ea-118">Appelez [IMAPITable::FindRow](imapitable-findrow.md) pour localiser la ligne dans la table de profils qui représente le profil par défaut.</span><span class="sxs-lookup"><span data-stu-id="2e2ea-118">Call [IMAPITable::FindRow](imapitable-findrow.md) to locate the row in the profile table that represents the default profile.</span></span> <span data-ttu-id="2e2ea-119">La **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) contient le nom du profil par défaut.</span><span class="sxs-lookup"><span data-stu-id="2e2ea-119">The **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) column contains the name of the default profile.</span></span>
    
 <span data-ttu-id="2e2ea-120">**Pour rechercher le nom du profil actuel**</span><span class="sxs-lookup"><span data-stu-id="2e2ea-120">**To find the name of the current profile**</span></span>
  
<span data-ttu-id="2e2ea-121">Pour rechercher le nom du profil actuel, complétez l’une des étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="2e2ea-121">To find the name of the current profile, complete one of the following steps:</span></span>
  
- <span data-ttu-id="2e2ea-122">En supposant que vous avez la structure [MAPIUID](mapiuid.md) représentant l’une des sections du profil actuel, passez-la dans le paramètre  _lpUID_ à [IMAPISession::OpenProfileSection](imapisession-openprofilesection.md).</span><span class="sxs-lookup"><span data-stu-id="2e2ea-122">Assuming that you have the [MAPIUID](mapiuid.md) structure representing one of the current profile's sections, pass it in the  _lpUID_ parameter to [IMAPISession::OpenProfileSection](imapisession-openprofilesection.md).</span></span> <span data-ttu-id="2e2ea-123">Récupérez la propriété **PR_PROFILE_NAME** ([PidTagProfileName](pidtagprofilename-canonical-property.md)) de la section de profil à l’aide de sa méthode [IMAPIProp::GetProps.](imapiprop-getprops.md)</span><span class="sxs-lookup"><span data-stu-id="2e2ea-123">Retrieve the profile section's **PR_PROFILE_NAME** ([PidTagProfileName](pidtagprofilename-canonical-property.md)) property using its [IMAPIProp::GetProps](imapiprop-getprops.md) method.</span></span> 
    
- <span data-ttu-id="2e2ea-124">Appelez [IMAPISession::GetStatusTable](imapisession-getstatustable.md) pour accéder à la table d’état et rechercher la ligne dont la colonne **PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md)) est définie sur MAPI_SUBSYSTEM.</span><span class="sxs-lookup"><span data-stu-id="2e2ea-124">Call [IMAPISession::GetStatusTable](imapisession-getstatustable.md) to access the status table and find the row that has its **PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md)) column set to MAPI_SUBSYSTEM.</span></span> <span data-ttu-id="2e2ea-125">La **PR_DISPLAY_NAME** colonne de cette ligne est le nom du profil.</span><span class="sxs-lookup"><span data-stu-id="2e2ea-125">The **PR_DISPLAY_NAME** column for this row is the profile name.</span></span> <span data-ttu-id="2e2ea-126">N’utilisez pas la table d’état au démarrage, car elle bloque une application tant que lepooler MAPI n’a pas terminé l’initialisation de tous les fournisseurs de transport.</span><span class="sxs-lookup"><span data-stu-id="2e2ea-126">Do not use the status table during start up because it blocks an application until the MAPI spooler has finished initializing all of the transport providers.</span></span> <span data-ttu-id="2e2ea-127">Cela peut dégrader vos performances.</span><span class="sxs-lookup"><span data-stu-id="2e2ea-127">This can degrade your performance.</span></span> 
    

