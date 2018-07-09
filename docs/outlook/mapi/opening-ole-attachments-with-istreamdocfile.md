---
title: Ouverture des pièces jointes OLE avec IStreamDocfile
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f91df63c-ff6d-4c63-a665-5bcfdabe7e0e
description: 'Dernière modification : 06 juillet 2012'
ms.openlocfilehash: 33e5b9e0112f562b192400498764a10682d006a6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784948"
---
# <a name="opening-ole-attachments-with-istreamdocfile"></a><span data-ttu-id="53e2a-103">Ouverture des pièces jointes OLE avec IStreamDocfile</span><span class="sxs-lookup"><span data-stu-id="53e2a-103">Opening OLE attachments with IStreamDocfile</span></span>

<span data-ttu-id="53e2a-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="53e2a-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="53e2a-105">Lorsque vous ouvrez la pièce jointe d’objet OLE, utilisez l’interface **IStreamDocfile** plutôt que de [IStream](http://msdn.microsoft.com/fr-fr/library/windows/desktop/aa380034%28v=vs.85%29.aspx) ou de [IStorage](http://msdn.microsoft.com/fr-fr/library/windows/desktop/aa380015%28v=vs.85%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="53e2a-105">When opening an OLE object attachment, use the **IStreamDocfile** interface rather than [IStream](http://msdn.microsoft.com/fr-fr/library/windows/desktop/aa380034%28v=vs.85%29.aspx) or [IStorage](http://msdn.microsoft.com/fr-fr/library/windows/desktop/aa380015%28v=vs.85%29.aspx).</span></span> 

<span data-ttu-id="53e2a-106">**IStreamDocfile** fournit un accès direct à l’objet à l’aide de stockage structuré, évite de devoir effectuer une opération de copie et réduit la surcharge.</span><span class="sxs-lookup"><span data-stu-id="53e2a-106">**IStreamDocfile** provides direct access to the object using structured storage, eliminating the need to perform a copy operation and reducing overhead.</span></span> <span data-ttu-id="53e2a-107">**IStreamDocfile** est une implémentation de **IStream** avec le contenu de l’objet stream garanti à mettre en forme en tant que stockage structuré.</span><span class="sxs-lookup"><span data-stu-id="53e2a-107">**IStreamDocfile** is a specific implementation of **IStream** with the content of the stream guaranteed to be formatted as structured storage.</span></span> <span data-ttu-id="53e2a-108">**IStreamDocfile** est implémentée par les fournisseurs de banque de messages.</span><span class="sxs-lookup"><span data-stu-id="53e2a-108">**IStreamDocfile** is implemented by message store providers.</span></span> 
  

