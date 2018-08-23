---
title: Identificateurs d’entrée à long terme
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a514275e-40c2-48db-8072-1dfc392a7ac6
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: e624ab4f39ef5a5385119779b0780ee7173a3ee7
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22586920"
---
# <a name="long-term-entry-identifiers"></a><span data-ttu-id="6eed6-103">Identificateurs d’entrée à long terme</span><span class="sxs-lookup"><span data-stu-id="6eed6-103">Long-Term Entry Identifiers</span></span>

  
  
<span data-ttu-id="6eed6-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6eed6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6eed6-105">Un identificateur d’entrée à long terme est affecté par un fournisseur de services à un objet lorsqu’un objet nécessite un identificateur ayant une durée de vie prolongée.</span><span class="sxs-lookup"><span data-stu-id="6eed6-105">A long-term entry identifier is assigned by a service provider to an object when an object requires an identifier with a prolonged lifespan.</span></span> <span data-ttu-id="6eed6-106">Identificateurs d’entrée à long terme sont toujours valables pour plusieurs semaines ou mois et peuvent être valides sur les autres stations de travail, selon le fournisseur.</span><span class="sxs-lookup"><span data-stu-id="6eed6-106">Long-term entry identifiers are always valid for weeks or months and can be valid on other workstations, depending on the provider.</span></span> <span data-ttu-id="6eed6-107">Les identificateurs à long terme créés par les fournisseurs de carnet d’adresses pour les destinataires personnalisés valent universel.</span><span class="sxs-lookup"><span data-stu-id="6eed6-107">The long-term identifiers created by address book providers for custom recipients are universally valid.</span></span> 
  
<span data-ttu-id="6eed6-108">Identificateurs d’entrée à long terme sont affectés à des banques de messages, les dossiers, messages, conteneurs de carnet d’adresses, messagerie utilisateurs et distribution listes.</span><span class="sxs-lookup"><span data-stu-id="6eed6-108">Long-term entry identifiers are assigned to message stores, folders, messages, address book containers, messaging users, and distribution lists.</span></span> <span data-ttu-id="6eed6-109">Les applications clientes d’appeler la méthode [IMAPIProp::GetProps](imapiprop-getprops.md) de ces objets, il est toujours un identificateur d’entrée à long terme qui est renvoyé.</span><span class="sxs-lookup"><span data-stu-id="6eed6-109">When client applications call the [IMAPIProp::GetProps](imapiprop-getprops.md) method of these objects, it is always a long-term entry identifier that is returned.</span></span> 
  
<span data-ttu-id="6eed6-110">Identificateurs d’entrée à long terme doivent être uniques parmi toutes les banques de messages dans le profil actif ; Par conséquent, lorsqu’un message ou un dossier est copié à partir d’une banque d’informations à un autre, il doit être affecté un nouvel identificateur d’entrée.</span><span class="sxs-lookup"><span data-stu-id="6eed6-110">Long-term entry identifiers must be unique across all message stores in the active profile; therefore, when a message or folder is copied from one message store to another, it must be assigned a new entry identifier.</span></span> <span data-ttu-id="6eed6-111">Lorsqu’un objet de banque de messages est déplacé, le fournisseur de banque de messages qui implémente le déplacement détermine si l’identificateur d’entrée d’origine reste valide.</span><span class="sxs-lookup"><span data-stu-id="6eed6-111">When a message store object is moved, the message store provider that implements the move determines whether the original entry identifier will remain valid.</span></span> <span data-ttu-id="6eed6-112">Certains fournisseurs de services attribuer de nouveaux identificateurs d’entrée aux objets déplacées ; d’autres ne le sont pas.</span><span class="sxs-lookup"><span data-stu-id="6eed6-112">Some service providers assign new entry identifiers to moved objects; others do not.</span></span> <span data-ttu-id="6eed6-113">S’il existe une modification, l’identificateur d’entrée sera inclus dans les informations transmises aux clients lorsqu’ils sont avertis du déplacement.</span><span class="sxs-lookup"><span data-stu-id="6eed6-113">If there is a change, the new entry identifier will be included in the information passed to clients when they are notified of the move.</span></span> 
  
<span data-ttu-id="6eed6-114">En règle générale, les fournisseurs de magasins de message implémentent le comportement suivant lorsque le déplacement de dossiers :</span><span class="sxs-lookup"><span data-stu-id="6eed6-114">Typically, message store providers implement the following behavior when they move folders:</span></span>
  
- <span data-ttu-id="6eed6-115">Lorsqu’un dossier est déplacé vers un autre magasin d’un type différent à partir d’une banque d’informations, l’identificateur d’entrée est garanti à modifier.</span><span class="sxs-lookup"><span data-stu-id="6eed6-115">When a folder is moved from one message store to another store of a different type, the entry identifier is guaranteed to change.</span></span>
    
- <span data-ttu-id="6eed6-116">Lorsqu’un dossier est déplacé vers un autre magasin du même type à partir d’une banque d’informations, l’identificateur d’entrée change presque toujours.</span><span class="sxs-lookup"><span data-stu-id="6eed6-116">When a folder is moved from one message store to another store of the same type, the entry identifier almost always changes.</span></span>
    
- <span data-ttu-id="6eed6-117">Lorsqu’un dossier est déplacé vers un autre emplacement dans le même magasin de message, l’identificateur d’entrée peut-être ou ne peut pas changer, selon le fournisseur de banque de messages.</span><span class="sxs-lookup"><span data-stu-id="6eed6-117">When a folder is moved to another location within the same message store, the entry identifier might or might not change, depending on the message store provider.</span></span>
    
<span data-ttu-id="6eed6-118">Renommer un dossier sans modifier son dossier parent généralement n’entraîne pas l’identificateur d’entrée à modifier.</span><span class="sxs-lookup"><span data-stu-id="6eed6-118">Renaming a folder without changing its parent folder usually does not cause the entry identifier to change.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="6eed6-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6eed6-119">See also</span></span>



[<span data-ttu-id="6eed6-120">Identificateurs d’entrée MAPI</span><span class="sxs-lookup"><span data-stu-id="6eed6-120">MAPI Entry Identifiers</span></span>](mapi-entry-identifiers.md)

