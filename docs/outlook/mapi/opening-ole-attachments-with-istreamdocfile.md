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
ms.openlocfilehash: 2de13be34e8d81f88bfba872dda6e5534eb431bd
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25386550"
---
# <a name="opening-ole-attachments-with-istreamdocfile"></a><span data-ttu-id="f4e70-103">Ouverture des pièces jointes OLE avec IStreamDocfile</span><span class="sxs-lookup"><span data-stu-id="f4e70-103">Opening OLE attachments with IStreamDocfile</span></span>

<span data-ttu-id="f4e70-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f4e70-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f4e70-105">Lorsque vous ouvrez la pièce jointe d’objet OLE, utilisez l’interface **IStreamDocfile** plutôt que de [IStream](https://msdn.microsoft.com/library/windows/desktop/aa380034%28v=vs.85%29.aspx) ou de [IStorage](https://msdn.microsoft.com/library/windows/desktop/aa380015%28v=vs.85%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="f4e70-105">When opening an OLE object attachment, use the **IStreamDocfile** interface rather than [IStream](https://msdn.microsoft.com/library/windows/desktop/aa380034%28v=vs.85%29.aspx) or [IStorage](https://msdn.microsoft.com/library/windows/desktop/aa380015%28v=vs.85%29.aspx).</span></span> 

<span data-ttu-id="f4e70-106">**IStreamDocfile** fournit un accès direct à l’objet à l’aide de stockage structuré, évite de devoir effectuer une opération de copie et réduit la surcharge.</span><span class="sxs-lookup"><span data-stu-id="f4e70-106">**IStreamDocfile** provides direct access to the object using structured storage, eliminating the need to perform a copy operation and reducing overhead.</span></span> <span data-ttu-id="f4e70-107">**IStreamDocfile** est une implémentation de **IStream** avec le contenu de l’objet stream garanti à mettre en forme en tant que stockage structuré.</span><span class="sxs-lookup"><span data-stu-id="f4e70-107">**IStreamDocfile** is a specific implementation of **IStream** with the content of the stream guaranteed to be formatted as structured storage.</span></span> <span data-ttu-id="f4e70-108">**IStreamDocfile** est implémentée par les fournisseurs de banque de messages.</span><span class="sxs-lookup"><span data-stu-id="f4e70-108">**IStreamDocfile** is implemented by message store providers.</span></span> 
  

