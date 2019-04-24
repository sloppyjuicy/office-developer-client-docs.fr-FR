---
title: Identificateurs d'entrée à long terme
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a514275e-40c2-48db-8072-1dfc392a7ac6
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: b65656992681618aa8a1c53217bdd7101bc2502b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307783"
---
# <a name="long-term-entry-identifiers"></a><span data-ttu-id="7715f-103">Identificateurs d'entrée à long terme</span><span class="sxs-lookup"><span data-stu-id="7715f-103">Long-Term Entry Identifiers</span></span>

  
  
<span data-ttu-id="7715f-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7715f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7715f-105">Un identificateur d'entrée à long terme est affecté par un fournisseur de services à un objet lorsqu'un objet requiert un identificateur avec une durée de vie prolongée.</span><span class="sxs-lookup"><span data-stu-id="7715f-105">A long-term entry identifier is assigned by a service provider to an object when an object requires an identifier with a prolonged lifespan.</span></span> <span data-ttu-id="7715f-106">Les identificateurs d'entrée à long terme sont toujours valides pendant des semaines ou des mois, et peuvent être valides sur d'autres stations de travail, selon le fournisseur.</span><span class="sxs-lookup"><span data-stu-id="7715f-106">Long-term entry identifiers are always valid for weeks or months and can be valid on other workstations, depending on the provider.</span></span> <span data-ttu-id="7715f-107">Les identificateurs à long terme créés par des fournisseurs de carnet d'adresses pour les destinataires personnalisés sont universellement valides.</span><span class="sxs-lookup"><span data-stu-id="7715f-107">The long-term identifiers created by address book providers for custom recipients are universally valid.</span></span> 
  
<span data-ttu-id="7715f-108">Les identificateurs d'entrée à long terme sont affectés à des banques de messages, des dossiers, des messages, des conteneurs de carnet d'adresses, des utilisateurs de messagerie et des listes de distribution.</span><span class="sxs-lookup"><span data-stu-id="7715f-108">Long-term entry identifiers are assigned to message stores, folders, messages, address book containers, messaging users, and distribution lists.</span></span> <span data-ttu-id="7715f-109">Lorsque les applications clientes appellent la méthode [IMAPIProp:: GetProps](imapiprop-getprops.md) de ces objets, il s'agit toujours d'un identificateur d'entrée à long terme renvoyé.</span><span class="sxs-lookup"><span data-stu-id="7715f-109">When client applications call the [IMAPIProp::GetProps](imapiprop-getprops.md) method of these objects, it is always a long-term entry identifier that is returned.</span></span> 
  
<span data-ttu-id="7715f-110">Les identificateurs d'entrée à long terme doivent être uniques dans toutes les banques de messages du profil actif; par conséquent, lorsqu'un message ou un dossier est copié d'une banque de messages à une autre, un nouvel identificateur d'entrée doit lui être attribué.</span><span class="sxs-lookup"><span data-stu-id="7715f-110">Long-term entry identifiers must be unique across all message stores in the active profile; therefore, when a message or folder is copied from one message store to another, it must be assigned a new entry identifier.</span></span> <span data-ttu-id="7715f-111">Lorsqu'un objet de banque de messages est déplacé, le fournisseur de banque de messages qui implémente le déplacement détermine si l'identificateur d'entrée d'origine reste valide.</span><span class="sxs-lookup"><span data-stu-id="7715f-111">When a message store object is moved, the message store provider that implements the move determines whether the original entry identifier will remain valid.</span></span> <span data-ttu-id="7715f-112">Certains fournisseurs de services affectent de nouveaux identificateurs d'entrée aux objets déplacés; d'autres non.</span><span class="sxs-lookup"><span data-stu-id="7715f-112">Some service providers assign new entry identifiers to moved objects; others do not.</span></span> <span data-ttu-id="7715f-113">En cas de modification, le nouvel identificateur d'entrée est inclus dans les informations transmises aux clients lorsqu'ils sont avertis du déplacement.</span><span class="sxs-lookup"><span data-stu-id="7715f-113">If there is a change, the new entry identifier will be included in the information passed to clients when they are notified of the move.</span></span> 
  
<span data-ttu-id="7715f-114">En règle générale, les fournisseurs de banque de messages implémentent le comportement suivant lorsqu'ils déplacent des dossiers:</span><span class="sxs-lookup"><span data-stu-id="7715f-114">Typically, message store providers implement the following behavior when they move folders:</span></span>
  
- <span data-ttu-id="7715f-115">Lorsqu'un dossier est déplacé d'une banque de messages vers une autre pour un autre type, l'identificateur de l'entrée est garanti.</span><span class="sxs-lookup"><span data-stu-id="7715f-115">When a folder is moved from one message store to another store of a different type, the entry identifier is guaranteed to change.</span></span>
    
- <span data-ttu-id="7715f-116">Lorsqu'un dossier est déplacé d'une banque de messages vers une autre banque du même type, l'identificateur de l'entrée est presque toujours modifié.</span><span class="sxs-lookup"><span data-stu-id="7715f-116">When a folder is moved from one message store to another store of the same type, the entry identifier almost always changes.</span></span>
    
- <span data-ttu-id="7715f-117">Lorsqu'un dossier est déplacé vers un autre emplacement dans le même magasin de messages, l'identificateur d'entrée peut être modifié ou non, selon le fournisseur de banque de messages.</span><span class="sxs-lookup"><span data-stu-id="7715f-117">When a folder is moved to another location within the same message store, the entry identifier might or might not change, depending on the message store provider.</span></span>
    
<span data-ttu-id="7715f-118">Le fait de renommer un dossier sans modifier son dossier parent ne provoque généralement pas la modification de l'identificateur d'entrée.</span><span class="sxs-lookup"><span data-stu-id="7715f-118">Renaming a folder without changing its parent folder usually does not cause the entry identifier to change.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="7715f-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7715f-119">See also</span></span>



[<span data-ttu-id="7715f-120">Identificateurs d'entrée MAPI</span><span class="sxs-lookup"><span data-stu-id="7715f-120">MAPI Entry Identifiers</span></span>](mapi-entry-identifiers.md)

