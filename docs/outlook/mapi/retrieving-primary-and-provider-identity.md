---
title: Récupération de l’identité fournisseur et principale
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d81bb81d-1708-4a8d-a4d5-c3ba087db9b7
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: da11cf684c4bdcfb94d33791ed7c61d2e322e1a7
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22586584"
---
# <a name="retrieving-primary-and-provider-identity"></a><span data-ttu-id="25208-103">Récupération de l’identité fournisseur et principale</span><span class="sxs-lookup"><span data-stu-id="25208-103">Retrieving Primary and Provider Identity</span></span>

  
  
<span data-ttu-id="25208-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="25208-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="25208-105">Fournisseurs de services, généralement les fournisseurs de carnet d’adresses, ont la possibilité de fournir une identité qui peut être utilisée pour représenter la session dans de nombreuses situations.</span><span class="sxs-lookup"><span data-stu-id="25208-105">Service providers, typically address book providers, have the option of supplying an identity that can be used to represent the session in a variety of situations.</span></span> <span data-ttu-id="25208-106">Trois propriétés décrivent l’identité d’un fournisseur :</span><span class="sxs-lookup"><span data-stu-id="25208-106">Three properties describe a provider's identity:</span></span>
  
- <span data-ttu-id="25208-107">**PR_IDENTITY_ENTRYID** ([PidTagIdentityEntryId](pidtagidentityentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="25208-107">**PR_IDENTITY_ENTRYID** ([PidTagIdentityEntryId](pidtagidentityentryid-canonical-property.md))</span></span> 
    
- <span data-ttu-id="25208-108">**PR_IDENTITY_DISPLAY** ([PidTagIdentityDisplay](pidtagidentitydisplay-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="25208-108">**PR_IDENTITY_DISPLAY** ([PidTagIdentityDisplay](pidtagidentitydisplay-canonical-property.md))</span></span> 
    
- <span data-ttu-id="25208-109">**PR_IDENTITY_SEARCH_KEY** ([PidTagIdentitySearchKey](pidtagidentitysearchkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="25208-109">**PR_IDENTITY_SEARCH_KEY** ([PidTagIdentitySearchKey](pidtagidentitysearchkey-canonical-property.md))</span></span> 
    
<span data-ttu-id="25208-110">Ces propriétés sont définies à l’identificateur d’entrée, un nom d’affichage et une clé de recherche de l’objet d’identité correspondant, qui est généralement un utilisateur de messagerie.</span><span class="sxs-lookup"><span data-stu-id="25208-110">These properties are set to the entry identifier, display name, and search key of the corresponding identity object, which is typically a messaging user.</span></span> <span data-ttu-id="25208-111">Fournisseurs de fournissent une identité également définir l’indicateur STATUS_PRIMARY_IDENTITY dans leur propriété **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="25208-111">Providers that supply an identity also set the STATUS_PRIMARY_IDENTITY flag in their **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) property.</span></span>
  
<span data-ttu-id="25208-112">Selon vos besoins, vous pouvez utiliser une identité d’un fournisseur particulier ou le principal pour la session.</span><span class="sxs-lookup"><span data-stu-id="25208-112">Depending on your needs, you might use a particular provider's identity or the primary identity for the session.</span></span> <span data-ttu-id="25208-113">Vous pouvez utiliser identité d’un fournisseur également pour l’affichage ou pour récupérer les propriétés, telles que **PR_RESOURCE_PATH** ([PidTagResourcePath](pidtagresourcepath-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="25208-113">You can use a provider's identity also for display purposes or to retrieve properties, such as **PR_RESOURCE_PATH** ([PidTagResourcePath](pidtagresourcepath-canonical-property.md)).</span></span> <span data-ttu-id="25208-114">**PR_RESOURCE_PATH**, si la valeur, contient le chemin d’accès aux fichiers utilisé ou créé par le fournisseur.</span><span class="sxs-lookup"><span data-stu-id="25208-114">**PR_RESOURCE_PATH**, if set, contains the path to files used or created by the provider.</span></span> <span data-ttu-id="25208-115">Récupérer la propriété **PR_RESOURCE_PATH** pour le fournisseur en fournissant l’identité principale lorsque vous souhaitez rechercher des fichiers qui s’appliquent à l’utilisateur de la session.</span><span class="sxs-lookup"><span data-stu-id="25208-115">Retrieve the **PR_RESOURCE_PATH** property for the provider supplying the primary identity when you want to locate files that pertain to the user of the session.</span></span> 
  
 <span data-ttu-id="25208-116">**Pour extraire l’identité d’un fournisseur spécifique**</span><span class="sxs-lookup"><span data-stu-id="25208-116">**To retrieve the identity of a specific provider**</span></span>
  
1. <span data-ttu-id="25208-117">Appelez [IMAPISession::GetStatusTable](imapisession-getstatustable.md) pour accéder à la table d’état.</span><span class="sxs-lookup"><span data-stu-id="25208-117">Call [IMAPISession::GetStatusTable](imapisession-getstatustable.md) to access the status table.</span></span> 
    
2. <span data-ttu-id="25208-118">Créer une restriction à l’aide d’une structure [SPropertyRestriction](spropertyrestriction.md) pour correspondre à la colonne **PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md)) avec le nom du fournisseur spécifié.</span><span class="sxs-lookup"><span data-stu-id="25208-118">Build a restriction using an [SPropertyRestriction](spropertyrestriction.md) structure to match the **PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md)) column with the name of the specified provider.</span></span> 
    
3. <span data-ttu-id="25208-119">Appel [IMAPITable::FindRow](imapitable-findrow.md) pour localiser la ligne du fournisseur.</span><span class="sxs-lookup"><span data-stu-id="25208-119">Call [IMAPITable::FindRow](imapitable-findrow.md) to locate the provider's row.</span></span> <span data-ttu-id="25208-120">Identité du fournisseur sera stockée dans la colonne **PR_IDENTITY_ENTRYID** , si elle existe.</span><span class="sxs-lookup"><span data-stu-id="25208-120">The provider's identity will be stored in the **PR_IDENTITY_ENTRYID** column, if it exists.</span></span> 
    
 <span data-ttu-id="25208-121">**Pour extraire l’identité principale d’une session**</span><span class="sxs-lookup"><span data-stu-id="25208-121">**To retrieve the primary identity for a session**</span></span>
  
- <span data-ttu-id="25208-122">Appelez [IMAPISession::QueryIdentity](imapisession-queryidentity.md).</span><span class="sxs-lookup"><span data-stu-id="25208-122">Call [IMAPISession::QueryIdentity](imapisession-queryidentity.md).</span></span> <span data-ttu-id="25208-123">**QueryIdentity** base identité de la session sur l’existence de la valeur STATUS_PRIMARY_IDENTITY dans la colonne **PR_RESOURCE_FLAGS** pour une des lignes de la table d’état.</span><span class="sxs-lookup"><span data-stu-id="25208-123">**QueryIdentity** bases session identity on the existence of the STATUS_PRIMARY_IDENTITY value in the **PR_RESOURCE_FLAGS** column for one of the rows in the status table.</span></span> <span data-ttu-id="25208-124">Si aucune des lignes état ont cette valeur, **QueryIdentity** assigne identité pour le premier fournisseur de services qui définit les trois propriétés PR_IDENTITY.</span><span class="sxs-lookup"><span data-stu-id="25208-124">If none of the status rows have this value set, **QueryIdentity** assigns identity to the first service provider that sets the three PR_IDENTITY properties.</span></span> <span data-ttu-id="25208-125">Si aucun fournisseur de services ne fournit une identité, **QueryIdentity** renvoie MAPI_W_NO_SERVICE.</span><span class="sxs-lookup"><span data-stu-id="25208-125">If no service provider supplies an identity, **QueryIdentity** returns MAPI_W_NO_SERVICE.</span></span> <span data-ttu-id="25208-126">Dans ce cas, vous devez créer une chaîne de caractères pour représenter un utilisateur générique qui peut servir à l’identité du principale.</span><span class="sxs-lookup"><span data-stu-id="25208-126">When this happens, you should create a character string to represent a generic user that can serve as the primary identity.</span></span> 
    
 <span data-ttu-id="25208-127">**Pour définir explicitement l’identité du principale d’une session**</span><span class="sxs-lookup"><span data-stu-id="25208-127">**To explicitly set the primary identity for a session**</span></span>
  
- <span data-ttu-id="25208-128">Appelez [IMsgServiceAdmin::SetPrimaryIdentity](imsgserviceadmin-setprimaryidentity.md).</span><span class="sxs-lookup"><span data-stu-id="25208-128">Call [IMsgServiceAdmin::SetPrimaryIdentity](imsgserviceadmin-setprimaryidentity.md).</span></span> <span data-ttu-id="25208-129">Passez la **MAPIUID** pour le fournisseur de services cible.</span><span class="sxs-lookup"><span data-stu-id="25208-129">Pass the **MAPIUID** for the target service provider.</span></span> 
    

