---
title: Création d’un profil à l’aide de code personnalisé
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 5632cd25-58f5-4b9c-906c-cd377abc3daf
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: c14d58e8a03633615798b50b256b9cc54fcc4f4c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22594732"
---
# <a name="creating-a-profile-by-using-custom-code"></a><span data-ttu-id="dbe39-103">Création d’un profil à l’aide de code personnalisé</span><span class="sxs-lookup"><span data-stu-id="dbe39-103">Creating a Profile by Using Custom Code</span></span>

  
  
<span data-ttu-id="dbe39-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="dbe39-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="dbe39-105">Si vous choisissez d’écrire du code pour créer un profil, assurez-vous de bien comprendre l’ordre des entrées de profil et le type et la quantité d’informations sont nécessaire pour chaque entrée.</span><span class="sxs-lookup"><span data-stu-id="dbe39-105">If you choose to write code to create a profile, make sure that you understand how to order profile entries and the type and amount of information that is needed for each entry.</span></span> <span data-ttu-id="dbe39-106">Les implications de l’ordre des entrées dans un profil est expliquée dans [Les profils MAPI](mapi-profiles.md).</span><span class="sxs-lookup"><span data-stu-id="dbe39-106">The implications of ordering entries in a profile is explained in [MAPI Profiles](mapi-profiles.md).</span></span>
  
 <span data-ttu-id="dbe39-107">**Pour créer un profil avec du code C ou C++**</span><span class="sxs-lookup"><span data-stu-id="dbe39-107">**To create a profile with C or C++ code**</span></span>
  
1. <span data-ttu-id="dbe39-108">Lisez le fichier d’en-tête pour chaque service de message.</span><span class="sxs-lookup"><span data-stu-id="dbe39-108">Read the header file for each message service.</span></span> <span data-ttu-id="dbe39-109">Comprendre les propriétés que vous devez configurer et que les valeurs que vous utilisez.</span><span class="sxs-lookup"><span data-stu-id="dbe39-109">Understand what properties you will need to configure and what values you will use.</span></span>
    
2. <span data-ttu-id="dbe39-110">Appelez la fonction [MAPIAdminProfiles](mapiadminprofiles.md) pour récupérer un pointeur d’interface **IProfAdmin** .</span><span class="sxs-lookup"><span data-stu-id="dbe39-110">Call the [MAPIAdminProfiles](mapiadminprofiles.md) function to retrieve an **IProfAdmin** interface pointer.</span></span> 
    
3. <span data-ttu-id="dbe39-111">Appelez [IProfAdmin::CreateProfile](iprofadmin-createprofile.md) pour créer votre profil.</span><span class="sxs-lookup"><span data-stu-id="dbe39-111">Call [IProfAdmin::CreateProfile](iprofadmin-createprofile.md) to create your profile.</span></span> <span data-ttu-id="dbe39-112">Si vous souhaitez créer un profil avec les services de message répertoriés dans la section **[Services par défaut]** du fichier MAPISVC.inf. Fichier, définir l’indicateur MAPI_DEFAULT_SERVICE.</span><span class="sxs-lookup"><span data-stu-id="dbe39-112">If you want to create a profile with the message services listed in the **[Default Services]** section of the MAPISVC.INF file, set the MAPI_DEFAULT_SERVICE flag.</span></span> <span data-ttu-id="dbe39-113">Si vous souhaitez permettre à l’utilisateur d’entrer les informations de configuration, définir l’indicateur MAPI_DIALOG.</span><span class="sxs-lookup"><span data-stu-id="dbe39-113">If you want to enable the user to enter configuration information, set the MAPI_DIALOG flag.</span></span> <span data-ttu-id="dbe39-114">Assurez-vous que vous définissez cet indicateur si ce n’est pas toutes les informations nécessaires sont disponibles via le fichier MAPISVC.inf. Fichier.</span><span class="sxs-lookup"><span data-stu-id="dbe39-114">Make sure that you set this flag if not all of the necessary information is available through the MAPISVC.INF file.</span></span> <span data-ttu-id="dbe39-115">**CreateProfile** appelle la fonction de point d’entrée pour chaque service de message à ajouter au profil avec MSG_SERVICE_CREATE défini en tant que paramètre _ulContext_ .</span><span class="sxs-lookup"><span data-stu-id="dbe39-115">**CreateProfile** calls the entry point function for each message service to be added to the profile with MSG_SERVICE_CREATE set as the  _ulContext_ parameter.</span></span> 
    
