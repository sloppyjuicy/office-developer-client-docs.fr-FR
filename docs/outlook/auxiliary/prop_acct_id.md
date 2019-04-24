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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327656"
---
# <a name="propacctid"></a><span data-ttu-id="a03c0-103">PROP_ACCT_ID</span><span class="sxs-lookup"><span data-stu-id="a03c0-103">PROP_ACCT_ID</span></span>

<span data-ttu-id="a03c0-104">Renvoie un identificateur qui identifie de manière unique un compte dans le profil dans lequel le compte est créé.</span><span class="sxs-lookup"><span data-stu-id="a03c0-104">Returns an identifier that uniquely identifies an account within the profile in which the account is created.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="a03c0-105">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="a03c0-105">Quick info</span></span>

<span data-ttu-id="a03c0-106">Voir [IOlkAccount](iolkaccount.md).</span><span class="sxs-lookup"><span data-stu-id="a03c0-106">See [IOlkAccount](iolkaccount.md).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a03c0-107">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="a03c0-107">Identifier:</span></span>  <br/> |<span data-ttu-id="a03c0-108">0x0001</span><span class="sxs-lookup"><span data-stu-id="a03c0-108">0x0001</span></span>  <br/> |
|<span data-ttu-id="a03c0-109">Type de propriété:</span><span class="sxs-lookup"><span data-stu-id="a03c0-109">Property type:</span></span>  <br/> |<span data-ttu-id="a03c0-110">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="a03c0-110">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="a03c0-111">Balise de propriété:</span><span class="sxs-lookup"><span data-stu-id="a03c0-111">Property tag:</span></span>  <br/> |<span data-ttu-id="a03c0-112">0x00010003</span><span class="sxs-lookup"><span data-stu-id="a03c0-112">0x00010003</span></span>  <br/> |
|<span data-ttu-id="a03c0-113">Access</span><span class="sxs-lookup"><span data-stu-id="a03c0-113">Access:</span></span>  <br/> |<span data-ttu-id="a03c0-114">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a03c0-114">Read-only</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a03c0-115">Remarques</span><span class="sxs-lookup"><span data-stu-id="a03c0-115">Remarks</span></span>

<span data-ttu-id="a03c0-116">Obtenez cette propriété à l'aide de [IOlkAccount:: getprop](iolkaccount-getprop.md).</span><span class="sxs-lookup"><span data-stu-id="a03c0-116">Get this property by using [IOlkAccount::GetProp](iolkaccount-getprop.md).</span></span> <span data-ttu-id="a03c0-117">Si le client tente de définir cette propriété, cette propriété renvoie **E_OLK_PROP_READ_ONLY**.</span><span class="sxs-lookup"><span data-stu-id="a03c0-117">If the client attempts to set this property, this property returns **E_OLK_PROP_READ_ONLY**.</span></span> 
  
<span data-ttu-id="a03c0-118">Cette propriété est différente de [PROP_ACCT_MINI_UID](prop_acct_mini_uid.md) en ce sens que sa valeur n'est unique que pour tous les comptes de ce profil dans lequel le compte a été créé, tandis que **prop\_ACCT_MINI_UID** identifie de manière unique le compte au sein de et en dehors du profil dans lequel le compte a été créé.</span><span class="sxs-lookup"><span data-stu-id="a03c0-118">This property is different from [PROP_ACCT_MINI_UID](prop_acct_mini_uid.md) in that its value is unique only among all the accounts within that profile in which the account was created, whereas **PROP\_ACCT_MINI_UID** uniquely identifies the account within and outside of the profile in which the account was created.</span></span> <span data-ttu-id="a03c0-119">Lorsqu'un message avec ces propriétés se déplace sur un deuxième ordinateur avec un profil Outlook différent et un autre ensemble de comptes, **PROP_ACCT_ID** peut éventuellement entrer en conflit avec un compte dans le profil du deuxième ordinateur et **PROP_ACCT_MINI_UID** peut identifier de manière unique le compte d'origine dans le profil d'origine.</span><span class="sxs-lookup"><span data-stu-id="a03c0-119">When a message with these properties roams onto a second computer with a different Outlook profile and different set of accounts, **PROP_ACCT_ID** can possibly conflict with an account in the profile of the second computer, and **PROP_ACCT_MINI_UID** can uniquely identify the original account in the original profile.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="a03c0-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a03c0-120">See also</span></span>

- [<span data-ttu-id="a03c0-121">À propos de l'API de gestion de compte</span><span class="sxs-lookup"><span data-stu-id="a03c0-121">About the Account Management API</span></span>](about-the-account-management-api.md)  
- [<span data-ttu-id="a03c0-122">Constantes (API de gestion des comptes)</span><span class="sxs-lookup"><span data-stu-id="a03c0-122">Constants (Account management API)</span></span>](constants-account-management-api.md)

