---
title: Pi�ces jointes OLE
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: febb6a5e-7c40-4f21-806e-7f827d1c37cf
ms.openlocfilehash: 5c6cd04e6d5a459df9806c0c281b4d5f35001ae4
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63380983"
---
# <a name="ole-attachments"></a>Pi�ces jointes OLE

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Pi�ces jointes qui sont des objets OLE sont cod�es en tant qu'objets de flux de donn�es OLE 1 pour assurer la compatibilit� descendante. Si l'objet d'origine est r�ellement un objet de **IStorage** OLE 2, l'objet doit �tre converti dans un flux OLE 1. Cette conversion est effectu�e � l'aide de la fonction **OleConvertIStorageToOLESTREAM**, qui fait partie des biblioth�ques Win32 OLE. 
  

