---
title: MAPIINIT_0
description: Décrit la propriété MAPIINIT_0 et fournit une syntaxe, des membres, des remarques et des liens de ressources supplémentaires.
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
ms.openlocfilehash: eafb98016fafa5471f650eba4a6ee23b481a719f
ms.sourcegitcommit: f872848fbeb5b2353179ad4bf4eab23f61f87666
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/01/2022
ms.locfileid: "65812761"
---
# <a name="mapiinit_0"></a>MAPIINIT_0

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Transmet les options à la fonction [MAPIInitialize](mapiinitialize.md) . 
  
|Propriété |Valeur |
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
  
> Valeur entière qui représente le numéro de version de la structure **MAPIINIT_0** . Le membre **ulVersion** est destiné à une extension future et ne représente pas la version de l’interface MAPI. Actuellement, **ulVersion** doit être défini sur MAPI_INIT_VERSION. 
    
 **ulFlags**
  
> Masque de bits des indicateurs utilisés pour contrôler l’initialisation de la session MAPI. Les indicateurs suivants peuvent être définis :
    
MAPI_MULTITHREAD_NOTIFICATIONS 
  
> MAPI doit générer des notifications à l’aide d’un thread dédié à la gestion des notifications au lieu du premier thread utilisé pour appeler **MAPIInitialize**.
    
MAPI_NT_SERVICE 
  
> L’appelant s’exécute en tant que service Windows. Les appelants qui ne s’exécutent pas en tant que service Windows ne doivent pas définir cet indicateur ; les appelants qui s’exécutent en tant que service doivent définir cet indicateur.
    
MAPI_NO_COINIT
  
> Définissez l’indicateur MAPI_NO_COINT afin que **MAPIInitialize** n’essaie pas d’initialiser COM avec un appel à [CoInitialize](https://msdn.microsoft.com/library/0f171cf4-87b9-43a6-97f2-80ed344fe376%28Office.15%29.aspx). Si une structure **MAPIINIT_0** est passée dans **MAPIInitialize** avec  _ulFlags_ défini sur MAPI_NO_COINIT, MAPI suppose que COM a déjà été initialisé et contourne l’appel à **CoInitialize**.
    
## <a name="remarks"></a>Remarques

Les clients multithreads doivent définir l’indicateur de MAPI_MULTITHREAD_NOTIFICATIONS. Si l’indicateur n’est pas défini, des notifications sont générées sur le thread utilisé pour effectuer le premier appel à **MAPIInitialize**. 
  
Pour plus d’informations sur le moment où définir cet indicateur et comment implémenter la sécurité des threads dans un client, consultez [Threading dans MAPI](threading-in-mapi.md). 
  
## <a name="see-also"></a>Voir aussi



[MAPIInitialize](mapiinitialize.md)


[Structures MAPI](mapi-structures.md)

