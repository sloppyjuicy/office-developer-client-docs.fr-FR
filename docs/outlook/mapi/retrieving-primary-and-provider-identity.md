---
title: Récupération de l'identité principale et de l'identité du fournisseur
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d81bb81d-1708-4a8d-a4d5-c3ba087db9b7
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: f59695eca2af71dd592c5b3a755d021ac53b3e31
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328636"
---
# <a name="retrieving-primary-and-provider-identity"></a><span data-ttu-id="080e3-103">Récupération de l'identité principale et de l'identité du fournisseur</span><span class="sxs-lookup"><span data-stu-id="080e3-103">Retrieving Primary and Provider Identity</span></span>

  
  
<span data-ttu-id="080e3-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="080e3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="080e3-105">Les fournisseurs de services, généralement les fournisseurs de carnets d'adresses, ont la possibilité de fournir une identité qui peut être utilisée pour représenter la session dans diverses situations.</span><span class="sxs-lookup"><span data-stu-id="080e3-105">Service providers, typically address book providers, have the option of supplying an identity that can be used to represent the session in a variety of situations.</span></span> <span data-ttu-id="080e3-106">Trois propriétés décrivent l'identité d'un fournisseur:</span><span class="sxs-lookup"><span data-stu-id="080e3-106">Three properties describe a provider's identity:</span></span>
  
