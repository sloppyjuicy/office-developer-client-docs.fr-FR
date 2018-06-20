---
title: PROP_ACCT_MINI_UID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 30d8268e-0c64-401d-8799-e8e1ba78b88f
description: Retourne un identificateur de compte qui est unique pour les profils Outlook.
ms.openlocfilehash: 9b2e30c0f57a54af219e68a8c2fe91e5dba4ddbe
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782813"
---
# <a name="propacctminiuid"></a><span data-ttu-id="c57ac-103">PROP_ACCT_MINI_UID</span><span class="sxs-lookup"><span data-stu-id="c57ac-103">PROP_ACCT_MINI_UID</span></span>

<span data-ttu-id="c57ac-104">Retourne un identificateur de compte qui est unique pour les profils Outlook.</span><span class="sxs-lookup"><span data-stu-id="c57ac-104">Returns an account identifier that is unique across Outlook profiles.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="c57ac-105">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="c57ac-105">Quick info</span></span>

<span data-ttu-id="c57ac-106">Voir [IOlkAccount](iolkaccount.md).</span><span class="sxs-lookup"><span data-stu-id="c57ac-106">See [IOlkAccount](iolkaccount.md).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c57ac-107">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="c57ac-107">Identifier:</span></span>  <br/> |<span data-ttu-id="c57ac-108">0x0003</span><span class="sxs-lookup"><span data-stu-id="c57ac-108">0x0003</span></span>  <br/> |
|<span data-ttu-id="c57ac-109">Type de propriété :</span><span class="sxs-lookup"><span data-stu-id="c57ac-109">Property type:</span></span>  <br/> |<span data-ttu-id="c57ac-110">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="c57ac-110">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="c57ac-111">Balise de propriété :</span><span class="sxs-lookup"><span data-stu-id="c57ac-111">Property tag:</span></span>  <br/> |<span data-ttu-id="c57ac-112">0x00030003</span><span class="sxs-lookup"><span data-stu-id="c57ac-112">0x00030003</span></span>  <br/> |
|<span data-ttu-id="c57ac-113">Access :</span><span class="sxs-lookup"><span data-stu-id="c57ac-113">Access:</span></span>  <br/> |<span data-ttu-id="c57ac-114">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c57ac-114">Read-only</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c57ac-115">Remarques</span><span class="sxs-lookup"><span data-stu-id="c57ac-115">Remarks</span></span>

<span data-ttu-id="c57ac-116">Obtenez cette propriété à l’aide de [IOlkAccount::GetProp](iolkaccount-getprop.md).</span><span class="sxs-lookup"><span data-stu-id="c57ac-116">Get this property by using [IOlkAccount::GetProp](iolkaccount-getprop.md).</span></span> <span data-ttu-id="c57ac-117">Si le client essaie de définir cette propriété, cette propriété renvoie **E_OLK_PROP_READ_ONLY**.</span><span class="sxs-lookup"><span data-stu-id="c57ac-117">If the client attempts to set this property, this property returns **E_OLK_PROP_READ_ONLY**.</span></span> 
  
<span data-ttu-id="c57ac-118">Cette propriété est différente de [PROP_ACCT_ID](prop_acct_id.md) dans la mesure où sa valeur identifie le compte au sein et en dehors du profil dans lequel le compte a été créé, tandis que **PROP_ACCT_ID** est unique seulement parmi tous les comptes au sein d’un profil dans lequel le compte a été créé.</span><span class="sxs-lookup"><span data-stu-id="c57ac-118">This property is different from [PROP_ACCT_ID](prop_acct_id.md) in that its value uniquely identifies the account within and outside of the profile in which the account was created, whereas **PROP_ACCT_ID** is unique only among all the accounts within that one profile in which the account was created.</span></span> <span data-ttu-id="c57ac-119">Lorsqu’un message avec ces propriétés se déplace sur un deuxième ordinateur avec un autre profil Outlook et un ensemble différent de comptes, **PROP_ACCT_MINI_UID** peuvent identifier le compte d’origine dans le profil d’origine.</span><span class="sxs-lookup"><span data-stu-id="c57ac-119">When a message with these properties roams onto a second computer with a different Outlook profile and different set of accounts, **PROP_ACCT_MINI_UID** can uniquely identify the original account in the original profile.</span></span> <span data-ttu-id="c57ac-120">Toutefois, **PROP_ACCT_ID** peut éventuellement entre en conflit avec un compte dans le profil de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="c57ac-120">However, **PROP_ACCT_ID** can possibly conflict with an account in the profile of the second computer.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="c57ac-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c57ac-121">See also</span></span>

- [<span data-ttu-id="c57ac-122">PROP_ACCT_ID</span><span class="sxs-lookup"><span data-stu-id="c57ac-122">PROP_ACCT_ID</span></span>](prop_acct_id.md)  
- [<span data-ttu-id="c57ac-123">À propos de l'API de gestion de compte</span><span class="sxs-lookup"><span data-stu-id="c57ac-123">About the Account Management API</span></span>](about-the-account-management-api.md) 
- [<span data-ttu-id="c57ac-124">Constantes (API de gestion des comptes)</span><span class="sxs-lookup"><span data-stu-id="c57ac-124">Constants (Account management API)</span></span>](constants-account-management-api.md)

