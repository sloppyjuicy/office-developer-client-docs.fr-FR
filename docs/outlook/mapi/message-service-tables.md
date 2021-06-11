---
title: Tables des services de messages
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b93ab837-3918-4427-b013-bedc6f5276e4
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: c644e89511033234aa45c5f82738e4c471ef646d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422494"
---
# <a name="message-service-tables"></a><span data-ttu-id="345b9-103">Tables des services de messages</span><span class="sxs-lookup"><span data-stu-id="345b9-103">Message Service Tables</span></span>

  
  
<span data-ttu-id="345b9-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="345b9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="345b9-105">Le tableau des services de message contient des informations sur les services de message dans le profil actuel.</span><span class="sxs-lookup"><span data-stu-id="345b9-105">The message service table contains information about the message services in the current profile.</span></span> <span data-ttu-id="345b9-106">Il existe une table de service de message pour chaque session MAPI, implémentée par MAPI et utilisée par des applications clientes à usage spécifique qui fournissent la prise en charge de la configuration.</span><span class="sxs-lookup"><span data-stu-id="345b9-106">There is one message service table for every MAPI session, implemented by MAPI and used by special purpose client applications that provide configuration support.</span></span> 
  
<span data-ttu-id="345b9-107">La table de service de message est une table statique.</span><span class="sxs-lookup"><span data-stu-id="345b9-107">The message service table is a static table.</span></span>
  
<span data-ttu-id="345b9-108">Les clients accèdent à la table de service de message en appelant la méthode [IMsgServiceAdmin::GetMsgServiceTable.](imsgserviceadmin-getmsgservicetable.md)</span><span class="sxs-lookup"><span data-stu-id="345b9-108">Clients access the message service table by calling the [IMsgServiceAdmin::GetMsgServiceTable](imsgserviceadmin-getmsgservicetable.md) method.</span></span> 
  
<span data-ttu-id="345b9-109">Les propriétés suivantes définissent la colonne requise dans la table de service de message :</span><span class="sxs-lookup"><span data-stu-id="345b9-109">The following properties make up the required column set in the message service table:</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="345b9-110">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="345b9-110">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="345b9-111">**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="345b9-111">**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="345b9-112">**PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="345b9-112">**PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="345b9-113">**PR_SERVICE_DLL_NAME** ([PidTagServiceDllName](pidtagservicedllname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="345b9-113">**PR_SERVICE_DLL_NAME** ([PidTagServiceDllName](pidtagservicedllname-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="345b9-114">**PR_SERVICE_ENTRY_NAME** ([PidTagServiceEntryName](pidtagserviceentryname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="345b9-114">**PR_SERVICE_ENTRY_NAME** ([PidTagServiceEntryName](pidtagserviceentryname-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="345b9-115">**PR_SERVICE_NAME** ([PidTagServiceName](pidtagservicename-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="345b9-115">**PR_SERVICE_NAME** ([PidTagServiceName](pidtagservicename-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="345b9-116">**PR_SERVICE_SUPPORT_FILES** ([PidTagServiceSupportFiles](pidtagservicesupportfiles-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="345b9-116">**PR_SERVICE_SUPPORT_FILES** ([PidTagServiceSupportFiles](pidtagservicesupportfiles-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="345b9-117">**PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="345b9-117">**PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md))</span></span>  <br/> |
   
 <span data-ttu-id="345b9-118">**PR_DISPLAY_NAME** est le nom affichable pour le service de message et la colonne de clé de tri par défaut.</span><span class="sxs-lookup"><span data-stu-id="345b9-118">**PR_DISPLAY_NAME** is the displayable name for the message service and the default sort key column.</span></span> 
  
 <span data-ttu-id="345b9-119">**PR_INSTANCE_KEY** sert de colonne d’index pour le tableau, identifiant de manière unique une ligne.</span><span class="sxs-lookup"><span data-stu-id="345b9-119">**PR_INSTANCE_KEY** serves as the index column for the table, uniquely identifying a row.</span></span> 
  
 <span data-ttu-id="345b9-120">**PR_RESOURCE_FLAGS** décrit les fonctionnalités du service de message.</span><span class="sxs-lookup"><span data-stu-id="345b9-120">**PR_RESOURCE_FLAGS** describes the message service's capabilities.</span></span> 
  
 <span data-ttu-id="345b9-121">**PR_SERVICE_DLL_NAME** est le nom de la DLL qui contient l’implémentation du service de message.</span><span class="sxs-lookup"><span data-stu-id="345b9-121">**PR_SERVICE_DLL_NAME** is the name of the DLL that contains the message service implementation.</span></span> 
  
 <span data-ttu-id="345b9-122">**PR_SERVICE_ENTRY_NAME** est le nom de la fonction de point d’entrée du service de message conforme au prototype [MSGSERVICEENTRY.](msgserviceentry.md)</span><span class="sxs-lookup"><span data-stu-id="345b9-122">**PR_SERVICE_ENTRY_NAME** is the name of the message service's entry point function that conforms to the [MSGSERVICEENTRY](msgserviceentry.md) prototype.</span></span> 
  
 <span data-ttu-id="345b9-123">**PR_SERVICE_NAME** est une entrée obligatoire dans la section **[Services]** dans MAPISVC.INF.</span><span class="sxs-lookup"><span data-stu-id="345b9-123">**PR_SERVICE_NAME** is a required entry in the **[Services]** section in MAPISVC.INF.</span></span> <span data-ttu-id="345b9-124">La valeur de cette propriété ne sera jamais modifiée ou localisée.</span><span class="sxs-lookup"><span data-stu-id="345b9-124">The value for this property will never be changed or localized.</span></span> <span data-ttu-id="345b9-125">**PR_SERVICE_NAME** permet d’identifier par programme le service de message.</span><span class="sxs-lookup"><span data-stu-id="345b9-125">**PR_SERVICE_NAME** can be used to programmatically identify the message service.</span></span> 
  
 <span data-ttu-id="345b9-126">**PR_SERVICE_SUPPORT_FILES** liste des fichiers qui doivent être installés avec le service de message.</span><span class="sxs-lookup"><span data-stu-id="345b9-126">**PR_SERVICE_SUPPORT_FILES** is a list of files that must be installed with the message service.</span></span> 
  
 <span data-ttu-id="345b9-127">**PR_SERVICE_UID** est un identificateur unique pour le service de message.</span><span class="sxs-lookup"><span data-stu-id="345b9-127">**PR_SERVICE_UID** is a unique identifier for the message service.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="345b9-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="345b9-128">See also</span></span>



[<span data-ttu-id="345b9-129">MAPI Tables</span><span class="sxs-lookup"><span data-stu-id="345b9-129">MAPI Tables</span></span>](mapi-tables.md)

