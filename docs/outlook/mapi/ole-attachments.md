---
title: Pi�ces jointes OLE
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: febb6a5e-7c40-4f21-806e-7f827d1c37cf
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: fb716ce014ec3c4b21ce2b021c1a9f6f291d511c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32279766"
---
# <a name="ole-attachments"></a>Pi�ces jointes OLE

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Pi�ces jointes qui sont des objets OLE sont cod�es en tant qu'objets de flux de donn�es OLE 1 pour assurer la compatibilit� descendante. Si l'objet d'origine est r�ellement un objet de **IStorage** OLE 2, l'objet doit �tre converti dans un flux OLE 1. Cette conversion est effectu�e � l'aide de la fonction **OleConvertIStorageToOLESTREAM**, qui fait partie des biblioth�ques Win32 OLE. 
  

