---
title: Tables des services de messagerie
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b93ab837-3918-4427-b013-bedc6f5276e4
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: c644e89511033234aa45c5f82738e4c471ef646d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356909"
---
# <a name="message-service-tables"></a><span data-ttu-id="a08da-103">Tables des services de messagerie</span><span class="sxs-lookup"><span data-stu-id="a08da-103">Message Service Tables</span></span>

  
  
<span data-ttu-id="a08da-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a08da-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a08da-105">La table service de messagerie contient des informations sur les services de messagerie dans le profil actif.</span><span class="sxs-lookup"><span data-stu-id="a08da-105">The message service table contains information about the message services in the current profile.</span></span> <span data-ttu-id="a08da-106">Il existe une table de service de messagerie pour chaque session MAPI, implémentée par MAPI et utilisée par des applications clientes à vocation spéciale qui fournissent la prise en charge de la configuration.</span><span class="sxs-lookup"><span data-stu-id="a08da-106">There is one message service table for every MAPI session, implemented by MAPI and used by special purpose client applications that provide configuration support.</span></span> 
  
<span data-ttu-id="a08da-107">La table des services de messagerie est une table statique.</span><span class="sxs-lookup"><span data-stu-id="a08da-107">The message service table is a static table.</span></span>
  
<span data-ttu-id="a08da-108">Les clients accèdent à la table de service de message en appelant la méthode [IMsgServiceAdmin:: GetMsgServiceTable](imsgserviceadmin-getmsgservicetable.md) .</span><span class="sxs-lookup"><span data-stu-id="a08da-108">Clients access the message service table by calling the [IMsgServiceAdmin::GetMsgServiceTable](imsgserviceadmin-getmsgservicetable.md) method.</span></span> 
  
<span data-ttu-id="a08da-109">Les propriétés suivantes constituent le jeu de colonnes obligatoire dans le tableau service de message:</span><span class="sxs-lookup"><span data-stu-id="a08da-109">The following properties make up the required column set in the message service table:</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a08da-110">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="a08da-110">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="a08da-111">**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="a08da-111">**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="a08da-112">**PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="a08da-112">**PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="a08da-113">**PR_SERVICE_DLL_NAME** ([PidTagServiceDllName](pidtagservicedllname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="a08da-113">**PR_SERVICE_DLL_NAME** ([PidTagServiceDllName](pidtagservicedllname-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="a08da-114">**PR_SERVICE_ENTRY_NAME** ([PidTagServiceEntryName](pidtagserviceentryname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="a08da-114">**PR_SERVICE_ENTRY_NAME** ([PidTagServiceEntryName](pidtagserviceentryname-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="a08da-115">**PR_SERVICE_NAME** ([PidTagServiceName](pidtagservicename-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="a08da-115">**PR_SERVICE_NAME** ([PidTagServiceName](pidtagservicename-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="a08da-116">**PR_SERVICE_SUPPORT_FILES** ([PidTagServiceSupportFiles](pidtagservicesupportfiles-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="a08da-116">**PR_SERVICE_SUPPORT_FILES** ([PidTagServiceSupportFiles](pidtagservicesupportfiles-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="a08da-117">**PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="a08da-117">**PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md))</span></span>  <br/> |
   
 <span data-ttu-id="a08da-118">**PR_DISPLAY_NAME** est le nom affichable pour le service de messagerie et la colonne clé de tri par défaut.</span><span class="sxs-lookup"><span data-stu-id="a08da-118">**PR_DISPLAY_NAME** is the displayable name for the message service and the default sort key column.</span></span> 
  
 <span data-ttu-id="a08da-119">**PR_INSTANCE_KEY** sert de colonne d'index pour la table et identifie de manière unique une ligne.</span><span class="sxs-lookup"><span data-stu-id="a08da-119">**PR_INSTANCE_KEY** serves as the index column for the table, uniquely identifying a row.</span></span> 
  
 <span data-ttu-id="a08da-120">**PR_RESOURCE_FLAGS** décrit les fonctionnalités du service de messagerie.</span><span class="sxs-lookup"><span data-stu-id="a08da-120">**PR_RESOURCE_FLAGS** describes the message service's capabilities.</span></span> 
  
 <span data-ttu-id="a08da-121">**PR_SERVICE_DLL_NAME** est le nom de la dll qui contient l'implémentation du service de messagerie.</span><span class="sxs-lookup"><span data-stu-id="a08da-121">**PR_SERVICE_DLL_NAME** is the name of the DLL that contains the message service implementation.</span></span> 
  
 <span data-ttu-id="a08da-122">**PR_SERVICE_ENTRY_NAME** est le nom de la fonction de point d'entrée du service de messagerie conforme au prototype [MSGSERVICEENTRY](msgserviceentry.md) .</span><span class="sxs-lookup"><span data-stu-id="a08da-122">**PR_SERVICE_ENTRY_NAME** is the name of the message service's entry point function that conforms to the [MSGSERVICEENTRY](msgserviceentry.md) prototype.</span></span> 
  
 <span data-ttu-id="a08da-123">**PR_SERVICE_NAME** est une entrée obligatoire dans la section **[services]** du fichier MAPISVC. inf.</span><span class="sxs-lookup"><span data-stu-id="a08da-123">**PR_SERVICE_NAME** is a required entry in the **[Services]** section in MAPISVC.INF.</span></span> <span data-ttu-id="a08da-124">La valeur de cette propriété ne sera jamais changée ou localisée.</span><span class="sxs-lookup"><span data-stu-id="a08da-124">The value for this property will never be changed or localized.</span></span> <span data-ttu-id="a08da-125">**PR_SERVICE_NAME** peut être utilisé pour identifier le service de messagerie par programme.</span><span class="sxs-lookup"><span data-stu-id="a08da-125">**PR_SERVICE_NAME** can be used to programmatically identify the message service.</span></span> 
  
 <span data-ttu-id="a08da-126">**PR_SERVICE_SUPPORT_FILES** est une liste de fichiers qui doit être installée avec le service de messagerie.</span><span class="sxs-lookup"><span data-stu-id="a08da-126">**PR_SERVICE_SUPPORT_FILES** is a list of files that must be installed with the message service.</span></span> 
  
 <span data-ttu-id="a08da-127">**PR_SERVICE_UID** est un identificateur unique pour le service de messagerie.</span><span class="sxs-lookup"><span data-stu-id="a08da-127">**PR_SERVICE_UID** is a unique identifier for the message service.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="a08da-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a08da-128">See also</span></span>



[<span data-ttu-id="a08da-129">Tables MAPI</span><span class="sxs-lookup"><span data-stu-id="a08da-129">MAPI Tables</span></span>](mapi-tables.md)

