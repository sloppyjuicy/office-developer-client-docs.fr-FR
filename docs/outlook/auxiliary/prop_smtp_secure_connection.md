---
title: PROP_SMTP_SECURE_CONNECTION
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: e316a424-d789-4ce5-bcc6-263049f3659e
description: Spécifie le type de connexion chiffrée à utiliser pour un compte SMTP.
ms.openlocfilehash: e1c8c8dacf953407d4cbb114aa5ee0a4cdb6acf5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782825"
---
# <a name="propsmtpsecureconnection"></a><span data-ttu-id="77aef-103">PROP_SMTP_SECURE_CONNECTION</span><span class="sxs-lookup"><span data-stu-id="77aef-103">PROP_SMTP_SECURE_CONNECTION</span></span>

<span data-ttu-id="77aef-104">Spécifie le type de connexion chiffrée à utiliser pour un compte SMTP.</span><span class="sxs-lookup"><span data-stu-id="77aef-104">Specifies the type of encrypted connection to use for an SMTP account.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="77aef-105">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="77aef-105">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="77aef-106">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="77aef-106">Identifier:</span></span>  <br/> |<span data-ttu-id="77aef-107">0x020A</span><span class="sxs-lookup"><span data-stu-id="77aef-107">0x020A</span></span>  <br/> |
|<span data-ttu-id="77aef-108">Type de propriété :</span><span class="sxs-lookup"><span data-stu-id="77aef-108">Property type:</span></span>  <br/> |<span data-ttu-id="77aef-109">PT_DWORD</span><span class="sxs-lookup"><span data-stu-id="77aef-109">PT_DWORD</span></span>  <br/> |
|<span data-ttu-id="77aef-110">Balise de propriété :</span><span class="sxs-lookup"><span data-stu-id="77aef-110">Property tag:</span></span>  <br/> |<span data-ttu-id="77aef-111">0x020A0003</span><span class="sxs-lookup"><span data-stu-id="77aef-111">0x020A0003</span></span>  <br/> |
|<span data-ttu-id="77aef-112">Access :</span><span class="sxs-lookup"><span data-stu-id="77aef-112">Access:</span></span>  <br/> |<span data-ttu-id="77aef-113">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="77aef-113">Read-only</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="77aef-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="77aef-114">Remarks</span></span>

<span data-ttu-id="77aef-115">La valeur peut être une des constantes suivantes.</span><span class="sxs-lookup"><span data-stu-id="77aef-115">The value can be one of the following constants.</span></span> <span data-ttu-id="77aef-116">Voir [constantes (gestion des comptes d’API)](constants-account-management-api.md) pour leurs valeurs.</span><span class="sxs-lookup"><span data-stu-id="77aef-116">See [Constants (Account management API)](constants-account-management-api.md) for their values.</span></span> 
  
|<span data-ttu-id="77aef-117">**Constantes**</span><span class="sxs-lookup"><span data-stu-id="77aef-117">**Constants**</span></span>|<span data-ttu-id="77aef-118">**Description**</span><span class="sxs-lookup"><span data-stu-id="77aef-118">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="77aef-119">**ENCRYPT_CONN_NO_SECURITY**</span><span class="sxs-lookup"><span data-stu-id="77aef-119">**ENCRYPT_CONN_NO_SECURITY**</span></span> <br/> |<span data-ttu-id="77aef-120">Ne pas utiliser un chiffrement.</span><span class="sxs-lookup"><span data-stu-id="77aef-120">Do not use any encryption.</span></span>  <br/> |
|<span data-ttu-id="77aef-121">**ENCRYPT_CONN_SSL**</span><span class="sxs-lookup"><span data-stu-id="77aef-121">**ENCRYPT_CONN_SSL**</span></span> <br/> |<span data-ttu-id="77aef-122">Utiliser le chiffrement de Secure Sockets Layer (SSL).</span><span class="sxs-lookup"><span data-stu-id="77aef-122">Use Secure Socket Layer (SSL) encryption.</span></span>  <br/> |
|<span data-ttu-id="77aef-123">**ENCRYPT_CONN_TLS**</span><span class="sxs-lookup"><span data-stu-id="77aef-123">**ENCRYPT_CONN_TLS**</span></span> <br/> |<span data-ttu-id="77aef-124">Utiliser le protocole de chiffrement et d’authentification de sécurité TLS (Transport Layer).</span><span class="sxs-lookup"><span data-stu-id="77aef-124">Use Transport Layer Security (TLS) encryption and authentication protocol.</span></span>  <br/> |
|<span data-ttu-id="77aef-125">**ENCRYPT_CONN_AUTO**</span><span class="sxs-lookup"><span data-stu-id="77aef-125">**ENCRYPT_CONN_AUTO**</span></span> <br/> |<span data-ttu-id="77aef-126">Détecter automatiquement et utiliser la méthode de chiffrement pris en charge par le serveur de messagerie.</span><span class="sxs-lookup"><span data-stu-id="77aef-126">Automatically detect and use the encryption method supported by the mail server.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="77aef-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="77aef-127">See also</span></span>

- [<span data-ttu-id="77aef-128">Message de la gestion des téléchargements pour les comptes POP3</span><span class="sxs-lookup"><span data-stu-id="77aef-128">Managing message downloads for POP3 accounts</span></span>](managing-message-downloads-for-pop3-accounts.md) 
- [<span data-ttu-id="77aef-129">Constantes (API de gestion des comptes)</span><span class="sxs-lookup"><span data-stu-id="77aef-129">Constants (Account management API)</span></span>](constants-account-management-api.md)

