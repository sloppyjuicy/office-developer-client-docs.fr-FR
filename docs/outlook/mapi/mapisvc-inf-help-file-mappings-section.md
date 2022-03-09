---
title: Section MapiSvc.inf [Mappages des fichiers d’aide]
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 62aee641-b73f-4f53-9e8d-adf010c9ea1a
ms.openlocfilehash: 109f7600c241439af4474e11433b865b2fd9f05b
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63369881"
---
# <a name="mapisvcinf-help-file-mappings-section"></a>Section MapiSvc.inf [Mappages des fichiers d’aide]

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
La section **[Mappages** des fichiers d’aide] contient des entrées qui maient chaque service de message au fichier qui fournit de l’aide pour les erreurs générées par le service. Les entrées de cette section utilisent le format suivant : 
  
 **[Help File Mappings]** _message service nameHelp_ =   _file name_
  
Le nom du service de message est le nom du service de message installé ; Le nom du fichier d’aide est le nom du fichier où résident les informations d’erreur. L’exemple suivant montre une section **type [Mappages** de fichiers d’aide] qui contient des entrées pour trois services : MAPI, le service MsgService et le service MS. 
  
```cpp
[Help File Mappings]
MAPI=MAPI.HLP
MsgService=MYHELP.HLP
MS=STORE.HLP

```


