---
title: PROP_SMTP_SECURE_CONNECTION
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: e316a424-d789-4ce5-bcc6-263049f3659e
description: Spécifie le type de connexion chiffrée à utiliser pour un compte SMTP.
ms.openlocfilehash: 67eae5c9c5ca1b7f664ceaac0463ef3f3c9a291a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421283"
---
# <a name="propsmtpsecureconnection"></a><span data-ttu-id="1932e-103">PROP_SMTP_SECURE_CONNECTION</span><span class="sxs-lookup"><span data-stu-id="1932e-103">PROP_SMTP_SECURE_CONNECTION</span></span>

<span data-ttu-id="1932e-104">Spécifie le type de connexion chiffrée à utiliser pour un compte SMTP.</span><span class="sxs-lookup"><span data-stu-id="1932e-104">Specifies the type of encrypted connection to use for an SMTP account.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="1932e-105">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="1932e-105">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1932e-106">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="1932e-106">Identifier:</span></span>  <br/> |<span data-ttu-id="1932e-107">0x020A</span><span class="sxs-lookup"><span data-stu-id="1932e-107">0x020A</span></span>  <br/> |
|<span data-ttu-id="1932e-108">Type de propriété:</span><span class="sxs-lookup"><span data-stu-id="1932e-108">Property type:</span></span>  <br/> |<span data-ttu-id="1932e-109">PT_DWORD</span><span class="sxs-lookup"><span data-stu-id="1932e-109">PT_DWORD</span></span>  <br/> |
|<span data-ttu-id="1932e-110">Balise de propriété:</span><span class="sxs-lookup"><span data-stu-id="1932e-110">Property tag:</span></span>  <br/> |<span data-ttu-id="1932e-111">0x020A0003</span><span class="sxs-lookup"><span data-stu-id="1932e-111">0x020A0003</span></span>  <br/> |
|<span data-ttu-id="1932e-112">Access</span><span class="sxs-lookup"><span data-stu-id="1932e-112">Access:</span></span>  <br/> |<span data-ttu-id="1932e-113">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="1932e-113">Read-only</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1932e-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="1932e-114">Remarks</span></span>

<span data-ttu-id="1932e-115">La valeur peut être l'une des constantes suivantes.</span><span class="sxs-lookup"><span data-stu-id="1932e-115">The value can be one of the following constants.</span></span> <span data-ttu-id="1932e-116">Voir [constants (API de gestion des comptes)](constants-account-management-api.md) pour leurs valeurs.</span><span class="sxs-lookup"><span data-stu-id="1932e-116">See [Constants (Account management API)](constants-account-management-api.md) for their values.</span></span> 
  
|<span data-ttu-id="1932e-117">**Constants**</span><span class="sxs-lookup"><span data-stu-id="1932e-117">**Constants**</span></span>|<span data-ttu-id="1932e-118">**Description**</span><span class="sxs-lookup"><span data-stu-id="1932e-118">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="1932e-119">**ENCRYPT_CONN_NO_SECURITY**</span><span class="sxs-lookup"><span data-stu-id="1932e-119">**ENCRYPT_CONN_NO_SECURITY**</span></span> <br/> |<span data-ttu-id="1932e-120">N'utilisez pas de chiffrement.</span><span class="sxs-lookup"><span data-stu-id="1932e-120">Do not use any encryption.</span></span>  <br/> |
|<span data-ttu-id="1932e-121">**ENCRYPT_CONN_SSL**</span><span class="sxs-lookup"><span data-stu-id="1932e-121">**ENCRYPT_CONN_SSL**</span></span> <br/> |<span data-ttu-id="1932e-122">Utilisez le chiffrement SSL (Secure Socket Layer).</span><span class="sxs-lookup"><span data-stu-id="1932e-122">Use Secure Socket Layer (SSL) encryption.</span></span>  <br/> |
|<span data-ttu-id="1932e-123">**ENCRYPT_CONN_TLS**</span><span class="sxs-lookup"><span data-stu-id="1932e-123">**ENCRYPT_CONN_TLS**</span></span> <br/> |<span data-ttu-id="1932e-124">Utilisez le protocole de chiffrement TLS (Transport Layer Security) et le protocole d'authentification.</span><span class="sxs-lookup"><span data-stu-id="1932e-124">Use Transport Layer Security (TLS) encryption and authentication protocol.</span></span>  <br/> |
|<span data-ttu-id="1932e-125">**ENCRYPT_CONN_AUTO**</span><span class="sxs-lookup"><span data-stu-id="1932e-125">**ENCRYPT_CONN_AUTO**</span></span> <br/> |<span data-ttu-id="1932e-126">Détecte et utilise automatiquement la méthode de chiffrement prise en charge par le serveur de messagerie.</span><span class="sxs-lookup"><span data-stu-id="1932e-126">Automatically detect and use the encryption method supported by the mail server.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="1932e-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1932e-127">See also</span></span>

- [<span data-ttu-id="1932e-128">Gestion des téléchargements de messages pour les comptes POP3</span><span class="sxs-lookup"><span data-stu-id="1932e-128">Managing message downloads for POP3 accounts</span></span>](managing-message-downloads-for-pop3-accounts.md) 
- [<span data-ttu-id="1932e-129">Constantes (API de gestion des comptes)</span><span class="sxs-lookup"><span data-stu-id="1932e-129">Constants (Account management API)</span></span>](constants-account-management-api.md)

