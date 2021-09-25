---
title: Initialisation d’OLE pour MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 53b65299-69f8-4fc0-8d9b-f666e814aaac
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 91552ba5a37915ad8a75bd49038e6e90585bd615
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59564098"
---
# <a name="initializing-ole-for-mapi"></a>Initialisation d’OLE pour MAPI

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Si vous utilisez également OLE, appelez la fonction [OLE OleInitialize](https://msdn.microsoft.com/library/ms690134%28v=VS.85%29.aspx) pour initialiser les bibliothèques OLE. **OleInitialize** initialise les données globales de la session et prépare les bibliothèques OLE à accepter les appels. Pour plus d’informations **sur l’appel de OleInitialize,** voir Windows SDK.
  

