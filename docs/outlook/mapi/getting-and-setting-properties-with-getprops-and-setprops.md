---
title: Obtention et définition de propriétés avec GetProps et SetProps
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 309d2b3d-dc71-4222-b293-4bfc467b5429
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 7d11f69c6da8560f5879ebc38498d852486bed8b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32299397"
---
# <a name="getting-and-setting-properties-with-getprops-and-setprops"></a><span data-ttu-id="9af7b-103">Obtention et définition de propriétés avec GetProps et SetProps</span><span class="sxs-lookup"><span data-stu-id="9af7b-103">Getting and setting properties with GetProps and SetProps</span></span>
 
<span data-ttu-id="9af7b-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9af7b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9af7b-105">Dans la mesure du possible, essayez de récupérer ou de modifier une propriété avec les méthodes [IMAPIProp::GetProps](imapiprop-getprops.md) et [IMAPIProp::SetProps.](imapiprop-setprops.md)</span><span class="sxs-lookup"><span data-stu-id="9af7b-105">Whenever possible, try to retrieve or modify a property with the [IMAPIProp::GetProps](imapiprop-getprops.md) and [IMAPIProp::SetProps](imapiprop-setprops.md) methods.</span></span> <span data-ttu-id="9af7b-106">À moins que la propriété que vous travaillez avec soit très grande, ces méthodes doivent être adéquates.</span><span class="sxs-lookup"><span data-stu-id="9af7b-106">Unless the property you are working with is very large, these methods should be adequate.</span></span> <span data-ttu-id="9af7b-107">L’autre solution consiste à lire ou à écrire dans un flux avec l’interface [IStream.](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9af7b-107">The other alternative is to read from or write to a stream with the [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) interface.</span></span> <span data-ttu-id="9af7b-108">Les flux peuvent gérer des propriétés très importantes, mais ils drainent davantage les ressources, car ils nécessitent les bibliothèques COM.</span><span class="sxs-lookup"><span data-stu-id="9af7b-108">Streams can handle very large properties successfully, but they are a greater drain on resources because they require the COM libraries.</span></span> <span data-ttu-id="9af7b-109">Utilisez l’interface **IStream** uniquement après l’échec de votre appel à **IMAPIProp::GetProps** ou **IMAPIProp::SetProps.**</span><span class="sxs-lookup"><span data-stu-id="9af7b-109">Use the **IStream** interface only after your call to **IMAPIProp::GetProps** or **IMAPIProp::SetProps** fails.</span></span> 
  

