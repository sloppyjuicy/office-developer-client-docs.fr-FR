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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426248"
---
# <a name="about-the-account-management-api"></a><span data-ttu-id="0840c-104">À propos de l’API de gestion des comptes</span><span class="sxs-lookup"><span data-stu-id="0840c-104">About the Account Management API</span></span>

<span data-ttu-id="0840c-105">L'API de gestion des comptes fournit l'accès aux informations de compte et prend en charge les notifications des modifications de compte.</span><span class="sxs-lookup"><span data-stu-id="0840c-105">The Account Management API provides access to account information and supports notifications of account changes.</span></span> <span data-ttu-id="0840c-106">En tant que clients de cette API, les fournisseurs de messagerie effectuent les opérations suivantes:</span><span class="sxs-lookup"><span data-stu-id="0840c-106">As clients of this API, mail providers do the following:</span></span>
  
1. <span data-ttu-id="0840c-107">Utilisez [IOlkAccountManager](iolkaccountmanager.md) pour gérer l'accès aux comptes et configurer des notifications sur les modifications de compte.</span><span class="sxs-lookup"><span data-stu-id="0840c-107">Use [IOlkAccountManager](iolkaccountmanager.md) to manage access to accounts and set up notifications about account changes.</span></span> 
    
2. <span data-ttu-id="0840c-108">Implémenter et utiliser [IOlkAccountNotify](iolkaccountnotify.md) pour envoyer des notifications sur les modifications de compte.</span><span class="sxs-lookup"><span data-stu-id="0840c-108">Implement and use [IOlkAccountNotify](iolkaccountnotify.md) to send notifications about account changes.</span></span> 
    
3. <span data-ttu-id="0840c-109">Utilisez [IOlkEnum](iolkenum.md) pour énumérer les comptes.</span><span class="sxs-lookup"><span data-stu-id="0840c-109">Use [IOlkEnum](iolkenum.md) to enumerate accounts.</span></span> 
    
4. <span data-ttu-id="0840c-110">Utilisez [IOlkAccount](iolkaccount.md) pour obtenir et définir des propriétés et d'autres informations sur un compte.</span><span class="sxs-lookup"><span data-stu-id="0840c-110">Use [IOlkAccount](iolkaccount.md) to get and set properties and other information about an account.</span></span> <span data-ttu-id="0840c-111">Les clients obtiennent cette interface via [IOlkAccountManager:: FindAccount](iolkaccountmanager-findaccount.md) ou [IOlkEnum:: GetNext](iolkenum-getnext.md) pour accéder à un compte individuel.</span><span class="sxs-lookup"><span data-stu-id="0840c-111">Clients obtain this interface through [IOlkAccountManager::FindAccount](iolkaccountmanager-findaccount.md) or [IOlkEnum::GetNext](iolkenum-getnext.md) to access an individual account.</span></span> 
    
5. <span data-ttu-id="0840c-112">Implémentez et utilisez [IOlkAccountHelper](iolkaccounthelper.md) pour fournir la fonctionnalité d'assistance du gestionnaire de comptes, notamment en obtenant le nom de profil d'un compte et la session MAPI actuelle.</span><span class="sxs-lookup"><span data-stu-id="0840c-112">Implement and use [IOlkAccountHelper](iolkaccounthelper.md) to provide the account manager helper functionality, including getting an account's profile name and the current MAPI session.</span></span> 
    
6. <span data-ttu-id="0840c-113">Implémentez et utilisez [IOlkErrorUnknown](iolkerrorunknown.md) pour fournir des informations supplémentaires sur une erreur dans **IOlkAccountManager**, **IOlkAccountNotify**et **IOlkAccount**.</span><span class="sxs-lookup"><span data-stu-id="0840c-113">Implement and use [IOlkErrorUnknown](iolkerrorunknown.md) to provide extra information about an error in **IOlkAccountManager**, **IOlkAccountNotify**, and **IOlkAccount**.</span></span> 

