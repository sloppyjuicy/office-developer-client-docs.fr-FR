---
title: À propos de l’API de gestion des comptes
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: eb6b921d-ecf8-3ce5-87ba-ac1632416b05
description: "L'API de gestion des comptes fournit l'accès aux informations de compte et prend en charge les notifications des modifications de compte. En tant que clients de cette API, les fournisseurs de messagerie effectuent les opérations suivantes:"
ms.openlocfilehash: 76520b7cc7f28ede28257729e4e4fbe2d5096290
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316939"
---
# <a name="about-the-account-management-api"></a><span data-ttu-id="8907f-104">À propos de l’API de gestion des comptes</span><span class="sxs-lookup"><span data-stu-id="8907f-104">About the Account Management API</span></span>

<span data-ttu-id="8907f-105">L'API de gestion des comptes fournit l'accès aux informations de compte et prend en charge les notifications des modifications de compte.</span><span class="sxs-lookup"><span data-stu-id="8907f-105">The Account Management API provides access to account information and supports notifications of account changes.</span></span> <span data-ttu-id="8907f-106">En tant que clients de cette API, les fournisseurs de messagerie effectuent les opérations suivantes:</span><span class="sxs-lookup"><span data-stu-id="8907f-106">As clients of this API, mail providers do the following:</span></span>
  
1. <span data-ttu-id="8907f-107">Utilisez [IOlkAccountManager](iolkaccountmanager.md) pour gérer l'accès aux comptes et configurer des notifications sur les modifications de compte.</span><span class="sxs-lookup"><span data-stu-id="8907f-107">Use [IOlkAccountManager](iolkaccountmanager.md) to manage access to accounts and set up notifications about account changes.</span></span> 
    
2. <span data-ttu-id="8907f-108">Implémenter et utiliser [IOlkAccountNotify](iolkaccountnotify.md) pour envoyer des notifications sur les modifications de compte.</span><span class="sxs-lookup"><span data-stu-id="8907f-108">Implement and use [IOlkAccountNotify](iolkaccountnotify.md) to send notifications about account changes.</span></span> 
    
3. <span data-ttu-id="8907f-109">Utilisez [IOlkEnum](iolkenum.md) pour énumérer les comptes.</span><span class="sxs-lookup"><span data-stu-id="8907f-109">Use [IOlkEnum](iolkenum.md) to enumerate accounts.</span></span> 
    
4. <span data-ttu-id="8907f-110">Utilisez [IOlkAccount](iolkaccount.md) pour obtenir et définir des propriétés et d'autres informations sur un compte.</span><span class="sxs-lookup"><span data-stu-id="8907f-110">Use [IOlkAccount](iolkaccount.md) to get and set properties and other information about an account.</span></span> <span data-ttu-id="8907f-111">Les clients obtiennent cette interface via [IOlkAccountManager:: FindAccount](iolkaccountmanager-findaccount.md) ou [IOlkEnum:: GetNext](iolkenum-getnext.md) pour accéder à un compte individuel.</span><span class="sxs-lookup"><span data-stu-id="8907f-111">Clients obtain this interface through [IOlkAccountManager::FindAccount](iolkaccountmanager-findaccount.md) or [IOlkEnum::GetNext](iolkenum-getnext.md) to access an individual account.</span></span> 
    
5. <span data-ttu-id="8907f-112">Implémentez et utilisez [IOlkAccountHelper](iolkaccounthelper.md) pour fournir la fonctionnalité d'assistance du gestionnaire de comptes, notamment en obtenant le nom de profil d'un compte et la session MAPI actuelle.</span><span class="sxs-lookup"><span data-stu-id="8907f-112">Implement and use [IOlkAccountHelper](iolkaccounthelper.md) to provide the account manager helper functionality, including getting an account's profile name and the current MAPI session.</span></span> 
    
6. <span data-ttu-id="8907f-113">Implémentez et utilisez [IOlkErrorUnknown](iolkerrorunknown.md) pour fournir des informations supplémentaires sur une erreur dans **IOlkAccountManager**, **IOlkAccountNotify**et **IOlkAccount**.</span><span class="sxs-lookup"><span data-stu-id="8907f-113">Implement and use [IOlkErrorUnknown](iolkerrorunknown.md) to provide extra information about an error in **IOlkAccountManager**, **IOlkAccountNotify**, and **IOlkAccount**.</span></span> 

