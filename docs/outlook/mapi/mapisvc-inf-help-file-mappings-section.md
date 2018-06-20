---
title: Section [aide File Mappings] de MapiSvc.inf
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 62aee641-b73f-4f53-9e8d-adf010c9ea1a
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 776f797d0c96d9173e114fd499d6cca0494a0a43
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784780"
---
# <a name="mapisvcinf-help-file-mappings-section"></a>Section [aide File Mappings] de MapiSvc.inf

  
  
**S’applique à**: Outlook 
  
La section **[Help File Mappings]** contient les entrées que chacun mapper un service de message pour le fichier qui fournit une aide pour les erreurs générées par le service. Entrées de cette section utilisent le format suivant : 
  
 **[Help File Mappings]** _nom de service de message_  =   _Fichier d’aide_
  
Le nom de service de message est le nom du service de message installés ; le nom de fichier est le nom du fichier où résident les informations d’erreur. L’exemple suivant montre une section **[Help File Mappings]** typique qui contient des entrées pour les trois services : MAPI, le service MsgService et le service MS. 
  
```cpp
[Help File Mappings]
MAPI=MAPI.HLP
MsgService=MYHELP.HLP
MS=STORE.HLP

```


