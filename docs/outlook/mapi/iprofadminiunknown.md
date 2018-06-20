---
title: IProfAdmin IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IProfAdmin
api_type:
- COM
ms.assetid: 274899cc-2894-4d99-84ec-f18121e856a0
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: c6192e6f92078f2f9bab0d55e9952d21ebb82af6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784382"
---
# <a name="iprofadmin--iunknown"></a><span data-ttu-id="07178-103">IProfAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="07178-103">IProfAdmin : IUnknown</span></span>

  
  
<span data-ttu-id="07178-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="07178-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="07178-105">Prend en charge l’administration des profils.</span><span class="sxs-lookup"><span data-stu-id="07178-105">Supports the administration of profiles.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="07178-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="07178-106">Header file:</span></span>  <br/> |<span data-ttu-id="07178-107">MAPIX.h</span><span class="sxs-lookup"><span data-stu-id="07178-107">Mapix.h</span></span>  <br/> |
|<span data-ttu-id="07178-108">Exposés par :</span><span class="sxs-lookup"><span data-stu-id="07178-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="07178-109">Objet d’administration de profil</span><span class="sxs-lookup"><span data-stu-id="07178-109">Profile administration object</span></span>  <br/> |
|<span data-ttu-id="07178-110">Implémentée par :</span><span class="sxs-lookup"><span data-stu-id="07178-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="07178-111">MAPI</span><span class="sxs-lookup"><span data-stu-id="07178-111">MAPI</span></span>  <br/> |
|<span data-ttu-id="07178-112">Appelée par :</span><span class="sxs-lookup"><span data-stu-id="07178-112">Called by:</span></span>  <br/> |<span data-ttu-id="07178-113">Applications clientes</span><span class="sxs-lookup"><span data-stu-id="07178-113">Client applications</span></span>  <br/> |
|<span data-ttu-id="07178-114">Identificateur de l’interface :</span><span class="sxs-lookup"><span data-stu-id="07178-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="07178-115">IID_IProfAdmin</span><span class="sxs-lookup"><span data-stu-id="07178-115">IID_IProfAdmin</span></span>  <br/> |
|<span data-ttu-id="07178-116">Type de pointeur :</span><span class="sxs-lookup"><span data-stu-id="07178-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="07178-117">LPPROFADMIN</span><span class="sxs-lookup"><span data-stu-id="07178-117">LPPROFADMIN</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="07178-118">Ordre vtable</span><span class="sxs-lookup"><span data-stu-id="07178-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="07178-119">GetLastError</span><span class="sxs-lookup"><span data-stu-id="07178-119">GetLastError</span></span>](iprofadmin-getlasterror.md) <br/> |<span data-ttu-id="07178-120">Retourne une structure [MAPIERROR](mapierror.md) qui contient des informations sur l’erreur précédente s’est produite pour un objet d’administration de profil.</span><span class="sxs-lookup"><span data-stu-id="07178-120">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous error that occurred to a profile administration object.</span></span>  <br/> |
|[<span data-ttu-id="07178-121">GetProfileTable</span><span class="sxs-lookup"><span data-stu-id="07178-121">GetProfileTable</span></span>](iprofadmin-getprofiletable.md) <br/> |<span data-ttu-id="07178-122">Permet d’accéder à la table de profil, un tableau qui contient des informations sur tous les profils disponibles.</span><span class="sxs-lookup"><span data-stu-id="07178-122">Provides access to the profile table, a table that contains information about all of the available profiles.</span></span>  <br/> |
|[<span data-ttu-id="07178-123">CreateProfile</span><span class="sxs-lookup"><span data-stu-id="07178-123">CreateProfile</span></span>](iprofadmin-createprofile.md) <br/> |<span data-ttu-id="07178-124">Crée un nouveau profil.</span><span class="sxs-lookup"><span data-stu-id="07178-124">Creates a new profile.</span></span>  <br/> |
|[<span data-ttu-id="07178-125">DeleteProfile</span><span class="sxs-lookup"><span data-stu-id="07178-125">DeleteProfile</span></span>](iprofadmin-deleteprofile.md) <br/> |<span data-ttu-id="07178-126">Supprime un profil.</span><span class="sxs-lookup"><span data-stu-id="07178-126">Deletes a profile.</span></span>  <br/> |
|[<span data-ttu-id="07178-127">ChangeProfilePassword</span><span class="sxs-lookup"><span data-stu-id="07178-127">ChangeProfilePassword</span></span>](iprofadmin-changeprofilepassword.md) <br/> |<span data-ttu-id="07178-128">Déconseillé.</span><span class="sxs-lookup"><span data-stu-id="07178-128">Deprecated.</span></span> <span data-ttu-id="07178-129">Modifie le mot de passe pour un profil.</span><span class="sxs-lookup"><span data-stu-id="07178-129">Changes the password for a profile.</span></span>  <br/> |
|[<span data-ttu-id="07178-130">CopyProfile</span><span class="sxs-lookup"><span data-stu-id="07178-130">CopyProfile</span></span>](iprofadmin-copyprofile.md) <br/> |<span data-ttu-id="07178-131">Copie d’un profil.</span><span class="sxs-lookup"><span data-stu-id="07178-131">Copies a profile.</span></span>  <br/> |
|[<span data-ttu-id="07178-132">RenameProfile</span><span class="sxs-lookup"><span data-stu-id="07178-132">RenameProfile</span></span>](iprofadmin-renameprofile.md) <br/> |<span data-ttu-id="07178-133">Affecte un nouveau nom à un profil.</span><span class="sxs-lookup"><span data-stu-id="07178-133">Assigns a new name to a profile.</span></span>  <br/> |
|[<span data-ttu-id="07178-134">SetDefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07178-134">SetDefaultProfile</span></span>](iprofadmin-setdefaultprofile.md) <br/> |<span data-ttu-id="07178-135">Active ou désactive le profil par défaut d’un client.</span><span class="sxs-lookup"><span data-stu-id="07178-135">Sets or clears a client's default profile.</span></span>  <br/> |
|[<span data-ttu-id="07178-136">AdminServices</span><span class="sxs-lookup"><span data-stu-id="07178-136">AdminServices</span></span>](iprofadmin-adminservices.md) <br/> |<span data-ttu-id="07178-137">Donne accès à un objet de l’administration de service de message pour apporter des modifications aux services de message dans un profil.</span><span class="sxs-lookup"><span data-stu-id="07178-137">Provides access to a message service administration object for making changes to the message services in a profile.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="07178-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="07178-138">See also</span></span>



[<span data-ttu-id="07178-139">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="07178-139">MAPI Interfaces</span></span>](mapi-interfaces.md)

