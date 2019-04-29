---
title: PROP_POP_LEAVE_ON_SERVER
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 22d7c1e8-48b9-4768-b4de-9a9f32a3aabb
description: Spécifie la conservation d'une copie d'un message sur le serveur pour un compte POP.
ms.openlocfilehash: e1bbddea0f10c07d630676960d1b330f6055e137
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410944"
---
# <a name="proppopleaveonserver"></a><span data-ttu-id="301f0-103">PROP_POP_LEAVE_ON_SERVER</span><span class="sxs-lookup"><span data-stu-id="301f0-103">PROP_POP_LEAVE_ON_SERVER</span></span>

<span data-ttu-id="301f0-104">Spécifie la conservation d'une copie d'un message sur le serveur pour un compte POP.</span><span class="sxs-lookup"><span data-stu-id="301f0-104">Specifies leaving a copy of a message on the server for a POP account.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="301f0-105">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="301f0-105">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="301f0-106">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="301f0-106">Identifier:</span></span>  <br/> |<span data-ttu-id="301f0-107">0x1000</span><span class="sxs-lookup"><span data-stu-id="301f0-107">0x1000</span></span>  <br/> |
|<span data-ttu-id="301f0-108">Type de propriété:</span><span class="sxs-lookup"><span data-stu-id="301f0-108">Property type:</span></span>  <br/> |<span data-ttu-id="301f0-109">PT_DWORD</span><span class="sxs-lookup"><span data-stu-id="301f0-109">PT_DWORD</span></span>  <br/> |
|<span data-ttu-id="301f0-110">Balise de propriété:</span><span class="sxs-lookup"><span data-stu-id="301f0-110">Property tag:</span></span>  <br/> |<span data-ttu-id="301f0-111">0x10000003</span><span class="sxs-lookup"><span data-stu-id="301f0-111">0x10000003</span></span>  <br/> |
|<span data-ttu-id="301f0-112">Access</span><span class="sxs-lookup"><span data-stu-id="301f0-112">Access:</span></span>  <br/> |<span data-ttu-id="301f0-113">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="301f0-113">Read-only</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="301f0-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="301f0-114">Remarks</span></span>

<span data-ttu-id="301f0-115">Le tableau suivant répertorie les valeurs possibles.</span><span class="sxs-lookup"><span data-stu-id="301f0-115">The following table lists the possible values.</span></span> <span data-ttu-id="301f0-116">Pour plus d'informations sur les constantes [, voir constants (API de gestion des comptes)](constants-account-management-api.md) .</span><span class="sxs-lookup"><span data-stu-id="301f0-116">See [Constants (Account management API)](constants-account-management-api.md) for more information on the constants.</span></span> 
  
|<span data-ttu-id="301f0-117">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="301f0-117">**Possible values**</span></span>|<span data-ttu-id="301f0-118">**Description**</span><span class="sxs-lookup"><span data-stu-id="301f0-118">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="301f0-119">**LEAVE_ON_SERVER**</span><span class="sxs-lookup"><span data-stu-id="301f0-119">**LEAVE_ON_SERVER**</span></span> <br/> |<span data-ttu-id="301f0-120">Conserve une copie du message sur le serveur POP après avoir téléchargé le message sur un appareil.</span><span class="sxs-lookup"><span data-stu-id="301f0-120">Leaves a copy of the message on the POP server after downloading the message to a device.</span></span>  <br/> |
|<span data-ttu-id="301f0-121">**REMOVE_AFTER**</span><span class="sxs-lookup"><span data-stu-id="301f0-121">**REMOVE_AFTER**</span></span> <br/> |<span data-ttu-id="301f0-122">Supprime le message du serveur POP après l'avoir téléchargé sur un appareil.</span><span class="sxs-lookup"><span data-stu-id="301f0-122">Removes the message from the POP server after downloading it to a device.</span></span>  <br/> |
|<span data-ttu-id="301f0-123">**REMOVE_ON_NUKE**</span><span class="sxs-lookup"><span data-stu-id="301f0-123">**REMOVE_ON_NUKE**</span></span> <br/> |<span data-ttu-id="301f0-124">Supprime le message du serveur POP uniquement une fois que l'utilisateur a supprimé le message du dossier éléments supprimés.</span><span class="sxs-lookup"><span data-stu-id="301f0-124">Removes the message from the POP server only after the user deletes the message from the Deleted Items folder.</span></span>  <br/> |
|<span data-ttu-id="301f0-125">**GET_REMOVE_AFTER_DAYS** ( _UL_)</span><span class="sxs-lookup"><span data-stu-id="301f0-125">**GET_REMOVE_AFTER_DAYS**( _ul_)</span></span>  <br/> |<span data-ttu-id="301f0-126">Obtient le nombre de jours après lequel le message sera supprimé du serveur POP.</span><span class="sxs-lookup"><span data-stu-id="301f0-126">Gets the number of days after which the message will be removed from the POP server.</span></span>  <br/> |
|<span data-ttu-id="301f0-127">**SET_REMOVE_AFTER_DAYS** ( _jours_)</span><span class="sxs-lookup"><span data-stu-id="301f0-127">**SET_REMOVE_AFTER_DAYS**( _days_)</span></span>  <br/> |<span data-ttu-id="301f0-128">Définit le nombre de jours après lequel le message sera supprimé du serveur POP.</span><span class="sxs-lookup"><span data-stu-id="301f0-128">Sets the number of days after which the message will be removed from the POP server.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="301f0-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="301f0-129">See also</span></span>

- [<span data-ttu-id="301f0-130">Gestion des téléchargements de messages pour les comptes POP3</span><span class="sxs-lookup"><span data-stu-id="301f0-130">Managing message downloads for POP3 accounts</span></span>](managing-message-downloads-for-pop3-accounts.md) 
- [<span data-ttu-id="301f0-131">Constantes (API de gestion des comptes)</span><span class="sxs-lookup"><span data-stu-id="301f0-131">Constants (Account management API)</span></span>](constants-account-management-api.md)

