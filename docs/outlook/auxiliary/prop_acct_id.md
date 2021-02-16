---
title: PROP_ACCT_ID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b72124aa-2e85-057c-9343-a40af60b91a0
description: Renvoie un identificateur qui identifie de manière unique un compte dans le profil dans lequel le compte est créé.
ms.openlocfilehash: dcb0a7935b9b764c44088971a1acb1f3647cbdb0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407164"
---
# <a name="prop_acct_id"></a><span data-ttu-id="16ae5-103">PROP_ACCT_ID</span><span class="sxs-lookup"><span data-stu-id="16ae5-103">PROP_ACCT_ID</span></span>

<span data-ttu-id="16ae5-104">Renvoie un identificateur qui identifie de manière unique un compte dans le profil dans lequel le compte est créé.</span><span class="sxs-lookup"><span data-stu-id="16ae5-104">Returns an identifier that uniquely identifies an account within the profile in which the account is created.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="16ae5-105">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="16ae5-105">Quick info</span></span>

<span data-ttu-id="16ae5-106">Voir [IOlkAccount](iolkaccount.md).</span><span class="sxs-lookup"><span data-stu-id="16ae5-106">See [IOlkAccount](iolkaccount.md).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="16ae5-107">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="16ae5-107">Identifier:</span></span>  <br/> |<span data-ttu-id="16ae5-108">0x0001</span><span class="sxs-lookup"><span data-stu-id="16ae5-108">0x0001</span></span>  <br/> |
|<span data-ttu-id="16ae5-109">Type de propriété :</span><span class="sxs-lookup"><span data-stu-id="16ae5-109">Property type:</span></span>  <br/> |<span data-ttu-id="16ae5-110">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="16ae5-110">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="16ae5-111">Balise de propriété :</span><span class="sxs-lookup"><span data-stu-id="16ae5-111">Property tag:</span></span>  <br/> |<span data-ttu-id="16ae5-112">0x00010003</span><span class="sxs-lookup"><span data-stu-id="16ae5-112">0x00010003</span></span>  <br/> |
|<span data-ttu-id="16ae5-113">Accès :</span><span class="sxs-lookup"><span data-stu-id="16ae5-113">Access:</span></span>  <br/> |<span data-ttu-id="16ae5-114">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="16ae5-114">Read-only</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="16ae5-115">Remarques</span><span class="sxs-lookup"><span data-stu-id="16ae5-115">Remarks</span></span>

<span data-ttu-id="16ae5-116">Obtenez cette propriété à [l’aide de IOlkAccount::GetProp](iolkaccount-getprop.md).</span><span class="sxs-lookup"><span data-stu-id="16ae5-116">Get this property by using [IOlkAccount::GetProp](iolkaccount-getprop.md).</span></span> <span data-ttu-id="16ae5-117">Si le client tente de définir cette propriété, cette propriété renvoie **E_OLK_PROP_READ_ONLY**.</span><span class="sxs-lookup"><span data-stu-id="16ae5-117">If the client attempts to set this property, this property returns **E_OLK_PROP_READ_ONLY**.</span></span> 
  
<span data-ttu-id="16ae5-118">Cette propriété est différente de [PROP_ACCT_MINI_UID](prop_acct_mini_uid.md) en ce que sa valeur est unique uniquement parmi tous les comptes au sein de ce profil dans lesquels le compte a été créé, tandis que PROP ACCT_MINI_UID identifie de manière unique le compte à l’intérieur et à l’extérieur du profil dans lequel le compte **\_ a** été créé.</span><span class="sxs-lookup"><span data-stu-id="16ae5-118">This property is different from [PROP_ACCT_MINI_UID](prop_acct_mini_uid.md) in that its value is unique only among all the accounts within that profile in which the account was created, whereas **PROP\_ACCT_MINI_UID** uniquely identifies the account within and outside of the profile in which the account was created.</span></span> <span data-ttu-id="16ae5-119">Lorsqu’un message avec ces propriétés se déplace sur un deuxième ordinateur avec un profil Outlook différent et un ensemble de comptes différent, **PROP_ACCT_ID** peut être en conflit avec un compte dans le profil du deuxième ordinateur, et **PROP_ACCT_MINI_UID** peut identifier de manière unique le compte d’origine dans le profil d’origine.</span><span class="sxs-lookup"><span data-stu-id="16ae5-119">When a message with these properties roams onto a second computer with a different Outlook profile and different set of accounts, **PROP_ACCT_ID** can possibly conflict with an account in the profile of the second computer, and **PROP_ACCT_MINI_UID** can uniquely identify the original account in the original profile.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="16ae5-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="16ae5-120">See also</span></span>

- [<span data-ttu-id="16ae5-121">À propos de l'API de gestion de compte</span><span class="sxs-lookup"><span data-stu-id="16ae5-121">About the Account Management API</span></span>](about-the-account-management-api.md)  
- [<span data-ttu-id="16ae5-122">Constantes (API de gestion des comptes)</span><span class="sxs-lookup"><span data-stu-id="16ae5-122">Constants (Account management API)</span></span>](constants-account-management-api.md)

