---
title: PROP_ACCT_DELIVERY_STORE
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f5db43e9-687b-d467-1be1-3737e3f91c27
description: Représente l’ID d’entrée de la banque de remise par défaut pour le compte.
ms.openlocfilehash: d803c539ec99da4d7fb31063f48237788f3ac3d9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418896"
---
# <a name="prop_acct_delivery_store"></a><span data-ttu-id="6ed58-103">PROP_ACCT_DELIVERY_STORE</span><span class="sxs-lookup"><span data-stu-id="6ed58-103">PROP_ACCT_DELIVERY_STORE</span></span>

<span data-ttu-id="6ed58-104">Représente l’ID d’entrée de la banque de remise par défaut pour le compte.</span><span class="sxs-lookup"><span data-stu-id="6ed58-104">Represents the Entry ID of the default delivery store for the account.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="6ed58-105">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="6ed58-105">Quick info</span></span>

<span data-ttu-id="6ed58-106">Voir [IOlkAccount](iolkaccount.md).</span><span class="sxs-lookup"><span data-stu-id="6ed58-106">See [IOlkAccount](iolkaccount.md).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="6ed58-107">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="6ed58-107">Identifier:</span></span>  <br/> |<span data-ttu-id="6ed58-108">0x0018</span><span class="sxs-lookup"><span data-stu-id="6ed58-108">0x0018</span></span>  <br/> |
|<span data-ttu-id="6ed58-109">Type de propriété :</span><span class="sxs-lookup"><span data-stu-id="6ed58-109">Property type:</span></span>  <br/> |<span data-ttu-id="6ed58-110">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="6ed58-110">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="6ed58-111">Balise de propriété :</span><span class="sxs-lookup"><span data-stu-id="6ed58-111">Property tag:</span></span>  <br/> |<span data-ttu-id="6ed58-112">0x00180102</span><span class="sxs-lookup"><span data-stu-id="6ed58-112">0x00180102</span></span>  <br/> |
|<span data-ttu-id="6ed58-113">Accès :</span><span class="sxs-lookup"><span data-stu-id="6ed58-113">Access:</span></span>  <br/> |<span data-ttu-id="6ed58-114">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="6ed58-114">Read/write</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6ed58-115">Remarques</span><span class="sxs-lookup"><span data-stu-id="6ed58-115">Remarks</span></span>

<span data-ttu-id="6ed58-116">Obtenez ou définissez cette propriété à l’aide de [IOlkAccount::GetProp](iolkaccount-getprop.md) ou [IOlkAccount::SetProp,](iolkaccount-setprop.md)respectivement.</span><span class="sxs-lookup"><span data-stu-id="6ed58-116">Get or set this property by using [IOlkAccount::GetProp](iolkaccount-getprop.md) or [IOlkAccount::SetProp](iolkaccount-setprop.md), respectively.</span></span>
  
<span data-ttu-id="6ed58-117">L’un des effets secondaires de la définition d’une banque comme magasin de remise par défaut pour un compte est que lors du démarrage d’Outlook, Outlook crée des dossiers de recherche pour cette banque s’ils n’existent pas déjà et liste la banque dans la barre To-Do.</span><span class="sxs-lookup"><span data-stu-id="6ed58-117">One of the side effects of setting a store as the default delivery store for an account is that when starting Outlook, Outlook creates search folders for that store if they do not already exist, and list the store in the To-Do Bar.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="6ed58-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6ed58-118">See also</span></span>

- [<span data-ttu-id="6ed58-119">À propos de l'API de gestion de compte</span><span class="sxs-lookup"><span data-stu-id="6ed58-119">About the Account Management API</span></span>](about-the-account-management-api.md)
- [<span data-ttu-id="6ed58-120">Constantes (API de gestion des comptes)</span><span class="sxs-lookup"><span data-stu-id="6ed58-120">Constants (Account management API)</span></span>](constants-account-management-api.md)

