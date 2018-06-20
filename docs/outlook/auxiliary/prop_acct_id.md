---
title: PROP_ACCT_ID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b72124aa-2e85-057c-9343-a40af60b91a0
description: Retourne un identificateur qui identifie de manière unique un compte dans le profil dans lequel le compte est créé.
ms.openlocfilehash: a4ae193b89132ea718e16aec82f592205f9771c3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782812"
---
# <a name="propacctid"></a><span data-ttu-id="375c8-103">PROP_ACCT_ID</span><span class="sxs-lookup"><span data-stu-id="375c8-103">PROP_ACCT_ID</span></span>

<span data-ttu-id="375c8-104">Retourne un identificateur qui identifie de manière unique un compte dans le profil dans lequel le compte est créé.</span><span class="sxs-lookup"><span data-stu-id="375c8-104">Returns an identifier that uniquely identifies an account within the profile in which the account is created.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="375c8-105">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="375c8-105">Quick info</span></span>

<span data-ttu-id="375c8-106">Voir [IOlkAccount](iolkaccount.md).</span><span class="sxs-lookup"><span data-stu-id="375c8-106">See [IOlkAccount](iolkaccount.md).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="375c8-107">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="375c8-107">Identifier:</span></span>  <br/> |<span data-ttu-id="375c8-108">0x0001</span><span class="sxs-lookup"><span data-stu-id="375c8-108">0x0001</span></span>  <br/> |
|<span data-ttu-id="375c8-109">Type de propriété :</span><span class="sxs-lookup"><span data-stu-id="375c8-109">Property type:</span></span>  <br/> |<span data-ttu-id="375c8-110">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="375c8-110">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="375c8-111">Balise de propriété :</span><span class="sxs-lookup"><span data-stu-id="375c8-111">Property tag:</span></span>  <br/> |<span data-ttu-id="375c8-112">0 x 00010003</span><span class="sxs-lookup"><span data-stu-id="375c8-112">0x00010003</span></span>  <br/> |
|<span data-ttu-id="375c8-113">Access :</span><span class="sxs-lookup"><span data-stu-id="375c8-113">Access:</span></span>  <br/> |<span data-ttu-id="375c8-114">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="375c8-114">Read-only</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="375c8-115">Remarques</span><span class="sxs-lookup"><span data-stu-id="375c8-115">Remarks</span></span>

<span data-ttu-id="375c8-116">Obtenez cette propriété à l’aide de [IOlkAccount::GetProp](iolkaccount-getprop.md).</span><span class="sxs-lookup"><span data-stu-id="375c8-116">Get this property by using [IOlkAccount::GetProp](iolkaccount-getprop.md).</span></span> <span data-ttu-id="375c8-117">Si le client essaie de définir cette propriété, cette propriété renvoie **E_OLK_PROP_READ_ONLY**.</span><span class="sxs-lookup"><span data-stu-id="375c8-117">If the client attempts to set this property, this property returns **E_OLK_PROP_READ_ONLY**.</span></span> 
  
<span data-ttu-id="375c8-118">Cette propriété est différente de [PROP_ACCT_MINI_UID](prop_acct_mini_uid.md) dans la mesure où sa valeur est unique seulement parmi tous les comptes dans ce profil dans lequel le compte a été créé, tandis que **propriétés\_ACCT_MINI_UID** identifie de manière unique le compte et à l’extérieur du profil dans lequel le compte a été créé.</span><span class="sxs-lookup"><span data-stu-id="375c8-118">This property is different from [PROP_ACCT_MINI_UID](prop_acct_mini_uid.md) in that its value is unique only among all the accounts within that profile in which the account was created, whereas **PROP\_ACCT_MINI_UID** uniquely identifies the account within and outside of the profile in which the account was created.</span></span> <span data-ttu-id="375c8-119">Lorsqu’un message avec ces propriétés se déplace sur un deuxième ordinateur avec un autre profil Outlook et un ensemble différent de comptes, **PROP_ACCT_ID** peut éventuellement entrer en conflit avec un compte dans le profil du deuxième ordinateur et **PROP_ACCT_MINI_UID** peuvent identifier le compte d’origine dans le profil d’origine.</span><span class="sxs-lookup"><span data-stu-id="375c8-119">When a message with these properties roams onto a second computer with a different Outlook profile and different set of accounts, **PROP_ACCT_ID** can possibly conflict with an account in the profile of the second computer, and **PROP_ACCT_MINI_UID** can uniquely identify the original account in the original profile.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="375c8-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="375c8-120">See also</span></span>

- [<span data-ttu-id="375c8-121">À propos de l'API de gestion de compte</span><span class="sxs-lookup"><span data-stu-id="375c8-121">About the Account Management API</span></span>](about-the-account-management-api.md)  
- [<span data-ttu-id="375c8-122">Constantes (API de gestion des comptes)</span><span class="sxs-lookup"><span data-stu-id="375c8-122">Constants (Account management API)</span></span>](constants-account-management-api.md)

