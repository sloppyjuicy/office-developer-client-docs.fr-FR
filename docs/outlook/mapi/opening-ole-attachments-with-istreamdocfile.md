---
title: Ouverture des pièces jointes OLE avec IStreamDocfile
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f91df63c-ff6d-4c63-a665-5bcfdabe7e0e
description: 'Last modified: July 06, 2012'
ms.openlocfilehash: 2de13be34e8d81f88bfba872dda6e5534eb431bd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326228"
---
# <a name="opening-ole-attachments-with-istreamdocfile"></a>Ouverture des pièces jointes OLE avec IStreamDocfile

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Lors de l’ouverture d’une pièce jointe d’objet OLE, utilisez l’interface **IStreamDocfile** plutôt que [IStream](https://msdn.microsoft.com/library/windows/desktop/aa380034%28v=vs.85%29.aspx) ou [IStorage](https://msdn.microsoft.com/library/windows/desktop/aa380015%28v=vs.85%29.aspx). 

**IStreamDocfile** fournit un accès direct à l’objet à l’aide d’un stockage structuré, ce qui élimine la nécessité d’effectuer une opération de copie et réduit la surcharge. **IStreamDocfile est** une implémentation spécifique **d’IStream** avec le contenu du flux dont la mise en forme est garantie en tant que stockage structuré. **IStreamDocfile est** implémenté par les fournisseurs de magasins de messages. 
  

