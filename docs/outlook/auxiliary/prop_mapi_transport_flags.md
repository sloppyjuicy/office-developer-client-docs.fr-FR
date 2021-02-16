---
title: PROP_MAPI_TRANSPORT_FLAGS
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 12cfe096-6882-c0be-b248-87567cb71e83
description: Représente les paramètres de transport qu’Outlook utilise pour déterminer les tâches de synchronisation nécessaires et pour désactiver les éléments d’interface utilisateur que le compte ne prend pas en charge.
ms.openlocfilehash: 707306c3bfbeebdd18f82bacfc121274be08aa50
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404525"
---
# <a name="prop_mapi_transport_flags"></a><span data-ttu-id="1118b-103">PROP_MAPI_TRANSPORT_FLAGS</span><span class="sxs-lookup"><span data-stu-id="1118b-103">PROP_MAPI_TRANSPORT_FLAGS</span></span>

<span data-ttu-id="1118b-104">Représente les paramètres de transport qu’Outlook utilise pour déterminer les tâches de synchronisation nécessaires et pour désactiver les éléments d’interface utilisateur que le compte ne prend pas en charge.</span><span class="sxs-lookup"><span data-stu-id="1118b-104">Represents transport settings that Outlook uses to determine the necessary synchronization tasks and to disable the user interface (UI) elements that the account does not support.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="1118b-105">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="1118b-105">Quick info</span></span>

<span data-ttu-id="1118b-106">Voir [IOlkAccount](iolkaccount.md).</span><span class="sxs-lookup"><span data-stu-id="1118b-106">See [IOlkAccount](iolkaccount.md).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="1118b-107">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="1118b-107">Identifier:</span></span>  <br/> |<span data-ttu-id="1118b-108">0x2010</span><span class="sxs-lookup"><span data-stu-id="1118b-108">0x2010</span></span>  <br/> |
|<span data-ttu-id="1118b-109">Type de propriété :</span><span class="sxs-lookup"><span data-stu-id="1118b-109">Property type:</span></span>  <br/> |<span data-ttu-id="1118b-110">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="1118b-110">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="1118b-111">Balise de propriété :</span><span class="sxs-lookup"><span data-stu-id="1118b-111">Property tag:</span></span>  <br/> |<span data-ttu-id="1118b-112">0x20100102</span><span class="sxs-lookup"><span data-stu-id="1118b-112">0x20100102</span></span>  <br/> |
|<span data-ttu-id="1118b-113">Accès :</span><span class="sxs-lookup"><span data-stu-id="1118b-113">Access:</span></span>  <br/> |<span data-ttu-id="1118b-114">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="1118b-114">Read/write</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1118b-115">Remarques</span><span class="sxs-lookup"><span data-stu-id="1118b-115">Remarks</span></span>

<span data-ttu-id="1118b-116">Obtenez ou définissez cette propriété à l’aide [d’IOlkAccount::GetProp](iolkaccount-getprop.md) ou [IOlkAccount::SetProp,](iolkaccount-setprop.md)respectivement.</span><span class="sxs-lookup"><span data-stu-id="1118b-116">Get or set this property by using [IOlkAccount::GetProp](iolkaccount-getprop.md) or [IOlkAccount::SetProp](iolkaccount-setprop.md), respectively.</span></span>
  
<span data-ttu-id="1118b-117">Renvoie **MAPIACCT_SEND_ONLY** si le compte peut uniquement envoyer des messages, mais ne peut pas recevoir de messages.</span><span class="sxs-lookup"><span data-stu-id="1118b-117">Returns **MAPIACCT_SEND_ONLY** if the account can only send messages but cannot receive messages.</span></span> <span data-ttu-id="1118b-118">Dans ce cas, Outlook désactive l’interface utilisateur qui ne s’applique pas à ce type de comptes (par exemple, l’interface utilisateur pour **l’envoi/réception).**</span><span class="sxs-lookup"><span data-stu-id="1118b-118">In this case, Outlook disables UI that does not apply to this type of accounts (for example, the UI for **Send/Receive**).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="1118b-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1118b-119">See also</span></span>

- [<span data-ttu-id="1118b-120">À propos de l'API de gestion de compte</span><span class="sxs-lookup"><span data-stu-id="1118b-120">About the Account Management API</span></span>](about-the-account-management-api.md)  
- [<span data-ttu-id="1118b-121">Constantes (API de gestion des comptes)</span><span class="sxs-lookup"><span data-stu-id="1118b-121">Constants (Account management API)</span></span>](constants-account-management-api.md)

