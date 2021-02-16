---
title: Vue d’ensemble du fournisseur de carnet d’adresses MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ead51434-ae19-4c34-aa7a-bdeeccca5bd9
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: ee628f4b11cb174c05a16ca60c9ec830a0e9abbe
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426540"
---
# <a name="mapi-address-book-provider-overview"></a><span data-ttu-id="806e7-103">Vue d’ensemble du fournisseur de carnet d’adresses MAPI</span><span class="sxs-lookup"><span data-stu-id="806e7-103">MAPI address book provider overview</span></span>
  
<span data-ttu-id="806e7-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="806e7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="806e7-105">Les fournisseurs de carnets d’adresses gèrent l’accès aux informations d’annuaire.</span><span class="sxs-lookup"><span data-stu-id="806e7-105">Address book providers handle access to directory information.</span></span> <span data-ttu-id="806e7-106">Les informations d’annuaire sont constituées de données pour deux types de destinataires de message : les utilisateurs de messagerie individuels et les groupes d’utilisateurs de messagerie fréquemment adressés ensemble dans des listes de distribution.</span><span class="sxs-lookup"><span data-stu-id="806e7-106">Directory information consists of data for two types of message recipients: individual messaging users and groups of messaging users who are commonly addressed together in distribution lists.</span></span> <span data-ttu-id="806e7-107">Selon le type de destinataire et le fournisseur de carnet d’adresses, un large éventail d’informations peuvent être disponibles.</span><span class="sxs-lookup"><span data-stu-id="806e7-107">Depending on the type of recipient and the address book provider, there is a wide range of information that can be made available.</span></span> <span data-ttu-id="806e7-108">Par exemple, tous les fournisseurs de carnet d’adresses stockent le nom, l’adresse et le type d’adresse d’un destinataire.</span><span class="sxs-lookup"><span data-stu-id="806e7-108">For example, all address book providers store a recipient's name, address, and address type.</span></span>
  
<span data-ttu-id="806e7-109">Chaque fournisseur de carnet d’adresses organise ces données à l’aide d’un ou plusieurs conteneurs.</span><span class="sxs-lookup"><span data-stu-id="806e7-109">Each address book provider organizes this data by using one or more containers.</span></span> <span data-ttu-id="806e7-110">Le nombre et la structure des conteneurs dépendent de l’implémentation du fournisseur de carnet d’adresses.</span><span class="sxs-lookup"><span data-stu-id="806e7-110">The number and structure of the containers depends on the address book provider's implementation.</span></span> <span data-ttu-id="806e7-111">Par exemple, un fournisseur de carnet d’adresses peut utiliser un seul conteneur pour contenir toutes les informations, un autre peut utiliser un conteneur de niveau supérieur qui contient des sous-conteneurs et un troisième peut utiliser plusieurs conteneurs de niveau supérieur, chacun contenant des sous-conteneurs.</span><span class="sxs-lookup"><span data-stu-id="806e7-111">For example, one address book provider might use a single container to hold all of the information, another might use one top-level container that holds subcontainers, and a third might use several top-level containers, each holding subcontainers.</span></span> <span data-ttu-id="806e7-112">Une hiérarchie de conteneur de carnet d’adresses peut être assez profonde ; il n’existe aucune limite au nombre de sous-ensembles qui peuvent être utilisés.</span><span class="sxs-lookup"><span data-stu-id="806e7-112">An address book container hierarchy can be quite deep; there is no limit to the number of subcontainers that can be used.</span></span>
  
<span data-ttu-id="806e7-113">L’illustration suivante illustre une organisation de carnet d’adresses MAPI classique.</span><span class="sxs-lookup"><span data-stu-id="806e7-113">The following illustration shows a typical MAPI address book organization.</span></span>
  
<span data-ttu-id="806e7-114">**Organisation de carnet d’adresses**</span><span class="sxs-lookup"><span data-stu-id="806e7-114">**Address book organization**</span></span>
  
<span data-ttu-id="806e7-115">![Organisation de carnet d’adresses](media/amapi_04.gif "Organisation Carnet d’adresses")</span><span class="sxs-lookup"><span data-stu-id="806e7-115">![Address book organization](media/amapi_04.gif "Address book organization")</span></span>
  
<span data-ttu-id="806e7-116">MAPI intègre toutes les informations fournies par les fournisseurs de carnets d’adresses installés dans un carnet d’adresses unique, en présentant un affichage unifié à l’application cliente.</span><span class="sxs-lookup"><span data-stu-id="806e7-116">MAPI integrates all the information supplied by the installed address book providers into a single address book, presenting a unified view to the client application.</span></span> <span data-ttu-id="806e7-117">La liste intégrée affiche les conteneurs de niveau supérieur affichés par chacun des fournisseurs de carnet d’adresses installés.</span><span class="sxs-lookup"><span data-stu-id="806e7-117">The integrated list shows the top-level containers displayed by each of the installed address book providers.</span></span> <span data-ttu-id="806e7-118">La plupart des fournisseurs de carnet d’adresses exposent uniquement quelques conteneurs (généralement un à trois) au niveau supérieur pour être inclus dans le niveau supérieur du carnet d’adresses intégré MAPI.</span><span class="sxs-lookup"><span data-stu-id="806e7-118">Most address book providers expose only a few containers (typically one to three) at the top level for inclusion in the top level of the MAPI integrated address book.</span></span> <span data-ttu-id="806e7-119">Par exemple, un fournisseur de carnet d’adresses peut rendre disponibles « Tous les utilisateurs » et « Utilisateurs locaux » en tant que deux conteneurs au niveau supérieur.</span><span class="sxs-lookup"><span data-stu-id="806e7-119">For example, an address book provider might make available "All Users" and "Local Users" as two containers at the top level.</span></span>
  
<span data-ttu-id="806e7-120">Les utilisateurs d’applications clientes peuvent afficher le contenu des conteneurs de carnet d’adresses et, dans certains cas, en modifier le contenu.</span><span class="sxs-lookup"><span data-stu-id="806e7-120">The users of client applications can view the contents of address book containers and, in some cases, modify the contents.</span></span> <span data-ttu-id="806e7-121">Les conteneurs de carnet d’adresses peuvent être créés avec différents niveaux d’accès, selon le fournisseur de carnet d’adresses.</span><span class="sxs-lookup"><span data-stu-id="806e7-121">Address book containers can be created with different access levels, depending on the address book provider.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="806e7-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="806e7-122">See also</span></span>

- [<span data-ttu-id="806e7-123">Fonctionnalités et architecture MAPI</span><span class="sxs-lookup"><span data-stu-id="806e7-123">MAPI Features and Architecture</span></span>](mapi-features-and-architecture.md)