- <span data-ttu-id="080e3-107">**PR_IDENTITY_ENTRYID** ([PidTagIdentityEntryId](pidtagidentityentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="080e3-107">**PR_IDENTITY_ENTRYID** ([PidTagIdentityEntryId](pidtagidentityentryid-canonical-property.md))</span></span> 
    
- <span data-ttu-id="080e3-108">**PR_IDENTITY_DISPLAY** ([PidTagIdentityDisplay](pidtagidentitydisplay-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="080e3-108">**PR_IDENTITY_DISPLAY** ([PidTagIdentityDisplay](pidtagidentitydisplay-canonical-property.md))</span></span> 
    
- <span data-ttu-id="080e3-109">**PR_IDENTITY_SEARCH_KEY** ([PidTagIdentitySearchKey](pidtagidentitysearchkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="080e3-109">**PR_IDENTITY_SEARCH_KEY** ([PidTagIdentitySearchKey](pidtagidentitysearchkey-canonical-property.md))</span></span> 
    
<span data-ttu-id="080e3-110">Ces propriétés sont définies sur l'identificateur d'entrée, le nom d'affichage et la clé de recherche de l'objet Identity correspondant, qui est en général un utilisateur de messagerie.</span><span class="sxs-lookup"><span data-stu-id="080e3-110">These properties are set to the entry identifier, display name, and search key of the corresponding identity object, which is typically a messaging user.</span></span> <span data-ttu-id="080e3-111">Les fournisseurs qui fournissent une identité définissent également l'indicateur STATUS_PRIMARY_IDENTITY dans leur propriété **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="080e3-111">Providers that supply an identity also set the STATUS_PRIMARY_IDENTITY flag in their **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) property.</span></span>
  
<span data-ttu-id="080e3-112">En fonction de vos besoins, vous pouvez utiliser l'identité d'un fournisseur particulier ou l'identité principale de la session.</span><span class="sxs-lookup"><span data-stu-id="080e3-112">Depending on your needs, you might use a particular provider's identity or the primary identity for the session.</span></span> <span data-ttu-id="080e3-113">Vous pouvez également utiliser l'identité d'un fournisseur à des fins d'affichage ou pour récupérer des propriétés, telles que **PR_RESOURCE_PATH** ([PidTagResourcePath](pidtagresourcepath-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="080e3-113">You can use a provider's identity also for display purposes or to retrieve properties, such as **PR_RESOURCE_PATH** ([PidTagResourcePath](pidtagresourcepath-canonical-property.md)).</span></span> <span data-ttu-id="080e3-114">**PR_RESOURCE_PATH**, si défini, contient le chemin d'accès aux fichiers utilisés ou créés par le fournisseur.</span><span class="sxs-lookup"><span data-stu-id="080e3-114">**PR_RESOURCE_PATH**, if set, contains the path to files used or created by the provider.</span></span> <span data-ttu-id="080e3-115">Récupérez la propriété **PR_RESOURCE_PATH** pour le fournisseur qui fournit l'identité principale lorsque vous souhaitez localiser des fichiers qui se rapportent à l'utilisateur de la session.</span><span class="sxs-lookup"><span data-stu-id="080e3-115">Retrieve the **PR_RESOURCE_PATH** property for the provider supplying the primary identity when you want to locate files that pertain to the user of the session.</span></span> 
  
 <span data-ttu-id="080e3-116">**Pour récupérer l'identité d'un fournisseur spécifique**</span><span class="sxs-lookup"><span data-stu-id="080e3-116">**To retrieve the identity of a specific provider**</span></span>
  
1. <span data-ttu-id="080e3-117">Appelez [IMAPISession:: GetStatusTable](imapisession-getstatustable.md) pour accéder à la table d'État.</span><span class="sxs-lookup"><span data-stu-id="080e3-117">Call [IMAPISession::GetStatusTable](imapisession-getstatustable.md) to access the status table.</span></span> 
    
2. <span data-ttu-id="080e3-118">Créer une restriction à l'aide d'une structure [SPropertyRestriction](spropertyrestriction.md) pour faire correspondre la colonne **PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md)) avec le nom du fournisseur spécifié.</span><span class="sxs-lookup"><span data-stu-id="080e3-118">Build a restriction using an [SPropertyRestriction](spropertyrestriction.md) structure to match the **PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md)) column with the name of the specified provider.</span></span> 
    
3. <span data-ttu-id="080e3-119">Appelez [IMAPITable:: FindRow](imapitable-findrow.md) pour localiser la ligne du fournisseur.</span><span class="sxs-lookup"><span data-stu-id="080e3-119">Call [IMAPITable::FindRow](imapitable-findrow.md) to locate the provider's row.</span></span> <span data-ttu-id="080e3-120">L'identité du fournisseur est stockée dans la colonne **PR_IDENTITY_ENTRYID** , si elle existe.</span><span class="sxs-lookup"><span data-stu-id="080e3-120">The provider's identity will be stored in the **PR_IDENTITY_ENTRYID** column, if it exists.</span></span> 
    
 <span data-ttu-id="080e3-121">**Pour récupérer l'identité principale pour une session**</span><span class="sxs-lookup"><span data-stu-id="080e3-121">**To retrieve the primary identity for a session**</span></span>
  
- <span data-ttu-id="080e3-122">Appelez [IMAPISession:: QueryIdentity](imapisession-queryidentity.md).</span><span class="sxs-lookup"><span data-stu-id="080e3-122">Call [IMAPISession::QueryIdentity](imapisession-queryidentity.md).</span></span> <span data-ttu-id="080e3-123">**QueryIdentity** base l'identité de session sur l'existence de la valeur STATUS_PRIMARY_IDENTITY dans la colonne **PR_RESOURCE_FLAGS** pour l'une des lignes du tableau d'État.</span><span class="sxs-lookup"><span data-stu-id="080e3-123">**QueryIdentity** bases session identity on the existence of the STATUS_PRIMARY_IDENTITY value in the **PR_RESOURCE_FLAGS** column for one of the rows in the status table.</span></span> <span data-ttu-id="080e3-124">Si aucune des lignes d'État n'a cette valeur définie, **QueryIdentity** affecte l'identité au premier fournisseur de services qui définit les trois propriétés PR_IDENTITY.</span><span class="sxs-lookup"><span data-stu-id="080e3-124">If none of the status rows have this value set, **QueryIdentity** assigns identity to the first service provider that sets the three PR_IDENTITY properties.</span></span> <span data-ttu-id="080e3-125">Si aucun fournisseur de services ne fournit une identité, **QueryIdentity** renvoie MAPI_W_NO_SERVICE.</span><span class="sxs-lookup"><span data-stu-id="080e3-125">If no service provider supplies an identity, **QueryIdentity** returns MAPI_W_NO_SERVICE.</span></span> <span data-ttu-id="080e3-126">Dans ce cas, vous devez créer une chaîne de caractères qui représente un utilisateur générique qui peut servir d'identité principale.</span><span class="sxs-lookup"><span data-stu-id="080e3-126">When this happens, you should create a character string to represent a generic user that can serve as the primary identity.</span></span> 
    
 <span data-ttu-id="080e3-127">**Pour définir explicitement l'identité principale d'une session**</span><span class="sxs-lookup"><span data-stu-id="080e3-127">**To explicitly set the primary identity for a session**</span></span>
  
- <span data-ttu-id="080e3-128">Appelez [IMsgServiceAdmin:: SetPrimaryIdentity](imsgserviceadmin-setprimaryidentity.md).</span><span class="sxs-lookup"><span data-stu-id="080e3-128">Call [IMsgServiceAdmin::SetPrimaryIdentity](imsgserviceadmin-setprimaryidentity.md).</span></span> <span data-ttu-id="080e3-129">TransMettez le **MAPIUID** pour le fournisseur de services cible.</span><span class="sxs-lookup"><span data-stu-id="080e3-129">Pass the **MAPIUID** for the target service provider.</span></span> 
    

