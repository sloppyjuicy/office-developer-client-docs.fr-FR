---
title: Ouverture d’un conteneur du carnet d’adresses
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 89383b27-618c-4ccb-9e16-f66235c98bfe
description: 'Dernière modification: 08 08, 2011'
ms.openlocfilehash: 97fa9f9750174c112c431c62f6171f674856fa86
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436740"
---
# <a name="opening-an-address-book-container"></a><span data-ttu-id="bc5e3-103">Ouverture d’un conteneur du carnet d’adresses</span><span class="sxs-lookup"><span data-stu-id="bc5e3-103">Opening an address book container</span></span>

<span data-ttu-id="bc5e3-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bc5e3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bc5e3-105">Après avoir ouvert le carnet d'adresses intégré MAPI, ouvrez un ou plusieurs conteneurs du carnet d'adresses pour accéder aux destinataires qu'ils contiennent.</span><span class="sxs-lookup"><span data-stu-id="bc5e3-105">After opening the MAPI integrated address book, open one or more address book containers to access the recipients within them.</span></span>
  
<span data-ttu-id="bc5e3-106">Pour ouvrir le conteneur de niveau supérieur du carnet d'adresses, appelez [IAddrBook:: OpenEntry](iaddrbook-openentry.md) avec un identificateur d'entrée null.</span><span class="sxs-lookup"><span data-stu-id="bc5e3-106">To open the top-level container of the address book, call [IAddrBook::OpenEntry](iaddrbook-openentry.md) with a NULL entry identifier.</span></span> 
  
<span data-ttu-id="bc5e3-107">Les conteneurs du carnet d'adresses peuvent être implémentés avec un accès en lecture seule ou en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="bc5e3-107">Address book containers can be implemented with read-only or read/write access.</span></span> <span data-ttu-id="bc5e3-108">Les conteneurs en lecture seule sont utilisés uniquement pour la navigation.</span><span class="sxs-lookup"><span data-stu-id="bc5e3-108">Read-only containers are used only for browsing.</span></span> <span data-ttu-id="bc5e3-109">Les conteneurs en lecture/écriture peuvent être modifiés, ce qui permet aux clients de créer de nouvelles entrées et de supprimer et modifier des entrées existantes.</span><span class="sxs-lookup"><span data-stu-id="bc5e3-109">Read/write containers can be modified, allowing clients to create new entries and delete and modify existing entries.</span></span> <span data-ttu-id="bc5e3-110">Tous les conteneurs de carnet d'adresses personnel (Cap) sont implémentés en tant que conteneurs en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="bc5e3-110">All personal address book (PAB) containers are implemented as read/write containers.</span></span> 
  
<span data-ttu-id="bc5e3-111">Pour ouvrir un conteneur de niveau inférieur, appelez **OpenEntry** et spécifiez l'identificateur d'entrée du conteneur à ouvrir.</span><span class="sxs-lookup"><span data-stu-id="bc5e3-111">To open any lower level container, call **OpenEntry** and specify the entry identifier of the container to be opened.</span></span> 
  
## <a name="open-the-container-designated-as-the-pab"></a><span data-ttu-id="bc5e3-112">Ouvrir le conteneur désigné comme PAB</span><span class="sxs-lookup"><span data-stu-id="bc5e3-112">Open the container designated as the PAB</span></span>
  
1. <span data-ttu-id="bc5e3-113">Appelez [IAddrBook:: GetPAB](iaddrbook-getpab.md) pour récupérer l'identificateur d'entrée du carnet d'appels.</span><span class="sxs-lookup"><span data-stu-id="bc5e3-113">Call [IAddrBook::GetPAB](iaddrbook-getpab.md) to retrieve the PAB's entry identifier.</span></span> 
    
2. <span data-ttu-id="bc5e3-114">TransMettez cet identificateur d'entrée à [IAddrBook:: OpenEntry](iaddrbook-openentry.md).</span><span class="sxs-lookup"><span data-stu-id="bc5e3-114">Pass this entry identifier to [IAddrBook::OpenEntry](iaddrbook-openentry.md).</span></span>
    
## <a name="open-a-container-that-is-not-the-pab"></a><span data-ttu-id="bc5e3-115">Ouvrir un conteneur qui n'est pas le PAB</span><span class="sxs-lookup"><span data-stu-id="bc5e3-115">Open a container that is not the PAB</span></span>
  
