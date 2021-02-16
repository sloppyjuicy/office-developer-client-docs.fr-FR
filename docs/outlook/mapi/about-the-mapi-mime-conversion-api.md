---
title: À propos de l’API de conversion MAPI-MIME
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: ffdfdff8-985d-35de-73b1-c34e1932cb9f
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 7123b2deaa9ae0f26002b486df229ad589009f53
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420436"
---
# <a name="about-the-mapi-mime-conversion-api"></a><span data-ttu-id="31e5a-103">À propos de l’API de conversion MAPI-MIME</span><span class="sxs-lookup"><span data-stu-id="31e5a-103">About the MAPI-MIME Conversion API</span></span>

  
  
<span data-ttu-id="31e5a-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="31e5a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="31e5a-105">L’API de conversion MAPI-MIME permet aux fournisseurs de messagerie de convertir entre des objets MIME et des messages MAPI.</span><span class="sxs-lookup"><span data-stu-id="31e5a-105">The MAPI-MIME Conversion API allows mail providers to convert between MIME objects and MAPI messages.</span></span> <span data-ttu-id="31e5a-106">Il fournit des définitions de constantes, des identificateurs de classe et des identificateurs d’interface, comme indiqué dans les [constantes MAPI.](mapi-constants.md)</span><span class="sxs-lookup"><span data-stu-id="31e5a-106">It provides constant definitions, class identifiers, and interface identifiers as shown in [MAPI Constants](mapi-constants.md).</span></span> <span data-ttu-id="31e5a-107">Les fournisseurs de messagerie doivent cocréer une instance **[d’IConverterSession](iconvertersessioniunknown.md)** en appelant la fonction **CoCreateInstance.**</span><span class="sxs-lookup"><span data-stu-id="31e5a-107">Mail providers must cocreate an instance of **[IConverterSession](iconvertersessioniunknown.md)** by calling the **CoCreateInstance** function.</span></span> 
  

