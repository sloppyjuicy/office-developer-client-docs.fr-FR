---
title: Ouverture des pièces jointes OLE avec IStreamDocfile
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f91df63c-ff6d-4c63-a665-5bcfdabe7e0e
description: 'Dernière modification : 06 juillet 2012'
ms.openlocfilehash: 2de13be34e8d81f88bfba872dda6e5534eb431bd
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25386550"
---
# <a name="opening-ole-attachments-with-istreamdocfile"></a>Ouverture des pièces jointes OLE avec IStreamDocfile

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Lorsque vous ouvrez la pièce jointe d’objet OLE, utilisez l’interface **IStreamDocfile** plutôt que de [IStream](https://msdn.microsoft.com/library/windows/desktop/aa380034%28v=vs.85%29.aspx) ou de [IStorage](https://msdn.microsoft.com/library/windows/desktop/aa380015%28v=vs.85%29.aspx). 

**IStreamDocfile** fournit un accès direct à l’objet à l’aide de stockage structuré, évite de devoir effectuer une opération de copie et réduit la surcharge. **IStreamDocfile** est une implémentation de **IStream** avec le contenu de l’objet stream garanti à mettre en forme en tant que stockage structuré. **IStreamDocfile** est implémentée par les fournisseurs de banque de messages. 
  