1. <span data-ttu-id="bc5e3-116">Appelez [IAddrBook:: OpenEntry](iaddrbook-openentry.md) avec un identificateur d'entrée null pour ouvrir le conteneur racine du carnet d'adresses.</span><span class="sxs-lookup"><span data-stu-id="bc5e3-116">Call [IAddrBook::OpenEntry](iaddrbook-openentry.md) with a NULL entry identifier to open the address book's root container.</span></span> 
    
2. <span data-ttu-id="bc5e3-117">Appelez la méthode [IMAPIContainer:: GetHierarchyTable](imapicontainer-gethierarchytable.md) du conteneur racine pour récupérer sa table de hiérarchie, c'est-à-dire une liste de tous les conteneurs de niveau supérieur dans le carnet d'adresses.</span><span class="sxs-lookup"><span data-stu-id="bc5e3-117">Call the root container's [IMAPIContainer::GetHierarchyTable](imapicontainer-gethierarchytable.md) method to retrieve its hierarchy table — a list of all of the top-level containers in the address book.</span></span> 
    
3. <span data-ttu-id="bc5e3-118">Si le conteneur à ouvrir est d'un type spécifique:</span><span class="sxs-lookup"><span data-stu-id="bc5e3-118">If the container to be opened is of a specific type:</span></span>
    
   - <span data-ttu-id="bc5e3-119">Créez une structure **SPropertyRestriction** avec **PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md)) pour la balise de propriété, le type du conteneur pour la valeur de propriété et RELOP_EQ pour la relation.</span><span class="sxs-lookup"><span data-stu-id="bc5e3-119">Create an **SPropertyRestriction** structure with **PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md)) for the property tag, the container's type for the property value, and RELOP_EQ for the relation.</span></span> <span data-ttu-id="bc5e3-120">**PR_DISPLAY_TYPE** peut être défini sur plusieurs valeurs, parmi celles-ci:</span><span class="sxs-lookup"><span data-stu-id="bc5e3-120">**PR_DISPLAY_TYPE** can be set to many values, among them:</span></span> 
    
   - <span data-ttu-id="bc5e3-121">DT_GLOBAL pour limiter la table de hiérarchie aux conteneurs appartenant à la liste d'adresses globale.</span><span class="sxs-lookup"><span data-stu-id="bc5e3-121">DT_GLOBAL to limit the hierarchy table to containers that belong in the global address list.</span></span>
    
   - <span data-ttu-id="bc5e3-122">DT_LOCAL pour limiter le tableau aux conteneurs appartenant à un carnet d'adresses local.</span><span class="sxs-lookup"><span data-stu-id="bc5e3-122">DT_LOCAL to limit the table to containers belonging to a local address book.</span></span>
    
   - <span data-ttu-id="bc5e3-123">DT_MODIFIABLE pour limiter la table aux conteneurs pouvant être modifiés.</span><span class="sxs-lookup"><span data-stu-id="bc5e3-123">DT_MODIFIABLE to limit the table to containers that can be modified.</span></span>
    
   - <span data-ttu-id="bc5e3-124">Créer une structure [SPropTagArray](sproptagarray.md) qui inclut **PR_ENTRYID**, **PR_DISPLAY_TYPE**et toutes les autres colonnes intéressantes.</span><span class="sxs-lookup"><span data-stu-id="bc5e3-124">Create an [SPropTagArray](sproptagarray.md) structure that includes **PR_ENTRYID**, **PR_DISPLAY_TYPE**, and any other columns of interest.</span></span> 
    
   - <span data-ttu-id="bc5e3-125">Appelez [HrQueryAllRows](hrqueryallrows.md), en transmettant votre restriction de propriété et votre tableau de balises de propriété.</span><span class="sxs-lookup"><span data-stu-id="bc5e3-125">Call [HrQueryAllRows](hrqueryallrows.md), passing your property restriction and property tag array.</span></span> <span data-ttu-id="bc5e3-126">**HrQueryAllRows** renverra zéro ou plusieurs lignes, une ligne pour chaque conteneur qui appartient au type spécifié.</span><span class="sxs-lookup"><span data-stu-id="bc5e3-126">**HrQueryAllRows** will return zero or more rows, one row for every container that belongs to the specified type.</span></span> <span data-ttu-id="bc5e3-127">Soyez prêt à gérer le retour d'un nombre quelconque de lignes.</span><span class="sxs-lookup"><span data-stu-id="bc5e3-127">Be prepared to handle the return of any number of rows.</span></span> 
    
   - <span data-ttu-id="bc5e3-128">Appelez **IAddrBook:: OpenEntry** avec l'identificateur d'entrée à partir de la colonne **PR_ENTRYID** de la ligne qui représente le conteneur d'intérêt.</span><span class="sxs-lookup"><span data-stu-id="bc5e3-128">Call **IAddrBook::OpenEntry** with the entry identifier from the **PR_ENTRYID** column of the row that represents the container of interest.</span></span> 
    
