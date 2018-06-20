---
title: À propos de l’API de Conversion MAPI MIME
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: ffdfdff8-985d-35de-73b1-c34e1932cb9f
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 43ce3ecea6b80bace2bcc2bd333b5c1839514f7d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782854"
---
# <a name="about-the-mapi-mime-conversion-api"></a><span data-ttu-id="d9bf5-103">À propos de l’API de Conversion MAPI MIME</span><span class="sxs-lookup"><span data-stu-id="d9bf5-103">About the MAPI-MIME Conversion API</span></span>

  
  
<span data-ttu-id="d9bf5-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="d9bf5-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="d9bf5-105">Les API de Conversion MAPI MIME permet à des fournisseurs de messagerie convertir les objets MIME et les messages MAPI.</span><span class="sxs-lookup"><span data-stu-id="d9bf5-105">The MAPI-MIME Conversion API allows mail providers to convert between MIME objects and MAPI messages.</span></span> <span data-ttu-id="d9bf5-106">Il fournit des définitions de constantes, les identificateurs de classe et les identificateurs d’interface comme indiqué dans [Une des constantes MAPI](mapi-constants.md).</span><span class="sxs-lookup"><span data-stu-id="d9bf5-106">It provides constant definitions, class identifiers, and interface identifiers as shown in [MAPI Constants](mapi-constants.md).</span></span> <span data-ttu-id="d9bf5-107">Fournisseurs de messagerie doivent co-créer une instance de **[IConverterSession](iconvertersessioniunknown.md)** en appelant la fonction **CoCreateInstance** .</span><span class="sxs-lookup"><span data-stu-id="d9bf5-107">Mail providers must cocreate an instance of **[IConverterSession](iconvertersessioniunknown.md)** by calling the **CoCreateInstance** function.</span></span> 
  

