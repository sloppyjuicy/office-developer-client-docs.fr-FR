---
title: À propos de l’API de conversion MAPI-MIME
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: ffdfdff8-985d-35de-73b1-c34e1932cb9f
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 23e68d18a6de93a99d2db32c1d93dac33d9a1225
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22575265"
---
# <a name="about-the-mapi-mime-conversion-api"></a><span data-ttu-id="bbe4b-103">À propos de l’API de conversion MAPI-MIME</span><span class="sxs-lookup"><span data-stu-id="bbe4b-103">About the MAPI-MIME Conversion API</span></span>

  
  
<span data-ttu-id="bbe4b-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bbe4b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bbe4b-105">Les API de Conversion MAPI MIME permet à des fournisseurs de messagerie convertir les objets MIME et les messages MAPI.</span><span class="sxs-lookup"><span data-stu-id="bbe4b-105">The MAPI-MIME Conversion API allows mail providers to convert between MIME objects and MAPI messages.</span></span> <span data-ttu-id="bbe4b-106">Il fournit des définitions de constantes, les identificateurs de classe et les identificateurs d’interface comme indiqué dans [Une des constantes MAPI](mapi-constants.md).</span><span class="sxs-lookup"><span data-stu-id="bbe4b-106">It provides constant definitions, class identifiers, and interface identifiers as shown in [MAPI Constants](mapi-constants.md).</span></span> <span data-ttu-id="bbe4b-107">Fournisseurs de messagerie doivent co-créer une instance de **[IConverterSession](iconvertersessioniunknown.md)** en appelant la fonction **CoCreateInstance** .</span><span class="sxs-lookup"><span data-stu-id="bbe4b-107">Mail providers must cocreate an instance of **[IConverterSession](iconvertersessioniunknown.md)** by calling the **CoCreateInstance** function.</span></span> 
  

