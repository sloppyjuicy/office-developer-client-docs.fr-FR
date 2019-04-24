---
title: Ouverture des pièces jointes OLE avec IStreamDocfile
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f91df63c-ff6d-4c63-a665-5bcfdabe7e0e
description: 'Dernière modification: juillet 06, 2012'
ms.openlocfilehash: 2de13be34e8d81f88bfba872dda6e5534eb431bd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326228"
---
# <a name="opening-ole-attachments-with-istreamdocfile"></a>Ouverture des pièces jointes OLE avec IStreamDocfile

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Lors de l'ouverture d'une pièce jointe OLE, utilisez l'interface **IStreamDocfile** au lieu de [IStream](https://msdn.microsoft.com/library/windows/desktop/aa380034%28v=vs.85%29.aspx) ou [IStorage](https://msdn.microsoft.com/library/windows/desktop/aa380015%28v=vs.85%29.aspx). 

**IStreamDocfile** fournit un accès direct à l'objet à l'aide du stockage structuré, éliminant la nécessité d'effectuer une opération de copie et de réduire la charge. **IStreamDocfile** est une implémentation spécifique d' **IStream** avec le contenu du flux garanti être formaté en tant que stockage structuré. **IStreamDocfile** est implémenté par les fournisseurs de banque de messages. 
  

