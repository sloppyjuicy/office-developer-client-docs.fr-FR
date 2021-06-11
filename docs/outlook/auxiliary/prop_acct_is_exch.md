---
title: PROP_ACCT_IS_EXCH
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 599bfc7d-7b62-7cc1-69ff-6db04c96a49b
description: Cette valeur a la valeur True si le compte est Exchange client.
ms.openlocfilehash: 2df750b208ff9d2a18cb0d7c22ec6b32b658c7b4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418231"
---
# <a name="prop_acct_is_exch"></a><span data-ttu-id="5680c-103">PROP_ACCT_IS_EXCH</span><span class="sxs-lookup"><span data-stu-id="5680c-103">PROP_ACCT_IS_EXCH</span></span>

<span data-ttu-id="5680c-104">Cette valeur a la valeur True si le compte est Exchange client.</span><span class="sxs-lookup"><span data-stu-id="5680c-104">True if the account is an Exchange account.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="5680c-105">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="5680c-105">Quick info</span></span>

<span data-ttu-id="5680c-106">Voir [IOlkAccount](iolkaccount.md).</span><span class="sxs-lookup"><span data-stu-id="5680c-106">See [IOlkAccount](iolkaccount.md).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="5680c-107">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="5680c-107">Identifier:</span></span>  <br/> |<span data-ttu-id="5680c-108">0x0014</span><span class="sxs-lookup"><span data-stu-id="5680c-108">0x0014</span></span>  <br/> |
|<span data-ttu-id="5680c-109">Type de propriété :</span><span class="sxs-lookup"><span data-stu-id="5680c-109">Property type:</span></span>  <br/> |<span data-ttu-id="5680c-110">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="5680c-110">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="5680c-111">Balise de propriété :</span><span class="sxs-lookup"><span data-stu-id="5680c-111">Property tag:</span></span>  <br/> |<span data-ttu-id="5680c-112">0x00140003</span><span class="sxs-lookup"><span data-stu-id="5680c-112">0x00140003</span></span>  <br/> |
|<span data-ttu-id="5680c-113">Accès :</span><span class="sxs-lookup"><span data-stu-id="5680c-113">Access:</span></span>  <br/> |<span data-ttu-id="5680c-114">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5680c-114">Read-only</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5680c-115">Remarques</span><span class="sxs-lookup"><span data-stu-id="5680c-115">Remarks</span></span>

<span data-ttu-id="5680c-116">Obtenez cette propriété à [l’aide de IOlkAccount::GetProp](iolkaccount-getprop.md).</span><span class="sxs-lookup"><span data-stu-id="5680c-116">Get this property by using [IOlkAccount::GetProp](iolkaccount-getprop.md).</span></span> <span data-ttu-id="5680c-117">Si le client tente de définir cette propriété, cette propriété renvoie **E_OLK_PROP_READ_ONLY**.</span><span class="sxs-lookup"><span data-stu-id="5680c-117">If the client attempts to set this property, this property returns **E_OLK_PROP_READ_ONLY**.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="5680c-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5680c-118">See also</span></span>

- [<span data-ttu-id="5680c-119">À propos de l'API de gestion de compte</span><span class="sxs-lookup"><span data-stu-id="5680c-119">About the Account Management API</span></span>](about-the-account-management-api.md) 
- [<span data-ttu-id="5680c-120">Constantes (API de gestion des comptes)</span><span class="sxs-lookup"><span data-stu-id="5680c-120">Constants (Account management API)</span></span>](constants-account-management-api.md)

