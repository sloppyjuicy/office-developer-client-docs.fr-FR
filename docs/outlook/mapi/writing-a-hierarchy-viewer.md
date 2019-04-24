---
title: Écriture d'une visionneuse de hiérarchie
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4c939a8c-8148-4add-b181-5a12e6d32309
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 5f6ebd20afc3b8d029fa7c632c55982862664055
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32325640"
---
# <a name="writing-a-hierarchy-viewer"></a><span data-ttu-id="e3346-103">Écriture d'une visionneuse de hiérarchie</span><span class="sxs-lookup"><span data-stu-id="e3346-103">Writing a Hierarchy Viewer</span></span>

  
  
<span data-ttu-id="e3346-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e3346-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e3346-105">Une visionneuse de hiérarchie est un composant d'interface utilisateur qui permet d'afficher les tables de hiérarchie des conteneurs de dossiers et de carnet d'adresses.</span><span class="sxs-lookup"><span data-stu-id="e3346-105">A hierarchy viewer is a user interface component that is used for displaying folder and address book container hierarchy tables.</span></span> <span data-ttu-id="e3346-106">Les visionneuses hiérarchies peuvent afficher les membres de la hiérarchie à différents niveaux, en développant et en adjudicatrices chaque niveau à la demande.</span><span class="sxs-lookup"><span data-stu-id="e3346-106">Hierarchy viewers can display members of the hierarchy at different levels, expanding and contracting each level on demand.</span></span>
  
<span data-ttu-id="e3346-107">La propriété Container, **PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md)), contrôle le niveau auquel un membre de la hiérarchie est affiché.</span><span class="sxs-lookup"><span data-stu-id="e3346-107">The container property, **PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md)), controls the level at which a hierarchy member is displayed.</span></span> <span data-ttu-id="e3346-108">Les entrées qui représentent des conteneurs ou des dossiers de carnet d'adresses de niveau supérieur ont leur propriété **PR_DEPTH** définie sur zéro.</span><span class="sxs-lookup"><span data-stu-id="e3346-108">Entries that represent top-level address book containers or folders have their **PR_DEPTH** property set to zero.</span></span> <span data-ttu-id="e3346-109">La valeur de cette propriété est incrémentée de manière séquentielle pour les entrées dans des niveaux séquentiels.</span><span class="sxs-lookup"><span data-stu-id="e3346-109">The value of this property is incremented sequentially for entries in sequential levels.</span></span> <span data-ttu-id="e3346-110">Autrement dit, lorsqu'un utilisateur sélectionne un conteneur de niveau supérieur, affichez tous les conteneurs avec **PR_DEPTH** défini sur 1.</span><span class="sxs-lookup"><span data-stu-id="e3346-110">That is, when a user selects a top-level container to expand, display all containers with **PR_DEPTH** set to 1.</span></span> <span data-ttu-id="e3346-111">Lorsqu'un utilisateur développe l'un de ces sous-conteneurs, affiche les conteneurs avec **PR_DEPTH** défini sur 2, et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="e3346-111">When a user expands one of these subcontainers, display the containers with **PR_DEPTH** set to 2, and so on.</span></span> 
  
<span data-ttu-id="e3346-112">Les visualiseurs de hiérarchie prennent en charge une plage de profondeurs différente.</span><span class="sxs-lookup"><span data-stu-id="e3346-112">Hierarchy viewers support a different range of depths.</span></span> <span data-ttu-id="e3346-113">Vous pouvez limiter votre visionneuse à un ou deux niveaux, ou vous pouvez prendre en charge plusieurs niveaux, si l'affichage d'une hiérarchie trop vaste est une priorité.</span><span class="sxs-lookup"><span data-stu-id="e3346-113">You can limit your viewer to only one or two levels or you can support multiple levels, if displaying an expansive hierarchy is a priority.</span></span> 
  
<span data-ttu-id="e3346-114">Le carnet d'adresses fournit une visionneuse de hiérarchie pour les conteneurs de niveau supérieur dans le carnet d'adresses.</span><span class="sxs-lookup"><span data-stu-id="e3346-114">The address book provides a hierarchy viewer for the top-level containers in the address book.</span></span> 
  
 <span data-ttu-id="e3346-115">**Pour accéder à la table de hiérarchie de carnets d'adresses**</span><span class="sxs-lookup"><span data-stu-id="e3346-115">**To access the address book hierarchy table**</span></span>
  
