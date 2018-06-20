---
title: Fournisseurs de magasin de génération et l’utilisation d’identificateurs d’entrée dans un message
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 0c43546a-4788-4852-bc89-d6baa4f33c94
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 3bfda4a1dbe464c744917c2e9b3ca66eaf88fd20
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783415"
---
# <a name="generating-and-using-entry-identifiers-in-message-store-providers"></a><span data-ttu-id="75761-103">Fournisseurs de magasin de génération et l’utilisation d’identificateurs d’entrée dans un message</span><span class="sxs-lookup"><span data-stu-id="75761-103">Generating and using entry identifiers in message store providers</span></span>

<span data-ttu-id="75761-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="75761-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="75761-105">Lorsqu’un nouveau dossier ou un message est créé dans une banque de messages, le fournisseur de banque de message doit affecter à cet objet un identificateur d’entrée afin que les applications clientes peuvent faire.</span><span class="sxs-lookup"><span data-stu-id="75761-105">When a new folder or message is created in a message store, the message store provider has to assign that object an entry identifier so that client applications can refer to it.</span></span> <span data-ttu-id="75761-106">Fournisseurs de banque de message pouvant réutiliser les anciens identificateurs d’entrée à long terme d’objets supprimés ou créer de nouveaux identificateurs.</span><span class="sxs-lookup"><span data-stu-id="75761-106">Message store providers can either reuse the defunct long-term entry identifiers of deleted objects or create new identifiers.</span></span> <span data-ttu-id="75761-107">Il y a aucun moyen d’une ou l’autre pour les fournisseurs de banque de messages ; Toutefois, s’il est possible, un fournisseur de magasin de message doit toujours générer nouveaux identificateurs d’entrée à long terme pour les nouveaux objets plutôt que d’anciens réutilisation.</span><span class="sxs-lookup"><span data-stu-id="75761-107">There is no requirement one way or the other for message store providers; however, if it is feasible, a message store provider should always generate new long-term entry identifiers for new objects rather than reusing old ones.</span></span> <span data-ttu-id="75761-108">Il convient de réutiliser les identificateurs d’entrée à court terme lorsqu’ils se rapportent aux objets sont supprimés.</span><span class="sxs-lookup"><span data-stu-id="75761-108">It is fine to reuse short-term entry identifiers when the objects they refer to are deleted.</span></span>
  
<span data-ttu-id="75761-109">La raison de cette suppression est que les clients peuvent effectuer les identificateurs d’entrée, parfois pour de longues périodes.</span><span class="sxs-lookup"><span data-stu-id="75761-109">The reason for this deletion is that clients can cache entry identifiers, sometimes for long periods of time.</span></span> <span data-ttu-id="75761-110">Si cela se produit et le fournisseur de banque de messages réutilise les identificateurs d’entrée, il est possible de l’identificateur d’entrée faire référence à un autre objet lorsque le client s’ouvre l’identificateur d’entrée que lorsqu’il obtenu tout d’abord l’identificateur d’entrée.</span><span class="sxs-lookup"><span data-stu-id="75761-110">If that happens and the message store provider does reuse entry identifiers, it is possible for the entry identifier to refer to a different object when the client opens the entry identifier than when it first obtained the entry identifier.</span></span> <span data-ttu-id="75761-111">Si le fournisseur de banque de messages ne réutilise pas les identificateurs d’entrée, ou au moins utilise un modèle génération identificateur d’entrée n’est pas extensible pour beaucoup de temps, ce problème ne peut pas se produire.</span><span class="sxs-lookup"><span data-stu-id="75761-111">If the message store provider does not reuse entry identifiers — or at least uses an entry identifier generation scheme that does not repeat for a very long time — this problem cannot occur.</span></span>
  
<span data-ttu-id="75761-112">De même, les fournisseurs de magasins de message doivent essayer de conserver les identificateurs d’entrée pour les dossiers et messages lorsqu’ils sont déplacés dans la banque de messages.</span><span class="sxs-lookup"><span data-stu-id="75761-112">Similarly, message store providers should attempt to preserve entry identifiers for folders and messages when they are moved in the message store.</span></span> <span data-ttu-id="75761-113">Si le fournisseur de banque de message peut faire que, les références à des objets dans le magasin ne prendra non valides lorsque l’objet est déplacé vers un autre emplacement dans le magasin.</span><span class="sxs-lookup"><span data-stu-id="75761-113">If the message store provider can do that, references to objects in the store will not become invalid when the object is moved to a different location in the store.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="75761-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="75761-114">See also</span></span>

- [<span data-ttu-id="75761-115">Fonctionnalit�s de la banque de messages</span><span class="sxs-lookup"><span data-stu-id="75761-115">Message Store Features</span></span>](message-store-features.md)

