---
title: PROP_SMTP_AUTH_METHOD
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 4202cafc-9011-406d-90b3-8dabf531c90b
description: Spécifie la méthode d’authentification à utiliser pour le compte SMTP.
ms.openlocfilehash: 0c52f1eeca8f7ac3e63cccf712dd672c2247be6a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782829"
---
# <a name="propsmtpauthmethod"></a><span data-ttu-id="f4bcf-103">PROP_SMTP_AUTH_METHOD</span><span class="sxs-lookup"><span data-stu-id="f4bcf-103">PROP_SMTP_AUTH_METHOD</span></span>

<span data-ttu-id="f4bcf-104">Spécifie la méthode d’authentification à utiliser pour le compte SMTP.</span><span class="sxs-lookup"><span data-stu-id="f4bcf-104">Specifies the authentication method to use for the SMTP account.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="f4bcf-105">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="f4bcf-105">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f4bcf-106">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="f4bcf-106">Identifier:</span></span>  <br/> |<span data-ttu-id="f4bcf-107">0x0208</span><span class="sxs-lookup"><span data-stu-id="f4bcf-107">0x0208</span></span>  <br/> |
|<span data-ttu-id="f4bcf-108">Type de propriété :</span><span class="sxs-lookup"><span data-stu-id="f4bcf-108">Property type:</span></span>  <br/> |<span data-ttu-id="f4bcf-109">PT_DWORD</span><span class="sxs-lookup"><span data-stu-id="f4bcf-109">PT_DWORD</span></span>  <br/> |
|<span data-ttu-id="f4bcf-110">Balise de propriété :</span><span class="sxs-lookup"><span data-stu-id="f4bcf-110">Property tag:</span></span>  <br/> |<span data-ttu-id="f4bcf-111">0x02080003</span><span class="sxs-lookup"><span data-stu-id="f4bcf-111">0x02080003</span></span>  <br/> |
|<span data-ttu-id="f4bcf-112">Access :</span><span class="sxs-lookup"><span data-stu-id="f4bcf-112">Access:</span></span>  <br/> |<span data-ttu-id="f4bcf-113">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f4bcf-113">Read-only</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f4bcf-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="f4bcf-114">Remarks</span></span>

<span data-ttu-id="f4bcf-115">La valeur est un masque binaire composé des constantes suivantes.</span><span class="sxs-lookup"><span data-stu-id="f4bcf-115">The value is a bitmask of the following constants.</span></span> <span data-ttu-id="f4bcf-116">Voir [constantes (gestion des comptes d’API)](constants-account-management-api.md) pour leurs valeurs.</span><span class="sxs-lookup"><span data-stu-id="f4bcf-116">See [Constants (Account management API)](constants-account-management-api.md) for their values.</span></span> 
  
- <span data-ttu-id="f4bcf-117">**SMTP_AUTH_SAME_AS_POP** consiste à utiliser les mêmes informations d’identification en tant que serveur de courrier entrant, fourni par [PROP_INET_USER](prop_inet_user.md) et [PROP_INET_PASSWORD](prop_inet_password.md).</span><span class="sxs-lookup"><span data-stu-id="f4bcf-117">**SMTP_AUTH_SAME_AS_POP** means using the same credentials as my incoming mail server, as provided by [PROP_INET_USER](prop_inet_user.md) and [PROP_INET_PASSWORD](prop_inet_password.md).</span></span>
    
- <span data-ttu-id="f4bcf-118">**SMTP_AUTH_USER_PASS** signifie utilisant les informations d’identification fournie par [PROP_SMTP_USER](prop_smtp_user.md) et [PROP_SMTP_PASSWORD](prop_smtp_password.md).</span><span class="sxs-lookup"><span data-stu-id="f4bcf-118">**SMTP_AUTH_USER_PASS** means using the credentials as provided by [PROP_SMTP_USER](prop_smtp_user.md) and [PROP_SMTP_PASSWORD](prop_smtp_password.md).</span></span>
    
- <span data-ttu-id="f4bcf-119">**SMTP_AUTH_RECEIVE_BEFORE_SEND** signifie que la demande de l’utilisateur à se connecter au serveur de messagerie entrant avant l’envoi du courrier.</span><span class="sxs-lookup"><span data-stu-id="f4bcf-119">**SMTP_AUTH_RECEIVE_BEFORE_SEND** means requesting the user to log on to the incoming mail server before sending mail.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="f4bcf-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f4bcf-120">See also</span></span>

- [<span data-ttu-id="f4bcf-121">Message de la gestion des téléchargements pour les comptes POP3</span><span class="sxs-lookup"><span data-stu-id="f4bcf-121">Managing message downloads for POP3 accounts</span></span>](managing-message-downloads-for-pop3-accounts.md)  
- [<span data-ttu-id="f4bcf-122">Constantes (API de gestion des comptes)</span><span class="sxs-lookup"><span data-stu-id="f4bcf-122">Constants (Account management API)</span></span>](constants-account-management-api.md)

