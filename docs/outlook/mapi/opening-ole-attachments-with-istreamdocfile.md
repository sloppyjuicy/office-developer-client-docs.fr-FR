---
title: Ouverture des pièces jointes OLE avec IStreamDocfile
description: IStreamDocfile fournit un accès direct à l’objet à l’aide d’un stockage structuré, ce qui élimine la nécessité d’effectuer une opération de copie et réduit la surcharge.
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: f91df63c-ff6d-4c63-a665-5bcfdabe7e0e
ms.openlocfilehash: f6bfabee60d42dba6b532c7a5328b92145207ca8
ms.sourcegitcommit: 1b44c8f9eac3aedaf7fe7ec70c808fe8ed7d4b99
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/02/2022
ms.locfileid: "65852382"
---
# <a name="opening-ole-attachments-with-istreamdocfile"></a>Ouverture des pièces jointes OLE avec IStreamDocfile

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Lors de l’ouverture d’une pièce jointe d’objet OLE, utilisez l’interface **IStreamDocfile** plutôt que [IStream](https://msdn.microsoft.com/library/windows/desktop/aa380034%28v=vs.85%29.aspx) ou [IStorage](https://msdn.microsoft.com/library/windows/desktop/aa380015%28v=vs.85%29.aspx). 

**IStreamDocfile** fournit un accès direct à l’objet à l’aide d’un stockage structuré, ce qui élimine la nécessité d’effectuer une opération de copie et réduit la surcharge. **IStreamDocfile** est une implémentation spécifique **d’IStream** avec le contenu du flux garanti comme un stockage structuré. **IStreamDocfile** est implémenté par les fournisseurs de magasins de messages. 
  

