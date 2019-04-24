---
title: À propos de l’API de conversion MAPI-MIME
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: ffdfdff8-985d-35de-73b1-c34e1932cb9f
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 7123b2deaa9ae0f26002b486df229ad589009f53
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321818"
---
# <a name="about-the-mapi-mime-conversion-api"></a><span data-ttu-id="22d0c-103">À propos de l’API de conversion MAPI-MIME</span><span class="sxs-lookup"><span data-stu-id="22d0c-103">About the MAPI-MIME Conversion API</span></span>

  
  
<span data-ttu-id="22d0c-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="22d0c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="22d0c-105">L'API de conversion MAPI-MIME permet aux fournisseurs de courrier de convertir les objets MIME et les messages MAPI.</span><span class="sxs-lookup"><span data-stu-id="22d0c-105">The MAPI-MIME Conversion API allows mail providers to convert between MIME objects and MAPI messages.</span></span> <span data-ttu-id="22d0c-106">Elle fournit des définitions, des identificateurs de classe et des identificateurs d'interface constants, comme indiqué dans les [constantes MAPI](mapi-constants.md).</span><span class="sxs-lookup"><span data-stu-id="22d0c-106">It provides constant definitions, class identifiers, and interface identifiers as shown in [MAPI Constants](mapi-constants.md).</span></span> <span data-ttu-id="22d0c-107">Les fournisseurs de messagerie doivent créer une instance de **[IConverterSession](iconvertersessioniunknown.md)** en appelant la fonction **CoCreateInstance** .</span><span class="sxs-lookup"><span data-stu-id="22d0c-107">Mail providers must cocreate an instance of **[IConverterSession](iconvertersessioniunknown.md)** by calling the **CoCreateInstance** function.</span></span> 
  

