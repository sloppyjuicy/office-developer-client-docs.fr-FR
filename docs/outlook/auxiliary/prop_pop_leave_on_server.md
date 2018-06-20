---
title: PROP_POP_LEAVE_ON_SERVER
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 22d7c1e8-48b9-4768-b4de-9a9f32a3aabb
description: Spécifie la conservation d’une copie d’un message sur le serveur pour un compte POP.
ms.openlocfilehash: 9f986ff60a5824ece0a8bb91619323b58ec8b87a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782816"
---
# <a name="proppopleaveonserver"></a><span data-ttu-id="d49a8-103">PROP_POP_LEAVE_ON_SERVER</span><span class="sxs-lookup"><span data-stu-id="d49a8-103">PROP_POP_LEAVE_ON_SERVER</span></span>

<span data-ttu-id="d49a8-104">Spécifie la conservation d’une copie d’un message sur le serveur pour un compte POP.</span><span class="sxs-lookup"><span data-stu-id="d49a8-104">Specifies leaving a copy of a message on the server for a POP account.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="d49a8-105">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="d49a8-105">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d49a8-106">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="d49a8-106">Identifier:</span></span>  <br/> |<span data-ttu-id="d49a8-107">0 x 1000</span><span class="sxs-lookup"><span data-stu-id="d49a8-107">0x1000</span></span>  <br/> |
|<span data-ttu-id="d49a8-108">Type de propriété :</span><span class="sxs-lookup"><span data-stu-id="d49a8-108">Property type:</span></span>  <br/> |<span data-ttu-id="d49a8-109">PT_DWORD</span><span class="sxs-lookup"><span data-stu-id="d49a8-109">PT_DWORD</span></span>  <br/> |
|<span data-ttu-id="d49a8-110">Balise de propriété :</span><span class="sxs-lookup"><span data-stu-id="d49a8-110">Property tag:</span></span>  <br/> |<span data-ttu-id="d49a8-111">0x10000003</span><span class="sxs-lookup"><span data-stu-id="d49a8-111">0x10000003</span></span>  <br/> |
|<span data-ttu-id="d49a8-112">Access :</span><span class="sxs-lookup"><span data-stu-id="d49a8-112">Access:</span></span>  <br/> |<span data-ttu-id="d49a8-113">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d49a8-113">Read-only</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d49a8-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="d49a8-114">Remarks</span></span>

<span data-ttu-id="d49a8-115">Le tableau suivant répertorie les valeurs possibles.</span><span class="sxs-lookup"><span data-stu-id="d49a8-115">The following table lists the possible values.</span></span> <span data-ttu-id="d49a8-116">Pour plus d’informations sur l’une des constantes, voir [constantes (gestion des comptes d’API)](constants-account-management-api.md) .</span><span class="sxs-lookup"><span data-stu-id="d49a8-116">See [Constants (Account management API)](constants-account-management-api.md) for more information on the constants.</span></span> 
  
|<span data-ttu-id="d49a8-117">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="d49a8-117">**Possible values**</span></span>|<span data-ttu-id="d49a8-118">**Description**</span><span class="sxs-lookup"><span data-stu-id="d49a8-118">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="d49a8-119">**LEAVE_ON_SERVER**</span><span class="sxs-lookup"><span data-stu-id="d49a8-119">**LEAVE_ON_SERVER**</span></span> <br/> |<span data-ttu-id="d49a8-120">Laisse une copie du message sur le serveur POP après avoir téléchargé le message sur un périphérique.</span><span class="sxs-lookup"><span data-stu-id="d49a8-120">Leaves a copy of the message on the POP server after downloading the message to a device.</span></span>  <br/> |
|<span data-ttu-id="d49a8-121">**REMOVE_AFTER**</span><span class="sxs-lookup"><span data-stu-id="d49a8-121">**REMOVE_AFTER**</span></span> <br/> |<span data-ttu-id="d49a8-122">Supprime le message à partir du serveur POP après le téléchargement pour un périphérique.</span><span class="sxs-lookup"><span data-stu-id="d49a8-122">Removes the message from the POP server after downloading it to a device.</span></span>  <br/> |
|<span data-ttu-id="d49a8-123">**REMOVE_ON_NUKE**</span><span class="sxs-lookup"><span data-stu-id="d49a8-123">**REMOVE_ON_NUKE**</span></span> <br/> |<span data-ttu-id="d49a8-124">Supprime le message à partir du serveur POP uniquement une fois que l’utilisateur supprime le message à partir du dossier éléments supprimés.</span><span class="sxs-lookup"><span data-stu-id="d49a8-124">Removes the message from the POP server only after the user deletes the message from the Deleted Items folder.</span></span>  <br/> |
|<span data-ttu-id="d49a8-125">**GET_REMOVE_AFTER_DAYS** ( _ul_)</span><span class="sxs-lookup"><span data-stu-id="d49a8-125">**GET_REMOVE_AFTER_DAYS**( _ul_)</span></span>  <br/> |<span data-ttu-id="d49a8-126">Obtient le nombre de jours après lequel le message sera supprimé du serveur POP.</span><span class="sxs-lookup"><span data-stu-id="d49a8-126">Gets the number of days after which the message will be removed from the POP server.</span></span>  <br/> |
|<span data-ttu-id="d49a8-127">**SET_REMOVE_AFTER_DAYS** ( _jours_)</span><span class="sxs-lookup"><span data-stu-id="d49a8-127">**SET_REMOVE_AFTER_DAYS**( _days_)</span></span>  <br/> |<span data-ttu-id="d49a8-128">Définit le nombre de jours après lequel le message sera supprimé du serveur POP.</span><span class="sxs-lookup"><span data-stu-id="d49a8-128">Sets the number of days after which the message will be removed from the POP server.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d49a8-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d49a8-129">See also</span></span>

- [<span data-ttu-id="d49a8-130">Message de la gestion des téléchargements pour les comptes POP3</span><span class="sxs-lookup"><span data-stu-id="d49a8-130">Managing message downloads for POP3 accounts</span></span>](managing-message-downloads-for-pop3-accounts.md) 
- [<span data-ttu-id="d49a8-131">Constantes (API de gestion des comptes)</span><span class="sxs-lookup"><span data-stu-id="d49a8-131">Constants (Account management API)</span></span>](constants-account-management-api.md)

