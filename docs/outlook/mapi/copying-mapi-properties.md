---
title: Copie des propriétés MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a52f4bcd-6e17-4623-a469-53be1f2758b1
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 2f9ee7221f523d7c92d91746f5cd719fad821a27
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783088"
---
# <a name="copying-mapi-properties"></a><span data-ttu-id="746de-103">Copie des propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="746de-103">Copying MAPI Properties</span></span>

  
  
<span data-ttu-id="746de-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="746de-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="746de-105">Clients et fournisseurs de services peuvent copier une ou plusieurs des propriétés d’un objet avec les fonctions de l’API des méthodes **IMAPIProp** suivantes :</span><span class="sxs-lookup"><span data-stu-id="746de-105">Clients and service providers can copy one or more of an object's properties with the following **IMAPIProp** methods and API functions:</span></span> 
  
- <span data-ttu-id="746de-106">La méthode [IMAPIProp::CopyTo](imapiprop-copyto.md) copie toutes les propriétés d’un objet à un autre objet, si vous le souhaitez à l’exception des propriétés sélectionnées.</span><span class="sxs-lookup"><span data-stu-id="746de-106">The [IMAPIProp::CopyTo](imapiprop-copyto.md) method copies all of an object's properties to another object, optionally excluding selected properties.</span></span> <span data-ttu-id="746de-107">**CopyTo** est utilisé pour la copie ou le déplacement de n’importe quel type d’objet.</span><span class="sxs-lookup"><span data-stu-id="746de-107">**CopyTo** is used for copying or moving any type of object.</span></span> 
    
- <span data-ttu-id="746de-108">La méthode [IMAPIProp::CopyProps](imapiprop-copyprops.md) copie les propriétés sélectionnées d’un objet.</span><span class="sxs-lookup"><span data-stu-id="746de-108">The [IMAPIProp::CopyProps](imapiprop-copyprops.md) method copies selected properties of an object.</span></span> <span data-ttu-id="746de-109">**CopyProps** est utilisée principalement avec des messages.</span><span class="sxs-lookup"><span data-stu-id="746de-109">**CopyProps** is used mainly with messages.</span></span> <span data-ttu-id="746de-110">Lorsqu’un client crée une copie transférée d’un message ou d’une réponse, poignées **CopyProps** copie les propriétés appropriées à partir du message d’origine.</span><span class="sxs-lookup"><span data-stu-id="746de-110">When a client creates a forwarded copy of a message or a reply, **CopyProps** handles copying the appropriate properties from the original message.</span></span> 
    
- <span data-ttu-id="746de-111">La fonction [PropCopyMore](propcopymore.md) copie une seule valeur de propriété d’un emplacement vers un autre.</span><span class="sxs-lookup"><span data-stu-id="746de-111">The [PropCopyMore](propcopymore.md) function copies a single property value from one location to another.</span></span> <span data-ttu-id="746de-112">Utilisez **PropCopyMore** avec précaution.</span><span class="sxs-lookup"><span data-stu-id="746de-112">Use **PropCopyMore** with caution.</span></span> <span data-ttu-id="746de-113">Il est possible, lors de la copie d’une valeur à la fois — pour allouer de nombreux petits blocs de mémoire et provoquer le fragment de mémoire.</span><span class="sxs-lookup"><span data-stu-id="746de-113">It is possible — when copying one value at a time — to allocate many small blocks of memory and cause memory to fragment.</span></span> 
    
- <span data-ttu-id="746de-114">La fonction [ScCopyProps](sccopyprops.md) copie les valeurs de propriété en bloc.</span><span class="sxs-lookup"><span data-stu-id="746de-114">The [ScCopyProps](sccopyprops.md) function copies property values in bulk.</span></span> <span data-ttu-id="746de-115">**ScCopyProps** peut copier les valeurs de propriété qui ont été générés à partir des blocs de mémoire.</span><span class="sxs-lookup"><span data-stu-id="746de-115">**ScCopyProps** can copy property values that have been built from disjointed blocks of memory.</span></span> <span data-ttu-id="746de-116">Il retourne un nouveau tableau de propriété.</span><span class="sxs-lookup"><span data-stu-id="746de-116">It returns a new property array.</span></span> 
    
- <span data-ttu-id="746de-117">Si le tableau renvoyé par **ScCopyProps** de la propriété doit être stocké sur disque, utilisez la fonction [ScRelocProps](screlocprops.md) pour ajuster les pointeurs.</span><span class="sxs-lookup"><span data-stu-id="746de-117">If the property array returned by **ScCopyProps** is to be stored on disk, use the [ScRelocProps](screlocprops.md) function to adjust the pointers.</span></span> <span data-ttu-id="746de-118">**ScRelocProps** doit être appelée deux fois ; une fois pour ajuster les adresses avant d’écrire l’opération de données, puis à nouveau lors de l’opération de lecture.</span><span class="sxs-lookup"><span data-stu-id="746de-118">**ScRelocProps** should be called twice; once to adjust the addresses before writing the data operation and then again during the read operation.</span></span> <span data-ttu-id="746de-119">La fonction **ScRelocProps** suppose que le tableau de valeurs de propriété alloué initialement dans une affectation unique.</span><span class="sxs-lookup"><span data-stu-id="746de-119">The **ScRelocProps** function assumes that the property value array was originally allocated in a single allocation.</span></span> 
    
<span data-ttu-id="746de-120">Les fonctions API décrites dans les précédente liste Propriétés en mémoire, au lieu d’un objet à un autre objet.</span><span class="sxs-lookup"><span data-stu-id="746de-120">The API functions described in the preceding list copy properties in memory rather than from one object to another object.</span></span> <span data-ttu-id="746de-121">Ces fonctions sont actuellement pris en charge, mais ne peuvent pas pris en charge dans une version future.</span><span class="sxs-lookup"><span data-stu-id="746de-121">These functions are presently supported, but might not be supported in a future release.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="746de-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="746de-122">See also</span></span>



[<span data-ttu-id="746de-123">Vue d'ensemble de la propri�t� MAPI</span><span class="sxs-lookup"><span data-stu-id="746de-123">MAPI Property Overview</span></span>](mapi-property-overview.md)