4. <span data-ttu-id="bc5e3-129">Si le conteneur à ouvrir appartient à un fournisseur de carnets d'adresses spécifique:</span><span class="sxs-lookup"><span data-stu-id="bc5e3-129">If the container to be opened belongs to a specific address book provider:</span></span>
    
   - <span data-ttu-id="bc5e3-130">Créez une structure [SPropertyRestriction](spropertyrestriction.md) avec **PR_AB_PROVIDERS** ([PidTagAbProviders](pidtagabproviders-canonical-property.md)) pour la balise de propriété, une valeur spécifique au fournisseur pour la valeur de la propriété et RELOP_EQ pour la relation.</span><span class="sxs-lookup"><span data-stu-id="bc5e3-130">Create an [SPropertyRestriction](spropertyrestriction.md) structure with **PR_AB_PROVIDERS** ([PidTagAbProviders](pidtagabproviders-canonical-property.md)) for the property tag, a provider-specific value for the property value, and RELOP_EQ for the relation.</span></span> <span data-ttu-id="bc5e3-131">En règle générale, la valeur spécifique au fournisseur est un identificateur global unique ou un GUID.</span><span class="sxs-lookup"><span data-stu-id="bc5e3-131">Typically the provider-specific value is a globally unique identifier or GUID.</span></span> <span data-ttu-id="bc5e3-132">Cette valeur est publiée dans l'un des fichiers d'en-tête du fournisseur de carnet d'adresses.</span><span class="sxs-lookup"><span data-stu-id="bc5e3-132">You will find this value published in one of the address book provider's header files.</span></span> 
    
   - <span data-ttu-id="bc5e3-133">Créer une structure [SPropTagArray](sproptagarray.md) qui inclut la **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)), **PR_AB_PROVIDERS**et toutes les autres colonnes intéressantes.</span><span class="sxs-lookup"><span data-stu-id="bc5e3-133">Create an [SPropTagArray](sproptagarray.md) structure that includes **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)), **PR_AB_PROVIDERS**, and any other columns of interest.</span></span> 
    
   - <span data-ttu-id="bc5e3-134">Appelez [HrQueryAllRows](hrqueryallrows.md), en transmettant votre restriction de propriété et votre tableau de balises de propriété.</span><span class="sxs-lookup"><span data-stu-id="bc5e3-134">Call [HrQueryAllRows](hrqueryallrows.md), passing your property restriction and property tag array.</span></span> <span data-ttu-id="bc5e3-135">**HrQueryAllRows** ne renvoie aucune ligne si le fournisseur de carnet d'adresses spécifié n'est pas dans le profil.</span><span class="sxs-lookup"><span data-stu-id="bc5e3-135">**HrQueryAllRows** will return zero rows if the specified address book provider is not in the profile.</span></span> <span data-ttu-id="bc5e3-136">Elle peut renvoyer une ou plusieurs lignes pour les conteneurs de niveau supérieur du fournisseur, en fonction de la façon dont le fournisseur est organisé.</span><span class="sxs-lookup"><span data-stu-id="bc5e3-136">It can return one or more rows for the provider's top-level containers, depending on how the provider is organized.</span></span> 
    
   - <span data-ttu-id="bc5e3-137">Appelez [IAddrBook:: OpenEntry](iaddrbook-openentry.md) avec l'identificateur d'entrée à partir de la colonne **PR_ENTRYID** de la ligne qui représente le conteneur d'intérêt.</span><span class="sxs-lookup"><span data-stu-id="bc5e3-137">Call [IAddrBook::OpenEntry](iaddrbook-openentry.md) with the entry identifier from the **PR_ENTRYID** column of the row that represents the container of interest.</span></span> <span data-ttu-id="bc5e3-138">Si le conteneur qui vous intéresse n'est pas un conteneur de niveau supérieur, recherchez le conteneur de niveau supérieur et parcourez la hiérarchie.</span><span class="sxs-lookup"><span data-stu-id="bc5e3-138">If the container that you are interested in is not a top-level container, find the top-level container and traverse the hierarchy.</span></span> 
    

