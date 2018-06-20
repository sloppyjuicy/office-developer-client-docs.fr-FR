---
title: PROP_MAPI_TRANSPORT_FLAGS
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 12cfe096-6882-c0be-b248-87567cb71e83
description: Représente les paramètres de transport Outlook utilise pour déterminer les tâches de synchronisation et pour désactiver les éléments de l’interface utilisateur du compte ne prenant pas en charge.
ms.openlocfilehash: 95b61ea994557be76303f8b9b0541353b6ed13f6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782815"
---
# <a name="propmapitransportflags"></a><span data-ttu-id="2f6bb-103">PROP_MAPI_TRANSPORT_FLAGS</span><span class="sxs-lookup"><span data-stu-id="2f6bb-103">PROP_MAPI_TRANSPORT_FLAGS</span></span>

<span data-ttu-id="2f6bb-104">Représente les paramètres de transport Outlook utilise pour déterminer les tâches de synchronisation et pour désactiver les éléments de l’interface utilisateur du compte ne prenant pas en charge.</span><span class="sxs-lookup"><span data-stu-id="2f6bb-104">Represents transport settings that Outlook uses to determine the necessary synchronization tasks and to disable the user interface (UI) elements that the account does not support.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="2f6bb-105">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="2f6bb-105">Quick info</span></span>

<span data-ttu-id="2f6bb-106">Voir [IOlkAccount](iolkaccount.md).</span><span class="sxs-lookup"><span data-stu-id="2f6bb-106">See [IOlkAccount](iolkaccount.md).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="2f6bb-107">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="2f6bb-107">Identifier:</span></span>  <br/> |<span data-ttu-id="2f6bb-108">0x2010</span><span class="sxs-lookup"><span data-stu-id="2f6bb-108">0x2010</span></span>  <br/> |
|<span data-ttu-id="2f6bb-109">Type de propriété :</span><span class="sxs-lookup"><span data-stu-id="2f6bb-109">Property type:</span></span>  <br/> |<span data-ttu-id="2f6bb-110">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="2f6bb-110">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="2f6bb-111">Balise de propriété :</span><span class="sxs-lookup"><span data-stu-id="2f6bb-111">Property tag:</span></span>  <br/> |<span data-ttu-id="2f6bb-112">0x20100102</span><span class="sxs-lookup"><span data-stu-id="2f6bb-112">0x20100102</span></span>  <br/> |
|<span data-ttu-id="2f6bb-113">Access :</span><span class="sxs-lookup"><span data-stu-id="2f6bb-113">Access:</span></span>  <br/> |<span data-ttu-id="2f6bb-114">En lecture-écriture.</span><span class="sxs-lookup"><span data-stu-id="2f6bb-114">Read/write</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2f6bb-115">Remarques</span><span class="sxs-lookup"><span data-stu-id="2f6bb-115">Remarks</span></span>

<span data-ttu-id="2f6bb-116">Obtenir ou définir cette propriété à l’aide de [IOlkAccount::GetProp](iolkaccount-getprop.md) ou [IOlkAccount::SetProp](iolkaccount-setprop.md), respectivement.</span><span class="sxs-lookup"><span data-stu-id="2f6bb-116">Get or set this property by using [IOlkAccount::GetProp](iolkaccount-getprop.md) or [IOlkAccount::SetProp](iolkaccount-setprop.md), respectively.</span></span>
  
<span data-ttu-id="2f6bb-117">Renvoie **MAPIACCT_SEND_ONLY** si le compte peut uniquement envoyer des messages, mais ne peut pas recevoir de messages.</span><span class="sxs-lookup"><span data-stu-id="2f6bb-117">Returns **MAPIACCT_SEND_ONLY** if the account can only send messages but cannot receive messages.</span></span> <span data-ttu-id="2f6bb-118">Dans ce cas, Outlook désactive l’interface utilisateur qui ne s’applique pas à ce type de compte (par exemple, l’interface utilisateur pour **l’Envoi/réception**).</span><span class="sxs-lookup"><span data-stu-id="2f6bb-118">In this case, Outlook disables UI that does not apply to this type of accounts (for example, the UI for **Send/Receive**).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="2f6bb-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2f6bb-119">See also</span></span>

- [<span data-ttu-id="2f6bb-120">À propos de l'API de gestion de compte</span><span class="sxs-lookup"><span data-stu-id="2f6bb-120">About the Account Management API</span></span>](about-the-account-management-api.md)  
- [<span data-ttu-id="2f6bb-121">Constantes (API de gestion des comptes)</span><span class="sxs-lookup"><span data-stu-id="2f6bb-121">Constants (Account management API)</span></span>](constants-account-management-api.md)

