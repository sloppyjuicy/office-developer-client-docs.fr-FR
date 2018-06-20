---
title: À propos de l’API de gestion de compte
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: eb6b921d-ecf8-3ce5-87ba-ac1632416b05
description: 'L’API de gestion de compte permet d’accéder aux informations de compte et prend en charge les notifications des modifications de compte. Comme des clients de cette API, les fournisseurs de messagerie procédez comme suit :'
ms.openlocfilehash: 678143def25395c47f1c17cc99dcdcd1fb145e1c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782543"
---
# <a name="about-the-account-management-api"></a><span data-ttu-id="cfe19-104">À propos de l’API de gestion de compte</span><span class="sxs-lookup"><span data-stu-id="cfe19-104">About the Account Management API</span></span>

<span data-ttu-id="cfe19-105">L’API de gestion de compte permet d’accéder aux informations de compte et prend en charge les notifications des modifications de compte.</span><span class="sxs-lookup"><span data-stu-id="cfe19-105">The Account Management API provides access to account information and supports notifications of account changes.</span></span> <span data-ttu-id="cfe19-106">Comme des clients de cette API, les fournisseurs de messagerie procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="cfe19-106">As clients of this API, mail providers do the following:</span></span>
  
1. <span data-ttu-id="cfe19-107">Utilisez [IOlkAccountManager](iolkaccountmanager.md) pour gérer l’accès aux comptes et configurer des notifications sur les modifications de compte.</span><span class="sxs-lookup"><span data-stu-id="cfe19-107">Use [IOlkAccountManager](iolkaccountmanager.md) to manage access to accounts and set up notifications about account changes.</span></span> 
    
2. <span data-ttu-id="cfe19-108">Mettre en œuvre et [IOlkAccountNotify](iolkaccountnotify.md) permet d’envoyer des notifications sur les modifications de compte.</span><span class="sxs-lookup"><span data-stu-id="cfe19-108">Implement and use [IOlkAccountNotify](iolkaccountnotify.md) to send notifications about account changes.</span></span> 
    
3. <span data-ttu-id="cfe19-109">Utilisez [IOlkEnum](iolkenum.md) pour énumérer les comptes.</span><span class="sxs-lookup"><span data-stu-id="cfe19-109">Use [IOlkEnum](iolkenum.md) to enumerate accounts.</span></span> 
    
4. <span data-ttu-id="cfe19-110">Utilisez [IOlkAccount](iolkaccount.md) pour obtenir et définir des propriétés et autres informations sur un compte.</span><span class="sxs-lookup"><span data-stu-id="cfe19-110">Use [IOlkAccount](iolkaccount.md) to get and set properties and other information about an account.</span></span> <span data-ttu-id="cfe19-111">Les clients obtiennent cette interface via [IOlkAccountManager::FindAccount](iolkaccountmanager-findaccount.md) ou [IOlkEnum::GetNext](iolkenum-getnext.md) pour accéder à un compte individuel.</span><span class="sxs-lookup"><span data-stu-id="cfe19-111">Clients obtain this interface through [IOlkAccountManager::FindAccount](iolkaccountmanager-findaccount.md) or [IOlkEnum::GetNext](iolkenum-getnext.md) to access an individual account.</span></span> 
    
5. <span data-ttu-id="cfe19-112">Mettre en œuvre et utiliser [IOlkAccountHelper](iolkaccounthelper.md) pour fournir les fonctionnalités d’assistance de gestionnaire de compte, y compris pour obtenir le nom du profil d’un compte et la session MAPI en cours.</span><span class="sxs-lookup"><span data-stu-id="cfe19-112">Implement and use [IOlkAccountHelper](iolkaccounthelper.md) to provide the account manager helper functionality, including getting an account's profile name and the current MAPI session.</span></span> 
    
6. <span data-ttu-id="cfe19-113">Mettre en œuvre et permet de fournir des informations supplémentaires sur une erreur dans **IOlkAccountManager**, **IOlkAccountNotify**et **IOlkAccount** [IOlkErrorUnknown](iolkerrorunknown.md) .</span><span class="sxs-lookup"><span data-stu-id="cfe19-113">Implement and use [IOlkErrorUnknown](iolkerrorunknown.md) to provide extra information about an error in **IOlkAccountManager**, **IOlkAccountNotify**, and **IOlkAccount**.</span></span> 

