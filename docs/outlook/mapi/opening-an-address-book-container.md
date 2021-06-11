---
title: Ouverture d’un conteneur du carnet d’adresses
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 89383b27-618c-4ccb-9e16-f66235c98bfe
description: 'Last modified: November 08, 2011'
ms.openlocfilehash: 97fa9f9750174c112c431c62f6171f674856fa86
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436740"
---
# <a name="opening-an-address-book-container"></a><span data-ttu-id="886af-103">Ouverture d’un conteneur du carnet d’adresses</span><span class="sxs-lookup"><span data-stu-id="886af-103">Opening an address book container</span></span>

<span data-ttu-id="886af-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="886af-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="886af-105">Après avoir ouvert le carnet d’adresses intégré MAPI, ouvrez un ou plusieurs conteneurs de carnet d’adresses pour accéder aux destinataires qu’ils intègrent.</span><span class="sxs-lookup"><span data-stu-id="886af-105">After opening the MAPI integrated address book, open one or more address book containers to access the recipients within them.</span></span>
  
<span data-ttu-id="886af-106">Pour ouvrir le conteneur de niveau supérieur du carnet d’adresses, appelez [IAddrBook::OpenEntry](iaddrbook-openentry.md) avec un identificateur d’entrée NULL.</span><span class="sxs-lookup"><span data-stu-id="886af-106">To open the top-level container of the address book, call [IAddrBook::OpenEntry](iaddrbook-openentry.md) with a NULL entry identifier.</span></span> 
  
<span data-ttu-id="886af-107">Les conteneurs de carnet d’adresses peuvent être implémentés avec un accès en lecture seule ou en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="886af-107">Address book containers can be implemented with read-only or read/write access.</span></span> <span data-ttu-id="886af-108">Les conteneurs en lecture seule sont utilisés uniquement pour la navigation.</span><span class="sxs-lookup"><span data-stu-id="886af-108">Read-only containers are used only for browsing.</span></span> <span data-ttu-id="886af-109">Les conteneurs en lecture/écriture peuvent être modifiés, ce qui permet aux clients de créer de nouvelles entrées et de supprimer et de modifier des entrées existantes.</span><span class="sxs-lookup"><span data-stu-id="886af-109">Read/write containers can be modified, allowing clients to create new entries and delete and modify existing entries.</span></span> <span data-ttu-id="886af-110">Tous les conteneurs de carnet d’adresses personnels (PAB) sont implémentés en tant que conteneurs en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="886af-110">All personal address book (PAB) containers are implemented as read/write containers.</span></span> 
  
<span data-ttu-id="886af-111">Pour ouvrir un conteneur de niveau inférieur, appelez **OpenEntry** et spécifiez l’identificateur d’entrée du conteneur à ouvrir.</span><span class="sxs-lookup"><span data-stu-id="886af-111">To open any lower level container, call **OpenEntry** and specify the entry identifier of the container to be opened.</span></span> 
  
## <a name="open-the-container-designated-as-the-pab"></a><span data-ttu-id="886af-112">Ouvrir le conteneur désigné en tant que PAB</span><span class="sxs-lookup"><span data-stu-id="886af-112">Open the container designated as the PAB</span></span>
  
1. <span data-ttu-id="886af-113">Appelez [IAddrBook::GetPAB](iaddrbook-getpab.md) pour récupérer l’identificateur d’entrée du carnet d’identité.</span><span class="sxs-lookup"><span data-stu-id="886af-113">Call [IAddrBook::GetPAB](iaddrbook-getpab.md) to retrieve the PAB's entry identifier.</span></span> 
    
2. <span data-ttu-id="886af-114">Passez cet identificateur d’entrée [à IAddrBook::OpenEntry](iaddrbook-openentry.md).</span><span class="sxs-lookup"><span data-stu-id="886af-114">Pass this entry identifier to [IAddrBook::OpenEntry](iaddrbook-openentry.md).</span></span>
    
## <a name="open-a-container-that-is-not-the-pab"></a><span data-ttu-id="886af-115">Ouvrir un conteneur qui n’est pas le PAB</span><span class="sxs-lookup"><span data-stu-id="886af-115">Open a container that is not the PAB</span></span>
  