1. <span data-ttu-id="e3346-116">Appelez [IAddrBook:: OpenEntry](iaddrbook-openentry.md), en transmettant un identificateur d'entrée null, pour ouvrir le conteneur racine du carnet d'adresses.</span><span class="sxs-lookup"><span data-stu-id="e3346-116">Call [IAddrBook::OpenEntry](iaddrbook-openentry.md), passing a null entry identifier, to open the address book's root container.</span></span>
    
2. <span data-ttu-id="e3346-117">Appelez la méthode [IMAPIContainer:: GetHierarchyTable](imapicontainer-gethierarchytable.md) du conteneur racine pour accéder à la table de hiérarchie du carnet d'adresses MAPI.</span><span class="sxs-lookup"><span data-stu-id="e3346-117">Call the root container's [IMAPIContainer::GetHierarchyTable](imapicontainer-gethierarchytable.md) method to access the hierarchy table of the MAPI address book.</span></span> 
    
 <span data-ttu-id="e3346-118">**Pour accéder à la table de hiérarchie de la Banque de messages par défaut**</span><span class="sxs-lookup"><span data-stu-id="e3346-118">**To access the default message store's hierarchy table**</span></span>
  
1. <span data-ttu-id="e3346-119">Appelez [IMAPISession:: GetMsgStoresTable](imapisession-getmsgstorestable.md) pour accéder à la table de banque de messages.</span><span class="sxs-lookup"><span data-stu-id="e3346-119">Call [IMAPISession::GetMsgStoresTable](imapisession-getmsgstorestable.md) to access the message store table.</span></span> 
    
2. <span data-ttu-id="e3346-120">Créez une restriction à l'aide de la structure [SPropertyRestriction](spropertyrestriction.md) pour limiter la table aux seules lignes dont la propriété **PR_DEFAULT_STORE** ([PIDTAGDEFAULTSTORE](pidtagdefaultstore-canonical-property.md)) a la valeur true.</span><span class="sxs-lookup"><span data-stu-id="e3346-120">Build a restriction using the [SPropertyRestriction](spropertyrestriction.md) structure to limit the table to only those rows that have a **PR_DEFAULT_STORE** ([PidTagDefaultStore](pidtagdefaultstore-canonical-property.md)) property set to TRUE.</span></span> 
    
3. <span data-ttu-id="e3346-121">Appelez [IMAPITable:: FindRow](imapitable-findrow.md), en lui transmettant le **SPropertyRestriction**, pour localiser la ligne représentant la Banque de messages par défaut.</span><span class="sxs-lookup"><span data-stu-id="e3346-121">Call [IMAPITable::FindRow](imapitable-findrow.md), passing it the **SPropertyRestriction**, to locate the row representing the default message store.</span></span> 
    
4. <span data-ttu-id="e3346-122">Appelez [IMAPISession:: OpenEntry](imapisession-openentry.md), en transmettant la propriété **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) à partir de la ligne de la Banque de messages par défaut dans la table de banque de messages.</span><span class="sxs-lookup"><span data-stu-id="e3346-122">Call [IMAPISession::OpenEntry](imapisession-openentry.md), passing in the **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property from the default message store's row in the message store table.</span></span>
    
5. <span data-ttu-id="e3346-123">Appelez la méthode [IMAPIProp:: GetProps](imapiprop-getprops.md) de la Banque de messages pour extraire la propriété **PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="e3346-123">Call the message store's [IMAPIProp::GetProps](imapiprop-getprops.md) method to retrieve the **PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md)) property.</span></span>
    
6. <span data-ttu-id="e3346-124">Appelez la méthode [IMsgStore:: OpenEntry](imsgstore-openentry.md) de la Banque de messages, en passant la propriété **PR_IPM_SUBTREE_ENTRYID** , pour ouvrir le dossier racine de la sous-arborescence IPM de la Banque de messages.</span><span class="sxs-lookup"><span data-stu-id="e3346-124">Call the message store's [IMsgStore::OpenEntry](imsgstore-openentry.md) method, passing the **PR_IPM_SUBTREE_ENTRYID** property, to open the root folder of the message store's IPM subtree.</span></span> 
    
7. <span data-ttu-id="e3346-125">Appelez la méthode [IMAPIContainer:: GetHierarchyTable](imapicontainer-gethierarchytable.md) du dossier racine IPM pour accéder à sa table de hiérarchie.</span><span class="sxs-lookup"><span data-stu-id="e3346-125">Call the IPM root folder's [IMAPIContainer::GetHierarchyTable](imapicontainer-gethierarchytable.md) method to access its hierarchy table.</span></span> 
    

