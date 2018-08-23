---
title: Restrictions de carnet d’adresses
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 6ace8c03-45a7-484b-8c12-516ac0e40dc2
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 54cd90cac6c00e8cf274e0b78a1bfec32401bb8d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576511"
---
# <a name="address-book-restrictions"></a><span data-ttu-id="369c4-103">Restrictions de carnet d’adresses</span><span class="sxs-lookup"><span data-stu-id="369c4-103">Address Book Restrictions</span></span>

  
  
<span data-ttu-id="369c4-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="369c4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="369c4-105">Fournisseurs de carnet d’adresses sont requis pour prendre en charge trois types de restrictions sur les tables des matières de leurs conteneurs :</span><span class="sxs-lookup"><span data-stu-id="369c4-105">Address book providers are required to support three types of restrictions on the contents tables of their containers:</span></span>
  
- <span data-ttu-id="369c4-106">Restrictions de propriété nom ambigu</span><span class="sxs-lookup"><span data-stu-id="369c4-106">Ambiguous name property restrictions</span></span>
    
- <span data-ttu-id="369c4-107">Restrictions de propriété de clé d’instance</span><span class="sxs-lookup"><span data-stu-id="369c4-107">Instance key property restrictions</span></span>
    
- <span data-ttu-id="369c4-108">Restrictions de contenu de nom complet préfixé</span><span class="sxs-lookup"><span data-stu-id="369c4-108">Prefixed display name content restrictions</span></span>
    
<span data-ttu-id="369c4-109">Restrictions de nom ambigu sont des restrictions de propriété à l’aide de la propriété **PR_ANR** ([PidTagAnr](pidtaganr-canonical-property.md)) pour faire correspondre les noms des destinataires avec des entrées dans les conteneurs de carnet d’adresses.</span><span class="sxs-lookup"><span data-stu-id="369c4-109">Ambiguous name restrictions are property restrictions using the **PR_ANR** ([PidTagAnr](pidtaganr-canonical-property.md)) property to match recipient names with entries in address book containers.</span></span> <span data-ttu-id="369c4-110">La restriction de propriété **PR_ANR** est un type « mieux deviner » de la recherche grâce à laquelle les fournisseurs de carnet d’adresses peuvent choisir la propriété correspondante qui convient le mieux pour leur conteneur.</span><span class="sxs-lookup"><span data-stu-id="369c4-110">The **PR_ANR** property restriction is a "best guess" type of search whereby address book providers can choose the matching property that works best for their container.</span></span> <span data-ttu-id="369c4-111">Par exemple, un fournisseur de carnet d’adresses peut implémenter la restriction **PR_ANR** par les noms des destinataires correspondants à la propriété **PR_ACCOUNT** ([PidTagAccount](pidtagaccount-canonical-property.md)) de chaque entrée de conteneur alors qu’un autre fournisseur peut utiliser **PR_DISPLAY _Ordinateur** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="369c4-111">For example, one address book provider might implement the **PR_ANR** restriction by matching recipient names against the **PR_ACCOUNT** ([PidTagAccount](pidtagaccount-canonical-property.md)) property of each container entry whereas another provider might use **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)).</span></span>
  
<span data-ttu-id="369c4-112">MAPI recommande que les implémentations de la restriction **PR_ANR** un équilibre entre la satisfaction client et des performances optimales.</span><span class="sxs-lookup"><span data-stu-id="369c4-112">MAPI recommends that implementations of the **PR_ANR** restriction strike a balance between adequate performance and user satisfaction.</span></span> <span data-ttu-id="369c4-113">Satisfaction des utilisateurs peut être compromise lorsqu’un fournisseur de carnet d’adresses implémente la restriction de telle sorte que trop ou trop peu de correspondance.</span><span class="sxs-lookup"><span data-stu-id="369c4-113">User satisfaction can be compromised when an address book provider implements the restriction in such a way that too few or too many matches are found.</span></span> <span data-ttu-id="369c4-114">Certains fournisseurs de carnet d’adresses prend en charge ce que l'on appelle un nom unique, ou courant, qui n’est pas affichable dans une boîte de dialogue, mais peut correspondre à une restriction de nom ambigu.</span><span class="sxs-lookup"><span data-stu-id="369c4-114">Some address book providers support what is known as a distinguished, or common, name that is not displayable in a dialog box but can match an ambiguous name restriction.</span></span> 
  