##  <a name="account-management-api-components"></a><span data-ttu-id="0840c-114">Composants de l'API de gestion des comptes</span><span class="sxs-lookup"><span data-stu-id="0840c-114">Account Management API components</span></span>

<span data-ttu-id="0840c-115">L'API de gestion des comptes fournit les définitions, les types de données, les interfaces, les propriétés nommées et les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="0840c-115">The Account Management API provides the following definitions, data types, interfaces, named properties, and properties.</span></span>
  
### <a name="definitions"></a><span data-ttu-id="0840c-116">Définitions</span><span class="sxs-lookup"><span data-stu-id="0840c-116">Definitions</span></span>
  
- [<span data-ttu-id="0840c-117">Constantes (API de gestion des comptes)</span><span class="sxs-lookup"><span data-stu-id="0840c-117">Constants (Account management API)</span></span>](constants-account-management-api.md)
    
### <a name="data-types"></a><span data-ttu-id="0840c-118">Types de données</span><span class="sxs-lookup"><span data-stu-id="0840c-118">Data types</span></span>
  
- [<span data-ttu-id="0840c-119">ACCT_BIN</span><span class="sxs-lookup"><span data-stu-id="0840c-119">ACCT_BIN</span></span>](acct_bin.md)
    
- [<span data-ttu-id="0840c-120">ACCT_VARIANT</span><span class="sxs-lookup"><span data-stu-id="0840c-120">ACCT_VARIANT</span></span>](acct_variant.md)
    
### <a name="interfaces"></a><span data-ttu-id="0840c-121">Interfaces</span><span class="sxs-lookup"><span data-stu-id="0840c-121">Interfaces</span></span>
  
- [<span data-ttu-id="0840c-122">IOlkAccount</span><span class="sxs-lookup"><span data-stu-id="0840c-122">IOlkAccount</span></span>](iolkaccount.md)
    
- [<span data-ttu-id="0840c-123">IOlkAccountHelper</span><span class="sxs-lookup"><span data-stu-id="0840c-123">IOlkAccountHelper</span></span>](iolkaccounthelper.md)
    
- [<span data-ttu-id="0840c-124">IOlkAccountManager</span><span class="sxs-lookup"><span data-stu-id="0840c-124">IOlkAccountManager</span></span>](iolkaccountmanager.md)
    
- [<span data-ttu-id="0840c-125">IOlkAccountNotify</span><span class="sxs-lookup"><span data-stu-id="0840c-125">IOlkAccountNotify</span></span>](iolkaccountnotify.md)
    
- [<span data-ttu-id="0840c-126">IOlkEnum</span><span class="sxs-lookup"><span data-stu-id="0840c-126">IOlkEnum</span></span>](iolkenum.md)
    
- [<span data-ttu-id="0840c-127">IOlkErrorUnknown</span><span class="sxs-lookup"><span data-stu-id="0840c-127">IOlkErrorUnknown</span></span>](iolkerrorunknown.md)
    
### <a name="named-properties"></a><span data-ttu-id="0840c-128">Propriétés nommées</span><span class="sxs-lookup"><span data-stu-id="0840c-128">Named properties</span></span>
  
- [<span data-ttu-id="0840c-129">PidLidInternetAccountName</span><span class="sxs-lookup"><span data-stu-id="0840c-129">PidLidInternetAccountName</span></span>](pidlidinternetaccountname.md)
    
- [<span data-ttu-id="0840c-130">PidLidInternetAccountStamp</span><span class="sxs-lookup"><span data-stu-id="0840c-130">PidLidInternetAccountStamp</span></span>](pidlidinternetaccountstamp.md)
    
### <a name="properties"></a><span data-ttu-id="0840c-131">Propriétés</span><span class="sxs-lookup"><span data-stu-id="0840c-131">Properties</span></span>
  
- [<span data-ttu-id="0840c-132">PidTagNextSendAcct</span><span class="sxs-lookup"><span data-stu-id="0840c-132">PidTagNextSendAcct</span></span>](pidtagnextsendacct.md)
    
