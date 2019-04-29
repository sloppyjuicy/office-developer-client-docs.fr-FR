---
title: Génération et utilisation d’identificateurs d’entrées dans les fournisseurs de banques de messages
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 0c43546a-4788-4852-bc89-d6baa4f33c94
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 005742eaaba81600be249d52e5d8098e9f286f17
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437678"
---
# <a name="generating-and-using-entry-identifiers-in-message-store-providers"></a><span data-ttu-id="c1202-103">Génération et utilisation d’identificateurs d’entrées dans les fournisseurs de banques de messages</span><span class="sxs-lookup"><span data-stu-id="c1202-103">Generating and using entry identifiers in message store providers</span></span>

<span data-ttu-id="c1202-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c1202-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c1202-105">Lorsqu'un nouveau dossier ou message est créé dans une banque de messages, le fournisseur de banque de messages doit affecter cet objet à un identificateur d'entrée afin que les applications clientes puissent y faire référence.</span><span class="sxs-lookup"><span data-stu-id="c1202-105">When a new folder or message is created in a message store, the message store provider has to assign that object an entry identifier so that client applications can refer to it.</span></span> <span data-ttu-id="c1202-106">Les fournisseurs de banques de messages peuvent réutiliser les identificateurs d'entrée à long terme obsolètes des objets supprimés ou créer des identificateurs.</span><span class="sxs-lookup"><span data-stu-id="c1202-106">Message store providers can either reuse the defunct long-term entry identifiers of deleted objects or create new identifiers.</span></span> <span data-ttu-id="c1202-107">Il n'y a pas d'exigence d'une façon ou d'une autre pour les fournisseurs de banque de messages; Toutefois, si cela est possible, un fournisseur de banque de messages doit toujours générer de nouveaux identificateurs d'entrée à long terme pour les nouveaux objets au lieu de réutiliser les anciens.</span><span class="sxs-lookup"><span data-stu-id="c1202-107">There is no requirement one way or the other for message store providers; however, if it is feasible, a message store provider should always generate new long-term entry identifiers for new objects rather than reusing old ones.</span></span> <span data-ttu-id="c1202-108">Il convient de réutiliser des identificateurs d'entrée à court terme lorsque les objets auxquels ils font référence sont supprimés.</span><span class="sxs-lookup"><span data-stu-id="c1202-108">It is fine to reuse short-term entry identifiers when the objects they refer to are deleted.</span></span>
  
<span data-ttu-id="c1202-109">La raison de cette suppression est que les clients peuvent mettre en cache des identificateurs d'entrée, parfois pendant de longues périodes.</span><span class="sxs-lookup"><span data-stu-id="c1202-109">The reason for this deletion is that clients can cache entry identifiers, sometimes for long periods of time.</span></span> <span data-ttu-id="c1202-110">Si cela se produit et que le fournisseur de banque de messages réutilise des identificateurs d'entrée, il est possible que l'identificateur d'entrée fasse référence à un autre objet lorsque le client ouvre l'identificateur d'entrée plutôt que lors de la première obtention de l'identificateur d'entrée.</span><span class="sxs-lookup"><span data-stu-id="c1202-110">If that happens and the message store provider does reuse entry identifiers, it is possible for the entry identifier to refer to a different object when the client opens the entry identifier than when it first obtained the entry identifier.</span></span> <span data-ttu-id="c1202-111">Si le fournisseur de banque de messages ne réutilise pas les identificateurs d'entrée ou utilise au moins le schéma de génération de l'identificateur d'entrée qui n'est pas répété longtemps, ce problème ne peut pas se produire.</span><span class="sxs-lookup"><span data-stu-id="c1202-111">If the message store provider does not reuse entry identifiers — or at least uses an entry identifier generation scheme that does not repeat for a very long time — this problem cannot occur.</span></span>
  
<span data-ttu-id="c1202-112">De même, les fournisseurs de banques de messages doivent tenter de conserver les identificateurs d'entrée pour les dossiers et les messages lorsqu'ils sont déplacés dans la Banque de messages.</span><span class="sxs-lookup"><span data-stu-id="c1202-112">Similarly, message store providers should attempt to preserve entry identifiers for folders and messages when they are moved in the message store.</span></span> <span data-ttu-id="c1202-113">Si le fournisseur de banque de messages peut effectuer cette opération, les références aux objets dans le magasin ne deviennent pas valides lorsque l'objet est déplacé vers un autre emplacement du magasin.</span><span class="sxs-lookup"><span data-stu-id="c1202-113">If the message store provider can do that, references to objects in the store will not become invalid when the object is moved to a different location in the store.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="c1202-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c1202-114">See also</span></span>

- [<span data-ttu-id="c1202-115">Fonctionnalit�s de la banque de messages</span><span class="sxs-lookup"><span data-stu-id="c1202-115">Message Store Features</span></span>](message-store-features.md)

