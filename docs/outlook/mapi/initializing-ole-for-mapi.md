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
# <a name="initializing-ole-for-mapi"></a>Initialisation d’OLE pour MAPI

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Si vous utilisez également OLE, appelez la fonction OLE [OleInitialize](http://msdn.microsoft.com/en-us/library/ms690134%28v=VS.85%29.aspx) pour initialiser les bibliothèques OLE. **OleInitialize** initialise les données globales pour la session et prépare les bibliothèques OLE d’accepter les appels. Pour plus d’informations sur l' appelant **OleInitialize**, voir le Kit de développement Windows.
  