1. <span data-ttu-id="886af-116">Appelez [IAddrBook::OpenEntry](iaddrbook-openentry.md) avec un identificateur d’entrée NULL pour ouvrir le conteneur racine du carnet d’adresses.</span><span class="sxs-lookup"><span data-stu-id="886af-116">Call [IAddrBook::OpenEntry](iaddrbook-openentry.md) with a NULL entry identifier to open the address book's root container.</span></span> 
    
2. <span data-ttu-id="886af-117">Appelez la méthode [IMAPIContainer::GetHierarchyTable](imapicontainer-gethierarchytable.md) du conteneur racine pour récupérer sa table de hiérarchie , une liste de tous les conteneurs de niveau supérieur dans le carnet d’adresses.</span><span class="sxs-lookup"><span data-stu-id="886af-117">Call the root container's [IMAPIContainer::GetHierarchyTable](imapicontainer-gethierarchytable.md) method to retrieve its hierarchy table — a list of all of the top-level containers in the address book.</span></span> 
    
3. <span data-ttu-id="886af-118">Si le conteneur à ouvrir est d’un type spécifique :</span><span class="sxs-lookup"><span data-stu-id="886af-118">If the container to be opened is of a specific type:</span></span>
    
   - <span data-ttu-id="886af-119">Créez une structure **SPropertyRestriction** avec **PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md)) pour la balise de propriété, le type du conteneur pour la valeur de propriété et RELOP_EQ pour la relation.</span><span class="sxs-lookup"><span data-stu-id="886af-119">Create an **SPropertyRestriction** structure with **PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md)) for the property tag, the container's type for the property value, and RELOP_EQ for the relation.</span></span> <span data-ttu-id="886af-120">**PR_DISPLAY_TYPE** peuvent être définies sur de nombreuses valeurs, parmi celles-ci :</span><span class="sxs-lookup"><span data-stu-id="886af-120">**PR_DISPLAY_TYPE** can be set to many values, among them:</span></span> 
    
   - <span data-ttu-id="886af-121">DT_GLOBAL pour limiter la table de hiérarchie aux conteneurs qui appartiennent à la liste d’adresses globale.</span><span class="sxs-lookup"><span data-stu-id="886af-121">DT_GLOBAL to limit the hierarchy table to containers that belong in the global address list.</span></span>
    
   - <span data-ttu-id="886af-122">DT_LOCAL limiter la table aux conteneurs appartenant à un carnet d’adresses local.</span><span class="sxs-lookup"><span data-stu-id="886af-122">DT_LOCAL to limit the table to containers belonging to a local address book.</span></span>
    
   - <span data-ttu-id="886af-123">DT_MODIFIABLE limiter la table aux conteneurs qui peuvent être modifiés.</span><span class="sxs-lookup"><span data-stu-id="886af-123">DT_MODIFIABLE to limit the table to containers that can be modified.</span></span>
    
   - <span data-ttu-id="886af-124">Créez une structure [SPropTagArray](sproptagarray.md) qui inclut **PR_ENTRYID,** **PR_DISPLAY_TYPE** et toutes les autres colonnes d’intérêt.</span><span class="sxs-lookup"><span data-stu-id="886af-124">Create an [SPropTagArray](sproptagarray.md) structure that includes **PR_ENTRYID**, **PR_DISPLAY_TYPE**, and any other columns of interest.</span></span> 
    
   - <span data-ttu-id="886af-125">Appelez [HrQueryAllRows,](hrqueryallrows.md)en passant votre restriction de propriété et votre tableau de balises de propriétés.</span><span class="sxs-lookup"><span data-stu-id="886af-125">Call [HrQueryAllRows](hrqueryallrows.md), passing your property restriction and property tag array.</span></span> <span data-ttu-id="886af-126">**HrQueryAllRows** retourne zéro ou plusieurs lignes, une ligne pour chaque conteneur appartenant au type spécifié.</span><span class="sxs-lookup"><span data-stu-id="886af-126">**HrQueryAllRows** will return zero or more rows, one row for every container that belongs to the specified type.</span></span> <span data-ttu-id="886af-127">Soyez prêt à gérer le retour d’un nombre quelconque de lignes.</span><span class="sxs-lookup"><span data-stu-id="886af-127">Be prepared to handle the return of any number of rows.</span></span> 
    
   - <span data-ttu-id="886af-128">Appelez **IAddrBook::OpenEntry** avec l’identificateur d’entrée de PR_ENTRYID colonne de la ligne qui représente le conteneur d’intérêt. </span><span class="sxs-lookup"><span data-stu-id="886af-128">Call **IAddrBook::OpenEntry** with the entry identifier from the **PR_ENTRYID** column of the row that represents the container of interest.</span></span> 
    
