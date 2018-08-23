---
title: Écriture d’une visionneuse de hiérarchie
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4c939a8c-8148-4add-b181-5a12e6d32309
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 6ff394c95dfa3166d39dcba4b0c577dcfac7b8d8
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22581593"
---
# <a name="writing-a-hierarchy-viewer"></a><span data-ttu-id="8d19d-103">Écriture d’une visionneuse de hiérarchie</span><span class="sxs-lookup"><span data-stu-id="8d19d-103">Writing a Hierarchy Viewer</span></span>

  
  
<span data-ttu-id="8d19d-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8d19d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8d19d-105">Une visionneuse de hiérarchie est un composant d’interface utilisateur qui est utilisé pour l’affichage des tables de hiérarchie de conteneur livre dossier et l’adresse.</span><span class="sxs-lookup"><span data-stu-id="8d19d-105">A hierarchy viewer is a user interface component that is used for displaying folder and address book container hierarchy tables.</span></span> <span data-ttu-id="8d19d-106">Visionneuses de hiérarchie peuvent afficher les membres de la hiérarchie à différents niveaux, extension et réduction de chaque niveau de la demande.</span><span class="sxs-lookup"><span data-stu-id="8d19d-106">Hierarchy viewers can display members of the hierarchy at different levels, expanding and contracting each level on demand.</span></span>
  
<span data-ttu-id="8d19d-107">La propriété container, **PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md)), détermine le niveau auquel un membre de la hiérarchie est affiché.</span><span class="sxs-lookup"><span data-stu-id="8d19d-107">The container property, **PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md)), controls the level at which a hierarchy member is displayed.</span></span> <span data-ttu-id="8d19d-108">Entrées qui représentent les conteneurs de carnet d’adresses de niveau supérieur ou des dossiers ont leur propriété **PR_DEPTH** définie sur zéro.</span><span class="sxs-lookup"><span data-stu-id="8d19d-108">Entries that represent top-level address book containers or folders have their **PR_DEPTH** property set to zero.</span></span> <span data-ttu-id="8d19d-109">La valeur de cette propriété est incrémentée dans l’ordre des entrées de niveaux séquentiels.</span><span class="sxs-lookup"><span data-stu-id="8d19d-109">The value of this property is incremented sequentially for entries in sequential levels.</span></span> <span data-ttu-id="8d19d-110">Autrement dit, lorsqu’un utilisateur sélectionne un conteneur de niveau supérieur pour développer, afficher tous les conteneurs avec **PR_DEPTH** la valeur 1.</span><span class="sxs-lookup"><span data-stu-id="8d19d-110">That is, when a user selects a top-level container to expand, display all containers with **PR_DEPTH** set to 1.</span></span> <span data-ttu-id="8d19d-111">Lorsqu’un utilisateur développe une de ces sous-conteneurs, afficher les conteneurs avec set **PR_DEPTH** à 2 et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="8d19d-111">When a user expands one of these subcontainers, display the containers with **PR_DEPTH** set to 2, and so on.</span></span> 
  
<span data-ttu-id="8d19d-112">Visionneuses de hiérarchie prend en charge une plage des profondeurs différente.</span><span class="sxs-lookup"><span data-stu-id="8d19d-112">Hierarchy viewers support a different range of depths.</span></span> <span data-ttu-id="8d19d-113">Vous pouvez limiter l’afficheur uniquement un ou deux niveaux ou prennent en charge plusieurs niveaux, si l’affichage d’une hiérarchie l’est une priorité.</span><span class="sxs-lookup"><span data-stu-id="8d19d-113">You can limit your viewer to only one or two levels or you can support multiple levels, if displaying an expansive hierarchy is a priority.</span></span> 
  
<span data-ttu-id="8d19d-114">Le carnet d’adresses fournit une visionneuse de la hiérarchie pour les conteneurs de niveau supérieur dans le carnet d’adresses.</span><span class="sxs-lookup"><span data-stu-id="8d19d-114">The address book provides a hierarchy viewer for the top-level containers in the address book.</span></span> 
  
 <span data-ttu-id="8d19d-115">**Accès à la table de hiérarchie adresse téléchargeable**</span><span class="sxs-lookup"><span data-stu-id="8d19d-115">**To access the address book hierarchy table**</span></span>
  
