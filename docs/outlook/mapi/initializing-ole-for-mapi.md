---
title: Initialisation d’OLE pour MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 53b65299-69f8-4fc0-8d9b-f666e814aaac
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 87310916f4a54b308f0599ec5c1a4a3bfe83c376
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317226"
---
# <a name="initializing-ole-for-mapi"></a><span data-ttu-id="8a6c1-103">Initialisation d’OLE pour MAPI</span><span class="sxs-lookup"><span data-stu-id="8a6c1-103">Initializing OLE for MAPI</span></span>

  
  
<span data-ttu-id="8a6c1-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8a6c1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8a6c1-105">Si vous utilisez également OLE, appelez la fonction [OLE OleInitialize](https://msdn.microsoft.com/library/ms690134%28v=VS.85%29.aspx) pour initialiser les bibliothèques OLE.</span><span class="sxs-lookup"><span data-stu-id="8a6c1-105">If you also use OLE, call the OLE function [OleInitialize](https://msdn.microsoft.com/library/ms690134%28v=VS.85%29.aspx) to initialize the OLE libraries.</span></span> <span data-ttu-id="8a6c1-106">**OleInitialize** initialise les données globales de la session et prépare les bibliothèques OLE à accepter les appels.</span><span class="sxs-lookup"><span data-stu-id="8a6c1-106">**OleInitialize** initializes global data for the session and prepares the OLE libraries to accept calls.</span></span> <span data-ttu-id="8a6c1-107">Pour plus d’informations **sur l’appel de OleInitialize,** voir le SDK Windows.</span><span class="sxs-lookup"><span data-stu-id="8a6c1-107">For information about calling **OleInitialize**, see the Windows SDK.</span></span>
  

