---
title: PROP_ACCT_DELIVERY_STORE
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f5db43e9-687b-d467-1be1-3737e3f91c27
description: Représente l’identificateur d’entrée de la banque de remise par défaut pour le compte.
ms.openlocfilehash: 72c5325e70a6e8b42ee433d8d674c2b2ea0c8398
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782802"
---
# <a name="propacctdeliverystore"></a><span data-ttu-id="d1b69-103">PROP_ACCT_DELIVERY_STORE</span><span class="sxs-lookup"><span data-stu-id="d1b69-103">PROP_ACCT_DELIVERY_STORE</span></span>

<span data-ttu-id="d1b69-104">Représente l’identificateur d’entrée de la banque de remise par défaut pour le compte.</span><span class="sxs-lookup"><span data-stu-id="d1b69-104">Represents the Entry ID of the default delivery store for the account.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="d1b69-105">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="d1b69-105">Quick info</span></span>

<span data-ttu-id="d1b69-106">Voir [IOlkAccount](iolkaccount.md).</span><span class="sxs-lookup"><span data-stu-id="d1b69-106">See [IOlkAccount](iolkaccount.md).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="d1b69-107">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="d1b69-107">Identifier:</span></span>  <br/> |<span data-ttu-id="d1b69-108">0x0018</span><span class="sxs-lookup"><span data-stu-id="d1b69-108">0x0018</span></span>  <br/> |
|<span data-ttu-id="d1b69-109">Type de propriété :</span><span class="sxs-lookup"><span data-stu-id="d1b69-109">Property type:</span></span>  <br/> |<span data-ttu-id="d1b69-110">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="d1b69-110">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="d1b69-111">Balise de propriété :</span><span class="sxs-lookup"><span data-stu-id="d1b69-111">Property tag:</span></span>  <br/> |<span data-ttu-id="d1b69-112">0x00180102</span><span class="sxs-lookup"><span data-stu-id="d1b69-112">0x00180102</span></span>  <br/> |
|<span data-ttu-id="d1b69-113">Access :</span><span class="sxs-lookup"><span data-stu-id="d1b69-113">Access:</span></span>  <br/> |<span data-ttu-id="d1b69-114">En lecture-écriture.</span><span class="sxs-lookup"><span data-stu-id="d1b69-114">Read/write</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d1b69-115">Remarques</span><span class="sxs-lookup"><span data-stu-id="d1b69-115">Remarks</span></span>

<span data-ttu-id="d1b69-116">Obtenir ou définir cette propriété à l’aide de [IOlkAccount::GetProp](iolkaccount-getprop.md) ou [IOlkAccount::SetProp](iolkaccount-setprop.md), respectivement.</span><span class="sxs-lookup"><span data-stu-id="d1b69-116">Get or set this property by using [IOlkAccount::GetProp](iolkaccount-getprop.md) or [IOlkAccount::SetProp](iolkaccount-setprop.md), respectively.</span></span>
  
<span data-ttu-id="d1b69-117">Un des effets secondaires de la configuration d’un magasin en tant que la banque de remise par défaut d’un compte est que lors du démarrage d’Outlook, Outlook crée les dossiers de recherche de ce magasin si elles n’existe pas déjà et la banque dans la barre des tâches de la liste.</span><span class="sxs-lookup"><span data-stu-id="d1b69-117">One of the side effects of setting a store as the default delivery store for an account is that when starting Outlook, Outlook creates search folders for that store if they do not already exist, and list the store in the To-Do Bar.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="d1b69-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d1b69-118">See also</span></span>

- [<span data-ttu-id="d1b69-119">À propos de l'API de gestion de compte</span><span class="sxs-lookup"><span data-stu-id="d1b69-119">About the Account Management API</span></span>](about-the-account-management-api.md)
- [<span data-ttu-id="d1b69-120">Constantes (API de gestion des comptes)</span><span class="sxs-lookup"><span data-stu-id="d1b69-120">Constants (Account management API)</span></span>](constants-account-management-api.md)

