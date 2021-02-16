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
# <a name="initializing-ole-for-mapi"></a>Initialisation d’OLE pour MAPI

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Si vous utilisez également OLE, appelez la fonction [OLE OleInitialize](https://msdn.microsoft.com/library/ms690134%28v=VS.85%29.aspx) pour initialiser les bibliothèques OLE. **OleInitialize** initialise les données globales de la session et prépare les bibliothèques OLE à accepter les appels. Pour plus d’informations **sur l’appel de OleInitialize,** voir le SDK Windows.
  

