---
title: PROP_ACCT_USER_EMAIL_ADDR
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: fe447899-d37a-4775-a09d-13ba3a878008
description: Spécifie l’adresse e-mail du compte.
ms.openlocfilehash: 115941fdf2fdec01da8d6bc1320ac6cdc0930ffa
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436775"
---
# <a name="prop_acct_user_email_addr"></a><span data-ttu-id="4b34b-103">PROP_ACCT_USER_EMAIL_ADDR</span><span class="sxs-lookup"><span data-stu-id="4b34b-103">PROP_ACCT_USER_EMAIL_ADDR</span></span>

<span data-ttu-id="4b34b-104">Spécifie l’adresse e-mail du compte.</span><span class="sxs-lookup"><span data-stu-id="4b34b-104">Specifies the email address for the account.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="4b34b-105">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="4b34b-105">Quick info</span></span>

<span data-ttu-id="4b34b-106">Voir [IOlkAccount](iolkaccount.md).</span><span class="sxs-lookup"><span data-stu-id="4b34b-106">See [IOlkAccount](iolkaccount.md).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="4b34b-107">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="4b34b-107">Identifier:</span></span>  <br/> |<span data-ttu-id="4b34b-108">0x000C</span><span class="sxs-lookup"><span data-stu-id="4b34b-108">0x000C</span></span>  <br/> |
|<span data-ttu-id="4b34b-109">Type de propriété :</span><span class="sxs-lookup"><span data-stu-id="4b34b-109">Property type:</span></span>  <br/> |<span data-ttu-id="4b34b-110">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="4b34b-110">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="4b34b-111">Balise de propriété :</span><span class="sxs-lookup"><span data-stu-id="4b34b-111">Property tag:</span></span>  <br/> |<span data-ttu-id="4b34b-112">0x000C001F</span><span class="sxs-lookup"><span data-stu-id="4b34b-112">0x000C001F</span></span>  <br/> |
|<span data-ttu-id="4b34b-113">Accès :</span><span class="sxs-lookup"><span data-stu-id="4b34b-113">Access:</span></span>  <br/> |<span data-ttu-id="4b34b-114">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="4b34b-114">Read/write</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4b34b-115">Remarques</span><span class="sxs-lookup"><span data-stu-id="4b34b-115">Remarks</span></span>

 <span data-ttu-id="4b34b-116">**PROP_ACCT_USER_EMAIL_ADDR** n’est pas censé exister sur chaque compte.</span><span class="sxs-lookup"><span data-stu-id="4b34b-116">**PROP_ACCT_USER_EMAIL_ADDR** is not expected to exist on every account.</span></span> <span data-ttu-id="4b34b-117">Par exemple, un compte [](prop_mapi_identity_entryid.md) Exchange peut avoir des PROP_MAPI_IDENTITY_ENTRYID mais pas PROP_ACCT_USER_EMAIL_ADDR **,** alors que pour un compte SMTP/POP3, la situation est inversée.</span><span class="sxs-lookup"><span data-stu-id="4b34b-117">For example, an Exchange account could have [PROP_MAPI_IDENTITY_ENTRYID](prop_mapi_identity_entryid.md) but not **PROP_ACCT_USER_EMAIL_ADDR**, while for an SMTP/POP3 account, the situation is reversed.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="4b34b-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4b34b-118">See also</span></span>

- [<span data-ttu-id="4b34b-119">À propos de l'API de gestion de compte</span><span class="sxs-lookup"><span data-stu-id="4b34b-119">About the Account Management API</span></span>](about-the-account-management-api.md)

