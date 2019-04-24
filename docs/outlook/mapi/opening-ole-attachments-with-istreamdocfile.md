---
title: Ouverture des pièces jointes OLE avec IStreamDocfile
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f91df63c-ff6d-4c63-a665-5bcfdabe7e0e
description: 'Dernière modification: juillet 06, 2012'
ms.openlocfilehash: 2de13be34e8d81f88bfba872dda6e5534eb431bd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326228"
---
# <a name="opening-ole-attachments-with-istreamdocfile"></a><span data-ttu-id="ac824-103">Ouverture des pièces jointes OLE avec IStreamDocfile</span><span class="sxs-lookup"><span data-stu-id="ac824-103">Opening OLE attachments with IStreamDocfile</span></span>

<span data-ttu-id="ac824-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ac824-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ac824-105">Lors de l'ouverture d'une pièce jointe OLE, utilisez l'interface **IStreamDocfile** au lieu de [IStream](https://msdn.microsoft.com/library/windows/desktop/aa380034%28v=vs.85%29.aspx) ou [IStorage](https://msdn.microsoft.com/library/windows/desktop/aa380015%28v=vs.85%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="ac824-105">When opening an OLE object attachment, use the **IStreamDocfile** interface rather than [IStream](https://msdn.microsoft.com/library/windows/desktop/aa380034%28v=vs.85%29.aspx) or [IStorage](https://msdn.microsoft.com/library/windows/desktop/aa380015%28v=vs.85%29.aspx).</span></span> 

<span data-ttu-id="ac824-106">**IStreamDocfile** fournit un accès direct à l'objet à l'aide du stockage structuré, éliminant la nécessité d'effectuer une opération de copie et de réduire la charge.</span><span class="sxs-lookup"><span data-stu-id="ac824-106">**IStreamDocfile** provides direct access to the object using structured storage, eliminating the need to perform a copy operation and reducing overhead.</span></span> <span data-ttu-id="ac824-107">**IStreamDocfile** est une implémentation spécifique d' **IStream** avec le contenu du flux garanti être formaté en tant que stockage structuré.</span><span class="sxs-lookup"><span data-stu-id="ac824-107">**IStreamDocfile** is a specific implementation of **IStream** with the content of the stream guaranteed to be formatted as structured storage.</span></span> <span data-ttu-id="ac824-108">**IStreamDocfile** est implémenté par les fournisseurs de banque de messages.</span><span class="sxs-lookup"><span data-stu-id="ac824-108">**IStreamDocfile** is implemented by message store providers.</span></span> 
  

