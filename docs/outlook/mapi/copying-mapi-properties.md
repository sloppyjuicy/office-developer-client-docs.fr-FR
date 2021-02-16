---
title: Copie des propriétés MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a52f4bcd-6e17-4623-a469-53be1f2758b1
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: ae8e553cf2e19ae1ba06ca09aad84eae9f7d1238
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415046"
---
# <a name="copying-mapi-properties"></a><span data-ttu-id="8483e-103">Copie des propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="8483e-103">Copying MAPI Properties</span></span>

  
  
<span data-ttu-id="8483e-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8483e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8483e-105">Les clients et les fournisseurs de services peuvent copier une ou plusieurs propriétés d’un objet avec les méthodes et fonctions API **IMAPIProp** suivantes :</span><span class="sxs-lookup"><span data-stu-id="8483e-105">Clients and service providers can copy one or more of an object's properties with the following **IMAPIProp** methods and API functions:</span></span> 
  
- <span data-ttu-id="8483e-106">La [méthode IMAPIProp::CopyTo](imapiprop-copyto.md) copie toutes les propriétés d’un objet dans un autre objet, en excluant éventuellement les propriétés sélectionnées.</span><span class="sxs-lookup"><span data-stu-id="8483e-106">The [IMAPIProp::CopyTo](imapiprop-copyto.md) method copies all of an object's properties to another object, optionally excluding selected properties.</span></span> <span data-ttu-id="8483e-107">**CopyTo** est utilisé pour copier ou déplacer n’importe quel type d’objet.</span><span class="sxs-lookup"><span data-stu-id="8483e-107">**CopyTo** is used for copying or moving any type of object.</span></span> 
    
- <span data-ttu-id="8483e-108">La [méthode IMAPIProp::CopyProps](imapiprop-copyprops.md) copie les propriétés sélectionnées d’un objet.</span><span class="sxs-lookup"><span data-stu-id="8483e-108">The [IMAPIProp::CopyProps](imapiprop-copyprops.md) method copies selected properties of an object.</span></span> <span data-ttu-id="8483e-109">**CopyProps est** utilisé principalement avec les messages.</span><span class="sxs-lookup"><span data-stu-id="8483e-109">**CopyProps** is used mainly with messages.</span></span> <span data-ttu-id="8483e-110">Lorsqu’un client crée une copie avancée d’un message ou d’une réponse, **CopyProps** gère la copie des propriétés appropriées à partir du message d’origine.</span><span class="sxs-lookup"><span data-stu-id="8483e-110">When a client creates a forwarded copy of a message or a reply, **CopyProps** handles copying the appropriate properties from the original message.</span></span> 
    
- <span data-ttu-id="8483e-111">La [fonction PropCopyMore](propcopymore.md) copie une valeur de propriété unique d’un emplacement à un autre.</span><span class="sxs-lookup"><span data-stu-id="8483e-111">The [PropCopyMore](propcopymore.md) function copies a single property value from one location to another.</span></span> <span data-ttu-id="8483e-112">Utilisez **PropCopyMore avec** précaution.</span><span class="sxs-lookup"><span data-stu-id="8483e-112">Use **PropCopyMore** with caution.</span></span> <span data-ttu-id="8483e-113">Il est possible, lors de la copie d’une valeur à la fois, d’allouer de nombreux petits blocs de mémoire et de fragmenter la mémoire.</span><span class="sxs-lookup"><span data-stu-id="8483e-113">It is possible — when copying one value at a time — to allocate many small blocks of memory and cause memory to fragment.</span></span> 
    
- <span data-ttu-id="8483e-114">La [fonction ScCopyProps](sccopyprops.md) copie les valeurs des propriétés en bloc.</span><span class="sxs-lookup"><span data-stu-id="8483e-114">The [ScCopyProps](sccopyprops.md) function copies property values in bulk.</span></span> <span data-ttu-id="8483e-115">**ScCopyProps peut** copier des valeurs de propriétés qui ont été construites à partir de blocs de mémoire disjoints.</span><span class="sxs-lookup"><span data-stu-id="8483e-115">**ScCopyProps** can copy property values that have been built from disjointed blocks of memory.</span></span> <span data-ttu-id="8483e-116">Elle renvoie un nouveau tableau de propriétés.</span><span class="sxs-lookup"><span data-stu-id="8483e-116">It returns a new property array.</span></span> 
    
- <span data-ttu-id="8483e-117">Si le tableau de propriétés renvoyé par **ScCopyProps** doit être stocké sur disque, utilisez la [fonction ScRelocProps](screlocprops.md) pour ajuster les pointeurs.</span><span class="sxs-lookup"><span data-stu-id="8483e-117">If the property array returned by **ScCopyProps** is to be stored on disk, use the [ScRelocProps](screlocprops.md) function to adjust the pointers.</span></span> <span data-ttu-id="8483e-118">**ScRelocProps** doit être appelé deux fois ; une fois pour ajuster les adresses avant d’écrire l’opération de données, puis à nouveau pendant l’opération de lecture.</span><span class="sxs-lookup"><span data-stu-id="8483e-118">**ScRelocProps** should be called twice; once to adjust the addresses before writing the data operation and then again during the read operation.</span></span> <span data-ttu-id="8483e-119">La **fonction ScRelocProps** suppose que le tableau de valeurs de propriétés a été initialement alloué dans une allocation unique.</span><span class="sxs-lookup"><span data-stu-id="8483e-119">The **ScRelocProps** function assumes that the property value array was originally allocated in a single allocation.</span></span> 
    
<span data-ttu-id="8483e-120">Les fonctions d’API décrites dans la liste précédente copient les propriétés en mémoire plutôt que d’un objet à un autre.</span><span class="sxs-lookup"><span data-stu-id="8483e-120">The API functions described in the preceding list copy properties in memory rather than from one object to another object.</span></span> <span data-ttu-id="8483e-121">Ces fonctions sont actuellement prise en charge, mais elles peuvent ne pas l’être dans une prochaine version.</span><span class="sxs-lookup"><span data-stu-id="8483e-121">These functions are presently supported, but might not be supported in a future release.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="8483e-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8483e-122">See also</span></span>



[<span data-ttu-id="8483e-123">Vue d’ensemble de la propriété MAPI</span><span class="sxs-lookup"><span data-stu-id="8483e-123">MAPI Property Overview</span></span>](mapi-property-overview.md)

