---
title: Ouverture des pièces jointes OLE avec IStreamDocfile
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: f91df63c-ff6d-4c63-a665-5bcfdabe7e0e
description: 'Last modified: July 06, 2012'
ms.openlocfilehash: 923d3945d31cf15ccc0262c2628e2b38489054fe
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59625132"
---
# <a name="opening-ole-attachments-with-istreamdocfile"></a>Ouverture des pièces jointes OLE avec IStreamDocfile

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Lors de l’ouverture d’une pièce jointe d’objet OLE, utilisez l’interface **IStreamDocfile** plutôt que [IStream](https://msdn.microsoft.com/library/windows/desktop/aa380034%28v=vs.85%29.aspx) ou [IStorage](https://msdn.microsoft.com/library/windows/desktop/aa380015%28v=vs.85%29.aspx). 

**IStreamDocfile** fournit un accès direct à l’objet à l’aide d’un stockage structuré, ce qui élimine la nécessité d’effectuer une opération de copie et réduit la surcharge. **IStreamDocfile est** une implémentation spécifique **d’IStream** avec le contenu du flux dont la mise en forme est garantie en tant que stockage structuré. **IStreamDocfile est** implémenté par les fournisseurs de magasins de messages. 
  

