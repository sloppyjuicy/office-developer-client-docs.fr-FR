---
title: Ajouts MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 78e2806d-bb6f-cd96-21f1-b7c667c73c33
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: fefa77a15cc2b8c72a41b29e6299f159a893cee8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322161"
---
# <a name="about-mapi-additions"></a><span data-ttu-id="97d2f-103">Ajouts MAPI</span><span class="sxs-lookup"><span data-stu-id="97d2f-103">About MAPI additions</span></span>

<span data-ttu-id="97d2f-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="97d2f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="97d2f-105">Les ajouts MAPI sont des API qui appartiennent à l'interface MAPI (Messaging Application Programming Interface), telles que les types de données, les fonctions et les propriétés, qui n'étaient précédemment pas exposés et documentés dans le cadre du Guide de référence du programmeur MAPI.</span><span class="sxs-lookup"><span data-stu-id="97d2f-105">MAPI additions are APIs that belong to Messaging Application Programming Interface (MAPI), such as data types, functions, and properties, that were previously not exposed and documented as part of the MAPI Programmer's Reference.</span></span> <span data-ttu-id="97d2f-106">Elles incluent les définitions et les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="97d2f-106">They include the following definitions and properties.</span></span>
  
## <a name="constant-definitions"></a><span data-ttu-id="97d2f-107">Définitions des constantes</span><span class="sxs-lookup"><span data-stu-id="97d2f-107">Constant definitions</span></span>

