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
ms.openlocfilehash: 1b361e025b631418eb63c5c74da264beadec2974
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439561"
---
# <a name="short-term-entry-identifiers"></a><span data-ttu-id="50684-103">Identificateurs d’entrée à court terme</span><span class="sxs-lookup"><span data-stu-id="50684-103">Short-term entry identifiers</span></span>

<span data-ttu-id="50684-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="50684-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="50684-105">Un identificateur d'entrée à court terme est affecté par un fournisseur de services à un objet lorsque ce dernier doit être construit rapidement et n'a pas besoin de la dernière fois ou de la distance.</span><span class="sxs-lookup"><span data-stu-id="50684-105">A short-term entry identifier is assigned by a service provider to an object when the identifier must be constructed quickly and does not need to last over time or distance.</span></span> <span data-ttu-id="50684-106">L'unicité d'un identificateur d'entrée à court terme n'est garantie que pendant la durée de vie de la session en cours sur le poste de travail actuel.</span><span class="sxs-lookup"><span data-stu-id="50684-106">The uniqueness of a short-term entry identifier is guaranteed only over the life of the current session on the current workstation.</span></span> <span data-ttu-id="50684-107">En règle générale, un identificateur d'entrée à court terme est valide uniquement jusqu'à ce que l'objet qu'elle représente soit libéré.</span><span class="sxs-lookup"><span data-stu-id="50684-107">Typically, a short-term entry identifier is valid only until the object that it represents is released.</span></span> 
  
<span data-ttu-id="50684-108">Les identificateurs d'entrée à court terme sont affectés aux lignes des tableaux et aux entrées dans les boîtes de dialogue, où il est nécessaire de fournir des données rapides pour la navigation.</span><span class="sxs-lookup"><span data-stu-id="50684-108">Short-term entry identifiers are assigned to rows in tables and to entries in dialog boxes, where it is necessary to provide data quickly for browsing.</span></span> <span data-ttu-id="50684-109">Par exemple, les fournisseurs de banque de messages affectent des identificateurs d'entrée à court terme à des lignes de messages dans une table de contenu et à des destinataires dans une table de destinataires.</span><span class="sxs-lookup"><span data-stu-id="50684-109">For example, message store providers assign short-term entry identifiers to rows of messages in a contents table and to recipients in a recipients table.</span></span> 

<span data-ttu-id="50684-110">Les clients peuvent utiliser ces identificateurs d'entrée à court terme pour ouvrir les objets représentés par les lignes du tableau.</span><span class="sxs-lookup"><span data-stu-id="50684-110">Clients can use these short-term entry identifiers to open the objects represented by the table rows.</span></span> <span data-ttu-id="50684-111">Toutefois, à la différence des identificateurs d'entrée à long terme pouvant être utilisés avec l'une des méthodes **OpenEntry** , les identificateurs d'entrée à court terme doivent être utilisés avec la méthode **OpenEntry** du conteneur.</span><span class="sxs-lookup"><span data-stu-id="50684-111">However, unlike long-term entry identifiers that can be used with any of the **OpenEntry** methods, short-term entry identifiers should be used with the container's **OpenEntry** method.</span></span> 
  
## <a name="implementing-short-term-entry-identifiers"></a><span data-ttu-id="50684-112">Implémentation d'identificateurs d'entrée à court terme</span><span class="sxs-lookup"><span data-stu-id="50684-112">Implementing short-term entry identifiers</span></span>

<span data-ttu-id="50684-113">Les méthodes les plus courantes pour implémenter des identificateurs d'entrée à court terme sont les suivantes:</span><span class="sxs-lookup"><span data-stu-id="50684-113">The most common ways to implement short-term entry identifiers include the following:</span></span>
  
- <span data-ttu-id="50684-114">Rendre les identificateurs d'entrée à court terme identiques aux identificateurs à long terme, en laissant tous les indicateurs non définis.</span><span class="sxs-lookup"><span data-stu-id="50684-114">Making the short-term entry identifiers the same as the long-term identifiers, leaving all of the flags unset.</span></span> 
    
- <span data-ttu-id="50684-115">Définition des identificateurs d'entrée à court terme différemment des identificateurs à long terme, définition de tous les indicateurs.</span><span class="sxs-lookup"><span data-stu-id="50684-115">Making the short-term entry identifiers different from the long-term identifiers, setting all of the flags.</span></span> 
    
<span data-ttu-id="50684-116">Les clients peuvent identifier un identificateur d'entrée à court terme du deuxième type en examinant son membre **abFlags** comme suit:</span><span class="sxs-lookup"><span data-stu-id="50684-116">Clients can identify a short-term entry identifier of the second type by examining its **abFlags** member as follows:</span></span> 
  
```cpp
abFlags[0] = 0xFF;
 
```

<span data-ttu-id="50684-117">Certains fournisseurs de services effacent un ou plusieurs indicateurs pour créer des identificateurs d'entrée à court terme qui ont une plus grande validité.</span><span class="sxs-lookup"><span data-stu-id="50684-117">Some service providers clear one or more flags to create short-term entry identifiers that have greater validity.</span></span> <span data-ttu-id="50684-118">Par exemple, les membres **abFlags** suivants représentent des identificateurs d'entrée à court terme pouvant être utilisés pour plusieurs jours ou plusieurs sessions:</span><span class="sxs-lookup"><span data-stu-id="50684-118">For example, the following **abFlags** members represent short-term entry identifiers that can be used for multiple days or for multiple sessions:</span></span> 
  
```cpp
abFlags[0] = 0xFF & ~MAPI_NOW;
abFlags[0] = 0xFF & ~MAPI_THISSESSION;
 
```

<span data-ttu-id="50684-119">Les clients acquièrent, utilisent et éliminent rapidement les identificateurs d'entrée à court terme.</span><span class="sxs-lookup"><span data-stu-id="50684-119">Clients quickly acquire, use, and discard short-term entry identifiers.</span></span> <span data-ttu-id="50684-120">La plupart du temps, ils peuvent être utilisés de la même manière que les identificateurs d'entrée à long terme.</span><span class="sxs-lookup"><span data-stu-id="50684-120">For the most part, they can be used in the same manner as long-term entry identifiers.</span></span> <span data-ttu-id="50684-121">Elles peuvent être récupérées à partir d'une table, transmises à la méthode **OpenEntry** et comparées à la méthode **CompareEntryIDs** .</span><span class="sxs-lookup"><span data-stu-id="50684-121">They can be retrieved from a table, passed to the **OpenEntry** method, and compared with the **CompareEntryIDs** method.</span></span> <span data-ttu-id="50684-122">La seule exception est qu'ils ne sont jamais renvoyés à partir de la méthode [IMAPIProp:: GetProps](imapiprop-getprops.md) .</span><span class="sxs-lookup"><span data-stu-id="50684-122">The one exception is that they are never returned from the [IMAPIProp::GetProps](imapiprop-getprops.md) method.</span></span> <span data-ttu-id="50684-123">Les propriétés renvoyées par **GetProps** sont toujours des identificateurs d'entrée à long terme.</span><span class="sxs-lookup"><span data-stu-id="50684-123">The properties returned from **GetProps** are always long-term entry identifiers.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="50684-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="50684-124">See also</span></span>

- [<span data-ttu-id="50684-125">Identificateurs d'entrée MAPI</span><span class="sxs-lookup"><span data-stu-id="50684-125">MAPI Entry Identifiers</span></span>](mapi-entry-identifiers.md)