##  <a name="account-management-api-components"></a><span data-ttu-id="8907f-114">Composants de l'API de gestion des comptes</span><span class="sxs-lookup"><span data-stu-id="8907f-114">Account Management API components</span></span>

<span data-ttu-id="8907f-115">L'API de gestion des comptes fournit les définitions, les types de données, les interfaces, les propriétés nommées et les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="8907f-115">The Account Management API provides the following definitions, data types, interfaces, named properties, and properties.</span></span>
  
### <a name="definitions"></a><span data-ttu-id="8907f-116">Définitions</span><span class="sxs-lookup"><span data-stu-id="8907f-116">Definitions</span></span>
  
- [<span data-ttu-id="8907f-117">Constantes (API de gestion des comptes)</span><span class="sxs-lookup"><span data-stu-id="8907f-117">Constants (Account management API)</span></span>](constants-account-management-api.md)
    
### <a name="data-types"></a><span data-ttu-id="8907f-118">Types de données</span><span class="sxs-lookup"><span data-stu-id="8907f-118">Data types</span></span>
  
- [<span data-ttu-id="8907f-119">ACCT_BIN</span><span class="sxs-lookup"><span data-stu-id="8907f-119">ACCT_BIN</span></span>](acct_bin.md)
    
- [<span data-ttu-id="8907f-120">ACCT_VARIANT</span><span class="sxs-lookup"><span data-stu-id="8907f-120">ACCT_VARIANT</span></span>](acct_variant.md)
    
### <a name="interfaces"></a><span data-ttu-id="8907f-121">Interfaces</span><span class="sxs-lookup"><span data-stu-id="8907f-121">Interfaces</span></span>
  
- [<span data-ttu-id="8907f-122">IOlkAccount</span><span class="sxs-lookup"><span data-stu-id="8907f-122">IOlkAccount</span></span>](iolkaccount.md)
    
- [<span data-ttu-id="8907f-123">IOlkAccountHelper</span><span class="sxs-lookup"><span data-stu-id="8907f-123">IOlkAccountHelper</span></span>](iolkaccounthelper.md)
    
- [<span data-ttu-id="8907f-124">IOlkAccountManager</span><span class="sxs-lookup"><span data-stu-id="8907f-124">IOlkAccountManager</span></span>](iolkaccountmanager.md)
    
- [<span data-ttu-id="8907f-125">IOlkAccountNotify</span><span class="sxs-lookup"><span data-stu-id="8907f-125">IOlkAccountNotify</span></span>](iolkaccountnotify.md)
    
- [<span data-ttu-id="8907f-126">IOlkEnum</span><span class="sxs-lookup"><span data-stu-id="8907f-126">IOlkEnum</span></span>](iolkenum.md)
    
- [<span data-ttu-id="8907f-127">IOlkErrorUnknown</span><span class="sxs-lookup"><span data-stu-id="8907f-127">IOlkErrorUnknown</span></span>](iolkerrorunknown.md)
    
### <a name="named-properties"></a><span data-ttu-id="8907f-128">Propriétés nommées</span><span class="sxs-lookup"><span data-stu-id="8907f-128">Named properties</span></span>
  
- [<span data-ttu-id="8907f-129">PidLidInternetAccountName</span><span class="sxs-lookup"><span data-stu-id="8907f-129">PidLidInternetAccountName</span></span>](pidlidinternetaccountname.md)
    
- [<span data-ttu-id="8907f-130">PidLidInternetAccountStamp</span><span class="sxs-lookup"><span data-stu-id="8907f-130">PidLidInternetAccountStamp</span></span>](pidlidinternetaccountstamp.md)
    
### <a name="properties"></a><span data-ttu-id="8907f-131">Propriétés</span><span class="sxs-lookup"><span data-stu-id="8907f-131">Properties</span></span>
  
