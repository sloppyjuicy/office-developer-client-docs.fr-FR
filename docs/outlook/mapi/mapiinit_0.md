---
title: MAPIINIT_0
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.MAPIINIT_0
api_type:
- COM
ms.assetid: 70739711-ff43-407d-bc8b-6baf7a476fef
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 8f94c4b5eac189a672771a91e6b9969462f187ef
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59610124"
---
# <a name="mapiinit_0"></a>MAPIINIT_0

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Transmet les options à la [fonction MAPIInitialize.](mapiinitialize.md) 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |MAPIX. H  <br/> |
   
```cpp
typedef struct
{
  ULONG ulVersion;
  ULONG ulFlags;
} MAPIINIT_0, FAR *LPMAPIINIT_0;

```

## <a name="members"></a>Members

 **ulVersion**
  
> Valeur entière qui représente le numéro de version de la structure **de MAPIINIT_0.** Le **membre ulVersion** est pour une expansion future et ne représente pas la version de l’interface MAPI. Actuellement, **ulVersion** doit être définie sur MAPI_INIT_VERSION. 
    
 **ulFlags**
  
> Masque de bits des indicateurs utilisés pour contrôler l’initialisation de la session MAPI. Les indicateurs suivants peuvent être définies :
    
MAPI_MULTITHREAD_NOTIFICATIONS 
  
> MAPI doit générer des notifications à l’aide d’un thread dédié à la gestion des notifications au lieu du premier thread utilisé pour appeler **MAPIInitialize**.
    
MAPI_NT_SERVICE 
  
> L’appelant est en cours d’exécution en tant Windows service. Les appelants qui ne s’exécutent pas en tant que service Windows ne doivent pas définir cet indicateur . les appelants qui s’exécutent en tant que service doivent définir cet indicateur.
    
MAPI_NO_COINIT
  
> Définissez l MAPI_NO_COINT de sorte que **MAPIInitialize** n’essaie pas d’initialiser COM avec un appel à [CoInitialize](https://msdn.microsoft.com/library/0f171cf4-87b9-43a6-97f2-80ed344fe376%28Office.15%29.aspx). Si une structure MAPIINIT_0 est passée dans **MAPIInitialize** avec _ulFlags_ définie sur MAPI_NO_COINIT, MAPI suppose que COM **a** déjà été initialisé et ignorera l’appel à **CoInitialize**.
    
## <a name="remarks"></a>Remarques

Les clients multithread doivent définir l’MAPI_MULTITHREAD_NOTIFICATIONS’indicateur. Si l’indicateur n’est pas définie, des notifications sont générées sur le thread utilisé pour effectuer le premier appel à **MAPIInitialize**. 
  
Pour plus d’informations sur le moment où définir cet indicateur et comment implémenter la sécurité des threads dans un client, voir [Threading dans MAPI](threading-in-mapi.md). 
  
## <a name="see-also"></a>Voir aussi



[MAPIInitialize](mapiinitialize.md)


[Structures MAPI](mapi-structures.md)

