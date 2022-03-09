---
title: Initialisation d’OLE pour MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 53b65299-69f8-4fc0-8d9b-f666e814aaac
ms.openlocfilehash: 79ec96a024c76a10853fa1180d76c1f0bd650f11
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63369888"
---
# <a name="initializing-ole-for-mapi"></a>Initialisation d’OLE pour MAPI

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Si vous utilisez également OLE, appelez la fonction OLE [OleInitialize](https://msdn.microsoft.com/library/ms690134%28v=VS.85%29.aspx) pour initialiser les bibliothèques OLE. **OleInitialize** initialise les données globales de la session et prépare les bibliothèques OLE à accepter les appels. Pour plus d’informations **sur l’appel de OleInitialize**, voir Windows SDK.
  

