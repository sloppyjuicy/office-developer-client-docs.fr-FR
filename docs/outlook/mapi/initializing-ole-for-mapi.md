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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25388414"
---
# <a name="initializing-ole-for-mapi"></a>Initialisation d’OLE pour MAPI

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Si vous utilisez également OLE, appelez la fonction OLE [OleInitialize](https://msdn.microsoft.com/library/ms690134%28v=VS.85%29.aspx) pour initialiser les bibliothèques OLE. **OleInitialize** initialise les données globales pour la session et prépare les bibliothèques OLE d’accepter les appels. Pour plus d’informations sur l' appelant **OleInitialize**, voir le Kit de développement Windows.
  

