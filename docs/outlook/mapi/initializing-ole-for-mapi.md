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
ms.openlocfilehash: cd279c17574ce73b42d5e07e96ac817af71dc700
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589804"
---
# <a name="initializing-ole-for-mapi"></a><span data-ttu-id="bacea-103">Initialisation d’OLE pour MAPI</span><span class="sxs-lookup"><span data-stu-id="bacea-103">Initializing OLE for MAPI</span></span>

  
  
<span data-ttu-id="bacea-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bacea-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bacea-105">Si vous utilisez également OLE, appelez la fonction OLE [OleInitialize](http://msdn.microsoft.com/en-us/library/ms690134%28v=VS.85%29.aspx) pour initialiser les bibliothèques OLE.</span><span class="sxs-lookup"><span data-stu-id="bacea-105">If you also use OLE, call the OLE function [OleInitialize](http://msdn.microsoft.com/en-us/library/ms690134%28v=VS.85%29.aspx) to initialize the OLE libraries.</span></span> <span data-ttu-id="bacea-106">**OleInitialize** initialise les données globales pour la session et prépare les bibliothèques OLE d’accepter les appels.</span><span class="sxs-lookup"><span data-stu-id="bacea-106">**OleInitialize** initializes global data for the session and prepares the OLE libraries to accept calls.</span></span> <span data-ttu-id="bacea-107">Pour plus d’informations sur l' appelant **OleInitialize**, voir le Kit de développement Windows.</span><span class="sxs-lookup"><span data-stu-id="bacea-107">For information about calling **OleInitialize**, see the Windows SDK.</span></span>
  

