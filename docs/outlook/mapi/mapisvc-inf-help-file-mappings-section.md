---
title: Section [mappages de fichiers d'aide] MapiSvc. inf
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 62aee641-b73f-4f53-9e8d-adf010c9ea1a
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 4760c9965975bb5d950e51b707d28bee647ef99a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32269971"
---
# <a name="mapisvcinf-help-file-mappings-section"></a>Section [mappages de fichiers d'aide] MapiSvc. inf

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
La section **[Help file Mappings]** contient des entrées qui permettent de connecter chaque service de messagerie au fichier qui fournit de l'aide pour les erreurs générées par le service. Les entrées de cette section utilisent le format suivant: 
  
 **[Mappages de fichier d'aide]** _nom du service de messagerie_  =   _Nom du fichier d'aide_
  
Le nom du service de messagerie est le nom du service de messagerie installé; le nom du fichier d'aide est le nom du fichier où se trouvent les informations d'erreur. L'exemple suivant présente une section **[mappages de fichiers d'aide]** classique qui contient les entrées de trois services: MAPI, le service MSGSERVICE et MS service. 
  
```cpp
[Help File Mappings]
MAPI=MAPI.HLP
MsgService=MYHELP.HLP
MS=STORE.HLP

```


