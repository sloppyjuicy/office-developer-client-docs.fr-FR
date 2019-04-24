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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326487"
---
# <a name="proppopleaveonserver"></a><span data-ttu-id="39188-103">PROP_POP_LEAVE_ON_SERVER</span><span class="sxs-lookup"><span data-stu-id="39188-103">PROP_POP_LEAVE_ON_SERVER</span></span>

<span data-ttu-id="39188-104">Spécifie la conservation d'une copie d'un message sur le serveur pour un compte POP.</span><span class="sxs-lookup"><span data-stu-id="39188-104">Specifies leaving a copy of a message on the server for a POP account.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="39188-105">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="39188-105">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="39188-106">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="39188-106">Identifier:</span></span>  <br/> |<span data-ttu-id="39188-107">0x1000</span><span class="sxs-lookup"><span data-stu-id="39188-107">0x1000</span></span>  <br/> |
|<span data-ttu-id="39188-108">Type de propriété:</span><span class="sxs-lookup"><span data-stu-id="39188-108">Property type:</span></span>  <br/> |<span data-ttu-id="39188-109">PT_DWORD</span><span class="sxs-lookup"><span data-stu-id="39188-109">PT_DWORD</span></span>  <br/> |
|<span data-ttu-id="39188-110">Balise de propriété:</span><span class="sxs-lookup"><span data-stu-id="39188-110">Property tag:</span></span>  <br/> |<span data-ttu-id="39188-111">0x10000003</span><span class="sxs-lookup"><span data-stu-id="39188-111">0x10000003</span></span>  <br/> |
|<span data-ttu-id="39188-112">Access</span><span class="sxs-lookup"><span data-stu-id="39188-112">Access:</span></span>  <br/> |<span data-ttu-id="39188-113">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="39188-113">Read-only</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="39188-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="39188-114">Remarks</span></span>

<span data-ttu-id="39188-115">Le tableau suivant répertorie les valeurs possibles.</span><span class="sxs-lookup"><span data-stu-id="39188-115">The following table lists the possible values.</span></span> <span data-ttu-id="39188-116">Pour plus d'informations sur les constantes [, voir constants (API de gestion des comptes)](constants-account-management-api.md) .</span><span class="sxs-lookup"><span data-stu-id="39188-116">See [Constants (Account management API)](constants-account-management-api.md) for more information on the constants.</span></span> 
  
|<span data-ttu-id="39188-117">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="39188-117">**Possible values**</span></span>|<span data-ttu-id="39188-118">**Description**</span><span class="sxs-lookup"><span data-stu-id="39188-118">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="39188-119">**LEAVE_ON_SERVER**</span><span class="sxs-lookup"><span data-stu-id="39188-119">**LEAVE_ON_SERVER**</span></span> <br/> |<span data-ttu-id="39188-120">Conserve une copie du message sur le serveur POP après avoir téléchargé le message sur un appareil.</span><span class="sxs-lookup"><span data-stu-id="39188-120">Leaves a copy of the message on the POP server after downloading the message to a device.</span></span>  <br/> |
|<span data-ttu-id="39188-121">**REMOVE_AFTER**</span><span class="sxs-lookup"><span data-stu-id="39188-121">**REMOVE_AFTER**</span></span> <br/> |<span data-ttu-id="39188-122">Supprime le message du serveur POP après l'avoir téléchargé sur un appareil.</span><span class="sxs-lookup"><span data-stu-id="39188-122">Removes the message from the POP server after downloading it to a device.</span></span>  <br/> |
|<span data-ttu-id="39188-123">**REMOVE_ON_NUKE**</span><span class="sxs-lookup"><span data-stu-id="39188-123">**REMOVE_ON_NUKE**</span></span> <br/> |<span data-ttu-id="39188-124">Supprime le message du serveur POP uniquement une fois que l'utilisateur a supprimé le message du dossier éléments supprimés.</span><span class="sxs-lookup"><span data-stu-id="39188-124">Removes the message from the POP server only after the user deletes the message from the Deleted Items folder.</span></span>  <br/> |
|<span data-ttu-id="39188-125">**GET_REMOVE_AFTER_DAYS** ( _UL_)</span><span class="sxs-lookup"><span data-stu-id="39188-125">**GET_REMOVE_AFTER_DAYS**( _ul_)</span></span>  <br/> |<span data-ttu-id="39188-126">Obtient le nombre de jours après lequel le message sera supprimé du serveur POP.</span><span class="sxs-lookup"><span data-stu-id="39188-126">Gets the number of days after which the message will be removed from the POP server.</span></span>  <br/> |
|<span data-ttu-id="39188-127">**SET_REMOVE_AFTER_DAYS** ( _jours_)</span><span class="sxs-lookup"><span data-stu-id="39188-127">**SET_REMOVE_AFTER_DAYS**( _days_)</span></span>  <br/> |<span data-ttu-id="39188-128">Définit le nombre de jours après lequel le message sera supprimé du serveur POP.</span><span class="sxs-lookup"><span data-stu-id="39188-128">Sets the number of days after which the message will be removed from the POP server.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="39188-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="39188-129">See also</span></span>

- [<span data-ttu-id="39188-130">Gestion des téléchargements de messages pour les comptes POP3</span><span class="sxs-lookup"><span data-stu-id="39188-130">Managing message downloads for POP3 accounts</span></span>](managing-message-downloads-for-pop3-accounts.md) 
- [<span data-ttu-id="39188-131">Constantes (API de gestion des comptes)</span><span class="sxs-lookup"><span data-stu-id="39188-131">Constants (Account management API)</span></span>](constants-account-management-api.md)

