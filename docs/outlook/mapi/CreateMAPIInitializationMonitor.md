---
title: CreateMAPIInitializationMonitor
manager: lindalu
ms.date: 04/27/2021
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIWAITRESULT
api_type:
- COM
ms.assetid: 32a9758a-395d-4526-9610-3e4eeaf78c96
description: Moniteur d’initialisation MAPI
Last modified: April 27, 2021
ms.openlocfilehash: 13992b8094429b61e5f980653b621d0e188ce8c5
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59588328"
---
# <a name="createmapiinitializationmonitor"></a>CreateMAPIInitializationMonitor

**S’applique** à : Outlook 2016 | Outlook 2019
  
## <a name="mapi-initialization-monitor"></a>Moniteur d’initialisation MAPI

Parfois, une application qui utilise MAPI peut vouloir savoir quand l’initialisation est terminée. Par exemple, il a plusieurs threads qui pourraient initialiser MAPI, ou en réponse à l’initialisation de MAPI l’application souhaiterait effectuer un travail, mais ne souhaite pas toujours faire tourner la pile MAPI. Le moniteur d’initialisation fournit cette fonctionnalité via une fonction (exportée à partir de OLMAPI32.DLL) et quelques interfaces simples décrites ci-dessous.

```cpp
HRESULT CreateMAPIInitializationMonitor(IMAPIInitMonitor** ppInitMonitor); 
```

#### <a name="hresult-stdapicalltype-createmapiinitializationmonitorimapiinitmonitor-ppinitmonitor"></a>HRESULT STDAPICALLTYPE CreateMapiInitializationMonitor(IMAPIInitMonitor ppInitMonitor)

Ce point d’entrée exporté à partir de OLMAPI32.DLL permet à l’appelant de récupérer une interface pour interroger l’état d’initialisation actuel, configurer un rappel pour l’achèvement de l’initialisation ou bloquer le thread actuel jusqu’à ce qu’il soit terminé. L’objet renvoyé à partir de cette API est réutilisable et thread-safe et peut être appelé à partir de n’importe quel thread, pas seulement du thread qui l’a récupéré. En outre, contrairement aux autres objets exposés à partir de MAPI, cet objet est valide tant que la DLL est chargée, il peut être ré-utilisé entre les sessions d’initialisation et peut être utilisé avant ou après l’appel de MAPIInitialize. Renvoie le succès ou l’échec via un HRESULT standard COM et affecte un paramètre de sortie à une instance de IMAPIInitMonitor.
  
## <a name="parameters"></a>Paramètres
  
 _ppInitMonitor_
> [out] Pointeur pour recevoir l’instance nouvellement créée du moniteur d’initialisation MAPI.
  
## <a name="return-values"></a>Valeurs de retour

S_OK
> Une nouvelle instance du moniteur d’initialisation a été créée avec succès.

E_OUTOFMEMORY
> Il n’y avait pas assez de mémoire pour un nouvel objet.

## <a name="see-also"></a>Voir aussi
[IMAPIInitMonitor](imapiinitmonitoriunknown.md)

[IMAPIWaitResult](imapiwaitresultiunknown.md)
