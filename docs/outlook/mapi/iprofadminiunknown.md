---
title: /IUnknown IProfAdmin
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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: cbdfba68490b1e756f277c6e552235368a86f310
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434115"
---
# <a name="iprofadmin--iunknown"></a><span data-ttu-id="002f7-103">IProfAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="002f7-103">IProfAdmin : IUnknown</span></span>

  
  
<span data-ttu-id="002f7-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="002f7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="002f7-105">Prend en charge l'administration des profils.</span><span class="sxs-lookup"><span data-stu-id="002f7-105">Supports the administration of profiles.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="002f7-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="002f7-106">Header file:</span></span>  <br/> |<span data-ttu-id="002f7-107">Mapix. h</span><span class="sxs-lookup"><span data-stu-id="002f7-107">Mapix.h</span></span>  <br/> |
|<span data-ttu-id="002f7-108">Exposé par:</span><span class="sxs-lookup"><span data-stu-id="002f7-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="002f7-109">Objet d'administration des profils</span><span class="sxs-lookup"><span data-stu-id="002f7-109">Profile administration object</span></span>  <br/> |
|<span data-ttu-id="002f7-110">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="002f7-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="002f7-111">MAPI</span><span class="sxs-lookup"><span data-stu-id="002f7-111">MAPI</span></span>  <br/> |
|<span data-ttu-id="002f7-112">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="002f7-112">Called by:</span></span>  <br/> |<span data-ttu-id="002f7-113">Applications clientes</span><span class="sxs-lookup"><span data-stu-id="002f7-113">Client applications</span></span>  <br/> |
|<span data-ttu-id="002f7-114">Identificateur de l'interface:</span><span class="sxs-lookup"><span data-stu-id="002f7-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="002f7-115">IID_IProfAdmin</span><span class="sxs-lookup"><span data-stu-id="002f7-115">IID_IProfAdmin</span></span>  <br/> |
|<span data-ttu-id="002f7-116">Type de pointeur:</span><span class="sxs-lookup"><span data-stu-id="002f7-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="002f7-117">LPPROFADMIN</span><span class="sxs-lookup"><span data-stu-id="002f7-117">LPPROFADMIN</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="002f7-118">Ordre vtable</span><span class="sxs-lookup"><span data-stu-id="002f7-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="002f7-119">Généré</span><span class="sxs-lookup"><span data-stu-id="002f7-119">GetLastError</span></span>](iprofadmin-getlasterror.md) <br/> |<span data-ttu-id="002f7-120">Renvoie une structure [MAPIERROR](mapierror.md) qui contient des informations sur l'erreur précédente qui s'est produite sur un objet d'administration de profil.</span><span class="sxs-lookup"><span data-stu-id="002f7-120">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous error that occurred to a profile administration object.</span></span>  <br/> |
|[<span data-ttu-id="002f7-121">GetProfileTable</span><span class="sxs-lookup"><span data-stu-id="002f7-121">GetProfileTable</span></span>](iprofadmin-getprofiletable.md) <br/> |<span data-ttu-id="002f7-122">Fournit l'accès à la table de profils, une table qui contient des informations sur tous les profils disponibles.</span><span class="sxs-lookup"><span data-stu-id="002f7-122">Provides access to the profile table, a table that contains information about all of the available profiles.</span></span>  <br/> |
|[<span data-ttu-id="002f7-123">CreateProfile</span><span class="sxs-lookup"><span data-stu-id="002f7-123">CreateProfile</span></span>](iprofadmin-createprofile.md) <br/> |<span data-ttu-id="002f7-124">Crée un nouveau profil.</span><span class="sxs-lookup"><span data-stu-id="002f7-124">Creates a new profile.</span></span>  <br/> |
|[<span data-ttu-id="002f7-125">DeleteProfile</span><span class="sxs-lookup"><span data-stu-id="002f7-125">DeleteProfile</span></span>](iprofadmin-deleteprofile.md) <br/> |<span data-ttu-id="002f7-126">Supprime un profil.</span><span class="sxs-lookup"><span data-stu-id="002f7-126">Deletes a profile.</span></span>  <br/> |
|[<span data-ttu-id="002f7-127">ChangeProfilePassword</span><span class="sxs-lookup"><span data-stu-id="002f7-127">ChangeProfilePassword</span></span>](iprofadmin-changeprofilepassword.md) <br/> |<span data-ttu-id="002f7-128">Déconseillé.</span><span class="sxs-lookup"><span data-stu-id="002f7-128">Deprecated.</span></span> <span data-ttu-id="002f7-129">Modifie le mot de passe d'un profil.</span><span class="sxs-lookup"><span data-stu-id="002f7-129">Changes the password for a profile.</span></span>  <br/> |
|[<span data-ttu-id="002f7-130">CopyProfile</span><span class="sxs-lookup"><span data-stu-id="002f7-130">CopyProfile</span></span>](iprofadmin-copyprofile.md) <br/> |<span data-ttu-id="002f7-131">Copie un profil.</span><span class="sxs-lookup"><span data-stu-id="002f7-131">Copies a profile.</span></span>  <br/> |
|[<span data-ttu-id="002f7-132">RenameProfile</span><span class="sxs-lookup"><span data-stu-id="002f7-132">RenameProfile</span></span>](iprofadmin-renameprofile.md) <br/> |<span data-ttu-id="002f7-133">Affecte un nouveau nom à un profil.</span><span class="sxs-lookup"><span data-stu-id="002f7-133">Assigns a new name to a profile.</span></span>  <br/> |
|[<span data-ttu-id="002f7-134">SetDefaultProfile</span><span class="sxs-lookup"><span data-stu-id="002f7-134">SetDefaultProfile</span></span>](iprofadmin-setdefaultprofile.md) <br/> |<span data-ttu-id="002f7-135">Définit ou efface le profil par défaut d'un client.</span><span class="sxs-lookup"><span data-stu-id="002f7-135">Sets or clears a client's default profile.</span></span>  <br/> |
|[<span data-ttu-id="002f7-136">AdminServices</span><span class="sxs-lookup"><span data-stu-id="002f7-136">AdminServices</span></span>](iprofadmin-adminservices.md) <br/> |<span data-ttu-id="002f7-137">Permet d'accéder à un objet d'administration de service de messagerie pour apporter des modifications aux services de messagerie dans un profil.</span><span class="sxs-lookup"><span data-stu-id="002f7-137">Provides access to a message service administration object for making changes to the message services in a profile.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="002f7-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="002f7-138">See also</span></span>



[<span data-ttu-id="002f7-139">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="002f7-139">MAPI Interfaces</span></span>](mapi-interfaces.md)

