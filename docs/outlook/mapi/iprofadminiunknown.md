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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: cbdfba68490b1e756f277c6e552235368a86f310
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348852"
---
# <a name="iprofadmin--iunknown"></a><span data-ttu-id="e863a-103">IProfAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="e863a-103">IProfAdmin : IUnknown</span></span>

  
  
<span data-ttu-id="e863a-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e863a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e863a-105">Prend en charge l'administration des profils.</span><span class="sxs-lookup"><span data-stu-id="e863a-105">Supports the administration of profiles.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e863a-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="e863a-106">Header file:</span></span>  <br/> |<span data-ttu-id="e863a-107">Mapix. h</span><span class="sxs-lookup"><span data-stu-id="e863a-107">Mapix.h</span></span>  <br/> |
|<span data-ttu-id="e863a-108">Exposé par:</span><span class="sxs-lookup"><span data-stu-id="e863a-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="e863a-109">Objet d'administration des profils</span><span class="sxs-lookup"><span data-stu-id="e863a-109">Profile administration object</span></span>  <br/> |
|<span data-ttu-id="e863a-110">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="e863a-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="e863a-111">MAPI</span><span class="sxs-lookup"><span data-stu-id="e863a-111">MAPI</span></span>  <br/> |
|<span data-ttu-id="e863a-112">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="e863a-112">Called by:</span></span>  <br/> |<span data-ttu-id="e863a-113">Applications clientes</span><span class="sxs-lookup"><span data-stu-id="e863a-113">Client applications</span></span>  <br/> |
|<span data-ttu-id="e863a-114">Identificateur de l'interface:</span><span class="sxs-lookup"><span data-stu-id="e863a-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="e863a-115">IID_IProfAdmin</span><span class="sxs-lookup"><span data-stu-id="e863a-115">IID_IProfAdmin</span></span>  <br/> |
|<span data-ttu-id="e863a-116">Type de pointeur:</span><span class="sxs-lookup"><span data-stu-id="e863a-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="e863a-117">LPPROFADMIN</span><span class="sxs-lookup"><span data-stu-id="e863a-117">LPPROFADMIN</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="e863a-118">Ordre vtable</span><span class="sxs-lookup"><span data-stu-id="e863a-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="e863a-119">Généré</span><span class="sxs-lookup"><span data-stu-id="e863a-119">GetLastError</span></span>](iprofadmin-getlasterror.md) <br/> |<span data-ttu-id="e863a-120">Renvoie une structure [MAPIERROR](mapierror.md) qui contient des informations sur l'erreur précédente qui s'est produite sur un objet d'administration de profil.</span><span class="sxs-lookup"><span data-stu-id="e863a-120">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous error that occurred to a profile administration object.</span></span>  <br/> |
|[<span data-ttu-id="e863a-121">GetProfileTable</span><span class="sxs-lookup"><span data-stu-id="e863a-121">GetProfileTable</span></span>](iprofadmin-getprofiletable.md) <br/> |<span data-ttu-id="e863a-122">Fournit l'accès à la table de profils, une table qui contient des informations sur tous les profils disponibles.</span><span class="sxs-lookup"><span data-stu-id="e863a-122">Provides access to the profile table, a table that contains information about all of the available profiles.</span></span>  <br/> |
|[<span data-ttu-id="e863a-123">CreateProfile</span><span class="sxs-lookup"><span data-stu-id="e863a-123">CreateProfile</span></span>](iprofadmin-createprofile.md) <br/> |<span data-ttu-id="e863a-124">Crée un nouveau profil.</span><span class="sxs-lookup"><span data-stu-id="e863a-124">Creates a new profile.</span></span>  <br/> |
|[<span data-ttu-id="e863a-125">DeleteProfile</span><span class="sxs-lookup"><span data-stu-id="e863a-125">DeleteProfile</span></span>](iprofadmin-deleteprofile.md) <br/> |<span data-ttu-id="e863a-126">Supprime un profil.</span><span class="sxs-lookup"><span data-stu-id="e863a-126">Deletes a profile.</span></span>  <br/> |
|[<span data-ttu-id="e863a-127">ChangeProfilePassword</span><span class="sxs-lookup"><span data-stu-id="e863a-127">ChangeProfilePassword</span></span>](iprofadmin-changeprofilepassword.md) <br/> |<span data-ttu-id="e863a-128">Déconseillé.</span><span class="sxs-lookup"><span data-stu-id="e863a-128">Deprecated.</span></span> <span data-ttu-id="e863a-129">Modifie le mot de passe d'un profil.</span><span class="sxs-lookup"><span data-stu-id="e863a-129">Changes the password for a profile.</span></span>  <br/> |
|[<span data-ttu-id="e863a-130">CopyProfile</span><span class="sxs-lookup"><span data-stu-id="e863a-130">CopyProfile</span></span>](iprofadmin-copyprofile.md) <br/> |<span data-ttu-id="e863a-131">Copie un profil.</span><span class="sxs-lookup"><span data-stu-id="e863a-131">Copies a profile.</span></span>  <br/> |
|[<span data-ttu-id="e863a-132">RenameProfile</span><span class="sxs-lookup"><span data-stu-id="e863a-132">RenameProfile</span></span>](iprofadmin-renameprofile.md) <br/> |<span data-ttu-id="e863a-133">Affecte un nouveau nom à un profil.</span><span class="sxs-lookup"><span data-stu-id="e863a-133">Assigns a new name to a profile.</span></span>  <br/> |
|[<span data-ttu-id="e863a-134">SetDefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e863a-134">SetDefaultProfile</span></span>](iprofadmin-setdefaultprofile.md) <br/> |<span data-ttu-id="e863a-135">Définit ou efface le profil par défaut d'un client.</span><span class="sxs-lookup"><span data-stu-id="e863a-135">Sets or clears a client's default profile.</span></span>  <br/> |
|[<span data-ttu-id="e863a-136">AdminServices</span><span class="sxs-lookup"><span data-stu-id="e863a-136">AdminServices</span></span>](iprofadmin-adminservices.md) <br/> |<span data-ttu-id="e863a-137">Permet d'accéder à un objet d'administration de service de messagerie pour apporter des modifications aux services de messagerie dans un profil.</span><span class="sxs-lookup"><span data-stu-id="e863a-137">Provides access to a message service administration object for making changes to the message services in a profile.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e863a-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e863a-138">See also</span></span>



[<span data-ttu-id="e863a-139">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="e863a-139">MAPI Interfaces</span></span>](mapi-interfaces.md)