- [<span data-ttu-id="8907f-132">PidTagNextSendAcct</span><span class="sxs-lookup"><span data-stu-id="8907f-132">PidTagNextSendAcct</span></span>](pidtagnextsendacct.md)
    
- [<span data-ttu-id="8907f-133">PidTagPrimarySendAccount</span><span class="sxs-lookup"><span data-stu-id="8907f-133">PidTagPrimarySendAccount</span></span>](pidtagprimarysendaccount.md)
    
- [<span data-ttu-id="8907f-134">PROP_ACCT_DELIVERY_FOLDER</span><span class="sxs-lookup"><span data-stu-id="8907f-134">PROP_ACCT_DELIVERY_FOLDER</span></span>](prop_acct_delivery_folder.md)
    
- [<span data-ttu-id="8907f-135">PROP_ACCT_DELIVERY_STORE</span><span class="sxs-lookup"><span data-stu-id="8907f-135">PROP_ACCT_DELIVERY_STORE</span></span>](prop_acct_delivery_store.md)
    
- [<span data-ttu-id="8907f-136">PROP_ACCT_ID</span><span class="sxs-lookup"><span data-stu-id="8907f-136">PROP_ACCT_ID</span></span>](prop_acct_id.md)
    
- [<span data-ttu-id="8907f-137">PROP_ACCT_IS_EXCH</span><span class="sxs-lookup"><span data-stu-id="8907f-137">PROP_ACCT_IS_EXCH</span></span>](prop_acct_is_exch.md)
    
- [<span data-ttu-id="8907f-138">PROP_ACCT_NAME</span><span class="sxs-lookup"><span data-stu-id="8907f-138">PROP_ACCT_NAME</span></span>](prop_acct_name.md)
    
- [<span data-ttu-id="8907f-139">PROP_ACCT_PREFERENCES_UID</span><span class="sxs-lookup"><span data-stu-id="8907f-139">PROP_ACCT_PREFERENCES_UID</span></span>](prop_acct_preferences_uid.md)
    
- [<span data-ttu-id="8907f-140">PROP_ACCT_SEND_STAMP</span><span class="sxs-lookup"><span data-stu-id="8907f-140">PROP_ACCT_SEND_STAMP</span></span>](prop_acct_send_stamp.md)
    
- [<span data-ttu-id="8907f-141">PROP_ACCT_SENTITEMS_EID</span><span class="sxs-lookup"><span data-stu-id="8907f-141">PROP_ACCT_SENTITEMS_EID</span></span>](prop_acct_sentitems_eid.md)
    
- [<span data-ttu-id="8907f-142">PROP_ACCT_STAMP</span><span class="sxs-lookup"><span data-stu-id="8907f-142">PROP_ACCT_STAMP</span></span>](prop_acct_stamp.md)
    
- [<span data-ttu-id="8907f-143">PROP_ACCT_USER_EMAIL_ADDR</span><span class="sxs-lookup"><span data-stu-id="8907f-143">PROP_ACCT_USER_EMAIL_ADDR</span></span>](prop_acct_user_email_addr.md)
    
- [<span data-ttu-id="8907f-144">PROP_ACCT_USER_DISPLAY_NAME</span><span class="sxs-lookup"><span data-stu-id="8907f-144">PROP_ACCT_USER_DISPLAY_NAME</span></span>](prop_acct_user_display_name.md)
    
- [<span data-ttu-id="8907f-145">PROP_MAPI_EMSMDB_UID</span><span class="sxs-lookup"><span data-stu-id="8907f-145">PROP_MAPI_EMSMDB_UID</span></span>](prop_mapi_emsmdb_uid.md)
    
- [<span data-ttu-id="8907f-146">PROP_MAPI_IDENTITY_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="8907f-146">PROP_MAPI_IDENTITY_ENTRYID</span></span>](prop_mapi_identity_entryid.md)
    
- [<span data-ttu-id="8907f-147">PROP_MAPI_TRANSPORT_FLAGS</span><span class="sxs-lookup"><span data-stu-id="8907f-147">PROP_MAPI_TRANSPORT_FLAGS</span></span>](prop_mapi_transport_flags.md)
    

