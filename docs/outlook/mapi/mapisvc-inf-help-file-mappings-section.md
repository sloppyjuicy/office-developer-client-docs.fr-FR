---
title: Section MapiSvc.inf [Mappages des fichiers d’aide]
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 62aee641-b73f-4f53-9e8d-adf010c9ea1a
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 2192421ddcde6771fa0eb342fc07aa28a65ddc51
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59575441"
---
# <a name="mapisvcinf-help-file-mappings-section"></a>Section MapiSvc.inf [Mappages des fichiers d’aide]

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
La section **[Mappages** des fichiers d’aide] contient des entrées qui maient chaque service de message au fichier qui fournit de l’aide pour les erreurs générées par le service. Les entrées de cette section utilisent le format suivant : 
  
 **Nom de fichier d’aide** du service de _message_  =   [Mappages des fichiers _d’aide]_
  
Le nom du service de message est le nom du service de message installé ; Le nom du fichier d’aide est le nom du fichier où résident les informations d’erreur. L’exemple suivant montre une section **type [Mappages** de fichiers d’aide] qui contient des entrées pour trois services : MAPI, le service MsgService et le service MS. 
  
```cpp
[Help File Mappings]
MAPI=MAPI.HLP
MsgService=MYHELP.HLP
MS=STORE.HLP

```