4. <span data-ttu-id="886af-129">Si le conteneur à ouvrir appartient à un fournisseur de carnet d’adresses spécifique :</span><span class="sxs-lookup"><span data-stu-id="886af-129">If the container to be opened belongs to a specific address book provider:</span></span>
    
   - <span data-ttu-id="886af-130">Créez une structure [SPropertyRestriction](spropertyrestriction.md) avec **PR_AB_PROVIDERS** ([PidTagAbProviders](pidtagabproviders-canonical-property.md)) pour la balise de propriété, une valeur spécifique au fournisseur pour la valeur de propriété et RELOP_EQ pour la relation.</span><span class="sxs-lookup"><span data-stu-id="886af-130">Create an [SPropertyRestriction](spropertyrestriction.md) structure with **PR_AB_PROVIDERS** ([PidTagAbProviders](pidtagabproviders-canonical-property.md)) for the property tag, a provider-specific value for the property value, and RELOP_EQ for the relation.</span></span> <span data-ttu-id="886af-131">En règle générale, la valeur spécifique au fournisseur est un identificateur ou un GUID global unique.</span><span class="sxs-lookup"><span data-stu-id="886af-131">Typically the provider-specific value is a globally unique identifier or GUID.</span></span> <span data-ttu-id="886af-132">Vous trouverez cette valeur publiée dans l’un des fichiers d’en-tête du fournisseur de carnet d’adresses.</span><span class="sxs-lookup"><span data-stu-id="886af-132">You will find this value published in one of the address book provider's header files.</span></span> 
    
   - <span data-ttu-id="886af-133">Créez une structure [SPropTagArray](sproptagarray.md) qui inclut **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)), **PR_AB_PROVIDERS** et toutes les autres colonnes d’intérêt.</span><span class="sxs-lookup"><span data-stu-id="886af-133">Create an [SPropTagArray](sproptagarray.md) structure that includes **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)), **PR_AB_PROVIDERS**, and any other columns of interest.</span></span> 
    
   - <span data-ttu-id="886af-134">Appelez [HrQueryAllRows,](hrqueryallrows.md)en passant votre restriction de propriété et votre tableau de balises de propriétés.</span><span class="sxs-lookup"><span data-stu-id="886af-134">Call [HrQueryAllRows](hrqueryallrows.md), passing your property restriction and property tag array.</span></span> <span data-ttu-id="886af-135">**HrQueryAllRows** retourne zéro ligne si le fournisseur de carnet d’adresses spécifié ne se trouve pas dans le profil.</span><span class="sxs-lookup"><span data-stu-id="886af-135">**HrQueryAllRows** will return zero rows if the specified address book provider is not in the profile.</span></span> <span data-ttu-id="886af-136">Elle peut renvoyer une ou plusieurs lignes pour les conteneurs de niveau supérieur du fournisseur, selon la façon dont le fournisseur est organisé.</span><span class="sxs-lookup"><span data-stu-id="886af-136">It can return one or more rows for the provider's top-level containers, depending on how the provider is organized.</span></span> 
    
   - <span data-ttu-id="886af-137">Appelez [IAddrBook::OpenEntry](iaddrbook-openentry.md) avec l’identificateur d’entrée de PR_ENTRYID colonne de la ligne qui représente le conteneur d’intérêt. </span><span class="sxs-lookup"><span data-stu-id="886af-137">Call [IAddrBook::OpenEntry](iaddrbook-openentry.md) with the entry identifier from the **PR_ENTRYID** column of the row that represents the container of interest.</span></span> <span data-ttu-id="886af-138">Si le conteneur qui vous intéresse n’est pas un conteneur de niveau supérieur, recherchez le conteneur de niveau supérieur et parcourez la hiérarchie.</span><span class="sxs-lookup"><span data-stu-id="886af-138">If the container that you are interested in is not a top-level container, find the top-level container and traverse the hierarchy.</span></span> 
    