- <span data-ttu-id="97d2f-108">**[Constantes MAPI supplémentaires](mapi-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="97d2f-108">**[Additional MAPI Constants](mapi-constants.md)**</span></span>
  
## <a name="data-types"></a><span data-ttu-id="97d2f-109">Types de données</span><span class="sxs-lookup"><span data-stu-id="97d2f-109">Data types</span></span>

- <span data-ttu-id="97d2f-110">**[EXCHANGE_STORE_VERSION_NUM](exchange_store_version_num.md)**</span><span class="sxs-lookup"><span data-stu-id="97d2f-110">**[EXCHANGE_STORE_VERSION_NUM](exchange_store_version_num.md)**</span></span>
    
- <span data-ttu-id="97d2f-111">**[FollowUpStatus](followupstatus.md)**</span><span class="sxs-lookup"><span data-stu-id="97d2f-111">**[FollowUpStatus](followupstatus.md)**</span></span>
    
- <span data-ttu-id="97d2f-112">**[Gender](gender.md)**</span><span class="sxs-lookup"><span data-stu-id="97d2f-112">**[Gender](gender.md)**</span></span>
    
- <span data-ttu-id="97d2f-113">**[OlFlagIcon](olflagicon.md)**</span><span class="sxs-lookup"><span data-stu-id="97d2f-113">**[OlFlagIcon](olflagicon.md)**</span></span>
    
## <a name="functions"></a><span data-ttu-id="97d2f-114">Fonctions</span><span class="sxs-lookup"><span data-stu-id="97d2f-114">Functions</span></span>

- <span data-ttu-id="97d2f-115">**[FixMAPI](fixmapi.md)**</span><span class="sxs-lookup"><span data-stu-id="97d2f-115">**[FixMAPI](fixmapi.md)**</span></span>
    
## <a name="properties"></a><span data-ttu-id="97d2f-116">Propriétés</span><span class="sxs-lookup"><span data-stu-id="97d2f-116">Properties</span></span>

<span data-ttu-id="97d2f-117">Les propriétés suivantes sont généralement exposées par les objets message.</span><span class="sxs-lookup"><span data-stu-id="97d2f-117">The following properties are generally exposed by message objects.</span></span>
  
- <span data-ttu-id="97d2f-118">**[PR_BODY_W](pidtagbody-canonical-property.md)**</span><span class="sxs-lookup"><span data-stu-id="97d2f-118">**[PR_BODY_W](pidtagbody-canonical-property.md)**</span></span>
    
- <span data-ttu-id="97d2f-119">**[PR_CONFLICT_ITEMS](pidtagconflictitems-canonical-property.md)**</span><span class="sxs-lookup"><span data-stu-id="97d2f-119">**[PR_CONFLICT_ITEMS](pidtagconflictitems-canonical-property.md)**</span></span>
    
- <span data-ttu-id="97d2f-120">**[PR_DISPLAY_BCC_W](pidtagdisplaybcc-canonical-property.md)**</span><span class="sxs-lookup"><span data-stu-id="97d2f-120">**[PR_DISPLAY_BCC_W](pidtagdisplaybcc-canonical-property.md)**</span></span>
    
- <span data-ttu-id="97d2f-121">**[PR_DISPLAY_CC_W](pidtagdisplaycc-canonical-property.md)**</span><span class="sxs-lookup"><span data-stu-id="97d2f-121">**[PR_DISPLAY_CC_W](pidtagdisplaycc-canonical-property.md)**</span></span>
    
- <span data-ttu-id="97d2f-122">**[PR_DISPLAY_TO_W](pidtagdisplayto-canonical-property.md)**</span><span class="sxs-lookup"><span data-stu-id="97d2f-122">**[PR_DISPLAY_TO_W](pidtagdisplayto-canonical-property.md)**</span></span>
    
- <span data-ttu-id="97d2f-123">**[PR_FLAG_STATUS](pidtagflagstatus-canonical-property.md)**</span><span class="sxs-lookup"><span data-stu-id="97d2f-123">**[PR_FLAG_STATUS](pidtagflagstatus-canonical-property.md)**</span></span>
    
- <span data-ttu-id="97d2f-124">**[PR_FOLLOWUP_ICON](pidtagfollowupicon-canonical-property.md)**</span><span class="sxs-lookup"><span data-stu-id="97d2f-124">**[PR_FOLLOWUP_ICON](pidtagfollowupicon-canonical-property.md)**</span></span>
    
- <span data-ttu-id="97d2f-125">**[PR_INETMAIL_OVERRIDE_FORMAT](pidtaginternetmailoverrideformat-canonical-property.md)**</span><span class="sxs-lookup"><span data-stu-id="97d2f-125">**[PR_INETMAIL_OVERRIDE_FORMAT](pidtaginternetmailoverrideformat-canonical-property.md)**</span></span>
    
- <span data-ttu-id="97d2f-126">**[PR_MESSAGE_CLASS_W](pidtagmessageclass-canonical-property.md)**</span><span class="sxs-lookup"><span data-stu-id="97d2f-126">**[PR_MESSAGE_CLASS_W](pidtagmessageclass-canonical-property.md)**</span></span>
    
- <span data-ttu-id="97d2f-127">**[PR_MSG_EDITOR_FORMAT](pidtagmessageeditorformat-canonical-property.md)**</span><span class="sxs-lookup"><span data-stu-id="97d2f-127">**[PR_MSG_EDITOR_FORMAT](pidtagmessageeditorformat-canonical-property.md)**</span></span>
    
- <span data-ttu-id="97d2f-128">**[PR_NORMALIZED_SUBJECT_W](pidtagnormalizedsubject-canonical-property.md)**</span><span class="sxs-lookup"><span data-stu-id="97d2f-128">**[PR_NORMALIZED_SUBJECT_W](pidtagnormalizedsubject-canonical-property.md)**</span></span>
    
- <span data-ttu-id="97d2f-129">**[PR_SENDER_ADDRTYPE_W](pidtagsenderaddresstype-canonical-property.md)**</span><span class="sxs-lookup"><span data-stu-id="97d2f-129">**[PR_SENDER_ADDRTYPE_W](pidtagsenderaddresstype-canonical-property.md)**</span></span>
    
- <span data-ttu-id="97d2f-130">**[PR_SENDER_EMAIL_ADDRESS_W](pidtagsenderemailaddress-canonical-property.md)**</span><span class="sxs-lookup"><span data-stu-id="97d2f-130">**[PR_SENDER_EMAIL_ADDRESS_W](pidtagsenderemailaddress-canonical-property.md)**</span></span>
    
- <span data-ttu-id="97d2f-131">**[PR_SENDER_NAME_W](pidtagsendername-canonical-property.md)**</span><span class="sxs-lookup"><span data-stu-id="97d2f-131">**[PR_SENDER_NAME_W](pidtagsendername-canonical-property.md)**</span></span>
    
- <span data-ttu-id="97d2f-132">**[PR_SENT_REPRESENTING_ADDRTYPE_W](pidtagsentrepresentingaddresstype-canonical-property.md)**</span><span class="sxs-lookup"><span data-stu-id="97d2f-132">**[PR_SENT_REPRESENTING_ADDRTYPE_W](pidtagsentrepresentingaddresstype-canonical-property.md)**</span></span>
    
- <span data-ttu-id="97d2f-133">**[PR_SENT_REPRESENTING_EMAIL_ADDRESS_W](pidtagsentrepresentingemailaddress-canonical-property.md)**</span><span class="sxs-lookup"><span data-stu-id="97d2f-133">**[PR_SENT_REPRESENTING_EMAIL_ADDRESS_W](pidtagsentrepresentingemailaddress-canonical-property.md)**</span></span>
    
- <span data-ttu-id="97d2f-134">**[PR_SENT_REPRESENTING_NAME_W](pidtagsentrepresentingname-canonical-property.md)**</span><span class="sxs-lookup"><span data-stu-id="97d2f-134">**[PR_SENT_REPRESENTING_NAME_W](pidtagsentrepresentingname-canonical-property.md)**</span></span>
    
- <span data-ttu-id="97d2f-135">**[PR_SUBJECT_PREFIX_W](pidtagsubjectprefix-canonical-property.md)**</span><span class="sxs-lookup"><span data-stu-id="97d2f-135">**[PR_SUBJECT_PREFIX_W](pidtagsubjectprefix-canonical-property.md)**</span></span>
    
- <span data-ttu-id="97d2f-136">**[PR_SUBJECT_W](pidtagsubject-canonical-property.md)**</span><span class="sxs-lookup"><span data-stu-id="97d2f-136">**[PR_SUBJECT_W](pidtagsubject-canonical-property.md)**</span></span>
    
<span data-ttu-id="97d2f-137">Les propriétés suivantes sont exposées par les objets de tableau du contenu du carnet d'adresses.</span><span class="sxs-lookup"><span data-stu-id="97d2f-137">The following properties are exposed by address book contents table objects.</span></span>
  
- <span data-ttu-id="97d2f-138">**[PR_DISPLAY_TYPE_EX](pidtagdisplaytypeex-canonical-property.md)**</span><span class="sxs-lookup"><span data-stu-id="97d2f-138">**[PR_DISPLAY_TYPE_EX](pidtagdisplaytypeex-canonical-property.md)**</span></span>
    
<span data-ttu-id="97d2f-139">Les propriétés suivantes sont exposées par les objets conteneur du carnet d'adresses.</span><span class="sxs-lookup"><span data-stu-id="97d2f-139">The following properties are exposed by address book container objects.</span></span>
  
- <span data-ttu-id="97d2f-140">**[PR_EMS_AB_SERVER](pidtagemsabserver-canonical-property.md)**</span><span class="sxs-lookup"><span data-stu-id="97d2f-140">**[PR_EMS_AB_SERVER](pidtagemsabserver-canonical-property.md)**</span></span>
    
- <span data-ttu-id="97d2f-141">**[PR_EMS_AB_SERVER_A](pidtagemsabserver-canonical-property.md)**</span><span class="sxs-lookup"><span data-stu-id="97d2f-141">**[PR_EMS_AB_SERVER_A](pidtagemsabserver-canonical-property.md)**</span></span>
    
- <span data-ttu-id="97d2f-142">**[PR_EMS_AB_SERVER_W](pidtagemsabserver-canonical-property.md)**</span><span class="sxs-lookup"><span data-stu-id="97d2f-142">**[PR_EMS_AB_SERVER_W](pidtagemsabserver-canonical-property.md)**</span></span>
    
<span data-ttu-id="97d2f-143">Les propriétés suivantes sont exposées par les objets Folder.</span><span class="sxs-lookup"><span data-stu-id="97d2f-143">The following properties are exposed by folder objects.</span></span>
  
- <span data-ttu-id="97d2f-144">**[PR_AGING_GRANULARITY](pidtagaginggranularity-canonical-property.md)**</span><span class="sxs-lookup"><span data-stu-id="97d2f-144">**[PR_AGING_GRANULARITY](pidtagaginggranularity-canonical-property.md)**</span></span>
    
- <span data-ttu-id="97d2f-145">**[PR_AGING_PERIOD](pidtagagingperiod-canonical-property.md)**</span><span class="sxs-lookup"><span data-stu-id="97d2f-145">**[PR_AGING_PERIOD](pidtagagingperiod-canonical-property.md)**</span></span>
    
<span data-ttu-id="97d2f-146">Les propriétés suivantes sont exposées par les objets utilisateur de messagerie.</span><span class="sxs-lookup"><span data-stu-id="97d2f-146">The following properties are exposed by messaging user objects.</span></span>
  
- <span data-ttu-id="97d2f-147">**[PR_ASSISTANT_TELEPHONE_NUMBER_W](pidtagassistanttelephonenumber-canonical-property.md)**</span><span class="sxs-lookup"><span data-stu-id="97d2f-147">**[PR_ASSISTANT_TELEPHONE_NUMBER_W](pidtagassistanttelephonenumber-canonical-property.md)**</span></span>
    
- <span data-ttu-id="97d2f-148">**[PR_ASSISTANT_W](pidtagassistant-canonical-property.md)**</span><span class="sxs-lookup"><span data-stu-id="97d2f-148">**[PR_ASSISTANT_W](pidtagassistant-canonical-property.md)**</span></span>
    
- <span data-ttu-id="97d2f-149">**[PR_ATTACHMENT_CONTACTPHOTO](pidtagattachmentcontactphoto-canonical-property.md)**</span><span class="sxs-lookup"><span data-stu-id="97d2f-149">**[PR_ATTACHMENT_CONTACTPHOTO](pidtagattachmentcontactphoto-canonical-property.md)**</span></span>
    
- <span data-ttu-id="97d2f-150">**[PR_BIRTHDAY](pidtagbirthday-canonical-property.md)**</span><span class="sxs-lookup"><span data-stu-id="97d2f-150">**[PR_BIRTHDAY](pidtagbirthday-canonical-property.md)**</span></span>
    
- <span data-ttu-id="97d2f-151">**[PR_BUSINESS_FAX_NUMBER_W](pidtagbusinessfaxnumber-canonical-property.md)**</span><span class="sxs-lookup"><span data-stu-id="97d2f-151">**[PR_BUSINESS_FAX_NUMBER_W](pidtagbusinessfaxnumber-canonical-property.md)**</span></span>
    
- <span data-ttu-id="97d2f-152">**[PR_BUSINESS_HOME_PAGE_W](pidtagbusinesshomepage-canonical-property.md)**</span><span class="sxs-lookup"><span data-stu-id="97d2f-152">**[PR_BUSINESS_HOME_PAGE_W](pidtagbusinesshomepage-canonical-property.md)**</span></span>
    
- <span data-ttu-id="97d2f-153">**[PR_CALLBACK_TELEPHONE_NUMBER_W](pidtagcallbacktelephonenumber-canonical-property.md)**</span><span class="sxs-lookup"><span data-stu-id="97d2f-153">**[PR_CALLBACK_TELEPHONE_NUMBER_W](pidtagcallbacktelephonenumber-canonical-property.md)**</span></span>
    
- <span data-ttu-id="97d2f-154">**[PR_CAR_TELEPHONE_NUMBER_W](pidtagcartelephonenumber-canonical-property.md)**</span><span class="sxs-lookup"><span data-stu-id="97d2f-154">**[PR_CAR_TELEPHONE_NUMBER_W](pidtagcartelephonenumber-canonical-property.md)**</span></span>
    
- <span data-ttu-id="97d2f-155">**[PR_CELLULAR_TELEPHONE_NUMBER_W](pidtagmobiletelephonenumber-canonical-property.md)**</span><span class="sxs-lookup"><span data-stu-id="97d2f-155">**[PR_CELLULAR_TELEPHONE_NUMBER_W](pidtagmobiletelephonenumber-canonical-property.md)**</span></span>
    
- <span data-ttu-id="97d2f-156">**[PR_CHILDRENS_NAMES_W](pidtagchildrensnames-canonical-property.md)**</span><span class="sxs-lookup"><span data-stu-id="97d2f-156">**[PR_CHILDRENS_NAMES_W](pidtagchildrensnames-canonical-property.md)**</span></span>
    
- <span data-ttu-id="97d2f-157">**[PR_DEPARTMENT_NAME_W](pidtagdepartmentname-canonical-property.md)**</span><span class="sxs-lookup"><span data-stu-id="97d2f-157">**[PR_DEPARTMENT_NAME_W](pidtagdepartmentname-canonical-property.md)**</span></span>
    
- <span data-ttu-id="97d2f-158">**[PR_DISPLAY_NAME_PREFIX_W](pidtagdisplaynameprefix-canonical-property.md)**</span><span class="sxs-lookup"><span data-stu-id="97d2f-158">**[PR_DISPLAY_NAME_PREFIX_W](pidtagdisplaynameprefix-canonical-property.md)**</span></span>
    
- <span data-ttu-id="97d2f-159">**[PR_GENDER](pidtaggender-canonical-property.md)**</span><span class="sxs-lookup"><span data-stu-id="97d2f-159">**[PR_GENDER](pidtaggender-canonical-property.md)**</span></span>
    
- <span data-ttu-id="97d2f-160">**[PR_GENERATION_W](pidtaggeneration-canonical-property.md)**</span><span class="sxs-lookup"><span data-stu-id="97d2f-160">**[PR_GENERATION_W](pidtaggeneration-canonical-property.md)**</span></span>
    
- <span data-ttu-id="97d2f-161">**[PR_GIVEN_NAME_W](pidtaggivenname-canonical-property.md)**</span><span class="sxs-lookup"><span data-stu-id="97d2f-161">**[PR_GIVEN_NAME_W](pidtaggivenname-canonical-property.md)**</span></span>
    
- <span data-ttu-id="97d2f-162">**[PR_HOBBIES_W](pidtaghobbies-canonical-property.md)**</span><span class="sxs-lookup"><span data-stu-id="97d2f-162">**[PR_HOBBIES_W](pidtaghobbies-canonical-property.md)**</span></span>
    
- <span data-ttu-id="97d2f-163">**[PR_HOME_ADDRESS_CITY_W](pidtaghomeaddresscity-canonical-property.md)**</span><span class="sxs-lookup"><span data-stu-id="97d2f-163">**[PR_HOME_ADDRESS_CITY_W](pidtaghomeaddresscity-canonical-property.md)**</span></span>
    
- <span data-ttu-id="97d2f-164">**[PR_HOME_ADDRESS_COUNTRY_W](pidtaghomeaddresscountry-canonical-property.md)**</span><span class="sxs-lookup"><span data-stu-id="97d2f-164">**[PR_HOME_ADDRESS_COUNTRY_W](pidtaghomeaddresscountry-canonical-property.md)**</span></span>
    
- <span data-ttu-id="97d2f-165">**[PR_HOME_ADDRESS_POST_OFFICE_BOX_W](pidtaghomeaddresspostofficebox-canonical-property.md)**</span><span class="sxs-lookup"><span data-stu-id="97d2f-165">**[PR_HOME_ADDRESS_POST_OFFICE_BOX_W](pidtaghomeaddresspostofficebox-canonical-property.md)**</span></span>
    
- <span data-ttu-id="97d2f-166">**[PR_HOME_ADDRESS_POSTAL_CODE_W](pidtaghomeaddresspostalcode-canonical-property.md)**</span><span class="sxs-lookup"><span data-stu-id="97d2f-166">**[PR_HOME_ADDRESS_POSTAL_CODE_W](pidtaghomeaddresspostalcode-canonical-property.md)**</span></span>
    
- <span data-ttu-id="97d2f-167">**[PR_HOME_ADDRESS_STATE_OR_PROVINCE_W](pidtaghomeaddressstateorprovince-canonical-property.md)**</span><span class="sxs-lookup"><span data-stu-id="97d2f-167">**[PR_HOME_ADDRESS_STATE_OR_PROVINCE_W](pidtaghomeaddressstateorprovince-canonical-property.md)**</span></span>
    
- <span data-ttu-id="97d2f-168">**[PR_HOME_ADDRESS_STREET_W](pidtaghomeaddressstreet-canonical-property.md)**</span><span class="sxs-lookup"><span data-stu-id="97d2f-168">**[PR_HOME_ADDRESS_STREET_W](pidtaghomeaddressstreet-canonical-property.md)**</span></span>
    
- <span data-ttu-id="97d2f-169">**[PR_HOME_FAX_NUMBER_W](pidtaghomefaxnumber-canonical-property.md)**</span><span class="sxs-lookup"><span data-stu-id="97d2f-169">**[PR_HOME_FAX_NUMBER_W](pidtaghomefaxnumber-canonical-property.md)**</span></span>
    
- <span data-ttu-id="97d2f-170">**[PR_HOME_TELEPHONE_NUMBER_W](pidtaghometelephonenumber-canonical-property.md)**</span><span class="sxs-lookup"><span data-stu-id="97d2f-170">**[PR_HOME_TELEPHONE_NUMBER_W](pidtaghometelephonenumber-canonical-property.md)**</span></span>
    
- <span data-ttu-id="97d2f-171">**[PR_KEYWORD_W](pidtagkeyword-canonical-property.md)**</span><span class="sxs-lookup"><span data-stu-id="97d2f-171">**[PR_KEYWORD_W](pidtagkeyword-canonical-property.md)**</span></span>
    
- <span data-ttu-id="97d2f-172">**[PR_MANAGER_NAME_W](pidtagmanagername-canonical-property.md)**</span><span class="sxs-lookup"><span data-stu-id="97d2f-172">**[PR_MANAGER_NAME_W](pidtagmanagername-canonical-property.md)**</span></span>
    
- <span data-ttu-id="97d2f-173">**[PR_MIDDLE_NAME_W](pidtagmiddlename-canonical-property.md)**</span><span class="sxs-lookup"><span data-stu-id="97d2f-173">**[PR_MIDDLE_NAME_W](pidtagmiddlename-canonical-property.md)**</span></span>
    
- <span data-ttu-id="97d2f-174">**[PR_NICKNAME_W](pidtagnickname-canonical-property.md)**</span><span class="sxs-lookup"><span data-stu-id="97d2f-174">**[PR_NICKNAME_W](pidtagnickname-canonical-property.md)**</span></span>
    
- <span data-ttu-id="97d2f-175">**[PR_OFFICE_LOCATION_W](pidtagofficelocation-canonical-property.md)**</span><span class="sxs-lookup"><span data-stu-id="97d2f-175">**[PR_OFFICE_LOCATION_W](pidtagofficelocation-canonical-property.md)**</span></span>
    
- <span data-ttu-id="97d2f-176">**[PR_OFFICE_TELEPHONE_NUMBER_W](pidtagbusinesstelephonenumber-canonical-property.md)**</span><span class="sxs-lookup"><span data-stu-id="97d2f-176">**[PR_OFFICE_TELEPHONE_NUMBER_W](pidtagbusinesstelephonenumber-canonical-property.md)**</span></span>
    
- <span data-ttu-id="97d2f-177">**[PR_OTHER_ADDRESS_CITY_W](pidtagotheraddresscity-canonical-property.md)**</span><span class="sxs-lookup"><span data-stu-id="97d2f-177">**[PR_OTHER_ADDRESS_CITY_W](pidtagotheraddresscity-canonical-property.md)**</span></span>
    
- <span data-ttu-id="97d2f-178">**[PR_OTHER_ADDRESS_COUNTRY_W](pidtagotheraddresscountry-canonical-property.md)**</span><span class="sxs-lookup"><span data-stu-id="97d2f-178">**[PR_OTHER_ADDRESS_COUNTRY_W](pidtagotheraddresscountry-canonical-property.md)**</span></span>
    
- <span data-ttu-id="97d2f-179">**[PR_OTHER_ADDRESS_POST_OFFICE_BOX_W](pidtagotheraddresspostofficebox-canonical-property.md)**</span><span class="sxs-lookup"><span data-stu-id="97d2f-179">**[PR_OTHER_ADDRESS_POST_OFFICE_BOX_W](pidtagotheraddresspostofficebox-canonical-property.md)**</span></span>
    
- <span data-ttu-id="97d2f-180">**[PR_OTHER_ADDRESS_POSTAL_CODE_W](pidtagotheraddresspostalcode-canonical-property.md)**</span><span class="sxs-lookup"><span data-stu-id="97d2f-180">**[PR_OTHER_ADDRESS_POSTAL_CODE_W](pidtagotheraddresspostalcode-canonical-property.md)**</span></span>
    
- <span data-ttu-id="97d2f-181">**[PR_OTHER_ADDRESS_STATE_OR_PROVINCE_W](pidtagotheraddressstateorprovince-canonical-property.md)**</span><span class="sxs-lookup"><span data-stu-id="97d2f-181">**[PR_OTHER_ADDRESS_STATE_OR_PROVINCE_W](pidtagotheraddressstateorprovince-canonical-property.md)**</span></span>
    
- <span data-ttu-id="97d2f-182">**[PR_OTHER_ADDRESS_STREET_W](pidtagotheraddressstreet-canonical-property.md)**</span><span class="sxs-lookup"><span data-stu-id="97d2f-182">**[PR_OTHER_ADDRESS_STREET_W](pidtagotheraddressstreet-canonical-property.md)**</span></span>
    
- <span data-ttu-id="97d2f-183">**[PR_PAGER_TELEPHONE_NUMBER_W](pidtagpagertelephonenumber-canonical-property.md)**</span><span class="sxs-lookup"><span data-stu-id="97d2f-183">**[PR_PAGER_TELEPHONE_NUMBER_W](pidtagpagertelephonenumber-canonical-property.md)**</span></span>
    
- <span data-ttu-id="97d2f-184">**[PR_PERSONAL_HOME_PAGE_W](pidtagpersonalhomepage-canonical-property.md)**</span><span class="sxs-lookup"><span data-stu-id="97d2f-184">**[PR_PERSONAL_HOME_PAGE_W](pidtagpersonalhomepage-canonical-property.md)**</span></span>
    
- <span data-ttu-id="97d2f-185">**[PR_PRIMARY_TELEPHONE_NUMBER_W](pidtagprimarytelephonenumber-canonical-property.md)**</span><span class="sxs-lookup"><span data-stu-id="97d2f-185">**[PR_PRIMARY_TELEPHONE_NUMBER_W](pidtagprimarytelephonenumber-canonical-property.md)**</span></span>
    
- <span data-ttu-id="97d2f-186">**[PR_PROFESSION_W](pidtagprofession-canonical-property.md)**</span><span class="sxs-lookup"><span data-stu-id="97d2f-186">**[PR_PROFESSION_W](pidtagprofession-canonical-property.md)**</span></span>
    
- <span data-ttu-id="97d2f-187">**[PR_SPOUSE_NAME_W](pidtagspousename-canonical-property.md)**</span><span class="sxs-lookup"><span data-stu-id="97d2f-187">**[PR_SPOUSE_NAME_W](pidtagspousename-canonical-property.md)**</span></span>
    
- <span data-ttu-id="97d2f-188">**[PR_SURNAME_W](pidtagsurname-canonical-property.md)**</span><span class="sxs-lookup"><span data-stu-id="97d2f-188">**[PR_SURNAME_W](pidtagsurname-canonical-property.md)**</span></span>
    
- <span data-ttu-id="97d2f-189">**[PR_TITLE_W](pidtagtitle-canonical-property.md)**</span><span class="sxs-lookup"><span data-stu-id="97d2f-189">**[PR_TITLE_W](pidtagtitle-canonical-property.md)**</span></span>
    
- <span data-ttu-id="97d2f-190">**[PR_TTYTDD_PHONE_NUMBER_W](pidtagttytddphonenumber-canonical-property.md)**</span><span class="sxs-lookup"><span data-stu-id="97d2f-190">**[PR_TTYTDD_PHONE_NUMBER_W](pidtagttytddphonenumber-canonical-property.md)**</span></span>
    
- <span data-ttu-id="97d2f-191">**[PR_WEDDING_ANNIVERSARY](pidtagweddinganniversary-canonical-property.md)**</span><span class="sxs-lookup"><span data-stu-id="97d2f-191">**[PR_WEDDING_ANNIVERSARY](pidtagweddinganniversary-canonical-property.md)**</span></span>
    
<span data-ttu-id="97d2f-192">Les propriétés suivantes sont exposées par les objets de section de profil.</span><span class="sxs-lookup"><span data-stu-id="97d2f-192">The following properties are exposed by profile section objects.</span></span>
  
- <span data-ttu-id="97d2f-193">**[PR_PROFILE_SERVER_FULL_VERSION](pidtagprofileserverfullversion-canonical-property.md)**</span><span class="sxs-lookup"><span data-stu-id="97d2f-193">**[PR_PROFILE_SERVER_FULL_VERSION](pidtagprofileserverfullversion-canonical-property.md)**</span></span>
    
- <span data-ttu-id="97d2f-194">**[PR_PROFILE_SERVER_VERSION](pidtagprofileserverversion-canonical-property.md)**</span><span class="sxs-lookup"><span data-stu-id="97d2f-194">**[PR_PROFILE_SERVER_VERSION](pidtagprofileserverversion-canonical-property.md)**</span></span>
    
- <span data-ttu-id="97d2f-195">**[PR_PROVIDER_DISPLAY_NAME_W](pidtagproviderdisplayname-canonical-property.md)**</span><span class="sxs-lookup"><span data-stu-id="97d2f-195">**[PR_PROVIDER_DISPLAY_NAME_W](pidtagproviderdisplayname-canonical-property.md)**</span></span>
    
- <span data-ttu-id="97d2f-196">**[PR_PROVIDER_ICON_W](pidtagprovidericon-canonical-property.md)**</span><span class="sxs-lookup"><span data-stu-id="97d2f-196">**[PR_PROVIDER_ICON_W](pidtagprovidericon-canonical-property.md)**</span></span>
    
- <span data-ttu-id="97d2f-197">**[PR_ROH_FLAGS](pidtagrpcoverhttpflags-canonical-property.md)**</span><span class="sxs-lookup"><span data-stu-id="97d2f-197">**[PR_ROH_FLAGS](pidtagrpcoverhttpflags-canonical-property.md)**</span></span>
    
- <span data-ttu-id="97d2f-198">**[PR_ROH_PROXY_AUTH_SCHEME](pidtagrpcoverhttpproxyauthscheme-canonical-property.md)**</span><span class="sxs-lookup"><span data-stu-id="97d2f-198">**[PR_ROH_PROXY_AUTH_SCHEME](pidtagrpcoverhttpproxyauthscheme-canonical-property.md)**</span></span>
    
- <span data-ttu-id="97d2f-199">**[PR_ROH_PROXY_PRINCIPAL_NAME](pidtagrpcoverhttpproxyprincipalname-canonical-property.md)**</span><span class="sxs-lookup"><span data-stu-id="97d2f-199">**[PR_ROH_PROXY_PRINCIPAL_NAME](pidtagrpcoverhttpproxyprincipalname-canonical-property.md)**</span></span>
    
- <span data-ttu-id="97d2f-200">**[PR_ROH_PROXY_SERVER](pidtagrpcoverhttpproxyserver-canonical-property.md)**</span><span class="sxs-lookup"><span data-stu-id="97d2f-200">**[PR_ROH_PROXY_SERVER](pidtagrpcoverhttpproxyserver-canonical-property.md)**</span></span>
    
<span data-ttu-id="97d2f-201">Les propriétés suivantes sont exposées par les objets Store.</span><span class="sxs-lookup"><span data-stu-id="97d2f-201">The following properties are exposed by store objects.</span></span>
  
- <span data-ttu-id="97d2f-202">**[PR_IPM_APPOINTMENT_ENTRYID](pidtagipmappointmententryid-canonical-property.md)**</span><span class="sxs-lookup"><span data-stu-id="97d2f-202">**[PR_IPM_APPOINTMENT_ENTRYID](pidtagipmappointmententryid-canonical-property.md)**</span></span>
    
- <span data-ttu-id="97d2f-203">**[PR_IPM_CONTACT_ENTRYID](pidtagipmcontactentryid-canonical-property.md)**</span><span class="sxs-lookup"><span data-stu-id="97d2f-203">**[PR_IPM_CONTACT_ENTRYID](pidtagipmcontactentryid-canonical-property.md)**</span></span>
    
- <span data-ttu-id="97d2f-204">**[PR_IPM_DRAFTS_ENTRYID](pidtagipmdraftsentryid-canonical-property.md)**</span><span class="sxs-lookup"><span data-stu-id="97d2f-204">**[PR_IPM_DRAFTS_ENTRYID](pidtagipmdraftsentryid-canonical-property.md)**</span></span>
    
- <span data-ttu-id="97d2f-205">**[PR_IPM_JOURNAL_ENTRYID](pidtagipmjournalentryid-canonical-property.md)**</span><span class="sxs-lookup"><span data-stu-id="97d2f-205">**[PR_IPM_JOURNAL_ENTRYID](pidtagipmjournalentryid-canonical-property.md)**</span></span>
    
- <span data-ttu-id="97d2f-206">**[PR_IPM_NOTE_ENTRYID](pidtagipmnoteentryid-canonical-property.md)**</span><span class="sxs-lookup"><span data-stu-id="97d2f-206">**[PR_IPM_NOTE_ENTRYID](pidtagipmnoteentryid-canonical-property.md)**</span></span>
    
- <span data-ttu-id="97d2f-207">**[PR_IPM_TASK_ENTRYID](pidtagipmtaskentryid-canonical-property.md)**</span><span class="sxs-lookup"><span data-stu-id="97d2f-207">**[PR_IPM_TASK_ENTRYID](pidtagipmtaskentryid-canonical-property.md)**</span></span>
    
<span data-ttu-id="97d2f-208">Les propriétés suivantes sont exposées par les objets Store et sont utilisées pour rechercher des éléments spécifiques d'un courrier électronique dans la Banque.</span><span class="sxs-lookup"><span data-stu-id="97d2f-208">The following properties are exposed by store objects and are used in searching specific elements of an email on the store.</span></span>
  
- <span data-ttu-id="97d2f-209">**[PR_SEARCH_ATTACHMENTS_W](pidtagsearchattachments-canonical-property.md)**</span><span class="sxs-lookup"><span data-stu-id="97d2f-209">**[PR_SEARCH_ATTACHMENTS_W](pidtagsearchattachments-canonical-property.md)**</span></span>
    
- <span data-ttu-id="97d2f-210">**[PR_SEARCH_RECIP_EMAIL_BCC_W](pidtagsearchrecipientemailbcc-canonical-property.md)**</span><span class="sxs-lookup"><span data-stu-id="97d2f-210">**[PR_SEARCH_RECIP_EMAIL_BCC_W](pidtagsearchrecipientemailbcc-canonical-property.md)**</span></span>
    
- <span data-ttu-id="97d2f-211">**[PR_SEARCH_RECIP_EMAIL_CC_W](pidtagsearchrecipientemailcc-canonical-property.md)**</span><span class="sxs-lookup"><span data-stu-id="97d2f-211">**[PR_SEARCH_RECIP_EMAIL_CC_W](pidtagsearchrecipientemailcc-canonical-property.md)**</span></span>
    
- <span data-ttu-id="97d2f-212">**[PR_SEARCH_RECIP_EMAIL_TO_W](pidtagsearchrecipientemailto-canonical-property.md)**</span><span class="sxs-lookup"><span data-stu-id="97d2f-212">**[PR_SEARCH_RECIP_EMAIL_TO_W](pidtagsearchrecipientemailto-canonical-property.md)**</span></span>
    
## <a name="see-also"></a><span data-ttu-id="97d2f-213">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="97d2f-213">See also</span></span>

- [<span data-ttu-id="97d2f-214">Accès à une banque sur le serveur distant lorsqu’Outlook est en mode Exchange mis en cache</span><span class="sxs-lookup"><span data-stu-id="97d2f-214">Access a Store on the Remote Server When Outlook is in Cached Exchange Mode</span></span>](how-to-access-store-on-remote-server-in-cached-exchange-mode.md)  
- [<span data-ttu-id="97d2f-215">Détecter la version d'Exchange Server dans un profil Outlook</span><span class="sxs-lookup"><span data-stu-id="97d2f-215">Detect the Version of Exchange Server in an Outlook Profile</span></span>](how-to-detect-the-version-of-exchange-server-in-an-outlook-profile.md)
- [<span data-ttu-id="97d2f-216">Ouvrir une banque sur le serveur distant lorsqu’Outlook est en mode Exchange mis en cache</span><span class="sxs-lookup"><span data-stu-id="97d2f-216">Open a Store on the Remote Server When Outlook is in Cached Exchange Mode</span></span>](how-to-open-store-on-remote-server-in-cached-exchange-mode.md)
- [<span data-ttu-id="97d2f-217">Gérer un message dans un fichier OST sans appeler de synchronisation en mode Exchange mis en cache</span><span class="sxs-lookup"><span data-stu-id="97d2f-217">Manage a Message in an OST Without Invoking a Synchronization in Cached Exchange Mode</span></span>](how-to-manage-a-message-in-an-ost-without-invoking-a-synchronization.md)