##  <a name="account-management-api-components"></a><span data-ttu-id="cfe19-114">Composants d’API de gestion de compte</span><span class="sxs-lookup"><span data-stu-id="cfe19-114">Account Management API components</span></span>

<span data-ttu-id="cfe19-115">L’API de gestion de compte fournit les définitions suivantes, les types de données, des interfaces, nommé les propriétés et les propriétés.</span><span class="sxs-lookup"><span data-stu-id="cfe19-115">The Account Management API provides the following definitions, data types, interfaces, named properties, and properties.</span></span>
  
### <a name="definitions"></a><span data-ttu-id="cfe19-116">Définitions</span><span class="sxs-lookup"><span data-stu-id="cfe19-116">Definitions</span></span>
  
- [<span data-ttu-id="cfe19-117">Constantes (API de gestion des comptes)</span><span class="sxs-lookup"><span data-stu-id="cfe19-117">Constants (Account management API)</span></span>](constants-account-management-api.md)
    
### <a name="data-types"></a><span data-ttu-id="cfe19-118">Types de données</span><span class="sxs-lookup"><span data-stu-id="cfe19-118">Data types</span></span>
  
- [<span data-ttu-id="cfe19-119">ACCT_BIN</span><span class="sxs-lookup"><span data-stu-id="cfe19-119">ACCT_BIN</span></span>](acct_bin.md)
    
- [<span data-ttu-id="cfe19-120">ACCT_VARIANT</span><span class="sxs-lookup"><span data-stu-id="cfe19-120">ACCT_VARIANT</span></span>](acct_variant.md)
    
### <a name="interfaces"></a><span data-ttu-id="cfe19-121">Interfaces</span><span class="sxs-lookup"><span data-stu-id="cfe19-121">Interfaces</span></span>
  
- [<span data-ttu-id="cfe19-122">IOlkAccount</span><span class="sxs-lookup"><span data-stu-id="cfe19-122">IOlkAccount</span></span>](iolkaccount.md)
    
- [<span data-ttu-id="cfe19-123">IOlkAccountHelper</span><span class="sxs-lookup"><span data-stu-id="cfe19-123">IOlkAccountHelper</span></span>](iolkaccounthelper.md)
    
- [<span data-ttu-id="cfe19-124">IOlkAccountManager</span><span class="sxs-lookup"><span data-stu-id="cfe19-124">IOlkAccountManager</span></span>](iolkaccountmanager.md)
    
- [<span data-ttu-id="cfe19-125">IOlkAccountNotify</span><span class="sxs-lookup"><span data-stu-id="cfe19-125">IOlkAccountNotify</span></span>](iolkaccountnotify.md)
    
- [<span data-ttu-id="cfe19-126">IOlkEnum</span><span class="sxs-lookup"><span data-stu-id="cfe19-126">IOlkEnum</span></span>](iolkenum.md)
    
- [<span data-ttu-id="cfe19-127">IOlkErrorUnknown</span><span class="sxs-lookup"><span data-stu-id="cfe19-127">IOlkErrorUnknown</span></span>](iolkerrorunknown.md)
    
### <a name="named-properties"></a><span data-ttu-id="cfe19-128">Propriétés nommées</span><span class="sxs-lookup"><span data-stu-id="cfe19-128">Named properties</span></span>
  
- [<span data-ttu-id="cfe19-129">PidLidInternetAccountName</span><span class="sxs-lookup"><span data-stu-id="cfe19-129">PidLidInternetAccountName</span></span>](pidlidinternetaccountname.md)
    
- [<span data-ttu-id="cfe19-130">PidLidInternetAccountStamp</span><span class="sxs-lookup"><span data-stu-id="cfe19-130">PidLidInternetAccountStamp</span></span>](pidlidinternetaccountstamp.md)
    
### <a name="properties"></a><span data-ttu-id="cfe19-131">Propriétés</span><span class="sxs-lookup"><span data-stu-id="cfe19-131">Properties</span></span>
  