- [<span data-ttu-id="0840c-133">PidTagPrimarySendAccount</span><span class="sxs-lookup"><span data-stu-id="0840c-133">PidTagPrimarySendAccount</span></span>](pidtagprimarysendaccount.md)
    
- [<span data-ttu-id="0840c-134">PROP_ACCT_DELIVERY_FOLDER</span><span class="sxs-lookup"><span data-stu-id="0840c-134">PROP_ACCT_DELIVERY_FOLDER</span></span>](prop_acct_delivery_folder.md)
    
- [<span data-ttu-id="0840c-135">PROP_ACCT_DELIVERY_STORE</span><span class="sxs-lookup"><span data-stu-id="0840c-135">PROP_ACCT_DELIVERY_STORE</span></span>](prop_acct_delivery_store.md)
    
- [<span data-ttu-id="0840c-136">PROP_ACCT_ID</span><span class="sxs-lookup"><span data-stu-id="0840c-136">PROP_ACCT_ID</span></span>](prop_acct_id.md)
    
- [<span data-ttu-id="0840c-137">PROP_ACCT_IS_EXCH</span><span class="sxs-lookup"><span data-stu-id="0840c-137">PROP_ACCT_IS_EXCH</span></span>](prop_acct_is_exch.md)
    
- [<span data-ttu-id="0840c-138">PROP_ACCT_NAME</span><span class="sxs-lookup"><span data-stu-id="0840c-138">PROP_ACCT_NAME</span></span>](prop_acct_name.md)
    
- [<span data-ttu-id="0840c-139">PROP_ACCT_PREFERENCES_UID</span><span class="sxs-lookup"><span data-stu-id="0840c-139">PROP_ACCT_PREFERENCES_UID</span></span>](prop_acct_preferences_uid.md)
    
- [<span data-ttu-id="0840c-140">PROP_ACCT_SEND_STAMP</span><span class="sxs-lookup"><span data-stu-id="0840c-140">PROP_ACCT_SEND_STAMP</span></span>](prop_acct_send_stamp.md)
    
- [<span data-ttu-id="0840c-141">PROP_ACCT_SENTITEMS_EID</span><span class="sxs-lookup"><span data-stu-id="0840c-141">PROP_ACCT_SENTITEMS_EID</span></span>](prop_acct_sentitems_eid.md)
    
- [<span data-ttu-id="0840c-142">PROP_ACCT_STAMP</span><span class="sxs-lookup"><span data-stu-id="0840c-142">PROP_ACCT_STAMP</span></span>](prop_acct_stamp.md)
    
- [<span data-ttu-id="0840c-143">PROP_ACCT_USER_EMAIL_ADDR</span><span class="sxs-lookup"><span data-stu-id="0840c-143">PROP_ACCT_USER_EMAIL_ADDR</span></span>](prop_acct_user_email_addr.md)
    
- [<span data-ttu-id="0840c-144">PROP_ACCT_USER_DISPLAY_NAME</span><span class="sxs-lookup"><span data-stu-id="0840c-144">PROP_ACCT_USER_DISPLAY_NAME</span></span>](prop_acct_user_display_name.md)
    
- [<span data-ttu-id="0840c-145">PROP_MAPI_EMSMDB_UID</span><span class="sxs-lookup"><span data-stu-id="0840c-145">PROP_MAPI_EMSMDB_UID</span></span>](prop_mapi_emsmdb_uid.md)
    
- [<span data-ttu-id="0840c-146">PROP_MAPI_IDENTITY_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="0840c-146">PROP_MAPI_IDENTITY_ENTRYID</span></span>](prop_mapi_identity_entryid.md)
    
- [<span data-ttu-id="0840c-147">PROP_MAPI_TRANSPORT_FLAGS</span><span class="sxs-lookup"><span data-stu-id="0840c-147">PROP_MAPI_TRANSPORT_FLAGS</span></span>](prop_mapi_transport_flags.md)
    

