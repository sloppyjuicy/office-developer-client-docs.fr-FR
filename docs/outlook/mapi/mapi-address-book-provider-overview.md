---
title: Vue d’ensemble du fournisseur MAPI adresse téléchargeable
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ead51434-ae19-4c34-aa7a-bdeeccca5bd9
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 855b145bcca8007601eb8e841665306d4c58982f
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576560"
---
# <a name="mapi-address-book-provider-overview"></a><span data-ttu-id="12951-103">Vue d’ensemble du fournisseur MAPI adresse téléchargeable</span><span class="sxs-lookup"><span data-stu-id="12951-103">MAPI address book provider overview</span></span>
  
<span data-ttu-id="12951-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="12951-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="12951-105">Carnet d’adresses fournisseurs poignée de l’accès aux informations d’annuaire.</span><span class="sxs-lookup"><span data-stu-id="12951-105">Address book providers handle access to directory information.</span></span> <span data-ttu-id="12951-106">Informations d’annuaire se composent de données pour deux types de destinataires du message : individuels de messagerie des utilisateurs et groupes d’utilisateurs de messagerie qui sont généralement traités ensemble dans des listes de distribution.</span><span class="sxs-lookup"><span data-stu-id="12951-106">Directory information consists of data for two types of message recipients: individual messaging users and groups of messaging users who are commonly addressed together in distribution lists.</span></span> <span data-ttu-id="12951-107">Selon le type de destinataire et le fournisseur de carnet d’adresses, il est un large éventail d’informations qui peuvent être rendues disponibles.</span><span class="sxs-lookup"><span data-stu-id="12951-107">Depending on the type of recipient and the address book provider, there is a wide range of information that can be made available.</span></span> <span data-ttu-id="12951-108">Par exemple, tous les fournisseurs de carnet d’adresses stockent le nom, adresse et type d’adresse d’un destinataire.</span><span class="sxs-lookup"><span data-stu-id="12951-108">For example, all address book providers store a recipient's name, address, and address type.</span></span>
  
<span data-ttu-id="12951-109">Chaque fournisseur de carnet d’adresses organise ces données à l’aide d’un ou plusieurs conteneurs.</span><span class="sxs-lookup"><span data-stu-id="12951-109">Each address book provider organizes this data by using one or more containers.</span></span> <span data-ttu-id="12951-110">Le nombre et la structure des conteneurs varie selon l’implémentation du fournisseur de carnet d’adresses.</span><span class="sxs-lookup"><span data-stu-id="12951-110">The number and structure of the containers depends on the address book provider's implementation.</span></span> <span data-ttu-id="12951-111">Par exemple, un fournisseur de carnet d’adresses peut utiliser un seul conteneur pour stocker toutes les informations, une autre peut utiliser un conteneur de niveau supérieur qui contient les sous-conteneurs et une troisième peut utiliser plusieurs conteneurs de niveau supérieur, chaque sous-conteneurs de cette dernière.</span><span class="sxs-lookup"><span data-stu-id="12951-111">For example, one address book provider might use a single container to hold all of the information, another might use one top-level container that holds subcontainers, and a third might use several top-level containers, each holding subcontainers.</span></span> <span data-ttu-id="12951-112">Une hiérarchie de conteneur de carnets d’adresses peut être très profonde ; Il n’existe aucune limite au nombre de sous-conteneurs qui peut être utilisé.</span><span class="sxs-lookup"><span data-stu-id="12951-112">An address book container hierarchy can be quite deep; there is no limit to the number of subcontainers that can be used.</span></span>
  
<span data-ttu-id="12951-113">L’illustration suivante montre une organisation de carnet d’adresses MAPI par défaut.</span><span class="sxs-lookup"><span data-stu-id="12951-113">The following illustration shows a typical MAPI address book organization.</span></span>
  
<span data-ttu-id="12951-114">**Organisation de carnet d’adresses**</span><span class="sxs-lookup"><span data-stu-id="12951-114">**Address book organization**</span></span>
  
<span data-ttu-id="12951-115">![Organisation de carnet d’adresses] (media/amapi_04.gif "Organisation de carnet d’adresses")</span><span class="sxs-lookup"><span data-stu-id="12951-115">![Address book organization](media/amapi_04.gif "Address book organization")</span></span>
  
<span data-ttu-id="12951-116">MAPI intègre toutes les informations fournies par les fournisseurs de carnet d’adresses installé dans un carnet d’adresses unique, présentant une vue unifiée à l’application cliente.</span><span class="sxs-lookup"><span data-stu-id="12951-116">MAPI integrates all the information supplied by the installed address book providers into a single address book, presenting a unified view to the client application.</span></span> <span data-ttu-id="12951-117">La liste intégrée affiche les conteneurs de niveau supérieur affichés par chacun des fournisseurs de carnet d’adresses installé.</span><span class="sxs-lookup"><span data-stu-id="12951-117">The integrated list shows the top-level containers displayed by each of the installed address book providers.</span></span> <span data-ttu-id="12951-118">La plupart des fournisseurs de carnet d’adresses exposent uniquement quelques conteneurs (généralement une 1 à 3) au niveau supérieur à inclure dans la partie supérieure du carnet d’adresses intégré MAPI.</span><span class="sxs-lookup"><span data-stu-id="12951-118">Most address book providers expose only a few containers (typically one to three) at the top level for inclusion in the top level of the MAPI integrated address book.</span></span> <span data-ttu-id="12951-119">Par exemple, un fournisseur de carnet d’adresses peut rendre disponibles « tous les utilisateurs » et « Local » en tant que deux conteneurs de premier niveau.</span><span class="sxs-lookup"><span data-stu-id="12951-119">For example, an address book provider might make available "All Users" and "Local Users" as two containers at the top level.</span></span>
  
<span data-ttu-id="12951-120">Les utilisateurs d’applications clientes peuvent afficher le contenu de conteneurs de carnet d’adresses et, dans certains cas, modifier le contenu.</span><span class="sxs-lookup"><span data-stu-id="12951-120">The users of client applications can view the contents of address book containers and, in some cases, modify the contents.</span></span> <span data-ttu-id="12951-121">Conteneurs de carnet d’adresses peuvent être créés avec différents niveaux d’accès, selon le fournisseur de carnet d’adresses.</span><span class="sxs-lookup"><span data-stu-id="12951-121">Address book containers can be created with different access levels, depending on the address book provider.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="12951-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="12951-122">See also</span></span>

- [<span data-ttu-id="12951-123">Architecture et des fonctionnalités MAPI</span><span class="sxs-lookup"><span data-stu-id="12951-123">MAPI Features and Architecture</span></span>](mapi-features-and-architecture.md)