1. <span data-ttu-id="8d19d-116">Appelez [IAddrBook::OpenEntry](iaddrbook-openentry.md), en passant un identificateur d’entrée null, pour ouvrir le conteneur de racine du carnet d’adresses.</span><span class="sxs-lookup"><span data-stu-id="8d19d-116">Call [IAddrBook::OpenEntry](iaddrbook-openentry.md), passing a null entry identifier, to open the address book's root container.</span></span>
    
2. <span data-ttu-id="8d19d-117">Appelez la méthode de [IMAPIContainer::GetHierarchyTable](imapicontainer-gethierarchytable.md) du conteneur racine pour accéder à la table de hiérarchie du carnet d’adresses MAPI.</span><span class="sxs-lookup"><span data-stu-id="8d19d-117">Call the root container's [IMAPIContainer::GetHierarchyTable](imapicontainer-gethierarchytable.md) method to access the hierarchy table of the MAPI address book.</span></span> 
    
 <span data-ttu-id="8d19d-118">**Pour accéder à table de hiérarchie de la banque de messages par défaut**</span><span class="sxs-lookup"><span data-stu-id="8d19d-118">**To access the default message store's hierarchy table**</span></span>
  
1. <span data-ttu-id="8d19d-119">Appelez [IMAPISession::GetMsgStoresTable](imapisession-getmsgstorestable.md) pour accéder à la table.</span><span class="sxs-lookup"><span data-stu-id="8d19d-119">Call [IMAPISession::GetMsgStoresTable](imapisession-getmsgstorestable.md) to access the message store table.</span></span> 
    
2. <span data-ttu-id="8d19d-120">Créer une restriction à l’aide de la structure [SPropertyRestriction](spropertyrestriction.md) pour limiter la table pour que les lignes qui ont une propriété **PR_DEFAULT_STORE** ([PidTagDefaultStore](pidtagdefaultstore-canonical-property.md)) la valeur TRUE.</span><span class="sxs-lookup"><span data-stu-id="8d19d-120">Build a restriction using the [SPropertyRestriction](spropertyrestriction.md) structure to limit the table to only those rows that have a **PR_DEFAULT_STORE** ([PidTagDefaultStore](pidtagdefaultstore-canonical-property.md)) property set to TRUE.</span></span> 
    
3. <span data-ttu-id="8d19d-121">Appel [IMAPITable::FindRow](imapitable-findrow.md), en lui transmettant l' **SPropertyRestriction**, pour rechercher la ligne qui représente la banque de messages par défaut.</span><span class="sxs-lookup"><span data-stu-id="8d19d-121">Call [IMAPITable::FindRow](imapitable-findrow.md), passing it the **SPropertyRestriction**, to locate the row representing the default message store.</span></span> 
    
4. <span data-ttu-id="8d19d-122">Appelez [IMAPISession::OpenEntry](imapisession-openentry.md), en passant la propriété **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) à partir de la ligne de la banque de messages par défaut dans la table.</span><span class="sxs-lookup"><span data-stu-id="8d19d-122">Call [IMAPISession::OpenEntry](imapisession-openentry.md), passing in the **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property from the default message store's row in the message store table.</span></span>
    
5. <span data-ttu-id="8d19d-123">Appeler la méthode de [IMAPIProp::GetProps](imapiprop-getprops.md) de la banque de messages pour récupérer la propriété **PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="8d19d-123">Call the message store's [IMAPIProp::GetProps](imapiprop-getprops.md) method to retrieve the **PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md)) property.</span></span>
    
6. <span data-ttu-id="8d19d-124">Appelez la méthode de [IMsgStore::OpenEntry](imsgstore-openentry.md) de la banque de messages, en passant la propriété **PR_IPM_SUBTREE_ENTRYID** , pour ouvrir le dossier racine de la sous-arborescence IPM de la banque de messages.</span><span class="sxs-lookup"><span data-stu-id="8d19d-124">Call the message store's [IMsgStore::OpenEntry](imsgstore-openentry.md) method, passing the **PR_IPM_SUBTREE_ENTRYID** property, to open the root folder of the message store's IPM subtree.</span></span> 
    
7. <span data-ttu-id="8d19d-125">Appeler la méthode de [IMAPIContainer::GetHierarchyTable](imapicontainer-gethierarchytable.md) du dossier racine IPM pour accéder à la table de hiérarchie.</span><span class="sxs-lookup"><span data-stu-id="8d19d-125">Call the IPM root folder's [IMAPIContainer::GetHierarchyTable](imapicontainer-gethierarchytable.md) method to access its hierarchy table.</span></span> 
    

