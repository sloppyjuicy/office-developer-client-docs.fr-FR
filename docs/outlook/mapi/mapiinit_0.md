---
title: MAPIINIT_0
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.MAPIINIT_0
api_type:
- COM
ms.assetid: 70739711-ff43-407d-bc8b-6baf7a476fef
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: de31fe7d472b143ed8f3c108dca84a019b5ce103
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357294"
---
# <a name="mapiinit0"></a>MAPIINIT_0

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Transmet des options à la fonction [MAPIInitialize](mapiinitialize.md) . 
  
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
  
> Valeur entière qui représente le numéro de version de la structure **MAPIINIT_0** . Le membre **ulVersion** est destiné à une expansion future et ne représente pas la version de l'interface MAPI. Actuellement, **ulVersion** doit être défini sur MAPI_INIT_VERSION. 
    
 **ulFlags**
  
> Masque de réinitialisation des indicateurs utilisés pour contrôler l'initialisation de la session MAPI. Les indicateurs suivants peuvent être définis:
    
MAPI_MULTITHREAD_NOTIFICATIONS 
  
> MAPI doit générer des notifications à l'aide d'un thread dédié à la gestion des notifications au lieu du premier thread utilisé pour appeler **MAPIInitialize**.
    
MAPI_NT_SERVICE 
  
> L'appelant est exécuté en tant que service Windows. Les appelants qui ne s'exécutent pas en tant que service Windows ne doivent pas définir cet indicateur; les appelants qui s'exécutent en tant que service doivent définir cet indicateur.
    
MAPI_NO_COINIT
  
> Définissez l'indicateur MAPI_NO_COINT afin que **MAPIInitialize** n'essaie pas d'initialiser com avec un appel à [CoInitialize](https://msdn.microsoft.com/library/0f171cf4-87b9-43a6-97f2-80ed344fe376%28Office.15%29.aspx). Si une structure **MAPIINIT_0** est transmise à **MAPIInitialize** avec _ULFLAGS_ définie sur MAPI_NO_COINIT, MAPI suppose que com a déjà été initialisé et ignore l'appel à CoInitialize. ****
    
## <a name="remarks"></a>Remarques

Les clients multithread doivent définir l'indicateur MAPI_MULTITHREAD_NOTIFICATIONS. Si l'indicateur n'est pas défini, des notifications sont générées sur le thread utilisé pour effectuer le premier appel vers **MAPIInitialize**. 
  
Pour plus d'informations sur la définition de cet indicateur et sur l'implémentation de la sécurité des threads dans un client, voir [Threading in MAPI](threading-in-mapi.md). 
  
## <a name="see-also"></a>Voir aussi



[MAPIInitialize](mapiinitialize.md)


[Structures MAPI](mapi-structures.md)

