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
ms.openlocfilehash: 31b2353b76bbac5cd58cd791f4a289c7dbabdb78
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784732"
---
# <a name="mapiinit0"></a>MAPIINIT_0

  
  
**S’applique à**: Outlook 
  
Présente les options de la fonction [exécuter MAPIInitialize](mapiinitialize.md) . 
  
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

## <a name="members"></a>Membres

 **ulVersion**
  
> Valeur entière qui représente le numéro de version de la structure **MAPIINIT_0** . Le membre **ulVersion** est une expansion future et ne représente pas la version de l’interface MAPI. Actuellement, **ulVersion** doit être défini sur MAPI_INIT_VERSION. 
    
 **ulFlags**
  
> Masque de bits d’indicateurs utilisés pour contrôler l’initialisation de la session MAPI. Les indicateurs suivants peuvent être définis :
    
MAPI_MULTITHREAD_NOTIFICATIONS 
  
> MAPI doit générer des notifications à l’aide d’un thread dédié à la gestion plutôt que le premier thread utilisé pour appeler **exécuter MAPIInitialize**de la notification.
    
MAPI_NT_SERVICE 
  
> L’appelant est exécuté comme un service Windows. Appelants qui n’exécutent pas comme un service Windows ne doit pas définir cet indicateur ; Cet indicateur doivent être défini par les appelants qui sont en cours d’exécution en tant que service.
    
MAPI_NO_COINIT
  
> Définir l’indicateur MAPI_NO_COINT pour pouvoir **exécuter MAPIInitialize** n’essaie pas d’initialiser COM avec un appel à [CoInitialize](http://msdn.microsoft.com/library/0f171cf4-87b9-43a6-97f2-80ed344fe376%28Office.15%29.aspx). Si une structure **MAPIINIT_0** est passée à **exécuter MAPIInitialize** avec _ulFlags_ défini sur MAPI_NO_COINIT, MAPI part du principe que COM a déjà été initialisé et ignore l’appel à **CoInitialize**.
    
## <a name="remarks"></a>Remarques

Clients multithreads doivent définir l’indicateur MAPI_MULTITHREAD_NOTIFICATIONS. Si l’indicateur n’est pas définie, les notifications sont générées sur le thread utilisé pour le premier appel à **exécuter MAPIInitialize**. 
  
Pour plus d’informations sur le moment de définir cet indicateur et comment implémenter la sécurité des threads dans un client, voir [Threading MAPI](threading-in-mapi.md). 
  
## <a name="see-also"></a>Voir aussi



[Exécuter MAPIInitialize](mapiinitialize.md)


[Structures MAPI](mapi-structures.md)

