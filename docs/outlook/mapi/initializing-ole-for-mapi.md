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
# <a name="initializing-ole-for-mapi"></a>L’initialisation d’OLE pour MAPI

  
  
**S’applique à**: Outlook 
  
Si vous utilisez également OLE, appelez la fonction OLE [OleInitialize](http://msdn.microsoft.com/en-us/library/ms690134%28v=VS.85%29.aspx) pour initialiser les bibliothèques OLE. **OleInitialize** initialise les données globales pour la session et prépare les bibliothèques OLE d’accepter les appels. Pour plus d’informations sur l' appelant **OleInitialize**, voir le Kit de développement Windows.
  