<span data-ttu-id="369c4-115">Une implémentation typique peut être pour analyser le nom d’affichage du destinataire en mots, correspondant à une entrée qui contient tous les mots.</span><span class="sxs-lookup"><span data-stu-id="369c4-115">A typical implementation might be to parse the recipient's display name into words, matching any entry that contains all of the words.</span></span> <span data-ttu-id="369c4-116">Attention aux détails tels que la sensibilité à la position de word, si les mots non consécutifs sont filtrés et le choix des caractères de séparation peuvent varier.</span><span class="sxs-lookup"><span data-stu-id="369c4-116">Attention to details such as sensitivity to word position, whether nonconsecutive words are matched, and the choice of separator characters can vary.</span></span> <span data-ttu-id="369c4-117">Par exemple, si le nom est résolu est « L Bill », une restriction **PR_ANR** par défaut, sélectionnez les entrées suivantes comme correspondants :</span><span class="sxs-lookup"><span data-stu-id="369c4-117">For example, if the name to be resolved is "Bill L," a typical **PR_ANR** restriction would select the following entries as matching:</span></span> 
  
- <span data-ttu-id="369c4-118">Billy Larson</span><span class="sxs-lookup"><span data-stu-id="369c4-118">Billy Larson</span></span>
    
- <span data-ttu-id="369c4-119">Bill Lee</span><span class="sxs-lookup"><span data-stu-id="369c4-119">Bill Lee</span></span>
    
- <span data-ttu-id="369c4-120">Offres d’emploi Logan Bill.</span><span class="sxs-lookup"><span data-stu-id="369c4-120">Bill Logan Jr.</span></span> 
    
- <span data-ttu-id="369c4-121">Sam Bill Lee</span><span class="sxs-lookup"><span data-stu-id="369c4-121">Sam Bill Lee</span></span>
    
<span data-ttu-id="369c4-122">Restrictions clés instance ou des restrictions de propriété **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)), sont utilisées dans l’implémentation de zones de liste qui sont utilisés dans les applications clientes pour l’affichage des tables MAPI.</span><span class="sxs-lookup"><span data-stu-id="369c4-122">Instance key restrictions, or **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) property restrictions, are used in the implementation of list boxes that are used in client applications for viewing MAPI tables.</span></span> <span data-ttu-id="369c4-123">Certaines implémentations de zone de liste Autoriser les utilisateurs à effectuer des sélections multiples, défiler vers le haut ou vers le bas et de retour sur le premier élément sélectionné.</span><span class="sxs-lookup"><span data-stu-id="369c4-123">Some list box implementations allow users to make multiple selections, scroll up or down, and return to the first item selected.</span></span> <span data-ttu-id="369c4-124">Pour implémenter ce comportement, les clients appellent [IMAPITable::FindRow](imapitable-findrow.md), en passant une restriction de propriété sur la propriété **PR_INSTANCE_KEY** à la méthode.</span><span class="sxs-lookup"><span data-stu-id="369c4-124">To implement this behavior, clients call [IMAPITable::FindRow](imapitable-findrow.md), passing a property restriction on the **PR_INSTANCE_KEY** property to the method.</span></span> <span data-ttu-id="369c4-125">Fournisseurs de carnet d’adresses sont requis pour prendre en charge cette restriction.</span><span class="sxs-lookup"><span data-stu-id="369c4-125">Address book providers are required to support this restriction.</span></span> 
  
<span data-ttu-id="369c4-126">Une autre fonctionnalité de zones de liste utilisé pour l’affichage tableau est la capacité pour placer le curseur basé sur un jeu de caractères de préfixe.</span><span class="sxs-lookup"><span data-stu-id="369c4-126">Another feature of list boxes used for table viewing is the ability to position the cursor based on a set of prefix characters.</span></span> <span data-ttu-id="369c4-127">Lorsque l’utilisateur commence à taper des caractères de préfixe, le client place le curseur sur le premier élément qui commence par ces caractères.</span><span class="sxs-lookup"><span data-stu-id="369c4-127">As the user starts typing prefix characters, the client moves the cursor to the first item that begins with these characters.</span></span> <span data-ttu-id="369c4-128">Clients implémentent cette fonctionnalité avec une restriction de contenu en fonction de la propriété **PR_DISPLAY_NAME** et le niveau approximatif FL_PREFIX.</span><span class="sxs-lookup"><span data-stu-id="369c4-128">Clients implement this feature with a content restriction based on the **PR_DISPLAY_NAME** property and the FL_PREFIX fuzzy level.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="369c4-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="369c4-129">See also</span></span>



[<span data-ttu-id="369c4-130">Tables MAPI</span><span class="sxs-lookup"><span data-stu-id="369c4-130">MAPI Tables</span></span>](mapi-tables.md)

