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
ms.openlocfilehash: b95b83ad7eedff577e4c36365c9e451f4b458173
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784914"
---
# <a name="ole-attachments"></a>Pi�ces jointes OLE

  
  
**S’applique à**: Outlook 
  
Pi�ces jointes qui sont des objets OLE sont cod�es en tant qu'objets de flux de donn�es OLE 1 pour assurer la compatibilit� descendante. Si l'objet d'origine est r�ellement un objet de **IStorage** OLE 2, l'objet doit �tre converti dans un flux OLE 1. Cette conversion est effectu�e � l'aide de la fonction **OleConvertIStorageToOLESTREAM**, qui fait partie des biblioth�ques Win32 OLE. 
  

