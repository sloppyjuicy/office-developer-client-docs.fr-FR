---
title: Obtention et définition des propriétés avec GetProps et SetProps
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 309d2b3d-dc71-4222-b293-4bfc467b5429
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 7d11f69c6da8560f5879ebc38498d852486bed8b
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25395006"
---
# <a name="getting-and-setting-properties-with-getprops-and-setprops"></a><span data-ttu-id="4e294-103">Obtention et définition des propriétés avec GetProps et SetProps</span><span class="sxs-lookup"><span data-stu-id="4e294-103">Getting and setting properties with GetProps and SetProps</span></span>
 
<span data-ttu-id="4e294-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4e294-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4e294-105">La mesure du possible, essayez d’extraire ou de modifier une propriété avec les méthodes [IMAPIProp::GetProps](imapiprop-getprops.md) et [IMAPIProp::SetProps](imapiprop-setprops.md) .</span><span class="sxs-lookup"><span data-stu-id="4e294-105">Whenever possible, try to retrieve or modify a property with the [IMAPIProp::GetProps](imapiprop-getprops.md) and [IMAPIProp::SetProps](imapiprop-setprops.md) methods.</span></span> <span data-ttu-id="4e294-106">Sauf si la propriété que vous utilisez est très volumineuse, ces méthodes doivent être adéquates.</span><span class="sxs-lookup"><span data-stu-id="4e294-106">Unless the property you are working with is very large, these methods should be adequate.</span></span> <span data-ttu-id="4e294-107">L’autre solution consiste à lire ou écrire dans un stream à l’interface [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="4e294-107">The other alternative is to read from or write to a stream with the [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) interface.</span></span> <span data-ttu-id="4e294-108">Flux peuvent gérer des propriétés très volumineuses avec succès, mais ils sont une charge supérieure pour les ressources car ils ont besoin les bibliothèques COM.</span><span class="sxs-lookup"><span data-stu-id="4e294-108">Streams can handle very large properties successfully, but they are a greater drain on resources because they require the COM libraries.</span></span> <span data-ttu-id="4e294-109">Utiliser l’interface **IStream** uniquement après l’appel de **IMAPIProp::GetProps** ou **IMAPIProp::SetProps** échoue.</span><span class="sxs-lookup"><span data-stu-id="4e294-109">Use the **IStream** interface only after your call to **IMAPIProp::GetProps** or **IMAPIProp::SetProps** fails.</span></span> 
  

