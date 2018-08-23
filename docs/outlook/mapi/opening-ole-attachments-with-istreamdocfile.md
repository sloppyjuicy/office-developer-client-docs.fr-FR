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
ms.openlocfilehash: 1e11d9f663384f00e7fd867802ef63afe1dd7e9e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592737"
---
# <a name="opening-ole-attachments-with-istreamdocfile"></a>Ouverture des pièces jointes OLE avec IStreamDocfile

**S’applique à**: Outlook 2013 | Outlook 2016 
  
Lorsque vous ouvrez la pièce jointe d’objet OLE, utilisez l’interface **IStreamDocfile** plutôt que de [IStream](http://msdn.microsoft.com/en-us/library/windows/desktop/aa380034%28v=vs.85%29.aspx) ou de [IStorage](http://msdn.microsoft.com/en-us/library/windows/desktop/aa380015%28v=vs.85%29.aspx). 

**IStreamDocfile** fournit un accès direct à l’objet à l’aide de stockage structuré, évite de devoir effectuer une opération de copie et réduit la surcharge. **IStreamDocfile** est une implémentation de **IStream** avec le contenu de l’objet stream garanti à mettre en forme en tant que stockage structuré. **IStreamDocfile** est implémentée par les fournisseurs de banque de messages. 
  

