---
title: L’initialisation d’OLE pour MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 53b65299-69f8-4fc0-8d9b-f666e814aaac
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 6efe41c79cd85eb844ee19b8c54e200956c9b2a3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784303"
---
# <a name="initializing-ole-for-mapi"></a><span data-ttu-id="696d8-103">L’initialisation d’OLE pour MAPI</span><span class="sxs-lookup"><span data-stu-id="696d8-103">Initializing OLE for MAPI</span></span>

  
  
<span data-ttu-id="696d8-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="696d8-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="696d8-105">Si vous utilisez également OLE, appelez la fonction OLE [OleInitialize](http://msdn.microsoft.com/fr-fr/library/ms690134%28v=VS.85%29.aspx) pour initialiser les bibliothèques OLE.</span><span class="sxs-lookup"><span data-stu-id="696d8-105">If you also use OLE, call the OLE function [OleInitialize](http://msdn.microsoft.com/fr-fr/library/ms690134%28v=VS.85%29.aspx) to initialize the OLE libraries.</span></span> <span data-ttu-id="696d8-106">**OleInitialize** initialise les données globales pour la session et prépare les bibliothèques OLE d’accepter les appels.</span><span class="sxs-lookup"><span data-stu-id="696d8-106">**OleInitialize** initializes global data for the session and prepares the OLE libraries to accept calls.</span></span> <span data-ttu-id="696d8-107">Pour plus d’informations sur l' appelant **OleInitialize**, voir le Kit de développement Windows.</span><span class="sxs-lookup"><span data-stu-id="696d8-107">For information about calling **OleInitialize**, see the Windows SDK.</span></span>
  

