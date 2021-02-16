---
title: PROP_SMTP_AUTH_METHOD
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 4202cafc-9011-406d-90b3-8dabf531c90b
description: Spécifie la méthode d’authentification à utiliser pour le compte SMTP.
ms.openlocfilehash: bb5adeb1fe73ed8b7ab69ca584215b44e1a9e4b7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434640"
---
# <a name="prop_smtp_auth_method"></a><span data-ttu-id="7744a-103">PROP_SMTP_AUTH_METHOD</span><span class="sxs-lookup"><span data-stu-id="7744a-103">PROP_SMTP_AUTH_METHOD</span></span>

<span data-ttu-id="7744a-104">Spécifie la méthode d’authentification à utiliser pour le compte SMTP.</span><span class="sxs-lookup"><span data-stu-id="7744a-104">Specifies the authentication method to use for the SMTP account.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="7744a-105">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="7744a-105">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7744a-106">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="7744a-106">Identifier:</span></span>  <br/> |<span data-ttu-id="7744a-107">0x0208</span><span class="sxs-lookup"><span data-stu-id="7744a-107">0x0208</span></span>  <br/> |
|<span data-ttu-id="7744a-108">Type de propriété :</span><span class="sxs-lookup"><span data-stu-id="7744a-108">Property type:</span></span>  <br/> |<span data-ttu-id="7744a-109">PT_DWORD</span><span class="sxs-lookup"><span data-stu-id="7744a-109">PT_DWORD</span></span>  <br/> |
|<span data-ttu-id="7744a-110">Balise de propriété :</span><span class="sxs-lookup"><span data-stu-id="7744a-110">Property tag:</span></span>  <br/> |<span data-ttu-id="7744a-111">0x02080003</span><span class="sxs-lookup"><span data-stu-id="7744a-111">0x02080003</span></span>  <br/> |
|<span data-ttu-id="7744a-112">Accès :</span><span class="sxs-lookup"><span data-stu-id="7744a-112">Access:</span></span>  <br/> |<span data-ttu-id="7744a-113">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7744a-113">Read-only</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7744a-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="7744a-114">Remarks</span></span>

<span data-ttu-id="7744a-115">La valeur est un masque de bits des constantes suivantes.</span><span class="sxs-lookup"><span data-stu-id="7744a-115">The value is a bitmask of the following constants.</span></span> <span data-ttu-id="7744a-116">Voir [constantes (API de gestion des comptes)](constants-account-management-api.md) pour leurs valeurs.</span><span class="sxs-lookup"><span data-stu-id="7744a-116">See [Constants (Account management API)](constants-account-management-api.md) for their values.</span></span> 
  
- <span data-ttu-id="7744a-117">**SMTP_AUTH_SAME_AS_POP** signifie utiliser les mêmes informations d’identification que mon serveur de messagerie entrant, comme fourni par les PROP_INET_USER [et](prop_inet_user.md) [PROP_INET_PASSWORD](prop_inet_password.md).</span><span class="sxs-lookup"><span data-stu-id="7744a-117">**SMTP_AUTH_SAME_AS_POP** means using the same credentials as my incoming mail server, as provided by [PROP_INET_USER](prop_inet_user.md) and [PROP_INET_PASSWORD](prop_inet_password.md).</span></span>
    
- <span data-ttu-id="7744a-118">**SMTP_AUTH_USER_PASS** signifie utiliser les informations d’identification fournies par les [PROP_SMTP_USER](prop_smtp_user.md) et [PROP_SMTP_PASSWORD](prop_smtp_password.md).</span><span class="sxs-lookup"><span data-stu-id="7744a-118">**SMTP_AUTH_USER_PASS** means using the credentials as provided by [PROP_SMTP_USER](prop_smtp_user.md) and [PROP_SMTP_PASSWORD](prop_smtp_password.md).</span></span>
    
- <span data-ttu-id="7744a-119">**SMTP_AUTH_RECEIVE_BEFORE_SEND** demande à l’utilisateur de se connecter au serveur de messagerie entrant avant d’envoyer des messages.</span><span class="sxs-lookup"><span data-stu-id="7744a-119">**SMTP_AUTH_RECEIVE_BEFORE_SEND** means requesting the user to log on to the incoming mail server before sending mail.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="7744a-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7744a-120">See also</span></span>

- [<span data-ttu-id="7744a-121">Gestion des téléchargements de messages pour les comptes POP3</span><span class="sxs-lookup"><span data-stu-id="7744a-121">Managing message downloads for POP3 accounts</span></span>](managing-message-downloads-for-pop3-accounts.md)  
- [<span data-ttu-id="7744a-122">Constantes (API de gestion des comptes)</span><span class="sxs-lookup"><span data-stu-id="7744a-122">Constants (Account management API)</span></span>](constants-account-management-api.md)