- [<span data-ttu-id="cfe19-132">PidTagNextSendAcct</span><span class="sxs-lookup"><span data-stu-id="cfe19-132">PidTagNextSendAcct</span></span>](pidtagnextsendacct.md)
    
- [<span data-ttu-id="cfe19-133">PidTagPrimarySendAccount</span><span class="sxs-lookup"><span data-stu-id="cfe19-133">PidTagPrimarySendAccount</span></span>](pidtagprimarysendaccount.md)
    
- [<span data-ttu-id="cfe19-134">PROP_ACCT_DELIVERY_FOLDER</span><span class="sxs-lookup"><span data-stu-id="cfe19-134">PROP_ACCT_DELIVERY_FOLDER</span></span>](prop_acct_delivery_folder.md)
    
- [<span data-ttu-id="cfe19-135">PROP_ACCT_DELIVERY_STORE</span><span class="sxs-lookup"><span data-stu-id="cfe19-135">PROP_ACCT_DELIVERY_STORE</span></span>](prop_acct_delivery_store.md)
    
- [<span data-ttu-id="cfe19-136">PROP_ACCT_ID</span><span class="sxs-lookup"><span data-stu-id="cfe19-136">PROP_ACCT_ID</span></span>](prop_acct_id.md)
    
- [<span data-ttu-id="cfe19-137">PROP_ACCT_IS_EXCH</span><span class="sxs-lookup"><span data-stu-id="cfe19-137">PROP_ACCT_IS_EXCH</span></span>](prop_acct_is_exch.md)
    
- [<span data-ttu-id="cfe19-138">PROP_ACCT_NAME</span><span class="sxs-lookup"><span data-stu-id="cfe19-138">PROP_ACCT_NAME</span></span>](prop_acct_name.md)
    
- [<span data-ttu-id="cfe19-139">PROP_ACCT_PREFERENCES_UID</span><span class="sxs-lookup"><span data-stu-id="cfe19-139">PROP_ACCT_PREFERENCES_UID</span></span>](prop_acct_preferences_uid.md)
    
- [<span data-ttu-id="cfe19-140">PROP_ACCT_SEND_STAMP</span><span class="sxs-lookup"><span data-stu-id="cfe19-140">PROP_ACCT_SEND_STAMP</span></span>](prop_acct_send_stamp.md)
    
- [<span data-ttu-id="cfe19-141">PROP_ACCT_SENTITEMS_EID</span><span class="sxs-lookup"><span data-stu-id="cfe19-141">PROP_ACCT_SENTITEMS_EID</span></span>](prop_acct_sentitems_eid.md)
    
- [<span data-ttu-id="cfe19-142">PROP_ACCT_STAMP</span><span class="sxs-lookup"><span data-stu-id="cfe19-142">PROP_ACCT_STAMP</span></span>](prop_acct_stamp.md)
    
- [<span data-ttu-id="cfe19-143">PROP_ACCT_USER_EMAIL_ADDR</span><span class="sxs-lookup"><span data-stu-id="cfe19-143">PROP_ACCT_USER_EMAIL_ADDR</span></span>](prop_acct_user_email_addr.md)
    
- [<span data-ttu-id="cfe19-144">PROP_ACCT_USER_DISPLAY_NAME</span><span class="sxs-lookup"><span data-stu-id="cfe19-144">PROP_ACCT_USER_DISPLAY_NAME</span></span>](prop_acct_user_display_name.md)
    
- [<span data-ttu-id="cfe19-145">PROP_MAPI_EMSMDB_UID</span><span class="sxs-lookup"><span data-stu-id="cfe19-145">PROP_MAPI_EMSMDB_UID</span></span>](prop_mapi_emsmdb_uid.md)
    
- [<span data-ttu-id="cfe19-146">PROP_MAPI_IDENTITY_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="cfe19-146">PROP_MAPI_IDENTITY_ENTRYID</span></span>](prop_mapi_identity_entryid.md)
    
- [<span data-ttu-id="cfe19-147">PROP_MAPI_TRANSPORT_FLAGS</span><span class="sxs-lookup"><span data-stu-id="cfe19-147">PROP_MAPI_TRANSPORT_FLAGS</span></span>](prop_mapi_transport_flags.md)
    

