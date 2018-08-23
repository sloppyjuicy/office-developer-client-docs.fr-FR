---
title: Section [mappages de fichier d’aide] MapiSvc.inf
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 62aee641-b73f-4f53-9e8d-adf010c9ea1a
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 91c69489e1a72c5cd702a3c4d0392220a89c38fd
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22580382"
---
# <a name="mapisvcinf-help-file-mappings-section"></a>Section [mappages de fichier d’aide] MapiSvc.inf

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
La section **[Help File Mappings]** contient les entrées que chacun mapper un service de message pour le fichier qui fournit une aide pour les erreurs générées par le service. Entrées de cette section utilisent le format suivant : 
  
 **[Help File Mappings]** _nom de service de message_  =   _Fichier d’aide_
  
Le nom de service de message est le nom du service de message installés ; le nom de fichier est le nom du fichier où résident les informations d’erreur. L’exemple suivant montre une section **[Help File Mappings]** typique qui contient des entrées pour les trois services : MAPI, le service MsgService et le service MS. 
  
```cpp
[Help File Mappings]
MAPI=MAPI.HLP
MsgService=MYHELP.HLP
MS=STORE.HLP

```


