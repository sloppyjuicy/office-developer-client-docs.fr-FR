---
title: Identificateurs d’entrée à court terme
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 948e007a-ad68-4abd-9720-204c6584beb5
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 03352b55589138d406ad3e4ee0756fc44bca8c78
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22580613"
---
# <a name="short-term-entry-identifiers"></a><span data-ttu-id="65510-103">Identificateurs d’entrée à court terme</span><span class="sxs-lookup"><span data-stu-id="65510-103">Short-term entry identifiers</span></span>

<span data-ttu-id="65510-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="65510-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="65510-105">Un identificateur d’entrée à court terme est affecté par un fournisseur de services à un objet lorsque l’identificateur doit être construit rapidement et ne doit pas au dernier sur heure ou à distance.</span><span class="sxs-lookup"><span data-stu-id="65510-105">A short-term entry identifier is assigned by a service provider to an object when the identifier must be constructed quickly and does not need to last over time or distance.</span></span> <span data-ttu-id="65510-106">Le caractère unique d’un identificateur d’entrée à court terme est garanti uniquement pendant la durée de la session en cours sur la station de travail en cours.</span><span class="sxs-lookup"><span data-stu-id="65510-106">The uniqueness of a short-term entry identifier is guaranteed only over the life of the current session on the current workstation.</span></span> <span data-ttu-id="65510-107">En règle générale, un identificateur d’entrée à court terme est valide uniquement jusqu'à ce que l’objet qu’il représente.</span><span class="sxs-lookup"><span data-stu-id="65510-107">Typically, a short-term entry identifier is valid only until the object that it represents is released.</span></span> 
  
<span data-ttu-id="65510-108">Identificateurs d’entrée à court terme sont affectés aux lignes dans les tableaux et aux entrées de boîtes de dialogue, où il est nécessaire de fournir rapidement des données pour la navigation.</span><span class="sxs-lookup"><span data-stu-id="65510-108">Short-term entry identifiers are assigned to rows in tables and to entries in dialog boxes, where it is necessary to provide data quickly for browsing.</span></span> <span data-ttu-id="65510-109">Par exemple, les fournisseurs de magasins de message affecter à court terme identificateurs d’entrée aux lignes des messages dans une table des matières et aux destinataires dans un tableau de destinataires.</span><span class="sxs-lookup"><span data-stu-id="65510-109">For example, message store providers assign short-term entry identifiers to rows of messages in a contents table and to recipients in a recipients table.</span></span> 

<span data-ttu-id="65510-110">Clients peuvent utiliser ces identificateurs d’entrée à court terme pour ouvrir les objets représentés par les lignes de tableau.</span><span class="sxs-lookup"><span data-stu-id="65510-110">Clients can use these short-term entry identifiers to open the objects represented by the table rows.</span></span> <span data-ttu-id="65510-111">Toutefois, contrairement aux identificateurs d’entrée à long terme qui peuvent être utilisés avec l’une des méthodes **OpenEntry** , identificateurs d’entrée à court terme doivent être utilisés avec la méthode de **OpenEntry** du conteneur.</span><span class="sxs-lookup"><span data-stu-id="65510-111">However, unlike long-term entry identifiers that can be used with any of the **OpenEntry** methods, short-term entry identifiers should be used with the container's **OpenEntry** method.</span></span> 
  
## <a name="implementing-short-term-entry-identifiers"></a><span data-ttu-id="65510-112">L’implémentation d’identificateurs d’entrée à court terme</span><span class="sxs-lookup"><span data-stu-id="65510-112">Implementing short-term entry identifiers</span></span>

<span data-ttu-id="65510-113">Les méthodes les plus courantes pour implémenter les identificateurs d’entrée à court terme sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="65510-113">The most common ways to implement short-term entry identifiers include the following:</span></span>
  
- <span data-ttu-id="65510-114">Fabrication les identificateurs d’entrée à court terme comme les identificateurs à long terme, en laissant tous les indicateurs non définie.</span><span class="sxs-lookup"><span data-stu-id="65510-114">Making the short-term entry identifiers the same as the long-term identifiers, leaving all of the flags unset.</span></span> 
    
- <span data-ttu-id="65510-115">Rendre les identificateurs d’entrée à court terme diffère les identificateurs à long terme, la définition de tous les indicateurs.</span><span class="sxs-lookup"><span data-stu-id="65510-115">Making the short-term entry identifiers different from the long-term identifiers, setting all of the flags.</span></span> 
    
<span data-ttu-id="65510-116">Les clients peuvent identifier un identificateur d’entrée à court terme du second type en examinant son membre **abFlags** comme suit :</span><span class="sxs-lookup"><span data-stu-id="65510-116">Clients can identify a short-term entry identifier of the second type by examining its **abFlags** member as follows:</span></span> 
  
```cpp
abFlags[0] = 0xFF;
 
```

<span data-ttu-id="65510-117">Certains fournisseurs de services désactivez un ou plusieurs indicateurs pour créer des identificateurs d’entrée à court terme dont la validité supérieure.</span><span class="sxs-lookup"><span data-stu-id="65510-117">Some service providers clear one or more flags to create short-term entry identifiers that have greater validity.</span></span> <span data-ttu-id="65510-118">Par exemple, les membres **abFlags** suivants représentent les identificateurs d’entrée à court terme qui peuvent être utilisés pour plusieurs jours ou plusieurs sessions :</span><span class="sxs-lookup"><span data-stu-id="65510-118">For example, the following **abFlags** members represent short-term entry identifiers that can be used for multiple days or for multiple sessions:</span></span> 
  
```cpp
abFlags[0] = 0xFF & ~MAPI_NOW;
abFlags[0] = 0xFF & ~MAPI_THISSESSION;
 
```

<span data-ttu-id="65510-119">Clients rapidement acquièrent, utilisent et ignorer les identificateurs d’entrée à court terme.</span><span class="sxs-lookup"><span data-stu-id="65510-119">Clients quickly acquire, use, and discard short-term entry identifiers.</span></span> <span data-ttu-id="65510-120">Pour l’essentiel, ils peuvent être utilisés dans la même manière que les identificateurs d’entrée à long terme.</span><span class="sxs-lookup"><span data-stu-id="65510-120">For the most part, they can be used in the same manner as long-term entry identifiers.</span></span> <span data-ttu-id="65510-121">Il peuvent être récupérés à partir d’une table, transmises à la méthode **OpenEntry** , par rapport à la méthode **CompareEntryIDs** .</span><span class="sxs-lookup"><span data-stu-id="65510-121">They can be retrieved from a table, passed to the **OpenEntry** method, and compared with the **CompareEntryIDs** method.</span></span> <span data-ttu-id="65510-122">La seule exception est qu’ils ne sont jamais retournés par la méthode [IMAPIProp::GetProps](imapiprop-getprops.md) .</span><span class="sxs-lookup"><span data-stu-id="65510-122">The one exception is that they are never returned from the [IMAPIProp::GetProps](imapiprop-getprops.md) method.</span></span> <span data-ttu-id="65510-123">Les propriétés renvoyées à partir de **GetProps** sont toujours des identificateurs d’entrée à long terme.</span><span class="sxs-lookup"><span data-stu-id="65510-123">The properties returned from **GetProps** are always long-term entry identifiers.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="65510-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="65510-124">See also</span></span>

- [<span data-ttu-id="65510-125">Identificateurs d’entrée MAPI</span><span class="sxs-lookup"><span data-stu-id="65510-125">MAPI Entry Identifiers</span></span>](mapi-entry-identifiers.md)