4. <span data-ttu-id="dbe39-116">Appelez [IProfAdmin::AdminServices](iprofadmin-adminservices.md) pour obtenir un objet de l’administration de service de message.</span><span class="sxs-lookup"><span data-stu-id="dbe39-116">Call [IProfAdmin::AdminServices](iprofadmin-adminservices.md) to obtain a message service administration object.</span></span> 
    
5. <span data-ttu-id="dbe39-117">Utilisez l’objet de l’administration du service de message pour ajouter des services de messagerie au profil.</span><span class="sxs-lookup"><span data-stu-id="dbe39-117">Use the message service administration object to add message services to the profile.</span></span> <span data-ttu-id="dbe39-118">Pour chaque service de message que vous souhaitez ajouter :</span><span class="sxs-lookup"><span data-stu-id="dbe39-118">For each message service that you want to add:</span></span>
    
1. <span data-ttu-id="dbe39-119">Appelez la méthode [IMsgServiceAdmin::CreateMsgService](imsgserviceadmin-createmsgservice.md) pour créer le nouveau service de message.</span><span class="sxs-lookup"><span data-stu-id="dbe39-119">Call the [IMsgServiceAdmin::CreateMsgService](imsgserviceadmin-createmsgservice.md) method to create the new message service.</span></span> 
    
2. <span data-ttu-id="dbe39-120">Appelez [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md), en passant la structure **MAPIUID** du service que vous venez de créer et un tableau de valeurs de propriété avec ses propriétés de configuration.</span><span class="sxs-lookup"><span data-stu-id="dbe39-120">Call [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md), passing the **MAPIUID** structure of the service you just created and a property value array with its configuration properties.</span></span> 
    
6. <span data-ttu-id="dbe39-121">Pour récupérer l’identificateur d’un service nouvellement ajouté, qui est sa propriété **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)), appelez [IMsgServiceAdmin::GetMsgServiceTable](imsgserviceadmin-getmsgservicetable.md) pour accéder à la table de service de message, puis recherchez la ligne qui représente le service de message.</span><span class="sxs-lookup"><span data-stu-id="dbe39-121">To retrieve the identifier of a newly added service, which is its **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) property, call [IMsgServiceAdmin::GetMsgServiceTable](imsgserviceadmin-getmsgservicetable.md) to access the message service table and search for the row that represents the message service.</span></span> <span data-ttu-id="dbe39-122">La dernière ligne de la table devant représenter le service de message dernièrement ajouté.</span><span class="sxs-lookup"><span data-stu-id="dbe39-122">The last row in the table will represent the most recently added message service.</span></span> 
    
<span data-ttu-id="dbe39-123">Pour rendre un nouveau profil temporaire, appeler la méthode [IProfAdmin::DeleteProfile](iprofadmin-deleteprofile.md) immédiatement une fois que vous ouvrez une session.</span><span class="sxs-lookup"><span data-stu-id="dbe39-123">To make a new profile temporary, call the [IProfAdmin::DeleteProfile](iprofadmin-deleteprofile.md) method immediately after you log on.</span></span> <span data-ttu-id="dbe39-124">**DeleteProfile** marque le nouveau profil comme étant supprimée tout en les rendant utilisable pour la durée de la session.</span><span class="sxs-lookup"><span data-stu-id="dbe39-124">**DeleteProfile** will mark the new profile as deleted while making it usable for the duration of the session.</span></span> <span data-ttu-id="dbe39-125">Car il ne sera pas inclus dans le tableau de profil de la session, les autres clients ne pourront pas l’utiliser.</span><span class="sxs-lookup"><span data-stu-id="dbe39-125">Because it will not be included in the session's profile table, other clients will be unable to use it.</span></span> 
  

